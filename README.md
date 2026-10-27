# Roblox Child Protection Pipeline

📄 **Read the full policy report:** [PDF](reports/final-report.pdf) · [Markdown](reports/final-report.md)

A multi-agent research pipeline that studies **child protection laws and how well they
actually work on Roblox**, across eight jurisdictions. It combines three independent
research streams — the legal framework, real-world efficacy evidence, and a survey of
children themselves — and integrates them into one verified final report.

Everything runs inside Claude Code: a **Supervisor** agent tells you which stage to run
next, specialised **agents** do the research, a shared **Verifier** agent fact-checks each
output in place, and **skills** encode the detailed procedures each agent follows.

---

## Purpose

- Document what child-protection law requires of a platform like Roblox, by jurisdiction.
- Test those laws against reality — personal accounts, journalism, litigation, and
  enforcement actions showing where protections are bypassed or unenforced.
- Hear from children directly, via age-appropriate surveys (ages 6–12 and 13–17).
- Cross-check all three streams against each other and synthesise a single, source-traceable
  report on the **efficacy** (not just the existence) of these laws.

---

## Key findings

The full analysis is in `reports/final-report.md`. Headlines:

- Child protection laws applicable to Roblox are failing in practice across every
  measurable dimension — age verification, content filtering, and platform enforcement.
- Self-declared age is defeated in minutes with no technical skill, and its replacement,
  facial age verification, is defeated using a parent's or sibling's ID document.
- The dominant harm pattern — contact starting on Roblox and escalating to Discord,
  Snapchat, or Telegram — is not addressed by any legal framework in any jurisdiction.
- Children's own reports confirm the gap: most are aware of common bypass methods, a large
  share have encountered content they felt too young for, and almost none learned about
  the rules from a parent.
- Safety changes have consistently been reactive, introduced after litigation or
  regulatory pressure rather than proactively.
- The US's under-13/13–17 split leaves most teenage users without meaningful federal
  protection; other jurisdictions have stronger statutory frameworks but inconsistent
  enforcement against Roblox specifically.

---

## Repository layout

Files are organised into four folders by role:

| Folder | Contents |
|---|---|
| `reports/` | All research write-ups: `law-sources.md`, `literature-review.md`, `law-report.md`, `trend-report.md`, `survey-analysis.md`, `cross-verify-report.md`, `final-report.md`, `verification-report.md` |
| `survey/` | Survey instruments: `survey-group-a.md`, `survey-group-b.md`, `survey-methodology.md` |
| `data/` | `raw-data.md` (cleaned efficacy evidence) and the survey response CSVs `survey-results-a.csv`, `survey-results-b.csv` |
| `logs/` | Per-agent status files (`agent1-status.md` … `agent6-status.md`) and `patch-log.md` |
| `.claude/agents/` | Agent definitions |
| `.claude/skills/` | Skill definitions (`<name>/SKILL.md`) |

Every agent and skill file carries a **Pipeline Header** stating its purpose, inputs,
outputs, and which agents/skills it calls, with all paths pointing at these folders.

---

## Architecture

```
                                 ┌─────────────────┐
             you ──────────────▶ │   SUPERVISOR    │  checks disk, reports status,
                                 │  (orchestrator) │  tells you the single next command
                                 └────────┬────────┘
                                          │ (you run each stage in order)
          ┌───────────────┬──────────────┼───────────────┬───────────────────┐
          ▼               ▼              (no 3)            ▼                   ▼
   ┌─────────────┐ ┌─────────────┐              ┌─────────────┐      ┌──────────────────┐
   │   AGENT 1   │ │   AGENT 2   │              │   AGENT 4   │      │     AGENT 5      │
   │     Law     │ │  Efficacy   │              │   Survey    │      │     Survey       │
   │ Researcher  │ │ Researcher  │              │  Designer   │      │    Analyser      │
   └──────┬──────┘ └──────┬──────┘              └──────┬──────┘      └────────┬─────────┘
          │               │                            │                      │
          ▼               ▼                            ▼                      ▼
     reports/        data/raw-data.md            survey/survey-*.md     reports/
     law-*.md        reports/trend-report.md                            survey-analysis.md
          │               │                            │                      │
          └───────────────┴───────────┬────────────────┴──────────────────────┘
                                       ▼
                             ┌───────────────────┐
                             │     VERIFIER      │  shared, reusable. After each stage it
                             │ (surgical patcher)│  cross-checks claims vs sources and
                             └─────────┬─────────┘  patches the target file IN PLACE,
                                       │            logging to logs/patch-log.md
                                       ▼
                             ┌───────────────────┐
                             │      AGENT 6      │  cross-verifies the 3 streams, then
                             │   Final Report    │  integrates them into
                             └─────────┬─────────┘  reports/final-report.md
                                       ▼
                              reports/final-report.md
```

Flow of evidence: **Agent 1 → Agent 2 → Agent 4 → Agent 5 → Agent 6**, with the **Verifier**
invoked as a checkpoint after most producing stages. The Supervisor never runs agents
itself — it only reports status and hands you the next command.

---

## What each agent does

| Agent | Role | Reads | Writes | Skills it calls |
|---|---|---|---|---|
| **Supervisor** (`supervisor.md`) | Orchestrates: inspects disk, prints a stage-by-stage status table, gives the next command. | all stage outputs | nothing (status to screen) | none |
| **Agent 1 — Law Researcher** (`agent1-law-researcher.md`) | Builds the legal framework across the jurisdictions. | the web | `reports/law-sources.md`, `reports/literature-review.md`, `reports/law-report.md`, `logs/agent1-status.md` | literature-search → literature-review → law-report → report-restart |
| **Agent 2 — Efficacy Researcher** (`agent2-efficacy-researcher.md`) | Finds real-world accounts of laws being bypassed/unenforced and synthesises patterns. | Agent 1 outputs, web, Reddit/Twitter MCP | `data/raw-data.md`, `reports/trend-report.md`, `logs/agent2-status.md` | data-collection → raw-data-handler → trend-report → report-corrector |
| **Agent 4 — Survey Designer** (`agent4-survey-designer.md`) | Designs two age-appropriate surveys + methodology. | `reports/law-report.md`, `reports/trend-report.md` | `survey/survey-group-a.md`, `survey/survey-group-b.md`, `survey/survey-methodology.md`, `logs/agent4-status.md` | survey-designer |
| **Agent 5 — Survey Analyser** (`agent5-survey-analyser.md`) | Analyses collected survey responses into verified statistics. | `data/survey-results-*.csv`, `survey/survey-group-*.md`, `reports/trend-report.md` | `reports/survey-analysis.md`, `logs/agent5-status.md` | none — works from its own guardrails |
| **Agent 6 — Final Report** (`agent6-final-report.md`) | Cross-verifies the three streams, then writes the integrated final report. | all three streams | `reports/cross-verify-report.md`, `reports/final-report.md`, `logs/patch-log.md`, `logs/agent6-status.md` | cross-verifier → final-report |
| **Verifier** (`agent-verifier.md`) | Shared checkpoint. Cross-checks a target file against its sources and **patches it in place**. Invoked after Agents 1, 2, 4, 5. | caller-supplied target + source list | patched target, `logs/patch-log.md`, `reports/verification-report.md` | citation-verifier |

The jurisdictions covered by `reports/law-report.md` are: **United States, European Union,
United Kingdom, Australia, Brazil, UN/International, India, South Korea** (eight).

---

## Why there is no Agent 3

The pipeline runs **Agent 1 → 2 → 4 → 5 → 6**: a planned third agent, slotted between the
efficacy research and the survey design, was dropped before the pipeline was built, and
the later agents kept their original numbers (4, 5, 6) rather than being renumbered. The
gap is a naming artefact, not a missing or broken stage.

---

## How to run it

The pipeline is **gated**: each agent stops at checkpoints and waits for you to run the next
step. Nothing runs fully autonomously. Typical session, from the project root in Claude Code:

1. **Check status / get the next command.** Invoke the Supervisor
   (`.claude/agents/supervisor.md`). It lists what exists on disk and prints a single
   `NEXT STEP` command.
2. **Agent 1 (Law).** Run it. It produces `reports/law-sources.md` and stops. Run the
   **Verifier** on that file (target = `reports/law-sources.md`, source list = same / the web).
   Repeat for `literature-review.md`, then `law-report.md`. Agent 1 then self-checks and
   writes `logs/agent1-status.md`.
3. **Agent 2 (Efficacy).** Run it once Agent 1 is COMPLETE and verified. It collects → cleans →
   synthesises, producing `data/raw-data.md` and `reports/trend-report.md`. Verify both.
4. **Agent 4 (Survey design).** Produces the two survey instruments + methodology. Verify the
   survey files.
5. **Collect responses (manual, outside the pipeline).** Administer the surveys and drop the
   results in `data/survey-results-a.csv` and `data/survey-results-b.csv`.
6. **Agent 5 (Survey analysis).** Produces `reports/survey-analysis.md`. Verify it.
7. **Agent 6 (Final report).** Runs the cross-verifier over the three streams
   (`reports/cross-verify-report.md`), and if CLEARED, writes `reports/final-report.md`,
   self-verifies, and marks `logs/agent6-status.md` COMPLETE.

Re-run the Supervisor any time to see where you are and what to do next.

---

## What each output is

**`reports/`**
- `law-sources.md` — annotated bibliography of every legal source (Agent 1).
- `literature-review.md` — thematic synthesis of those sources (Agent 1).
- `law-report.md` — formal legal report: legislative timeline, per-jurisdiction analysis,
  cross-cutting themes, Roblox-specific exposure, gaps (Agent 1).
- `trend-report.md` — analytical synthesis of real-world bypass/enforcement patterns, with
  per-jurisdiction law-practice gap ratings (Agent 2).
- `survey-analysis.md` — findings from the child survey with verified statistics
  (Group A n=16, Group B n=17) (Agent 5).
- `cross-verify-report.md` — consistency check across the three streams; CLEARED/HOLD gate (Agent 6).
- `final-report.md` — the deliverable: a 10-section integrated report on the efficacy of child
  protection laws on Roblox (Agent 6).
- `verification-report.md` — the Verifier's audit log of claims and verdicts.

**`survey/`**
- `survey-group-a.md`, `survey-group-b.md` — the two survey instruments (ages 6–12 / 13–17).
- `survey-methodology.md` — design rationale, ethics, limitations.

**`data/`**
- `raw-data.md` — cleaned, deduplicated, categorised, credibility-tiered efficacy evidence
  (49 entries, all Tier A, paraphrased — no victim identifiers).
- `survey-results-a.csv`, `survey-results-b.csv` — raw survey responses (see "Data & ethics" below).

**`logs/`**
- `agent1-status.md` … `agent6-status.md` — per-stage completion status and handoff notes.
- `patch-log.md` — every surgical edit the Verifier/Agent 6 applied, with reason and source.

---

## Data & ethics

Survey responses in `data/` are anonymous: the only fields are a submission timestamp
and the answers themselves, with no names, emails, usernames, or other identifying
information in either the structured fields or the free text. One free-text answer in
`data/survey-results-a.csv` describes a specific facial-age-verification bypass method and
is redacted in this dataset — `[describes a method of bypassing facial age verification —
redacted]` — to avoid republishing a how-to for circumventing a child-safety control.
`data/raw-data.md` likewise contains no identifying information about minors: its 49
entries are paraphrased from public Tier-A sources (news outlets, NGO and government
filings, academic research), and its HUMAN REVIEW FLAGS section is empty.

### Consent

`survey/survey-methodology.md` recommends obtaining informed parental or guardian consent
before administering either survey, plus separate age-appropriate assent directly from
Group A children, with consent materials covering the survey's purpose, voluntary
participation, anonymity, and data handling. The document describes this as the intended
process; it does not confirm whether it was followed for the specific responses in
`data/survey-results-a.csv` and `data/survey-results-b.csv`.

All survey responses were collected with informed consent.

---
name: report-corrector
description: |
  Use this skill when Agent 2 has completed all three phases and needs to
  self-check its outputs before marking status as COMPLETE. Runs a gap checklist
  against all output files and triggers targeted restarts for any phase that fails.

  Trigger for:
  - Agent 2's Phase 4 QA run
  - Any instruction to "check outputs" or "run the corrector"
  - Any time agent2-status.md would otherwise be written as COMPLETE

  Don't trigger for:
  - Mid-phase checks (do those inline within each skill)
  - Checking Agent 1's outputs (out of scope)
license: MIT
---

# Report Corrector Skill

> ## Pipeline Header
> - **Purpose:** Agent 2's final quality gate — runs a gap checklist over Agent 2's outputs and triggers targeted restarts (not full reruns) for any failing section.
> - **Called by:** Agent 2 (`agent2-efficacy-researcher.md`), Phase 4. (Agent 1's equivalent gate is `report-restart`.)
> - **Inputs:** `data/raw-data.md`, `reports/trend-report.md`; `reports/law-report.md` for cross-checking.
> - **Output:** `logs/agent2-status.md` (COMPLETE or INCOMPLETE), plus any re-run section outputs.
> - **Calls:** may re-trigger `raw-data-handler` or `trend-report` for targeted fixes.

This skill is Agent 2's final quality gate. It checks all three output files,
identifies gaps, and triggers targeted restarts — not full reruns — for
any failing section.

---

## Step 1: File Existence Check

Verify these files exist and are non-empty:

| File | Required | Check |
|---|---|---|
| `data/raw-data.md` | Yes | Exists + > 2KB |
| `reports/trend-report.md` | Yes | Exists + > 5KB |
| `reports/law-report.md` (Agent 1) | Reference only | Accessible for cross-check |

If either output file is missing or empty, **restart that phase entirely** before continuing.

---

## Step 2: data/raw-data.md Gap Checklist

Run each check. Mark PASS or FAIL.

**Volume checks:**
- [ ] Total entries ≥ 40 (or ≥ 30 with documented explanation)
- [ ] Reddit entries ≥ 20
- [ ] Twitter entries ≥ 10
- [ ] Web/news entries ≥ 10

**Quality checks:**
- [ ] Every entry has a bypass category (no blank categories)
- [ ] Every entry has a credibility tier (A/B/C/D)
- [ ] Every entry has a jurisdiction tag (UNKNOWN is acceptable)
- [ ] No entry contains a minor's name, school, specific location, or other identifying detail
- [ ] HUMAN REVIEW FLAGS section is present
- [ ] Coverage Summary table is complete and numbers add up

**Coverage checks:**
- [ ] At least 5 of the 9 bypass categories have ≥ 1 entry
- [ ] At least 4 jurisdictions represented (UNKNOWN counts if ≥ 5 entries use it)

If any check FAILs → **targeted restart: re-run Phase 2 (raw-data-handler) only for the failing check**

---

## Step 3: reports/trend-report.md Gap Checklist

**Structure checks:**
- [ ] Executive Summary present and ≥ 3 sentences
- [ ] Methodology section present with entry counts
- [ ] Minimum 5 themes identified and written up
- [ ] Jurisdiction Analysis covers all 8 jurisdictions (or notes which are absent from data)
- [ ] Platform Enforcement Analysis present
- [ ] Overall Law Efficacy Rating table complete
- [ ] Key Findings list has ≥ 5 findings
- [ ] Limitations section present

**Evidence checks:**
- [ ] Every theme cites at least 2 entry references from `data/raw-data.md`
- [ ] Every jurisdiction rating is backed by at least 1 entry or explicitly noted as "no data"
- [ ] No claim uses language stronger than the evidence supports

**Cross-reference checks:**
- [ ] Report references `reports/law-report.md` themes at least once per major theme
- [ ] Law-practice gap ratings are calibrated (not all "Critical", not all "Low")
- [ ] Recommendations section present (even if brief)

If any check FAILs → **targeted restart: re-run only the failing section of Phase 3, not the full report**

---

## Step 4: Restart Protocol

When a targeted restart is triggered:

1. Log the failure: which check, which file, what was missing
2. Re-run **only** the failing phase/section
3. Re-check the repaired section before continuing
4. Do NOT re-run phases that already passed

A maximum of **3 restart attempts** per phase is allowed.
If a phase fails 3 times, write `logs/agent2-status.md` with status INCOMPLETE and
list the unresolved gaps for human review.

---

## Step 5: Write logs/agent2-status.md

Only write `logs/agent2-status.md` as COMPLETE if all checks in Steps 2 and 3 pass.

```markdown
# Agent 2 Status
**Agent:** Agent 2 — Law Efficacy Researcher
**Date:** [YYYY-MM-DD]
**Status:** COMPLETE / INCOMPLETE

---

## Phase Completion

| Phase | Status | Notes |
|---|---|---|
| Phase 1: Data Collection | PASS / FAIL | [entries collected, sources] |
| Phase 2: Data Cleaning | PASS / FAIL | [entry count, categories covered] |
| Phase 3: Trend Synthesis | PASS / FAIL | [themes, jurisdictions covered] |
| Phase 4: QA / Correction | PASS / FAIL | [restarts triggered, final state] |

---

## Output Files
- `data/raw-data.md` — [N entries, N categories, N jurisdictions]
- `reports/trend-report.md` — [N themes, N jurisdictions analysed]

---

## Unresolved Gaps (if INCOMPLETE)
[List any checks that could not be resolved after 3 restart attempts]

---

## Handoff Notes for Next Agent
[What the next agent — Agent 4 (Survey Designer) — should know before picking up from
here. Note: there is no Agent 3; see the project README.]
```

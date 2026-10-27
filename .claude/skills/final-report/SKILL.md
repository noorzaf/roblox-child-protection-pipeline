---
name: final-report
description: |
  Use this skill when Agent 6 needs to integrate law-report.md, trend-report.md,
  and survey-analysis.md into one comprehensive final report on the efficacy of
  child protection laws on Roblox. Governs structure, integration logic, and
  self-verification before completion.

  Trigger for:
  - Starting Agent 6
  - Any instruction to write the final report

  Don't trigger for:
  - Cross-verifying source reports against each other (use cross-verify skill)
  - Individual agent outputs (use their respective skills)
license: MIT
---

# Final Report Skill

> ## Pipeline Header
> - **Purpose:** Integrate the three research streams into the single comprehensive final report, then self-verify every statistic against its source.
> - **Called by:** Agent 6 (`agent6-final-report.md`), Phase 2 (after `cross-verifier` clears).
> - **Inputs:** `reports/law-report.md`, `reports/trend-report.md`, `reports/survey-analysis.md`, `survey/survey-methodology.md`; references `reports/law-sources.md` and `data/raw-data.md`.
> - **Outputs:** `reports/final-report.md`; patches logged to `logs/patch-log.md`.
> - **Next step:** Agent 6 writes `logs/agent6-status.md` once self-verification passes.

---

## Pre-Writing Checklist

Before writing a single line, confirm all inputs are available:

- [ ] `reports/law-report.md` — Agent 1 output
- [ ] `reports/trend-report.md` — Agent 2 output (patched in place by the Verifier)
- [ ] `reports/survey-analysis.md` — Agent 5 output
- [ ] `survey/survey-methodology.md` — Agent 4 output
- [ ] the `cross-verifier` skill (`.claude/skills/cross-verifier/SKILL.md`) has been run and passed

If cross-verification has not been run, run it first before proceeding.

---

## Report Structure

### Cover
```
Title: The Efficacy of Child Protection Laws on Roblox
Subtitle: A Multi-Stream Research Report
Date: [YYYY-MM-DD]
Research streams: Legal framework (Agent 1) | Real-world efficacy (Agent 2) | Child survey (Agent 5)
```

---

### Section 1: Executive Summary
- 5-7 sentences maximum
- Lead with the single most important finding
- One sentence per research stream
- End with the most urgent policy implication

---

### Section 2: Research Overview
- What this report covers and why
- How the three research streams relate to each other
- Methodology note: legal research + personal accounts + verified child survey
- Limitations: survey sample size (Group A n=16, Group B n=17), Reddit access blocked, Agent 2 sourced from journalism and litigation rather than community posts

---

### Section 3: Legal Framework
- Draw from `reports/law-report.md`
- Summarise the key legal obligations on Roblox across the 8 jurisdictions
- Focus on: age verification requirements, content filtering obligations, parental consent rules, enforcement mechanisms
- Do not reproduce the full law-report — synthesise the most relevant findings
- Flag the jurisdictions where legal obligations are weakest

---

### Section 4: Real-World Efficacy
- Draw from `reports/trend-report.md`
- What do personal accounts show about how well the laws work in practice?
- Organise by bypass category: age bypass, contact bypass, grooming, platform non-enforcement, cross-platform escalation
- Map failures against the legal framework from Section 3 — where is the gap between law and practice?
- Include the law-practice gap ratings from Agent 2

---

### Section 5: Children's Awareness and Experience
- Draw from `reports/survey-analysis.md`
- What do children themselves report about Roblox's age restrictions?
- Key findings: usage patterns, rule awareness, perceived effectiveness, bypass method awareness
- Highlight the most striking findings (93% Group A aware of false DOB bypass, 44% saw inappropriate content, no Group B respondent learned rules from a parent)
- Frame all findings with sample size caveat

---

### Section 6: Cross-Stream Analysis
This is the most important section — synthesise across all three streams.

For each major theme, bring together what the law says, what personal accounts show, and what children report:

**Theme A: Age Verification**
- What the law requires
- What personal accounts show about bypass rates
- What children report about awareness of bypass methods

**Theme B: Content Filtering**
- Legal obligations
- Real-world failures documented
- Children's self-reported exposure to inappropriate content

**Theme C: Platform Enforcement**
- What laws require Roblox to do
- Evidence of non-enforcement from Agent 2
- Children's perception of enforcement (Group B: 47% say not enough)

**Theme D: Parental Awareness**
- Legal framework around parental consent
- Real-world gap: no Group B respondent learned rules from a parent
- Implications for law design

**Theme E: Cross-Platform Escalation**
- Laws are platform-specific; harm is not
- Agent 2: 14 of 19 grooming cases escalated to Discord/WhatsApp
- Survey: children unaware this is a documented pattern

---

### Section 7: Key Findings
Numbered list of 8-12 findings, ordered by severity.
Each finding must:
- State the finding in one sentence
- Cite which research stream it comes from
- Note its policy implication in one sentence

---

### Section 8: Recommendations
For each finding, one concrete recommendation directed at:
- Roblox (platform)
- Regulators (by jurisdiction where relevant)
- Parents
- Policymakers

---

### Section 9: Limitations
- Survey sample sizes
- Reddit access blocked during Agent 2 collection
- Agent 2 sourced from journalism/litigation — community-level accounts underrepresented
- Jurisdictions with thin data coverage
- Report reflects state of laws and enforcement as of June 2026

---

### Section 10: References
- Cite `reports/law-sources.md` for all legal references
- Cite entry numbers from `data/raw-data.md` for Agent 2 claims
- Cite `reports/survey-analysis.md` for all survey statistics

---

## Writing Rules

- Every statistic must match its source document exactly
- Every claim about a law must be traceable to `reports/law-sources.md`
- Every claim about a personal account must be traceable to `data/raw-data.md`
- Every survey statistic must match `reports/survey-analysis.md`
- Frame survey findings with sample size caveat in every section that uses them
- Do not introduce new research not in the source documents
- Cross-stream synthesis is analysis, not new data — be clear about what is interpretation vs evidence

---

## Self-Verification Step

After writing `reports/final-report.md`, before writing `logs/agent6-status.md`:

1. Extract every statistic in the report
2. Verify each against its source document
3. Apply surgical patches for any mismatch
4. Check every cross-stream claim is supported by at least two research streams
5. Confirm all 10 sections are present
6. Confirm limitations section is honest about sample sizes

Only mark COMPLETE after self-verification passes.

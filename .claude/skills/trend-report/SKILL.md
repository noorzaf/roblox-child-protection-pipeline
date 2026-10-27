---
name: trend-report
description: |
  Use this skill when Agent 2 has a clean raw-data.md and needs to synthesise
  the data into a structured analytical report on patterns, law efficacy gaps,
  and jurisdiction-level findings. Produces trend-report.md.

  Trigger for:
  - Starting Agent 2's Phase 3 synthesis run
  - Any instruction to "synthesise the data" or "write the trend report"
  - Re-running synthesis after report-corrector finds gaps

  Don't trigger for:
  - Data collection (use data-collection skill)
  - Data cleaning (use raw-data-handler skill)
license: MIT
---

# Trend Report Skill

> ## Pipeline Header
> - **Purpose:** Agent 2's synthesis phase — turn the cleaned dataset into an analytical report on bypass patterns, per-jurisdiction law-practice gaps, and platform enforcement behaviour.
> - **Called by:** Agent 2 (`agent2-efficacy-researcher.md`), Phase 3.
> - **Inputs:** `data/raw-data.md`; `reports/law-report.md` for jurisdiction mapping.
> - **Output:** `reports/trend-report.md`.
> - **Next skill:** `report-corrector` (Agent 2's QA gate).

This skill governs how Agent 2 synthesises `data/raw-data.md` into `reports/trend-report.md` —
a structured analytical report mapping real-world bypass patterns against the
legal framework documented by Agent 1.

---

## Step 1: Pre-Synthesis Checklist

Before writing anything, confirm:
- [ ] `data/raw-data.md` exists and has passed its quality gate
- [ ] `reports/law-report.md` from Agent 1 is accessible (for jurisdiction mapping)
- [ ] Total entry count meets minimum (40+, or 30+ with explanation)

If `reports/law-report.md` is not accessible, note this and proceed with the 8 jurisdictions
from memory: United States, European Union, United Kingdom, Australia, Brazil,
UN/International, India, South Korea.

---

## Step 2: Theme Identification

Read through `raw-data.md` and identify **recurring themes** across entries.
A theme requires at least 3 independent entries to qualify.

Expected themes (based on bypass taxonomy):
1. **Age Gate Ineffectiveness** — How minors bypass age verification
2. **Platform Non-Enforcement** — Reports ignored or slow response
3. **Cross-Platform Migration** — Contact escalating off Roblox
4. **Grooming Pattern Signatures** — Common tactics used
5. **Parental Unawareness** — Gaps in parental knowledge of legal protections
6. **Jurisdictional Disparities** — Which jurisdictions have more accounts
7. **Law Awareness Gap** — Do victims know laws exist to protect them?

Add additional themes if the data supports them.

---

## Step 3: Jurisdiction Mapping

For each of the 8 jurisdictions in `reports/law-report.md`:

1. Count entries from that jurisdiction
2. Identify which bypass categories are most prevalent
3. Note any apparent gap between what the law requires and what the data shows happening
4. Rate the apparent law-practice gap: **Low / Medium / High / Critical**

Format:
```
### [Jurisdiction]
- **Entries:** N
- **Dominant bypass type:** [code]
- **Most cited failure:** [1 sentence]
- **Law-practice gap rating:** [Low/Medium/High/Critical]
- **Key evidence:** [1-2 entry references]
```

---

## Step 4: Platform Behaviour Analysis

Synthesise what the data shows about Roblox's actual enforcement behaviour:

- Average reported response time (if mentioned in entries)
- Reports that resulted in no action vs action taken
- Types of bypass that platform seems most/least responsive to
- Any accounts of platform actively correcting issues vs ignoring

---

## Step 5: Report Structure — `reports/trend-report.md`

```markdown
# Trend Report: Roblox Child Protection Law Efficacy
**Agent:** Agent 2 — Law Efficacy Researcher
**Date:** [YYYY-MM-DD]
**Data source:** raw-data.md (N entries, N jurisdictions)
**Cross-reference:** reports/law-report.md (Agent 1)

---

## Executive Summary
[3-5 sentences: what the data shows overall about law efficacy on Roblox]

---

## Methodology
- Sources: Reddit, Twitter/X, web news/NGO reports
- Collection period: [date range of sources]
- Total entries analysed: N
- Credibility breakdown: Tier A: N, Tier B: N, Tier C: N
- Jurisdictions represented: N of 9

---

## Theme 1: [Name]
**Prevalence:** N entries (N% of dataset)
**Summary:** [2-3 sentences describing the pattern]
**Representative evidence:** [2-3 paraphrased examples, cited by entry number]
**Law gap:** [Which laws appear to be failing here, referencing reports/law-report.md themes]

[Repeat for each theme — minimum 5 themes]

---

## Jurisdiction Analysis

[One subsection per jurisdiction — see Step 3 format]

---

## Platform Enforcement Analysis

[See Step 4]

---

## Overall Law Efficacy Rating

| Jurisdiction | Legal Framework (Agent 1) | Real-World Gap (Agent 2) | Overall Rating |
|---|---|---|---|
| US Federal | [summary] | [summary] | Strong / Partial / Weak / Failing |
...

---

## Key Findings

1. [Most significant finding]
2. [Second finding]
3. [Third finding]
[...up to 10]

---

## Limitations
- [What this data cannot show]
- [Survivorship/reporting bias notes]
- [Jurisdictions with thin data coverage]

---

## Recommendations for Follow-On Research (if applicable)
[What further research or legal analysis would strengthen these findings. Note: the
next pipeline stage is Agent 4 — there is no Agent 3; see the project README.]
```

---

## Step 6: Citation Standard

Every claim in the report must be traceable to at least one entry in `data/raw-data.md`.
Reference entries as: `[Entry N, data/raw-data.md]`

Do not make claims not supported by the collected data.
If you see a pattern but have fewer than 3 supporting entries, note it as
"tentative finding — requires additional data."

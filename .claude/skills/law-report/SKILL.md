---
name: law-report
description: |
  Use this skill to write a structured legal report from a synthesised literature review
  and annotated source list. Always run AFTER literature-search and literature-review
  skills have produced their outputs.

  Trigger for:
  - "Write the law report"
  - "Generate the structured legal report"
  - "Produce the report with timeline and jurisdiction analysis"
  - Any agent pipeline step where sources and a literature review exist and a
    formal legal report needs to be produced

  Don't trigger for:
  - Source gathering (use literature-search)
  - Synthesis (use literature-review)
  - Fact-checking or verification (use fact-check skill)
license: MIT
---

# Law Report Writing

> ## Pipeline Header
> - **Purpose:** Turn the synthesised review + source list into a formal, cited legal report with a timeline and per-jurisdiction analysis.
> - **Called by:** Agent 1 (`agent1-law-researcher.md`), Phase 3.
> - **Inputs:** `reports/law-sources.md` and `reports/literature-review.md`.
> - **Output:** `reports/law-report.md`.
> - **Next skill:** `report-restart` (Agent 1's QA gate).

This skill governs how to write a structured legal report from existing research materials.
The inputs are `reports/law-sources.md` (annotated bibliography) and `reports/literature-review.md`
(thematic synthesis). The output is a formal report suitable for use in policy research,
academic work, or regulatory analysis.

The goal is precision and structure — every claim cited, every jurisdiction covered,
every gap acknowledged.

---

## Step 1: Read Inputs Before Writing

Before writing a single line, read:
1. `reports/law-sources.md` — to know what sources are available
2. `reports/literature-review.md` — to understand the themes and conflicts already identified

Do not write from memory. Everything in the report must be traceable to these inputs.

---

## Step 2: Report Structure

```
# [Title]: Applicability to [Platform]

## Executive Summary (200 words max)
   - What laws apply, to whom, and what the key gaps are
   - Written for a non-specialist reader
   - No citations needed here — just the key takeaways

## 1. Legislative Timeline
   A chronological table:
   | Year | Law / Regulation | Jurisdiction | Key Provision | Status |
   - Cover from earliest relevant law to present
   - Status: Proposed / Passed / In force / Amended / Repealed

## 2. Laws by Jurisdiction
   For each jurisdiction:
   ### [Jurisdiction]
   - **Law name and year**
   - Purpose and scope
   - Key obligations on platforms
   - Who it applies to (age thresholds, platform size, geography)
   - Penalties for non-compliance
   - **Roblox-specific applicability** — does it apply? How? Any known compliance issues?

## 3. Cross-Cutting Themes
   Organised by theme, not jurisdiction:
   - Age verification and assurance requirements
   - Data collection and minimisation obligations
   - Default privacy settings and dark patterns
   - Advertising and monetisation restrictions
   - Reporting, audit, and enforcement mechanisms
   For each theme: what the laws require, where they agree, where they conflict

## 4. Platform-Specific Analysis
   - Which laws [platform] is currently subject to
   - Known compliance actions, investigations, or violations
   - What [platform] does that existing law does not clearly cover
   - The most significant legal exposure as of the report date

## 5. Gaps and Open Questions
   - Areas where law is unclear, contested, or silent
   - Jurisdictions with weak or no relevant legislation
   - Emerging issues not yet addressed by any law
   - Questions Agent 2 should investigate further

## 6. References
   Full source list, drawn from reports/law-sources.md
   Formatted as: [Number]. [Title] — [Organisation], [Year]. [URL]
```

---

## Step 3: Writing Rules

- **Every claim needs a citation** — format as [Source X] referencing law-sources.md
- **Jurisdiction sections must be self-contained** — a reader should understand each
  jurisdiction without reading the others
- **Be specific about Roblox** — don't just say "gaming platforms"; say what applies
  to Roblox specifically and why
- **Acknowledge uncertainty** — if a law's applicability to Roblox is contested or unclear, say so
- **No padding** — if a jurisdiction has no relevant law, write one sentence saying so
- **Plain language** — explain legal terms when first used; write for an intelligent non-lawyer
- **Date everything** — note the "as of" date for all legal statuses

---

## Step 4: Quality Check

Before saving, verify:
- Every section of the structure is present
- Legislative timeline covers all jurisdictions in law-sources.md
- Every jurisdiction in law-sources.md has a section in Part 2
- Every claim in Parts 2–4 has a citation
- Gaps section is honest — does not claim completeness where gaps exist
- Executive summary accurately reflects the body of the report
- References section matches reports/law-sources.md

---

## Output

Save the completed report to `reports/law-report.md`.

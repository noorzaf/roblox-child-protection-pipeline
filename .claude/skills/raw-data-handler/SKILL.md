---
name: raw-data-handler
description: |
  Use this skill when Agent 2 has finished collecting raw data and needs to clean,
  deduplicate, categorise, and credibility-tier all collected entries before synthesis.
  Takes the raw log from data-collection and produces a structured raw-data.md file.

  Trigger for:
  - Starting Agent 2's Phase 2 cleaning run
  - Any instruction to "clean and organise the collected data"
  - Re-running cleaning after report-corrector identifies categorisation gaps

  Don't trigger for:
  - Initial data collection (use data-collection skill)
  - Writing the synthesis report (use trend-report skill)
license: MIT
---

# Raw Data Handler Skill

> ## Pipeline Header
> - **Purpose:** Agent 2's cleaning phase — deduplicate, categorise (bypass taxonomy), credibility-tier, and jurisdiction-tag the raw log.
> - **Called by:** Agent 2 (`agent2-efficacy-researcher.md`), Phase 2.
> - **Input:** the raw log from the `data-collection` skill; references `reports/law-report.md` for the jurisdiction list.
> - **Output:** `data/raw-data.md`.
> - **Next skill:** `trend-report` synthesises `data/raw-data.md`.

This skill governs how Agent 2 transforms raw collected entries into a clean,
structured, research-grade dataset. The output is `data/raw-data.md`.

---

## Step 1: Deduplication

Before categorising anything, deduplicate the raw log:

- **Same URL** = exact duplicate; keep one, discard the rest
- **Same incident, different sources** = merge into one entry; list all source URLs; note "corroborated by N sources"
- **Same narrative pattern, different people** = keep both, tag as "recurring pattern"

Log the deduplication count:
```
Entries before deduplication: N
Duplicates removed: N
Merged (corroborated): N
Entries proceeding to categorisation: N
```

---

## Step 2: Bypass Taxonomy

Assign each entry **one primary category** and (optionally) one secondary category:

| Code | Category | Description |
|---|---|---|
| `AGE-BYP` | Age bypass | Under-13 account created, COPPA/age gate circumvented |
| `FILTER-BYP` | Content filter bypass | Adult/inappropriate content reached a minor |
| `CONTACT-BYP` | Contact restriction bypass | Adult circumvented DM/friend restrictions to reach a minor |
| `GROOM` | Grooming pattern | Sustained relationship-building toward exploitation |
| `PLAT-FAIL` | Platform non-enforcement | Report made; platform failed to act within legal timeframe |
| `LAW-UNAWARE` | Law unawareness | Subject unaware legal protections exist |
| `CROSS-PLAT` | Cross-platform escalation | Roblox contact escalated to Discord, WhatsApp, etc. |
| `LEGAL-ACTION` | Legal / law enforcement | Case resulted in arrest, complaint, or legal action |
| `POLICY-GAP` | Policy gap identified | Specific gap between law and platform policy noted |

---

## Step 3: Credibility Tiering

Assign each entry a credibility tier:

| Tier | Label | Criteria |
|---|---|---|
| A | High | Named journalist / NGO report / court record / regulatory filing |
| B | Medium | Upvoted Reddit post with corroborating comments, named parent account, engaged Twitter thread |
| C | Low-medium | Single Reddit/Twitter post, no corroboration, but plausible and detailed |
| D | Low | Vague, anonymous, single sentence, no detail |

Exclude Tier D entries from the trend-report unless you have fewer than 30 total entries — in which case include them with a clear D label.

---

## Step 4: Jurisdiction Tagging

Where possible, tag each entry with its jurisdiction:

`US-FED`, `US-CA`, `US-TX`, `UK`, `EU`, `AU`, `CA` (Canada), `UNKNOWN`

Reference the jurisdiction list from `reports/law-report.md` for the 8 jurisdictions Agent 1 covered.
Mark entries from jurisdictions outside the 9 as `OTHER-[country code]`.

---

## Step 5: Output Format — `data/raw-data.md`

Structure the output file as follows:

```markdown
# Raw Data: Roblox Law Efficacy — Personal Accounts
**Agent:** Agent 2 — Law Efficacy Researcher
**Date:** [YYYY-MM-DD]
**Total entries:** N
**After deduplication:** N

---

## Deduplication Log
[paste the dedup count block from Step 1]

---

## Data by Bypass Category

### AGE-BYP — Age Bypass (N entries)

| # | Date | Platform | Jurisdiction | Tier | Corroborated | Source URL |
|---|---|---|---|---|---|---|
| 1 | 2024-03 | Reddit | US-FED | B | No | https://... |

**Entry 1:**
[Paraphrased account — 2-4 sentences. No identifying minor details.]
*Bypass type: AGE-BYP | Secondary: — | Tier: B | Jurisdiction: US-FED*

---

[Repeat for each category]

---

## HUMAN REVIEW FLAGS
[List any entries flagged as potentially involving active/recent harm]
| # | Platform | URL | Reason for flag |
|---|---|---|---|

---

## Coverage Summary
| Category | Count | % of total |
|---|---|---|
| AGE-BYP | N | N% |
...

| Jurisdiction | Count |
|---|---|
| US-FED | N |
...

| Tier | Count |
|---|---|
| A | N |
...
```

---

## Step 6: Quality Gate

Before writing `data/raw-data.md`, verify:

- [ ] All entries have a bypass category assigned
- [ ] All entries have a credibility tier
- [ ] All entries have a jurisdiction tag (UNKNOWN is acceptable)
- [ ] No minor's identifying information is present in any entry
- [ ] HUMAN REVIEW FLAGS section is present (even if empty)
- [ ] Coverage Summary table is complete

If any check fails, fix it before writing the file.

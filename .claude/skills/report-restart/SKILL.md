---
name: report-restart
description: |
  Use this skill to self-check completed research outputs and restart the pipeline
  if gaps are found. Always run AFTER all other skills have produced their outputs.

  Trigger for:
  - "Check the report for gaps"
  - "Verify the report and restart if needed"
  - "Self-check phase"
  - Any agent pipeline step where outputs exist and need quality verification
    before being passed to the next agent

  Don't trigger for:
  - Writing or synthesis (use literature-review or law-report skills)
  - Source gathering (use literature-search)
license: MIT
---

# Report Reading and Restart Loop

> ## Pipeline Header
> - **Purpose:** Agent 1's final quality gate — re-reads all three Agent 1 outputs, checks for gaps, and either signs off COMPLETE or triggers surgical restarts of specific phases.
> - **Called by:** Agent 1 (`agent1-law-researcher.md`), Phase 4. (Agent 2 has its own equivalent gate, `report-corrector`.)
> - **Inputs:** `reports/law-sources.md`, `reports/literature-review.md`, `reports/law-report.md`.
> - **Output:** `logs/agent1-status.md` (COMPLETE or RESTARTING), plus any re-run phase outputs.
> - **Calls:** may re-trigger `literature-search`, `literature-review`, or `law-report` for targeted gap-filling.

This skill governs how to self-check completed research outputs and decide whether
to restart parts of the pipeline to fill gaps. The inputs are all output files
produced by previous phases. The output is either a clean status file (if complete)
or a targeted restart of specific phases (if gaps are found).

The goal is honest quality control — do not sign off on incomplete work.

---

## Step 1: Read All Output Files

Read every output file produced in the pipeline:
1. `reports/law-sources.md` — annotated bibliography
2. `reports/literature-review.md` — thematic synthesis
3. `reports/law-report.md` — structured legal report

Do not rely on memory of what was written. Read the actual files.

---

## Step 2: Check reports/law-sources.md

Verify:
- [ ] All required jurisdictions are represented (US, EU, UK, Australia, UN/International)
- [ ] All required source types are present (legislation, regulations, academic, enforcement, policy)
- [ ] Each source has: title, organisation, year, URL, relevance note, key finding
- [ ] Gap Analysis section exists and is specific
- [ ] No sources are cited without a URL or enough detail to locate them

**If gaps found:** Note exactly which jurisdictions or source types are missing.
Return to Phase 1 (literature-search) with targeted queries to fill only those gaps.
Do not redo the entire search — be surgical.

---

## Step 3: Check reports/literature-review.md

Verify:
- [ ] At least 4 themes are covered
- [ ] Each theme references at least 2 sources from reports/law-sources.md
- [ ] Conflicts between sources are flagged, not smoothed over
- [ ] Gap Analysis section exists
- [ ] No claims without citations

**If gaps found:** Note which themes are thin or uncited.
Return to Phase 2 (literature-review) to expand only those sections.

---

## Step 4: Check reports/law-report.md

Verify:
- [ ] Executive summary is present and accurate
- [ ] Legislative timeline covers all jurisdictions
- [ ] Every jurisdiction in law-sources.md has a section
- [ ] Every claim in Parts 2–4 has a citation traceable to reports/law-sources.md
- [ ] Roblox-specific analysis section is present and specific
- [ ] Gaps and Open Questions section is honest
- [ ] References section matches law-sources.md

**If gaps found:** Note exactly which sections are incomplete or uncited.
Return to Phase 3 (law-report) to fix only those sections.

---

## Step 5: Restart Decision

After checking all files, make one of two decisions:

**PASS** — all checks above are met (minor issues are noted but do not block):
- Write `logs/agent1-status.md` with status: COMPLETE
- List what was covered
- List any minor gaps that remain (for Agent 2 to be aware of)
- Confirm the report is ready to hand off

**RESTART** — one or more critical checks failed:
- Write `logs/agent1-status.md` with status: RESTARTING
- List exactly what failed and why
- List the targeted actions needed (e.g., "Re-run Phase 1 for Canada and South Korea only")
- Then immediately execute those targeted actions
- After completing them, re-run this skill from Step 1

---

## Step 6: logs/agent1-status.md Format

```
# Agent 1 Status

**Date:** [date]
**Status:** COMPLETE / RESTARTING

## What Was Covered
- Jurisdictions: [list]
- Source types: [list]
- Total sources: [number]
- Themes in literature review: [list]

## Quality Check Results
- law-sources.md: PASS / FAIL — [notes]
- literature-review.md: PASS / FAIL — [notes]
- law-report.md: PASS / FAIL — [notes]

## Gaps Remaining
[List any gaps that remain after all restarts, for Agent 2 awareness]

## Handoff Notes for Agent 2
[What Agent 2 should know before starting]
[Key findings Agent 2 should build on]
[Open questions Agent 2 should investigate]
```

---

## Rules

- **Be honest** — do not pass work that has real gaps just to finish faster
- **Be surgical on restarts** — only redo what is actually missing, not the whole pipeline
- **Maximum 2 restart loops** — if gaps persist after 2 restarts, mark them in the status
  file and pass anyway, with a clear note for Agent 2
- **Never delete existing output files** — append or overwrite only the specific sections
  that need fixing

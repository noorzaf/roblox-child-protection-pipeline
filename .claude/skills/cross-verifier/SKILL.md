---
name: cross-verify
description: |
  Use this skill before Agent 6 starts writing to check that law-report.md,
  trend-report.md, and survey-analysis.md are internally consistent with each
  other. Flags contradictions, gaps, and misalignments across the three research
  streams. Does not patch — produces a cross-verify-report.md for Agent 6 to
  read before writing the final report.

  Trigger for:
  - Before Agent 6 starts writing
  - Any instruction to cross-check the research streams against each other

  Don't trigger for:
  - Verifying a single document against its sources (use citation-verifier skill)
  - Writing the final report (use final-report skill)
license: MIT
---

# Cross-Verification Skill

> ## Pipeline Header
> - **Purpose:** Check consistency *across* the three research streams (does not patch) and produce a clearance decision for Agent 6.
> - **Called by:** Agent 6 (`agent6-final-report.md`), Phase 1.
> - **Inputs:** `reports/law-report.md`, `reports/trend-report.md`, `reports/survey-analysis.md`.
> - **Output:** `reports/cross-verify-report.md` with a CLEARED/HOLD decision.
> - **Next skill:** `final-report` (only if CLEARED TO PROCEED).
>
> Note: the skill name is `cross-verify`; its directory is `.claude/skills/cross-verifier/`.

---

## Purpose

This skill checks consistency ACROSS the three research streams — not within each one.
It looks for:
- Contradictions between what the law says and what personal accounts show
- Bypass methods that appear in Agent 2 data but not in the survey (or vice versa)
- Jurisdiction findings that conflict across streams
- Statistics or claims in one stream that are incompatible with another

---

## Step 1: Extract Key Claims from Each Stream

Read all three source documents and extract:

**From reports/law-report.md:**
- List of jurisdictions covered
- Key legal obligations per jurisdiction (age verification, content filtering, parental consent, enforcement)
- Penalty amounts and enforcement mechanisms
- Any explicit gaps or weaknesses noted

**From reports/trend-report.md:**
- Bypass categories documented and their prevalence
- Jurisdictions represented in personal accounts
- Platform enforcement failures documented
- Cross-platform escalation findings
- Law-practice gap ratings per jurisdiction

**From reports/survey-analysis.md:**
- Bypass methods children are aware of (ranked by awareness %)
- Children's perception of rule effectiveness
- Jurisdictions represented (if any)
- Key statistics: bypass awareness %, inappropriate content exposure %, enforcement scepticism %

---

## Step 2: Cross-Stream Consistency Checks

Run every check below. Mark each CONSISTENT, TENSION, or CONFLICT.

### Check 1: Jurisdiction Coverage
- Are the jurisdictions in law-report.md represented in Agent 2's personal accounts?
- Flag any jurisdiction that Agent 1 covers but Agent 2 found no personal accounts for
- Flag any jurisdiction in Agent 2 data not covered by Agent 1

### Check 2: Bypass Method Alignment
Compare bypass methods across Agent 2 and Agent 5:

| Method | In Agent 2 data? | In survey awareness? | Alignment |
|---|---|---|---|
| False date of birth | ? | ? | ? |
| Parent/sibling account | ? | ? | ? |
| Multiple accounts | ? | ? | ? |
| VPN | ? | ? | ? |
| Unofficial/modified client | ? | ? | ? |
| Cross-platform escalation | ? | Survey didn't cover | N/A |
| Facial age verification spoof | Agent 2? | Yes (Group A) | ? |

For each method: ALIGNED (both streams agree), TENSION (one stream shows more than other), GAP (in one stream only)

### Check 3: Enforcement Perception vs Evidence
- Agent 2: What does evidence show about Roblox's enforcement?
- Agent 5: What do children perceive about Roblox's enforcement? (Group B: 47% say not enough)
- Are these consistent or does one stream contradict the other?

### Check 4: Content Exposure Claims
- Agent 2: What inappropriate content exposure is documented?
- Agent 5: 44% of Group A reported seeing content they felt too young for
- Does Agent 2's documented content exposure align with survey self-reports?

### Check 5: Age Verification Effectiveness
- Law: What does each jurisdiction require for age verification?
- Agent 2: What bypass methods defeated age verification?
- Survey: 93% of Group A aware of false DOB bypass
- Are these three consistent in painting the same picture?

### Check 6: Parental Awareness Gap
- Law: What parental consent requirements exist?
- Agent 2: Any documented cases involving parental unawareness?
- Survey: No Group B respondent learned rules from a parent
- Is there a consistent finding across streams about parents being out of the loop?

### Check 7: Platform Non-Enforcement
- Agent 2: Specific cases of Roblox failing to act on reports
- Agent 5 Group B: 47% say Roblox doesn't enforce enough
- Law: What are Roblox's legal obligations to enforce?
- Do these three align into a coherent finding?

---

## Step 3: Flag Tensions and Conflicts

For every TENSION or CONFLICT found:

```
Issue [N]: [TENSION / CONFLICT]
Stream A: [what law-report / trend-report / survey-analysis says]
Stream B: [what the other stream says]
Implication for final report: [how Agent 6 should handle this]
Recommended framing: [suggested language that acknowledges the tension honestly]
```

---

## Step 4: Identify Cross-Stream Strengths

For every finding supported by ALL THREE streams — note it as a TRIPLE-CONFIRMED finding.
These are the strongest findings for the final report.

```
Triple-confirmed finding [N]:
- Law stream: [what law-report shows]
- Efficacy stream: [what trend-report shows]
- Survey stream: [what survey-analysis shows]
- Synthesis: [one sentence combining all three]
```

---

## Step 5: Write reports/cross-verify-report.md

```markdown
# Cross-Verification Report
**Date:** [YYYY-MM-DD]
**Streams checked:** reports/law-report.md, reports/trend-report.md, reports/survey-analysis.md
**Total checks run:** N
**Results:** N CONSISTENT, N TENSION, N CONFLICT

---

## Summary
[2-3 sentences: overall consistency assessment]

---

## Consistency Check Results

| Check | Topic | Result |
|---|---|---|
| 1 | Jurisdiction coverage | CONSISTENT / TENSION / CONFLICT |
| 2 | Bypass method alignment | [per method] |
| 3 | Enforcement perception vs evidence | |
| 4 | Content exposure | |
| 5 | Age verification effectiveness | |
| 6 | Parental awareness gap | |
| 7 | Platform non-enforcement | |

---

## Tensions and Conflicts
[Full detail on each tension/conflict with recommended framing]

---

## Triple-Confirmed Findings
[List of findings supported by all three streams — these are the strongest]

---

## Clearance for Agent 6
[CLEARED TO PROCEED / HOLD — resolve conflicts before writing]

If CLEARED: Agent 6 may proceed to the `final-report` skill (`.claude/skills/final-report/SKILL.md`)
If HOLD: list what must be resolved first
```

---

## Step 6: Quality Gate

- [ ] All 7 checks completed
- [ ] Every tension and conflict has a recommended framing for Agent 6
- [ ] Triple-confirmed findings are clearly identified
- [ ] reports/cross-verify-report.md written
- [ ] Clearance decision made

If 2 or fewer CONFLICTs: CLEARED TO PROCEED
If 3 or more CONFLICTs: HOLD — flag for human review before Agent 6 writes

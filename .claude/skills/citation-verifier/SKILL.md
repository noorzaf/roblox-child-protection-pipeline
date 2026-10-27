---
name: citation-verifier
description: |
  Use this skill when the Verifier Agent needs to cross-check every claim in
  literature-review.md against law-sources.md and live URLs.

  Trigger for:
  - Any instruction to verify, audit, or cross-check the literature review
  - Starting the Verifier Agent

  Don't trigger for:
  - Writing new research (use literature-review skill)
  - Collecting new sources (use literature-search skill)
license: MIT
---

# Citation Verifier Skill

> ## Pipeline Header
> - **Purpose:** Cross-check every claim in a target document against its source list and live URLs, assign a verdict per claim, and produce an audit report.
> - **Called by:** the Verifier agent (`agent-verifier.md`), after Agents 1, 2, 4, and 5.
> - **Inputs:** the caller's **target file** and **source list**. This skill is written with Agent 1's files as the running example (`reports/literature-review.md` vs `reports/law-sources.md`), but the Verifier applies the same procedure to any target/source pair it is given.
> - **Outputs:** `reports/verification-report.md` (audit log), the target file patched in place with a verification banner at the top, an entry in `logs/patch-log.md`, and a warning line appended to `logs/agent1-status.md` if integrity < 80%.

---

## Step 1: Extract All Claims

Read the target file (e.g. `reports/literature-review.md`) and extract every sentence or passage that:
- Cites a specific source by name or number
- States a legal fact (a law passed, a penalty amount, a date, a jurisdiction)
- Attributes a finding to an organisation or author

Log each as:
```
Claim [N]: "[paraphrased claim]"
Source cited: [source name or number as it appears in the review]
Location: [theme/section name in literature-review.md]
```

---

## Step 2: Match to the source list

For each claim, find the matching entry in the source list (e.g. `reports/law-sources.md`).

**Match = FOUND** if:
- The source name, author, or URL in the source list corresponds to what's cited
- The annotated summary in the source list is consistent with how the claim uses it

**Match = NOT FOUND** if:
- No entry in the source list corresponds to the cited source
- The source exists but its summary contradicts the claim

**Match = PARTIAL** if:
- The source exists but the claim overstates, understates, or slightly misrepresents it

---

## Step 3: Web-Fetch Spot Checks

For every NOT FOUND and PARTIAL match, and for a random 20% sample of FOUND matches:

1. Take the URL from the source list (or search for the source if no URL)
2. `web_fetch` the page
3. Confirm: does the source actually say what the claim attributes to it?

Log each spot check:
```
Spot check [N]:
- Claim: [N]
- URL fetched: [url]
- Result: CONFIRMED / CONTRADICTED / UNREACHABLE / PARTIAL
- Notes: [what the source actually says, in 1 sentence]
```

If a URL is unreachable, try one web search for the source title to find an
alternative URL. If still unreachable, mark as UNVERIFIABLE.

---

## Step 4: Verdict Per Claim

Assign each claim one of:

| Verdict | Meaning |
|---|---|
| `VERIFIED` | Source found, spot check confirmed, claim is accurate |
| `VERIFIED-UNSPOTCHECKED` | Source found in law-sources.md, not spot checked |
| `OVERSTATED` | Source exists but claim goes beyond what it says |
| `UNDERSTATED` | Source exists but claim misses important nuance |
| `WRONG-SOURCE` | Claim is attributed to the wrong source |
| `UNSUPPORTED` | No matching source found anywhere |
| `UNVERIFIABLE` | Source cited but URL dead and no alternative found |

---

## Step 5: Write reports/verification-report.md

```markdown
# Verification Report: Literature Review Audit
**Agent:** Verifier
**Date:** [YYYY-MM-DD]
**Files checked:** reports/literature-review.md, reports/law-sources.md
**Total claims extracted:** N
**Spot checks performed:** N

---

## Summary

| Verdict | Count | % |
|---|---|---|
| VERIFIED | N | N% |
| VERIFIED-UNSPOTCHECKED | N | N% |
| OVERSTATED | N | N% |
| UNDERSTATED | N | N% |
| WRONG-SOURCE | N | N% |
| UNSUPPORTED | N | N% |
| UNVERIFIABLE | N | N% |

**Overall integrity score:** N% (VERIFIED + VERIFIED-UNSPOTCHECKED) / total claims

---

## Claims Requiring Correction

[List only OVERSTATED, UNDERSTATED, WRONG-SOURCE, UNSUPPORTED, UNVERIFIABLE]

### Claim [N] — [VERDICT]
- **Original:** [what the literature review says]
- **Issue:** [what's wrong]
- **Correction:** [what it should say, or "remove if unsupported"]
- **Source:** [URL or law-sources.md entry]

---

## Full Claim Log

[Every claim with its verdict — for audit trail]

| # | Claim (brief) | Source cited | Verdict | Spot checked |
|---|---|---|---|---|
| 1 | ... | ... | VERIFIED | Yes |
...
```

---

## Step 6: Apply Corrections In Place

Apply the corrections identified in Step 4 directly to the target file (e.g.
`reports/literature-review.md`) — do not create a separate copy:

- **OVERSTATED:** Soften the language to match what the source actually says
- **UNDERSTATED:** Add a brief qualifier noting the nuance
- **WRONG-SOURCE:** Correct the citation to the right source
- **UNSUPPORTED:** Add a `[UNVERIFIED — source not confirmed]` inline flag
- **UNVERIFIABLE:** Add a `[UNVERIFIABLE — source URL dead]` inline flag

Change only the specific wrong phrase or sentence — never rewrite prose, restructure
sections, or add new content. Log every applied patch to `logs/patch-log.md`
(claim | original text | patched text | reason | source used to verify).

At the top of the target file, add:
```
> **Verification status:** Audited by Verifier Agent on [date].
> Integrity score: N%. See reports/verification-report.md for full audit log.
```

---

## Step 7: Quality Gate

Before finishing, confirm:

- [ ] Every claim in the target file has a verdict
- [ ] All NOT FOUND and PARTIAL matches were spot-checked
- [ ] `reports/verification-report.md` contains a full claim log
- [ ] The patched target file carries the verification banner at the top (patched in place)
- [ ] Integrity score is ≥ 80% — if below 80%, flag for human review before the next agent proceeds

If integrity score < 80%, write this warning in `logs/agent1-status.md`:
```
⚠️ VERIFIER WARNING: Integrity score below 80%. Human review recommended before Agent 2 proceeds.
```

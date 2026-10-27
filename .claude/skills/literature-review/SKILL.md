---
name: literature-review
description: |
  Use this skill to synthesise collected sources into a structured written literature review.
  Always run AFTER the literature-search skill has produced an annotated source list.

  Trigger for:
  - "Write a literature review on X"
  - "Synthesise these sources into a review"
  - "Summarise what the research says about X"
  - Any agent pipeline step where sources have been collected and need to be written up

  Don't trigger for:
  - Source gathering (use literature-search for that)
  - Single source summaries
  - Report writing (use the law-report skill for that)
license: MIT
---

# Literature Review

> ## Pipeline Header
> - **Purpose:** Synthesise the collected sources into a thematic written review (themes, agreements, conflicts, gaps).
> - **Called by:** Agent 1 (`agent1-law-researcher.md`), Phase 2.
> - **Input:** `reports/law-sources.md` (from the `literature-search` skill).
> - **Output:** `reports/literature-review.md`.
> - **Next skill:** `law-report` consumes both files.

This skill governs how to synthesise a collected source list into a coherent, structured
literature review. The input is an annotated bibliography (from the literature-search skill).
The output is a written review that identifies themes, agreements, conflicts, and gaps
across the sources.

The goal is synthesis, not summary — do not go source by source. Group sources by theme
and let the argument drive the structure.

---

## Step 1: Read and Organise Sources

Before writing, read the full source list and organise sources into clusters:

- **What themes emerge across multiple sources?** (e.g., "age verification gaps", "enforcement weakness")
- **Where do sources agree?** Note consensus positions
- **Where do sources conflict?** Flag explicitly — do not smooth over disagreements
- **What is missing?** Note gaps in the literature

Write out 4–8 themes before drafting. These become your section headings.

---

## Step 2: Structure

Use this structure for the literature review:

```
## 1. Introduction
   - Scope of the review (topic, jurisdictions, time range, source types)
   - Why this topic matters
   - Overview of what the review covers

## 2. [Theme 1]
   - What the sources say, synthesised across authors/laws
   - Points of agreement
   - Points of conflict (flagged explicitly)

## 3. [Theme 2]
   ... repeat for each theme ...

## 4. Gaps and Limitations
   - What the literature does not cover
   - Methodological weaknesses in existing studies
   - Jurisdictions or source types underrepresented

## 5. Conclusion
   - Key takeaways
   - What further research or investigation is warranted

## References
   - Full source list drawn from `reports/law-sources.md`
```

---

## Step 3: Writing Rules

- **Synthesise, don't summarise** — never go source by source; group by theme
- **Cite everything** — every claim must reference a source from the bibliography
- **Flag conflicts explicitly** — if Source A says X and Source B says Y, say so
- **Use plain language** — write for an intelligent non-specialist reader
- **No padding** — if a theme has only one source, say so and keep it brief
- **Recency matters** — weight recent sources more heavily on fast-moving topics
- **Never invent sources** — if you don't have a source for a claim, omit the claim

---

## Step 4: Quality Check

Before finalising, check:
- Every section has at least 2 sources (except flagged thin areas)
- No claims without citations
- Conflicts are noted, not smoothed over
- Gap Analysis is honest and specific
- Introduction accurately describes what the review covers

---

## Output

Save the literature review to `reports/literature-review.md`.

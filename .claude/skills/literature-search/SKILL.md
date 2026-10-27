---
name: literature-search
description: |
  Use this skill whenever sources need to be gathered systematically for a literature review,
  research brief, or evidence base — before any synthesis or writing happens.

  Trigger for:
  - Explicit source-gathering requests: "find papers on X", "search the literature for Y",
    "gather sources on Z", "find relevant laws and legislation about X"
  - Research prep: "what does the research say about X", "find academic articles on Y",
    "what laws exist around Z"
  - Agent pipelines: any step where an agent needs to collect evidence before writing a review
  - Multi-source tasks: requests that span academic papers, industry articles, AND legislation
    on a single topic
  - Jurisdiction-aware legal searches: "what are the US/UK/EU rules on X"

  Don't trigger for:
  - Synthesis or writing (use the literature-review skill for that)
  - Single quick fact lookups that don't require multi-source gathering
  - Tasks where the user already has their sources and just needs help writing
license: MIT
---

# Literature Search

> ## Pipeline Header
> - **Purpose:** Systematically gather and annotate sources before any synthesis — the evidence base for the legal research.
> - **Called by:** Agent 1 (`agent1-law-researcher.md`), Phase 1.
> - **Inputs:** a topic brief and jurisdiction/source-type context passed by the calling agent; the live web.
> - **Output:** an annotated source list, which Agent 1 saves to `reports/law-sources.md` (Step 6 format below).
> - **Next skill:** `literature-review` consumes that source list.

This skill governs how to systematically search for and collect sources across four categories:
academic papers, industry/news articles, laws and statutes, and regulatory/policy documents.
The output is a structured, annotated source list — ready to pass into a synthesis step or
used directly as a reference base.

The goal is breadth with quality filtering: covering all relevant source types, across the right
jurisdictions and time ranges, while screening out low-credibility or irrelevant results.

---

## Step 1: Decompose the Topic

Before issuing a single search, break the topic into its component dimensions. For each
dimension you will run separate, targeted queries.

Identify:
- **Core phenomenon** — what is the central subject? (e.g., "age verification on gaming platforms")
- **Sub-topics / mechanisms** — what aspects need sourcing? (e.g., "facial age estimation accuracy",
  "biometric spoofing", "child safety online")
- **Jurisdictions** — which legal/regulatory geographies apply? (e.g., US, UK, EU, global)
- **Time range** — seminal works only? Last 3 years? Current law?
- **Source types needed** — see Source Type Matrix below

Write out 6–12 targeted search queries before searching. Queries should be 2–6 words, specific,
and cover different angles.

---

## Step 2: Source Type Matrix

| Source Type | What it covers | Where to search | Priority signals |
|---|---|---|---|
| **Academic papers** | Empirical studies, technical evaluations, theoretical frameworks | Google Scholar, arXiv, PubMed, SSRN | Peer-reviewed, cited, institutional authors |
| **Industry / news articles** | Platform announcements, market data, expert commentary | Web search, trade publications, company blogs | Recency, named byline, reputable outlet |
| **Laws & statutes** | Binding legislation, acts of parliament, federal/state law | .gov, legislation.gov.uk, eur-lex.europa.eu, official gazettes | Official source, enactment date, jurisdiction |
| **Regulations & guidance** | Regulatory rules, agency guidance, enforcement notices | Regulator sites (FTC, Ofcom, EU Commission) | Official body, enforcement power |
| **Court cases** | Judicial interpretation, precedent, settlements | Court records, legal databases, news coverage | Court level, jurisdiction, outcome |
| **Policy reports** | Think tank analyses, NGO research, government studies | Organization websites, Google Scholar | Named authors, methodology transparency |
| **Standards** | Technical or industry standards | NIST, ISO, BSI, standards bodies | Official publication, version, year |

---

## Step 3: Search Execution

Run searches across all relevant dimensions. For each query:

**General rules:**
- Always search — never rely on memory for current legal status, recent papers, or live
  platform policies
- Start broad (1–3 words), then narrow (4–6 words) once you understand the landscape
- Use `web_fetch` when a result looks highly relevant — don't cite based on snippets alone
  for academic or legal sources

**For legislation specifically:**
- Query pattern: `[jurisdiction] [topic] law [year]` or `[jurisdiction] [topic] act`
- Always verify enactment status: proposed / passed / in force / repealed
- Note effective dates and amendment history
- Prefer `.gov`, `.gov.uk`, `eur-lex.europa.eu` over secondary summaries

**For academic papers specifically:**
- Query pattern: `[topic] research paper [year]` or `[topic] systematic review`
- Also try: `arxiv [topic]` for CS/AI/technical topics
- Full papers may be paywalled — capture title, authors, journal, year, DOI, and abstract if visible
- Prefer papers with institutional authors, clear methodology, and citation counts

**For recency:**
- Fast-moving topics (AI, regulation, platform policy): weight last 2–3 years heavily
- Established topics (privacy law, child psychology): include seminal older works too
- Always record publication year

---

## Step 4: Scale of Search

| Task size | Search calls | Coverage |
|---|---|---|
| Quick background | 3–5 | Core papers + 1–2 laws |
| Standard literature search | 8–15 | All source types, multiple jurisdictions |
| Comprehensive review | 15–25 | Full coverage, fetch key papers, resolve conflicts |

For comprehensive reviews: run separate passes per source type, then a gap-filling pass at the end.

---

## Step 5: Quality Filtering

**Include:**
- Peer-reviewed or institutionally published papers
- Official government/regulatory sources
- Named bylined journalism from reputable outlets
- Reports from established think tanks/NGOs with named authors
- Court rulings from official records

**Deprioritize or exclude:**
- Blog posts without named authors or institutional affiliation
- SEO-optimized "explainer" pages with thin original content
- Forums, Reddit, Quora
- Sources that only summarize other sources without original analysis
- Undated content on fast-moving topics

**Flag conflicts:** If two sources contradict each other (e.g., one says a law passed, another
says it didn't), note the conflict explicitly and search for a third source to resolve it.
Do not silently pick one.

---

## Step 6: Output Format

Return a structured source list organized by category. For each source:

```
### [Category]

1. **[Title]**
   - Authors / Organization: ...
   - Year: ...
   - Source / Outlet / Journal: ...
   - URL: ...
   - Relevance: 1–2 sentences on what it contributes to the topic
   - Key finding or provision: 1 sentence summary (in your own words)
   - Status (legislation only): [Proposed / Passed / In force / Repealed]
```

Close with a **Gap Analysis** noting:
- Source types or jurisdictions not well covered
- Topics where sources conflict
- Areas where the literature is thin and further searching is warranted

---

## Query Template Bank

**Academic:**
- `[topic] systematic review`
- `[topic] empirical study [year]`
- `[mechanism] accuracy evaluation`
- `[topic] [population] effects research`

**Legal / Legislative:**
- `[jurisdiction] [topic] law [year]`
- `[jurisdiction] [topic] act legislation`
- `[regulatory body] [topic] guidance`
- `[topic] bill congress senate [year]`

**Policy / Industry:**
- `[topic] policy report [organization]`
- `[regulator] enforcement [topic]`
- `[topic] white paper [year]`

**News / Articles:**
- `[topic] [year]` (recent coverage)
- `[platform or company] [topic] criticism`
- `[topic] expert analysis [year]`

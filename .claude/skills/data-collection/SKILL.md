---
name: data-collection
description: |
  Use this skill when Agent 2 needs to systematically search Reddit, Twitter/X,
  and the open web for personal accounts, forum posts, and news stories about
  child protection laws being bypassed on Roblox. Governs search strategy,
  query construction, source logging, and minimum data thresholds.

  Trigger for:
  - Starting Agent 2's Phase 1 collection run
  - Any instruction to "search Reddit/Twitter for bypass stories"
  - Re-running collection after a gap is found by the report-corrector skill

  Don't trigger for:
  - Cleaning or categorising already-collected data (use raw-data-handler)
  - Writing the synthesis report (use trend-report)
license: MIT
---

# Data Collection Skill

> ## Pipeline Header
> - **Purpose:** Agent 2's breadth-first search phase — collect real-world accounts of child-protection failures/bypasses on Roblox from Reddit, Twitter/X, and the web.
> - **Called by:** Agent 2 (`agent2-efficacy-researcher.md`), Phase 1.
> - **Inputs:** search queries (below); the `reddit-mcp` / `twitter-mcp` servers when available, plus web search/fetch.
> - **Output:** an in-progress raw log (Step 6 format) handed to the `raw-data-handler` skill — not yet a committed file.
> - **Next skill:** `raw-data-handler` cleans the log into `data/raw-data.md`.

This skill governs how Agent 2 searches for real-world accounts of child protection
failures and law bypasses on Roblox. The goal is breadth first, quality filtering second.

---

## Step 1: Understand What You Are Looking For

You are searching for **first-hand or reported accounts** of:

1. **Age bypass** — Users under 13 (or the local legal age) creating accounts without parental consent
2. **Content filter bypass** — Methods to expose minors to adult content on the platform
3. **Contact bypass** — Adults circumventing restrictions to contact minors privately
4. **Grooming accounts** — Patterns of adults using Roblox to groom children
5. **Law unawareness** — Parents or children unaware that legal protections exist
6. **Platform non-enforcement** — Platform failing to act on reports despite legal obligations
7. **Cross-platform escalation** — Contact starting on Roblox, moving to less regulated platforms

---

## Step 2: Reddit Search Strategy

**Preferred tool:** `search_reddit` MCP tool

**Target subreddits (search each separately):**
- `r/Roblox` — largest community, many parent/child accounts
- `r/RobloxHelp` — reports of problems and safety failures
- `r/Parenting` — parental concern accounts
- `r/onlinesafety` — policy-aware discussions
- `r/gaming` — cross-platform child safety discussions
- `r/childrenandtech` — tech safety for children
- `r/predators` — WARNING: approach carefully; only collect patterns, never details about victims

**Query bank — run ALL of these:**
```
Roblox predator story
Roblox grooming parent
Roblox age verification bypass
Roblox child contact adult
my child Roblox unsafe
Roblox COPPA violation
Roblox stranger contact kid
Roblox account underage
Roblox safety failure report
Roblox moderator did nothing
Roblox law bypassed
Roblox privacy settings child
```

**For each result:**
- Fetch the top-level post content
- Fetch top 10 comments if the post has 20+ comments — bypass stories often in replies
- Log the URL, subreddit, post date, upvotes (as proxy for credibility), and a paraphrased account

---

## Step 3: Twitter/X Search Strategy

**Preferred tool:** `search_twitter` MCP tool (requires TWITTER credentials in env)

**Query bank:**
```
Roblox child predator
Roblox grooming
Roblox age bypass
Roblox COPPA
Roblox minor unsafe
Roblox safety report ignored
Roblox stranger my kid
```

**Filtering rules for Twitter:**
- Only collect public posts (no DMs, no locked accounts)
- Prefer posts with engagement (replies/retweets) as credibility signal
- Skip posts that appear to be bot-generated or promotional
- Do NOT collect replies from minors about their own experiences — paraphrase only at the pattern level

---

## Step 4: Web Search Strategy

**Preferred tool:** Standard `web_search` + `web_fetch`

**Query bank:**
```
Roblox child predator news 2023 2024 2025
Roblox grooming case reported
Roblox parent safety complaint
Roblox COPPA FTC complaint
Roblox age verification failure investigation
Roblox child exploitation report
Roblox moderation failure news
journalist investigation Roblox child safety
```

**Source quality tiers for web:**
- **Tier 1:** News outlets with named journalists (BBC, Guardian, NYT, NBC, etc.)
- **Tier 2:** NGO and child safety org reports (NSPCC, IWF, NCMEC, Thorn)
- **Tier 3:** Parent/community blogs with named authors
- **Exclude:** Anonymous forums, SEO content farms, undated posts

---

## Step 5: Minimum Data Thresholds

Do NOT proceed to Phase 2 until all thresholds are met:

| Source | Minimum entries |
|---|---|
| Reddit posts/threads | 20 |
| Twitter/X posts | 10 |
| Web articles / news | 10 |
| **Total** | **40** |

If a threshold is not met, run additional queries before proceeding.
Log which threshold was missed and what additional searches were run.

---

## Step 6: Raw Log Format

For every data point collected, log in this format before passing to raw-data-handler:

```
### Entry [N]
- Platform: [Reddit / Twitter / Web]
- Source URL: [url]
- Date: [YYYY-MM or YYYY if month unavailable]
- Credibility signal: [upvotes / engagement / outlet tier / named author]
- Bypass type (initial tag): [from taxonomy in Step 1]
- Raw account (paraphrased, NO identifying details about minors):
  [2-4 sentences describing what was reported]
- Notes: [anything flagged — e.g. "may involve active harm", "jurisdiction unclear"]
```

---

## Step 7: Ethical Handling Rules

- **Never** reproduce full quotes containing a minor's name, age, school, or location
- **Never** link directly to posts that appear to involve an ongoing, unreported harm — flag for human review instead
- **Always** paraphrase; you are building a research record, not an archive of victim statements
- If you encounter a post where harm appears imminent or recent (within 7 days), add a **HUMAN REVIEW FLAG** to that entry and do not include it in the trend analysis

# Verification Report: Trend Report Audit
**Agent:** Verifier
**Date:** 2026-06-30
**Files checked:** trend-report.md, raw-data.md
**Total claims extracted:** 32
**Spot checks performed:** 10

---

## Summary

| Verdict | Count | % |
|---|---|---|
| VERIFIED | 8 | 25.0% |
| VERIFIED-UNSPOTCHECKED | 17 | 53.1% |
| OVERSTATED | 3 | 9.4% |
| UNDERSTATED | 1 | 3.1% |
| WRONG-SOURCE | 2 | 6.3% |
| UNSUPPORTED | 1 | 3.1% |
| UNVERIFIABLE | 0 | 0.0% |

**Overall integrity score: 78.1%** (25/32 claims VERIFIED or VERIFIED-UNSPOTCHECKED)

⚠️ **Score is below the 80% threshold. See agent1-status.md.**

---

## Claims Requiring Correction

### Claim 6 — WRONG-SOURCE
- **Original:** "Justin Adkins case (Entry 17): Contacted victim on Roblox in 2024, moved to Snapchat, used iPhone and Robux as inducements, coerced hundreds of explicit videos and photos. Roblox→Snapchat escalation documented by Florida AG press release."
- **Issue:** The Florida AG press release explicitly states Adkins "first interacted with the victim in 2024 on Fortnite, an online battle royale game." Roblox was part of the contact pattern (Robux sent alongside V-Bucks), but the initial contact platform was Fortnite, not Roblox. The trend report misattributes the initial contact platform. Raw-data Entry 17 carries a note flagging exactly this: "initial contact on Fortnite, not Roblox."
- **Correction:** "Justin Adkins case (Entry 17): First contacted victim on Fortnite in 2024, exchanged phone numbers, then moved the relationship to Snapchat. Adkins sent both V-Bucks (Fortnite currency) and Robux (Roblox currency) as inducements — Roblox was part of the contact pattern but was not the initial platform. He coerced hundreds of explicit videos and photos. Documented by Florida AG press release."
- **Source:** https://www.myfloridalegal.com/newsrelease/attorney-general-james-uthmeier-announces-arrest-extradition-snapchat-roblox-child

---

### Claim 11 — UNSUPPORTED
- **Original:** "A known predator was publicly identified by the Roblox community and went unaddressed for 18 months before he abducted and assaulted a 15-year-old [Entry 36]"
- **Issue:** Raw-data Entry 36 explicitly flags this claim as "[UNVERIFIABLE — a specific 18-month non-enforcement window predator case was attributed to this entry but is not confirmed in the Revealing Reality/The Gamer source; removed pending correct sourcing.]" Spot check of the source URL (The Gamer, Revealing Reality investigation) confirms the article contains no such individual case — it describes test account findings and the "systematic failure" quote. The 18-month claim is not present in Entry 36's source material and has been removed from the raw-data.
- **Correction:** Remove this specific factual claim or flag inline. The "Sonic Eclipse developer" case (Entry 10, 18-month inaction on IP+safety grounds) is a documented alternative that illustrates prolonged non-enforcement. Substitute: "A game developer creating sexually explicit content involving a 12-year-old received no safety-based enforcement response despite multiple community reports; action came only when Sega filed a copyright complaint [Entry 10]."
- **Source:** https://www.thegamer.com/roblox-child-safety-report-2025-adults-grooming-children-inappropriate-content/

---

### Claim 15 — OVERSTATED
- **Original:** "Robux as CSAM currency (Entry 23): A North Carolina lawsuit alleges a predator offered Robux in exchange for explicit photos from a 10-year-old."
- **Issue:** Raw-data Entry 23 explicitly flags: "[UNVERIFIABLE — state attribution to North Carolina not confirmed in source; general Robux-for-explicit-content pattern confirmed across multiple filings]." Spot check of the Entry 23 source URL (National Injury Advocates) confirms: no North Carolina case is named anywhere on the page. The state attribution is unverified.
- **Correction:** "Robux as CSAM currency (Entry 23): A lawsuit [state not confirmed in source] alleges a predator offered Robux in exchange for explicit photos from a 10-year-old girl. The general pattern of Robux used as CSAM transaction currency is confirmed across multiple filings."
- **Source:** https://www.nationalinjuryadvocates.com/10-critical-facts-about-roblox-child-grooming-every-parent-must-know/

---

### Claim 17 — OVERSTATED
- **Original:** "In the Oklahoma case (Entry 24), the perpetrator was in his 40s and posed as a 15-year-old."
- **Issue:** Raw-data Entry 24 explicitly flags: "[UNVERIFIABLE — state attribution to Oklahoma not confirmed in source; general Robux-as-trust-building-gift pattern confirmed across multiple filings]." The same source URL covers both Entry 23 and Entry 24; spot check confirmed no states are named for Robux-related cases.
- **Correction:** "In a case documented across multiple filings (Entry 24, state not confirmed in source), the perpetrator was in his 40s and posed as a 15-year-old, using Robux gifts as the primary trust-building tool before coercion."
- **Source:** https://www.nationalinjuryadvocates.com/10-critical-facts-about-roblox-child-grooming-every-parent-must-know/

---

### Claim 18 — WRONG-SOURCE
- **Original:** "Roblox's avatar-based identity system — where players 'rarely themselves' [Wikipedia citation, Entry 8] — structurally enables this misrepresentation without any detection mechanism."
- **Issue:** Spot check of the Wikipedia article (https://en.wikipedia.org/wiki/Child_safety_on_Roblox) confirmed the phrase "rarely themselves" does not appear in the article. Entry 8 in raw-data covers dark web bypass forums and Bloomberg Businessweek's investigation into filter evasion — not avatar identity. The quote is not attributable to Entry 8 or its source.
- **Correction:** Remove the "[Wikipedia citation, Entry 8]" attribution, or locate the correct source for the quote. The underlying point — that avatar-based identity enables misrepresentation — is supported by the grooming cases in GROOM entries but this specific quote lacks a verified source.
- **Source:** https://en.wikipedia.org/wiki/Child_safety_on_Roblox

---

### Claim 23 — OVERSTATED (Argentina component)
- **Original (in multiple sections):** "Documented in North Carolina, Oklahoma, and Argentina, predators used Robux offers as the initial incentive to coerce children…"
- **Issue:** Raw-data Entry 25 explicitly flags: "[UNVERIFIABLE — source confirms 'Latin America' and documented arrests but does not name Argentina specifically; jurisdiction tag changed to OTHER-LATAM]." Spot check of the Entry 25 source URL (fileabuselawsuit.com) confirms: the article references "Latin America" only — no jurisdiction within Latin America is named. "Argentina" in the trend report is an unsupported geographic specification.
- **Correction:** Replace "Argentina" with "Latin America (specific country not confirmed in source)". The compound claim at Claim 23 is also partially OVERSTATED because it combines the unverified NC and Oklahoma attributions; see Claims 15 and 17.
- **Source:** https://www.fileabuselawsuit.com/how-roblox-became-hunting-ground-for-pedophiles/

---

### Claim 28 — UNDERSTATED
- **Original (Jurisdiction Analysis, US Federal section):** "Entry 47 (state settlements totalling $34.5M+)"
- **Issue:** Raw-data Entry 47 itemises Alabama ($12.2M) + West Virginia ($11.08M) + Nevada ($12.5M) = approximately $35.78M, stated in raw-data as "~$35.8M." The trend-report's "$34.5M+" understates the raw-data figure by approximately $1.3M and does not match any derivable calculation from Entry 47's stated amounts. Note: the trend-report correctly states "combined ~$35.8M" in the Entry 41 representative evidence section (Theme 2), creating an internal inconsistency. The Jurisdiction Analysis figure is wrong; the Theme 2 figure is correct. Additional note: an independent external source (lawsuit-information-center.com) gives Nevada's settlement as $10M (not $12.5M), but since we are verifying against raw-data, the raw-data figure ($12.5M / ~$35.8M) is the reference.
- **Correction:** Change "state settlements totalling $34.5M+" to "state settlements totalling ~$35.8M" to match raw-data Entry 47 and the trend-report's own Theme 2 section.
- **Source:** raw-data.md Entry 47

---

## Spot Check Log

| # | Claim | URL fetched | Result | Notes |
|---|---|---|---|---|
| 1 | Claim 6 — Justin Adkins initial contact platform | https://www.myfloridalegal.com/newsrelease/... | CONTRADICTED | Source explicitly states initial contact was Fortnite; Roblox sent Robux alongside V-Bucks but was not the initiating platform |
| 2 | Claim 11 — 18-month predator window | https://www.thegamer.com/roblox-child-safety-report-2025-... | CONTRADICTED | Article contains no individual predator case or 18-month window; covers test account findings only |
| 3 | Claims 15, 17 — NC and Oklahoma Robux cases | https://www.nationalinjuryadvocates.com/10-critical-facts-about-roblox... | CONTRADICTED | No states named for Robux-for-explicit-content cases; AG lawsuits from TX, OK, LA, KY, FL mentioned but not in the Robux-case context |
| 4 | Claim 23 — Argentina attribution | https://www.fileabuselawsuit.com/how-roblox-became-hunting-ground-for-pedophiles/ | CONTRADICTED | "Latin America" only — Argentina not named |
| 5 | Claim 28 — settlement total $34.5M | https://www.lawsuit-information-center.com/roblox-sex-abuse-lawsuit.html | PARTIAL | External source gives Nevada as $10M (not $12.5M), total ~$33.28M — conflicts with both raw-data ($35.8M) and trend-report ($34.5M+). Verifying against raw-data: UNDERSTATED |
| 6 | Claim 9 — 675→13,316 CSAE statistic | https://milberg.com/news/13-year-old-groomed-kidnapped... | CONFIRMED | Milberg cites "Roblox's own internal data shows reports of suspected child sexual exploitation jumped from 675 in 2019 to 13,316 in 2023" |
| 7 | Claim 8 — Arkansas AG "two-stage pipeline" | https://www.biometricupdate.com/202606/arkansas-lawsuit-... | CONFIRMED | Exact quote confirmed; rejected internal safety proposals also confirmed |
| 8 | Claim 22 — arXiv contextual grooming weakness | https://arxiv.org/html/2605.04491 | CONFIRMED | Paper confirms system "grossly fails to detect unsafe content that emerges over the course of conversations" — grooming the largest gap category |
| 9 | Claim 26 — Hindenburg quote and 2% expense decline | https://hindenburgresearch.com/roblox/ | CONFIRMED | Both the "leadership doesn't want that" quote and 2% YoY decline in trust/safety expenses Q2 2024 confirmed |
| 10 | Claims 14, 10, 18 — Schlep; moderator ratio; "rarely themselves" | https://en.wikipedia.org/wiki/Child_safety_on_Roblox | CONFIRMED (14, 10) / NOT FOUND (18) | 10%+ stock decline confirmed; 3,000 moderators / 100M+ users confirmed; "rarely themselves" not found in article |

---

## Full Claim Log

| # | Claim (brief) | Source cited | Verdict | Spot checked |
|---|---|---|---|---|
| 1 | 95 accounts in 60 minutes; VPN eliminated CAPTCHA; no email/phone verification | Entry 1 | VERIFIED-UNSPOTCHECKED | No |
| 2 | Common Sense Media: "kids can quickly set up accounts claiming to be 18+" | Entry 1 | VERIFIED-UNSPOTCHECKED | No |
| 3 | Pre-Nov 2024: parental protections disabled by default; 13yo DOB → immediate 13+ access | Entry 4 | VERIFIED-UNSPOTCHECKED | No |
| 4 | Facial verification bypassed with parent's/sibling's ID or low-cost document services | Entry 6 | VERIFIED-UNSPOTCHECKED | No |
| 5 | Iowa trafficking: 37yo posed as teenager, 13yo left grandmother's home, trafficked across states | Entry 20 | VERIFIED | Yes |
| 6 | Justin Adkins "contacted victim on Roblox in 2024, moved to Snapchat" | Entry 17 | WRONG-SOURCE | Yes |
| 7 | German far-right: two perpetrators, two 12yo, WWII-themed games → Discord with Nazi content | Entry 43 | VERIFIED-UNSPOTCHECKED | No |
| 8 | Arkansas AG "two-stage predatory pipeline" exact quote | Entry 41 | VERIFIED | Yes |
| 9 | 675→13,316 CSAE (1,873% increase) from Roblox internal data | Entry 34 | VERIFIED | Yes |
| 10 | ~3,000 moderators for 100M+ daily users; 1 per 33,000 | Entry 35 | VERIFIED | Yes |
| 11 | Known predator unaddressed 18 months; abducted and assaulted 15yo | Entry 36 | UNSUPPORTED | Yes |
| 12 | Roblox rejected internal safety proposals (Arkansas AG allegation) | Entry 38 | VERIFIED | Yes |
| 13 | Sentinel AI submitted 1,200 NCMEC reports in H1 2025 | Entry 34 | VERIFIED-UNSPOTCHECKED | No |
| 14 | Schlep C&D caused 10%+ stock decline | Entry 37 | VERIFIED | Yes |
| 15 | North Carolina lawsuit: Robux for explicit photos from 10yo | Entry 23 | OVERSTATED | Yes |
| 16 | Timothy O'Conner taught victim to disable parental controls, escalated to Discord | Entry 18 | VERIFIED-UNSPOTCHECKED | No |
| 17 | Oklahoma case: perpetrator in 40s posed as 15yo, used Robux | Entry 24 | OVERSTATED | Yes (via Claim 15 spot check) |
| 18 | Avatar system — players "rarely themselves" [Wikipedia citation, Entry 8] | Entry 8 | WRONG-SOURCE | Yes |
| 19 | Until 2024 adults could DM children of any age; Snapchat solicited in public chat | Entry 12 | VERIFIED-UNSPOTCHECKED | No |
| 20 | Whisper chat unmonitored until Jan 2026; San Mateo County grooming case identified | Entry 13 | VERIFIED-UNSPOTCHECKED | No |
| 21 | 13yo-DOB accounts could publicly link Facebook, YouTube, Twitch, X | Entry 14 | VERIFIED-UNSPOTCHECKED | No |
| 22 | arXiv (May 2026): strong on one-shot violations; weak on contextual grooming over days | Entry 11 | VERIFIED | Yes |
| 23 | Robux as CSAM currency in North Carolina, Oklahoma, and Argentina | Entries 23, 24, 25 | OVERSTATED | Yes |
| 24 | FTC complaint by NCOSE/Fairplay (May 2026): Robux exchange rate obfuscated | Entry 30 | VERIFIED-UNSPOTCHECKED | No |
| 25 | Multiple plaintiffs relied on PEGI 7 / ESRB Everyone 10+ ratings | Entry 33 | VERIFIED-UNSPOTCHECKED | No |
| 26 | Hindenburg: "leadership doesn't want" safety measures; 2% YoY trust/safety decline Q2 2024 | Entry 32 | VERIFIED | Yes |
| 27 | Nevada settlement $12.5M + structural obligations including online safety awareness funding | Entry 47 | VERIFIED-UNSPOTCHECKED | No |
| 28 | State settlements totalling "$34.5M+" (Jurisdiction Analysis section) | Entry 47 | UNDERSTATED | Yes |
| 29 | Connecticut AG investigation May 2026; 8 states with active proceedings | Entry 48 | VERIFIED-UNSPOTCHECKED | No |
| 30 | NY Senator Gounardes "flood" of cases; compliance ≠ child safety acknowledgement | Entry 49 | VERIFIED-UNSPOTCHECKED | No |
| 31 | NCMEC logged 546,000 online-enticement reports in 2024; 192% jump over 2023 | Entry 39 | VERIFIED-UNSPOTCHECKED | No |
| 32 | 764/CVLT networks groomed children 10–17 on Roblox; FBI issued warnings | Entries 28, 46 | VERIFIED-UNSPOTCHECKED | No |

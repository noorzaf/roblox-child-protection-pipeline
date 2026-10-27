# Literature Review: International Child Protection Laws Applicable to Online Gaming Platforms (Roblox Focus)

Synthesis of 38 verified sources from `law-sources.md` (Phase 1, verified by the Verifier agent — integrity score 97%, see `patch-log.md`).

---

## 1. Introduction

This review synthesises 38 sources — primary legislation, regulatory guidance, court cases and enforcement actions, academic papers, and policy reports — addressing how child protection law applies to online gaming platforms, with Roblox as the focal case. Coverage spans the United States (federal and state), the European Union, the United Kingdom, Australia, Brazil, India, South Korea, and the UN/international framework, with sources ranging from COPPA's 1998 enactment to developments as recent as May 2026.

The topic matters because Roblox sits at the intersection of nearly every regulatory category this body of law addresses: it collects personal data from children, operates a virtual currency and player-to-player economy (Robux), provides default chat and user-generated content (UGC) features, and serves a predominantly under-18 global user base of 88M+ daily active users [UNVERIFIABLE — figure not found in law-sources.md; Roblox's own SEC filings reported ~97.8M DAU for Q1 2025, suggesting this figure may be outdated]. As of mid-2026, Roblox faces an active FTC complaint, multiple state attorney general suits, and a consolidated multidistrict litigation (MDL 3166) — making this not a hypothetical compliance exercise but a live, multi-front legal exposure.

The review is organised around seven themes: (2) the collapse of self-declaration and the fragmented rise of age assurance; (3) consent thresholds and the patchwork "age of childhood" (the 13–17 gap); (4) design-by-default standards, dark patterns, and addictive engagement features; (5) monetisation, virtual currencies, and advertising to minors; (6) enforcement track records and the shift toward design-liability litigation; (7) the unresolved "social media vs. gaming" classification question. Section 8 sets out gaps and limitations in the literature itself, and Section 9 concludes.

---

## 2. The Collapse of Self-Declaration and the Fragmented Rise of Age Assurance

There is strong cross-jurisdictional consensus that **self-declared age is no longer treated as a meaningful safeguard** — but equally strong divergence on what should replace it, and at what cost.

5Rights Foundation's foundational taxonomy (Item 36) concludes that self-declaration "provides no meaningful assurance and should not be relied upon for risk-relevant features," a framing later cited by both the ICO and Ofcom. Yet the most recent empirical evidence — the LSE/5Rights "Impact of Regulation on Children's Digital Lives: Phase 2" study (Item 37), which tracked 108 child-safety design changes across 70 platforms between 2024–2026 — found that despite 12 distinct age-assurance methods now in circulation industry-wide, **11 of the 70 platforms studied still rely on self-declaration alone**. This is the central empirical finding of the literature: regulatory consensus has moved well ahead of platform practice.

Legally, jurisdictions are responding in markedly different ways:

- **UK**: The Online Safety Act 2023 (Item 10) mandates "highly effective" age verification or estimation to prevent children encountering primary priority content, operationalised by Ofcom's Protection of Children Codes of Practice (Item 19, in force from July 2025), which apply specifically to gaming platforms with chat, avatars, matchmaking, and livestreaming.
- **Brazil**: The Digital ECA (Item 13, in force March 2026) goes furthest among sources reviewed, **explicitly prohibiting simple self-declaration of age** for "electronic games" and requiring under-16 accounts to be linked to a verified legal guardian.
- **US states**: Rather than mandating platform-level verification, Utah's App Store Accountability Act and Texas's 2025 app-store provisions (Items 5, 4) shift the verification burden upstream to Apple and Google — a structurally different model with direct implications for how a distributed platform like Roblox would be age-gated.
- **California**: The CAADCA's age-estimation provision (Item 3) remains **legally unresolved** — the Ninth Circuit's March 2026 ruling (Item 30) reinstated the law's "covered businesses" definition but specifically remanded the age-estimation requirement to the district court, leaving its constitutional status open.

A significant **conflict** runs through this theme. The EDPB's Guidelines 3/2025 (Item 18) names this directly as the "age-assurance paradox": DSA Article 28 obligates platforms to take measures protecting minors, while GDPR's data-minimisation principle cautions against collecting the additional identity data many verification methods require. The EDPB's preferred resolution — privacy-preserving, "double-blind" verification where neither platform nor verifier can link identity to activity — remains aspirational rather than widely implemented. The EFF (Item 38) goes further, arguing that mandatory age verification of *any* kind imposes surveillance and exclusion costs on the entire user base (citing ~34.5 million US adults without current ID, documented racial and trans-specific bias in facial age-estimation systems, and loss of anonymity for domestic violence survivors, LGBTQ+ youth, and journalists). DSA Article 28(3) (Item 8) attempts to thread this needle by clarifying that compliance does not require collecting *additional* personal data — but the Commission's own July 2025 guidelines (Item 17) do not fully resolve how platforms should reconcile this with the Article 28(1) duty to take "appropriate and proportionate measures."

Finally, Australia's social media minimum-age law (Item 12) illustrates a separate dimension of the age-assurance question: scope. Gaming platforms — including Roblox by name in subsequent advocacy framing (Item 26) — are **explicitly excluded** from the definition of "age-restricted social media platform," meaning no age-verification mandate under this law applies to Roblox in Australia at all, regardless of how the verification-method debate above is eventually resolved. This carve-out is examined further in Section 7.

---

## 3. Consent Thresholds and the Patchwork "Age of Childhood" (the 13–17 Gap)

A platform operating globally — as Roblox does — must navigate at least four materially different legal definitions of "child" for consent purposes, none of which align:

| Jurisdiction | Threshold for heightened protection | Source |
|---|---|---|
| US (COPPA) | Under 13 | Items 1, 2 |
| EU (GDPR Art. 8) | Under 16 by default, Member States may set 13–16 | Item 7 |
| UK (Children's Code) | "Likely to be accessed by children" — applied up to PEGI-16-rated services, i.e., effectively under 18 | Item 9 |
| India (DPDP Act/Rules) | Under 18 | Item 15 |
| Brazil (Digital ECA) | Under 16 requires guardian linkage | Item 13 |

This patchwork is the literature's clearest articulation of what this review terms the "13–17 gap" (a framing anticipated in the source list's entry for Item 34, though not used in the source list's own Gap Analysis section). In the US specifically, COPPA's bright-line cutoff at age 13 (Items 1, 2) means that the 13–17 cohort — a substantial share of Roblox's user base — falls outside federal data-privacy protection entirely once they pass that threshold, even though the design and monetisation features implicated in current Roblox litigation (Items 26–29) do not become less relevant to a 14-year-old than a 12-year-old. The American University WCL paper (Item 34) makes this argument directly, concluding that "COPPA's age-13 cutoff and notice-and-consent model are insufficient given modern platform design and data practices."

The Mercatus Center policy brief (Item 33) provides the clearest counter-perspective in the literature: it evaluates proposals such as the Kids Online Safety Act (KOSA) to extend COPPA-style protections to teenagers, but raises a **substantive conflict** — extending verifiable-consent and data-restriction regimes to 13–17-year-olds raises anonymous-speech and First Amendment concerns that do not arise (or arise less acutely) for under-13s, who have no independent constitutional speech interest recognised in this context. This is the same First Amendment fault line that produced the CAADCA injunction (Items 3, 30) — suggesting that any future US attempt to close the 13–17 gap legislatively will likely face the identical constitutional objection.

By contrast, the UK's "likely to be accessed by children" standard (Item 9) and Brazil's under-16 guardian-linkage requirement (Item 13) sidestep the binary cutoff problem by applying graduated, design-based obligations across the full under-18 range rather than a single hard age threshold — though neither has yet been tested against a First-Amendment-equivalent challenge, since neither jurisdiction has an analogous doctrine.

---

## 4. Design-by-Default: Privacy Settings, Dark Patterns, and Addictive Engagement Features

Outside the US, there is substantial convergence on the principle that platforms likely to be accessed by children should be **privacy-protective and disengagement-friendly by default**, not as an opt-in choice.

The UK Children's Code (Item 9) — 15 standards including high-privacy defaults, geolocation off by default, no "nudge techniques" toward lower privacy, and profiling off by default — was operationalised for game developers specifically by the ICO's 2023 guidance (Item 20), which recommends privacy-protective defaults, parental control tools, and "natural breaks/checkpoints" in gameplay design, and confirms that any game rated PEGI 16 or below falls within scope (squarely covering Roblox).

The EU's parallel framework arrived later but goes further on engagement mechanics specifically. The European Commission's July 2025 guidelines on DSA Article 28(1) (Item 17) recommend private-by-default minor accounts, restrictions on stranger contact, modified recommender systems, and — notably — **disabling addictive design features (streaks, autoplay, push notifications) by default**, plus prohibiting screenshotting or downloading of minors' content. This is the most granular design-standard articulation in the reviewed literature and maps closely onto features central to Roblox's product (chat with strangers, algorithmic experience recommendations, virtual-currency "streaks" and notifications).

The US presents a sharp **conflict** on this theme. California's AADC (Item 3) attempted a broadly similar design-code approach to the UK/EU model — Data Protection Impact Assessments, default privacy-protective settings, prohibitions on data use "materially detrimental" to children's wellbeing — but NetChoice v. Bonta (Item 30) found these provisions likely unconstitutional as content-based speech regulation under First Amendment strict scrutiny, with the Ninth Circuit's March 2026 ruling upholding the injunction on five of six challenged provisions. **The same design principles that are binding regulatory requirements in the UK and (via guidelines) the EU are, in their California legislative form, currently unenforceable in the US.**

However, a separate US legal track has emerged that reaches similar substantive ground via tort law rather than design-code legislation. FTC v. Epic Games (Item 22) — the largest COPPA penalty to date ($275M) plus a $245M consumer-redress order — established that **default-on chat exposing children to harassment** and dark-pattern purchase flows are themselves COPPA/FTC Act violations, independent of any design-code statute. Massachusetts v. Meta (Item 31), the highest-court precedent reviewed, extended this logic by holding that Section 230 does not immunise claims that a platform's *design features* (e.g., addictive engagement mechanics) injure children — distinguishing "design defect" claims from third-party-content claims. Taken together, Items 22 and 31 suggest that in the US, the EU/UK's regulatory design standards are being approximated through litigation and enforcement settlements rather than ex ante statutory mandates — a structurally different (and more case-by-case) accountability mechanism.

---

## 5. Monetisation, Virtual Currencies, and Advertising to Minors

This theme is where the literature most directly anticipates the allegations now levelled at Roblox specifically.

The EU's DSA Article 28(2) (Item 8) bans presenting profiling-based advertisements to users a platform knows, with reasonable certainty, are minors. The Commission's July 2025 guidelines (Item 17) go further, **explicitly naming "virtual currencies and loot boxes"** as commercial practices that can exploit children's lack of "commercial literacy" — i.e., their reduced ability to understand that virtual currency represents real money. Brazil's Digital ECA (Item 13) independently arrives at a similar position, banning profiling-based advertising and certain immersive (AR/VR/emotion-recognition) advertising techniques aimed at minors.

South Korea (Item 16) is the most prescriptive jurisdiction reviewed on monetisation mechanics specifically: monthly spending caps for under-18 users (KRW 70,000 / ~US$60), mandatory transparent disclosure of loot box probabilities, and a 2025 E-Commerce Act amendment targeting "dark patterns" in digital commerce generally. No other jurisdiction in this review imposes a hard spending cap.

US enforcement provides the closest direct precedents to the Roblox situation. FTC v. Epic Games (Item 22) penalised dark-pattern purchase flows that tricked users — including children — into unintended V-Bucks (virtual currency) purchases. FTC v. Cognosphere/HoYoverse (Item 24, January 2025) penalised a company for obscuring the real-money cost of in-game purchases and the odds of obtaining items via loot-box mechanics, and required the company to block under-16 users from making in-game purchases without parental consent.

The NCOSE/Fairplay FTC complaint against Roblox (Item 26, filed May 2026) applies this exact analytical template to Robux: it alleges the platform's "obfuscated Robux exchange rate" and "engagement-maximizing design features, virtual currency system, and voice/text chat" are "developmentally inappropriate," echoing the Epic and Cognosphere theories of liability almost point for point. Read alongside Items 22 and 24, this complaint is not a novel legal theory but an application of an already-established FTC enforcement pattern to a new platform.

A notable **gap** emerges here: none of the laws or enforcement actions reviewed directly address **player-to-player virtual economies** — i.e., cases where the "currency" in question can be earned, traded, or monetised by other users (including minor creators), as distinct from a simple platform-to-consumer purchase flow. South Korea's loot-box rules (Item 16) and the FTC's Epic/Cognosphere actions (Items 22, 24) all concern platform-operator-to-consumer transactions. Robux's creator-economy dimension — where child developers can earn real-world income — sits outside the scope of every monetisation-focused source reviewed.

---

## 6. Enforcement Track Record: Penalty Regimes and the Shift to Design-Liability Litigation

The FTC enforcement record (Items 22–25) shows an escalating and increasingly specific pattern: Epic Games ($275M COPPA penalty — the largest ever — plus $245M in consumer redress, 2022/2023), Microsoft/Xbox ($20M, 2023, for collecting full birthdate/contact data before any parental-consent check), Cognosphere/Genshin Impact ($20M, January 2025, for loot-box and purchase-cost obfuscation), and Disney ($10M, September 2025, under an expanding "actual knowledge" theory covering child-directed content even when mislabeled). Each of these establishes a specific factual pattern — default-on chat, pre-consent data collection at signup, obscured purchase mechanics, and platform-level knowledge of child-directed content — and **each pattern has a direct analogue in the allegations against Roblox** (Items 26–29): Roblox's self-declared-birthdate signup mirrors the Xbox theory (Item 23); its Robux exchange-rate allegations mirror Epic and Cognosphere (Items 22, 24); and the MDL's framing of "alleged knowledge that predators used the platform" (Item 29) mirrors the Disney "actual knowledge" theory (Item 25), albeit applied to safety rather than advertising classification.

Roblox's own litigation exposure has expanded rapidly within the source window: the NCOSE/Fairplay FTC complaint (Item 26, May 2026, investigation pending), Louisiana's suit (Item 27, August 2025, the first state AG suit, alleging no effective age verification and citing specific harmful UGC "experiences"), and Texas's suit (Item 28, November 2025, the third state to sue after Kentucky and Louisiana, relying on the 2023 SCOPE Act's consumer-protection provisions — the same statutory basis previously used against TikTok), with Florida and Oklahoma filing similar suits since, per Item 28. These have been consolidated into MDL 3166 (Item 29, December 2025), now covering 162 cases across 12 districts, with a settlement master appointed in February 2026 and negotiations ongoing as of the report date.

A central **conflict** in the literature concerns *which legal vehicle* is more durable for holding platforms accountable for design choices. Two parallel tracks emerge:

1. **Legislative design codes** (CAADCA, Item 3) — enjoined on First Amendment grounds (Item 30), with the core design-mandate provisions currently unenforceable.
2. **Common-law design-defect litigation** (Massachusetts v. Meta, Item 31; MDL 3166, Item 29) — the Massachusetts Supreme Judicial Court's April 2026 ruling that Section 230 does not bar "design defect" claims represents binding state-supreme-court precedent, and the MDL's framing of Roblox's issues as "systemic, platform-wide design issues" (Item 29) tracks this same theory.

The literature suggests that, at least in the US, **litigation under a design-defect/Section-230-exception theory is currently the more legally viable accountability path** than legislative design-code mandates — the opposite of the UK/EU position, where Article 28 guidelines (Item 17) and the Children's Code (Item 9) operate as binding *ex ante* regulatory standards without an equivalent constitutional obstacle.

---

## 7. The Unresolved "Social Media vs. Gaming" Classification Question

This theme surfaces a genuine, unresolved normative disagreement that the source list explicitly flags as a conflict rather than something to be smoothed over.

Australia's Online Safety Amendment (Social Media Minimum Age) Act 2024 (Item 12) defines "age-restricted social media platforms" by name (Facebook, Instagram, Snapchat, TikTok, YouTube, Reddit, X, Threads, Twitch, Kick) and **explicitly excludes online gaming services** from this definition. The eSafety Commissioner's framing (Item 21) presents this exclusion as a deliberate, narrow policy choice — avoiding "regulatory overlap" with Australia's existing classification (ratings) scheme for games, while still subjecting gaming platforms to baseline "Basic Online Safety Expectations" under the Online Safety Act 2021 (Items 11, 21).

Set against this, the NCOSE/Fairplay complaint against Roblox (Item 26) — and the broader child-safety advocacy framing it represents — argues that a UGC platform with default chat, stranger contact, and engagement-maximising design presents risks that are **functionally indistinguishable from social media**, regardless of whether the product is taxonomically a "game." The early implementation reports on Australia's ban (cited within Item 12's entry) noting "significant circumvention by minors" raise the further question of whether minors displaced from banned social media platforms migrate toward gaming platforms like Roblox that fall outside the ban's scope entirely — a second-order effect not directly addressed by any source in this review but a logical implication of Items 12 and 26 read together.

The UK takes the opposite definitional approach. The Online Safety Act 2023 (Item 10) defines its scope around "user-to-user services," and Ofcom has explicitly stated that **gaming platforms with chat/UGC functionality fall within scope** — with the Protection of Children Codes (Item 19) issuing gaming-specific guidance covering chat, avatars, matchmaking, and livestreaming risks (grooming, harassment, harmful content) on the same footing as social media.

The result is a genuine jurisdictional split: **UK law is architected so that a platform like Roblox is in-scope by definition; Australian law is architected so that it is out-of-scope by definition** — and both are considered settled, deliberate policy choices within their respective frameworks, not oversights. This review does not resolve which approach is correct; it notes the split as a structural fact that any cross-jurisdictional compliance analysis of Roblox must account for separately in each market.

---

## 8. Gaps and Limitations

Several limitations in the underlying source base constrain the conclusions above:

- **Jurisdictional gaps.** Canada is entirely absent from the literature search despite being explicitly required coverage — no Canadian child-online-safety legislation (including the status of the federal Online Harms Act, Bill C-63) was identified. South Korea's coverage (Item 16) is limited to monetisation/loot-box and dark-patterns regulation; its broader child-data-privacy framework (e.g., PIPA provisions on minors) is unaddressed.

- **Primary-source access.** Several foundational legal texts — 16 CFR Part 312 (COPPA Rule, Items 1–2), the EUR-Lex texts of GDPR and DSA Article 28 (Items 7–8) — could not be fetched directly due to access restrictions and are sourced via consistent secondary legal-industry summaries (corroborated across multiple independent law firms). GDPR Article 8 (Item 7) was the exception, verified directly via gdpr-info.eu. This means specific statutory section-number citations for COPPA's 2025 amendments and DSA Article 28 should be treated as well-corroborated but not independently primary-verified.

- **Thin academic literature on UGC gaming platforms specifically.** The three academic sources (Items 32–34) address COPPA and GDPR effectiveness generally; none focuses on UGC gaming platforms or virtual economies as a distinct category. Most "Roblox-specific" material in this review (Items 26–29) is journalism, law-firm commentary, or plaintiff-firm litigation summaries — useful for establishing the *legal* landscape but not independently verified accounts of Roblox's actual internal practices.

- **Item 35 (UNICEF Innocenti working paper).** Originally expected to be a key gaming-specific UN-affiliated source, its confirmed title — "Protecting Children in Online Gaming: Mitigating Risks from Organized Violence" — indicates a focus on extremism/organised-violence recruitment rather than the virtual-economy and age-assurance themes central to this review. Full text remains unverifiable after repeated fetch attempts; its relevance to the themes above is now uncertain rather than established.

---

## 9. Conclusion

Across 38 sources spanning eight jurisdictions and 28 years of legal development, several conclusions stand out:

1. **Self-declaration as an age-assurance method is now broadly discredited in principle but still common in practice** (Items 36–38) — the gap between regulatory consensus and platform implementation is itself a primary finding.

2. **The "age of childhood" varies by a factor of more than 30% across major jurisdictions** (13 in the US, 16 default in the EU, up to 18 in the UK/India/Brazil), and this patchwork directly produces the "13–17 gap" that leaves Roblox's core demographic outside the US's primary federal child-privacy statute (Items 1, 7, 9, 13, 15, 34).

3. **The EU and UK have moved to binding, granular, ex ante design standards** (default privacy, disabled addictive features, banned profiling ads to minors — Items 8, 9, 17, 19, 20), while **the equivalent US legislative approach (CAADCA) remains enjoined on First Amendment grounds** (Items 3, 30) — pushing US accountability toward common-law design-defect litigation instead (Items 22, 31).

4. **Monetisation regulation is most advanced in South Korea (hard spending caps, odds disclosure) and is increasingly an FTC enforcement priority in the US** (Items 16, 22, 24), but **no jurisdiction reviewed directly addresses player-to-player virtual economies** of the kind Robux represents — a structural gap that sits at the heart of, yet is unaddressed by, the current allegations against Roblox.

5. **Whether a UGC gaming platform should be regulated as "social media" remains genuinely unresolved** and is answered oppositely by UK and Australian law (Items 10, 12, 19, 21) — meaning Roblox's regulatory classification is not a single global question but a per-jurisdiction one.

Roblox's current legal exposure (Items 26–29) sits at the convergence point of nearly every gap identified above simultaneously: the 13–17 consent gap, the self-declaration-vs-verification unresolved transition, the absence of virtual-economy-specific monetisation rules, and the unsettled social-media/gaming classification question. Further research should prioritise: (a) Canada's framework and South Korea's general child-data regime, both currently absent; (b) the outcome of the CAADCA age-estimation remand (Item 30) and the MDL 3166 settlement (Item 29), both pending as of the report date; and (c) independent (non-litigation, non-platform) empirical research on UGC virtual economies and child users, which does not currently exist in the reviewed literature.

---

## References

Numbering follows `law-sources.md`.

**Laws & Statutes**
1. Children's Online Privacy Protection Act (COPPA), 15 U.S.C. §§ 6501–6505 (1998)
2. Children's Online Privacy Protection Rule, 16 CFR Part 312 — 2025 Amendments
3. California Age-Appropriate Design Code Act (CAADCA), Cal. Civ. Code §§ 1798.99.28–1798.99.40
4. Texas SCOPE Act (HB 18, 2023) and 2025 App Store Accountability provisions
5. Utah Social Media Regulation Act (2023) and App Store Accountability Act (2024)
6. Louisiana Act 456 (2023)
7. General Data Protection Regulation (GDPR), Regulation (EU) 2016/679 — Article 8
8. Digital Services Act (DSA), Regulation (EU) 2022/2065 — Article 28
9. UK Age Appropriate Design Code ("Children's Code")
10. UK Online Safety Act 2023
11. Online Safety Act 2021 (Cth) (Australia)
12. Online Safety Amendment (Social Media Minimum Age) Act 2024 (Cth)
13. Estatuto Digital da Criança e do Adolescente ("Digital ECA") (Brazil)
14. UN Convention on the Rights of the Child — General Comment No. 25 (2021)
15. India — Digital Personal Data Protection Act 2023 and DPDP Rules 2025
16. South Korea — Juvenile Protection Act; Game Industry Promotion Act; E-Commerce Act amendment 2025

**Regulations & Guidance**
17. European Commission — Guidelines on the protection of minors under Article 28(1) DSA (July 2025)
18. EDPB Guidelines 3/2025 on the interplay between the DSA and the GDPR
19. Ofcom — Protection of Children Codes of Practice (April 2025)
20. ICO — Guidance on Children's Code compliance for game developers (2023)
21. eSafety Commissioner (Australia) — Basic Online Safety Expectations & Age-Restricted Material Codes

**Court Cases & Enforcement Actions**
22. FTC v. Epic Games, Inc. (2022/2023)
23. FTC v. Microsoft Corporation (Xbox) (2023)
24. FTC v. Cognosphere Pte. Ltd. (Genshin Impact / HoYoverse) (January 2025)
25. FTC v. The Walt Disney Company (September 2025)
26. National Center on Sexual Exploitation & Fairplay — FTC Complaint against Roblox (May 2026)
27. Louisiana v. Roblox Corporation (August 2025)
28. Texas v. Roblox Corporation (November 2025)
29. In re: Roblox Corporation Child Sexual Exploitation and Assault Litigation, MDL No. 3166
30. NetChoice v. Bonta (California AADC litigation)
31. Massachusetts v. Meta Platforms, Inc. (Section 230 ruling, April 2026)

**Academic Papers**
32. Birrell et al. — "SoK: Technical Implementation and Human Impact of Internet Privacy Regulations" (2023)
33. Mercatus Center — "Protecting Children Online: Evaluating Possible Reforms in the Law and the Application of COPPA" (2023)
34. American University WCL — "Child Privacy in the Digital Era: Is COPPA Enough?" (2024)
35. UNICEF Innocenti — "Protecting Children in Online Gaming: Mitigating Risks from Organized Violence" (2025) [UNVERIFIABLE]

**Policy Reports**
36. 5Rights Foundation — "But How Do They Know It Is a Child?" (2021)
37. Digital Futures for Children (LSE) & 5Rights Foundation — "Impact of Regulation on Children's Digital Lives: Phase 2" (2026)
38. Electronic Frontier Foundation — "10 (Not So) Hidden Dangers of Age Verification" (December 2025)

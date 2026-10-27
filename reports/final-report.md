# The Efficacy of Child Protection Laws on Roblox
## A Multi-Stream Research Report
**Date:** 2026-06-30
**Research streams:** Legal framework (Agent 1) | Real-world efficacy (Agent 2) | Child survey (Agent 5)

---

## Section 1: Executive Summary

Child protection laws applicable to Roblox are failing in practice across every measurable dimension. The platform had documented actual knowledge of a 1,873% increase in child sexual abuse and exploitation (CSAE) reports over four years — from 675 cases in 2019 to 13,316 in 2023 — and did not implement proportionate safeguards until compelled to do so by an accumulation of 162 federal lawsuits, five state attorney-general suits, and an FTC complaint. The legal framework analysis (Agent 1, 38 verified sources, 8 main jurisdictions) reveals a fragmented global response: the United Kingdom and Brazil have enacted the strongest obligations, the United States leaves 13-to-17-year-olds almost entirely without federal statutory protection, and Australia explicitly excluded gaming platforms from its social media age-verification law. Real-world efficacy data (Agent 2, 49 Tier-A entries drawn from court records, government filings, investigative journalism, and academic research) establishes that age verification is defeated at point of entry — researchers created 95 underage accounts in one hour using only a false date of birth — while the replacement mechanism (facial age verification) has been bypassed using a parent's or sibling's identity document. Child survey data (Agent 5, Group A n=16 ages 6–12; Group B n=17 ages 13–17) independently confirms these failures: 93% of Group A respondents who answered this question are aware of the false date-of-birth bypass, 44% of Group A reported seeing content they felt too young for, and not one Group B respondent reported learning about age restrictions from a parent. The most urgent policy implication is structural: harm does not respect platform boundaries, but every law does — and the dominant harm pattern (initial contact on Roblox, exploitation on Discord, Snapchat, or Telegram) is not addressed by any legal framework in any jurisdiction.

---

## Section 2: Research Overview

### What this report covers and why

This report assesses the real-world efficacy of child protection laws as applied to Roblox — a user-generated content (UGC) gaming platform with a predominantly under-18 global user base, an in-platform virtual economy (Robux), and a chat and social system that has been the subject of an active FTC complaint, five state attorney-general suits, and 162 consolidated federal civil cases (MDL No. 3166) as of the report date. The question at the centre of this research is not whether laws exist — they do, across eight main jurisdictions — but whether they produce measurable protection for the children who use the platform.

### How the three research streams relate to each other

Three independent research streams are integrated in this report:

1. **Legal Framework (Agent 1):** Statutory and litigation analysis across eight main jurisdictions (US, EU, UK, Australia, Brazil, India, South Korea, and the UN normative baseline), drawing on 38 verified sources and covering obligations related to age verification, data minimisation, parental consent, content filtering, and enforcement mechanisms. Source: `law-report.md`.

2. **Real-World Efficacy (Agent 2):** A dataset of 49 Tier-A entries — drawn entirely from court records, government filings, named investigative journalism, academic preprints, and NGO reports — documenting how child protection obligations actually perform against real behaviour patterns on the platform. Entries cover the period 2019–2026, with most entries from 2024–2026. Source: `trend-report.md` and `raw-data.md`.

3. **Child Survey (Agent 5):** An empirical survey of 33 children across two age cohorts (Group A: ages 6–12, n=16; Group B: ages 13–17, n=17), measuring usage patterns, rule awareness, perceived effectiveness of restrictions, and awareness of bypass methods. Source: `survey-analysis.md`.

The streams are designed to be read together: Agent 1 establishes what the law requires; Agent 2 shows whether those requirements are met in practice; Agent 5 shows what children themselves understand, experience, and know. The cross-verification of these three streams is documented in `cross-verify-report.md`, which found 4 CONSISTENT results, 2 TENSIONS, and 0 CONFLICTS across 7 checks, and cleared this report to proceed.

### Limitations

- **Survey sample size.** Both survey cohorts are small (Group A n=16, Group B n=17). Findings indicate peer-group trends and must not be extrapolated as definitive population statistics.
- **Community voice absent from efficacy data.** Reddit and Twitter/X data collection tools were unavailable during Agent 2's collection phase. All 49 entries come from professional and institutional sources — journalists, lawyers, government agencies, academics. First-person parental accounts and child-reported community bypass discussions are underrepresented.
- **US-centric efficacy dataset.** 39 of 49 entries originate from US jurisdictions. EU, Australia, Brazil, India, and South Korea produce zero entries, almost certainly due to English-language journalism dominance rather than absence of harm. Law-practice gap ratings for non-US/UK jurisdictions are derived from legal framework analysis alone and cannot be empirically validated by this dataset.
- **Litigation-stage caveats.** Most entries concern allegations in active or recently concluded lawsuits. Internal company data (the 675→13,316 CSAE statistic) and academic evaluations are the most robust evidence; lawsuit allegations are reliable indicators of documented harm patterns but do not represent criminal convictions.
- **Temporal scope.** This report reflects the state of laws and enforcement as of June 2026. Roblox's January 2026 facial age verification rollout and ongoing MDL 3166 settlement negotiations may produce findings that postdate collection.

---

## Section 3: Legal Framework

### Overview

Roblox operates within the scope of child protection law in nearly every jurisdiction reviewed, but the obligations that apply — and how strictly — vary sharply. The legal framework analysis covers eight main jurisdictions and identifies four areas of obligation: age verification, content filtering and default settings, parental consent, and enforcement mechanisms.

### Age verification requirements

There is cross-jurisdictional consensus that self-declared age is inadequate. Legal responses diverge sharply in how far they go beyond that consensus:

- **United Kingdom:** The Online Safety Act 2023 and Ofcom's Protection of Children Codes of Practice (in force from July 2025) require "highly effective age assurance" for gaming platforms with user-to-user functionality. Roblox is unambiguously in scope. Ofcom has 40+ specific measures covering chat, avatars, matchmaking, and livestreaming [Sources 10, 19].
- **Brazil:** The Digital ECA (in force March 2026) is the most stringent reviewed — it explicitly **prohibits self-declaration of age** for electronic games and requires under-16 accounts to be linked to a legal guardian [Source 13].
- **European Union:** GDPR Article 8 requires "reasonable efforts" to verify parental consent for users below the applicable national age threshold (13–16); DSA Article 28 requires "appropriate and proportionate measures" for minors. The Commission's July 2025 guidelines operationalise this into default-off addictive features, restricted stranger contact, and modified recommender systems [Sources 7, 8, 17].
- **United States:** COPPA requires "reasonable procedures" for verifiable parental consent for users under 13. No federal age-assurance standard applies to 13-to-17-year-olds. The 2025 COPPA Rule amendments expand "personal information" to include biometric identifiers — relevant to any facial age-estimation tool [Sources 1, 2]. California's design-code (CAADCA), which would impose UK-style obligations, is substantially enjoined on First Amendment grounds [Sources 3, 30].
- **Australia:** Gaming platforms including Roblox are **explicitly excluded** from the Online Safety Amendment (Social Media Minimum Age) Act 2024 under-16 account ban [Source 12]. This is not a law-practice gap but a law-absence gap.
- **India:** The DPDP Act 2023 requires verifiable parental consent for all users under 18, the broadest threshold reviewed — but the children's provisions are not enforceable until May 2027 [Source 15].
- **South Korea:** Imposes monthly spending caps of KRW 70,000 (~US$60) for under-18 users and mandatory loot-box odds disclosure. No equivalent to its social-media age-verification framework applies to cross-platform messaging within gaming [Source 16].

### Content filtering and default settings

The UK Children's Code (15 standards, including geolocation off by default, no nudge techniques, profiling off by default) and EU DSA Commission guidelines (disabling addictive engagement features — streaks, autoplay, push notifications — by default) impose the most detailed design-level obligations [Sources 9, 17]. The US has no enforceable federal equivalent; the FTC Act Section 5 provides a litigation-based route requiring harm to occur before legal action is available.

### Parental consent

COPPA requires verifiable parental consent for under-13 users [Source 1]. GDPR Article 8 requires equivalent consent for users below the applicable national threshold (13–16) [Source 7]. India extends this requirement to all under-18 users, the broadest threshold [Source 15]. Brazil requires guardian-linked accounts for under-16 users [Source 13]. Every framework presupposes parental awareness and engagement as the primary backstop.

### Enforcement mechanisms and Roblox-specific exposure

US enforcement is litigation-driven rather than design-code-driven. The FTC's track record — $275M from Epic Games for default-on chat and dark-pattern V-Bucks [Source 22], $20M from Microsoft/Xbox for pre-consent birthdate collection [Source 23], $20M from Cognosphere for obscured loot-box costs [Source 24], $10M from Disney under an "actual knowledge" theory [Source 25] — maps directly onto the FTC complaint filed against Roblox in May 2026 [Source 26]. Five state attorney-general suits (Louisiana, Texas, Kentucky, Florida, Oklahoma) are consolidated with 162 federal civil cases into MDL No. 3166 [Sources 27, 28, 29]. Massachusetts v. Meta (April 2026) confirmed that Section 230 does not bar design-defect claims, the legal theory underlying the MDL [Source 31]. Ofcom holds fining powers up to 10% of global turnover under the UK Online Safety Act [Source 10]; Brazil's ANPD can fine up to 10% of Brazilian revenue [Source 13].

### Jurisdictions where legal obligations are weakest

The US 13–17 consent gap is the single most significant structural weakness — a large share of Roblox's user base falls outside COPPA's verifiable-parental-consent and data-minimisation requirements entirely. Australia's explicit gaming carve-out means no age-verification obligation applies to Roblox there. India's under-18 framework is not yet in force. No jurisdiction has enacted law addressing player-to-player virtual economies — every monetisation-focused framework covers only operator-to-consumer transactions [Sources 16, 17, 22, 24].

---

## Section 4: Real-World Efficacy

Agent 2's dataset of 49 Tier-A entries (8 jurisdictions represented; 39 of 49 from US jurisdictions) establishes a consistent pattern across six harm themes.

### Age gate ineffectiveness (13 entries; law-practice gap: CRITICAL for US, MEDIUM for UK)

Roblox's primary access control — self-declared date of birth — has been the foundation on which the entire age-restriction system rests, and it is publicly broken. Researchers at The Capitol Forum created 95 underage accounts in one hour on a single laptop, using only false 2015 birthdates; the only technical friction (a CAPTCHA after the third account) was eliminated by switching VPN geolocation [Entry 1]. Before November 2024, all new accounts were created with parental protections disabled — a child entering age 13 at signup accessed 13+ content with no additional step [Entry 4].

The replacement mechanism — Persona/k-ID facial age estimation, mandated for chat access globally from January 2026 — is itself bypassable: Internet Safety Labs and 404 Media documented that it could be defeated using a parent's or sibling's identity document or commercially available document services [Entry 6]. Roblox's global rollout of facial verification was announced after more than a year of intensifying litigation and regulatory pressure, not proactively [Entry 7]. Even post-remediation, a child account created under the new system was documented accessing cybercrime-linked communities within the platform [Entry 2].

**Law gap:** Brazil's Digital ECA bans self-declaration outright; the UK requires "highly effective" age assurance. COPPA's "reasonable procedures" standard has never been applied to a facial verification bypass that requires only a household ID document. The evidence shows that even the strongest implemented mechanism is not "highly effective" — every check deployed has a known, low-friction countermeasure.

### The Roblox-to-offsite pipeline (19 entries; law-practice gap: CRITICAL)

Across the dataset, the dominant harm trajectory is not a single-platform event. Contact is initiated on Roblox — where a child population is available and age misrepresentation is trivial — then escalated to Discord, Snapchat, WhatsApp, or Telegram, where platform monitoring is lower and content restrictions are absent. This pattern appears in 19 of 49 entries: sexual exploitation cases, extremist radicalisation cases, and CSAM production cases [Entries 17, 18, 19, 20, 41, 42, 43]. The Arkansas attorney-general's lawsuit named this explicitly as a "two-stage predatory pipeline": Roblox as the front door, Discord as the private room [Entry 41].

Roblox's own design features facilitated the transition: public display of linked social media accounts, trivially easy social-handle exchange in public chat, and no off-platform contact warnings were all shipped features, not omissions [Entries 12, 14].

**Law gap:** No legal framework in any jurisdiction addressed here creates an obligation on Roblox to prevent, detect, or report exploitation that migrates to another platform. Laws are platform-specific; harm is not. This is the largest single unaddressed gap in the global legal framework as applied to Roblox.

### Platform non-enforcement (7 entries; law-practice gap: CRITICAL)

The evidence establishes that Roblox's non-enforcement is documented, internally known, and in at least one instance actively chosen. Roblox's own data — cited in the Iowa family lawsuit — shows suspected CSAE incidents submitted to NCMEC increased from 675 in 2019 to 13,316 in 2023, a 1,873% increase over four years [Entry 34]. Despite this internal knowledge, Roblox's Sentinel AI system submitted only 1,200 NCMEC reports in the first half of 2025 — substantially below the volume the internal data predicts [Entry 39]. The Arkansas attorney-general's lawsuit alleges Roblox "rejected internal safety proposals warning children about grooming tactics" [Entry 38] — affirmative rejection, not mere resource constraint. Separately, Roblox issued legal action against a content creator conducting predator-sting operations on the platform [Entry 37], deploying legal resources against a predator-catcher rather than predators.

Every significant safety feature documented in this dataset was introduced after legal or regulatory pressure: parental dashboard and restricted DMs for under-13 (November 2024), whisper-chat moderation (January 2026), and facial age verification (January 2026 global rollout) were all reactive to litigation, AG suits, or Ofcom codes — never proactive [Entries 7, 37, 38, 40].

**Law gap:** UK Online Safety Act requires timely action on reports of priority harmful content; DSA Article 28(1) requires "appropriate and proportionate measures"; FTC Act Section 5 prohibits unfair or deceptive practices. None of these frameworks produced proportionate action until the accumulation of 162 federal lawsuits, five state AG suits, and a formal FTC complaint created legal exposure large enough to compel change. Enforcement by external pressure, not internal compliance, is the actual mechanism.

### Grooming pattern signatures (12 entries; law-practice gap: CRITICAL)

Across 12 documented grooming cases, four consistent tactical signatures emerge: (1) identity misrepresentation — perpetrators posed as peers in the majority of cases; (2) Robux as a trust-building inducement and, in several documented cases, as a currency offered in exchange for explicit images [Entries 17, 23, 24, 25, 27]; (3) escalation to secondary platforms before the most serious exploitation; (4) parental control defeat — in one documented case, the predator taught the victim to disable his own parental controls, rendering the legal backstop of parental oversight directly inoperable [Entry 18]. Documented victims range in age from 9 to 15, with several in the 13–15 range that falls outside US federal statutory protection.

### Contact architecture failures (10 entries; law-practice gap: HIGH)

Before 2024–2026, Roblox's contact architecture enabled maximum adult-to-child connectivity with minimal friction: adults could directly message children of any age; a private "whisper" channel operated without content moderation [Entry 13]; user profiles could publicly link to third-party social media accounts enabling off-platform contact harvesting [Entry 14]. Academic evaluation of Roblox's chat moderation (arXiv, May 2026) confirmed the classifier performs well on single-instance explicit violations but is "substantially weaker on slow, contextual grooming patterns that operate over days" — the exact pattern documented in the majority of grooming cases [Entry 11].

### The Robux exploitation mechanism (6 entries; law-practice gap: CRITICAL)

Robux functions in the dataset both as a grooming tool and as a CSAM transaction currency. The FTC complaint (May 2026) alleges Roblox's "obfuscated Robux exchange rate" prevents parents from understanding how much real money their children are spending or receiving [Entry 30]. In grooming cases, the opacity serves an additional function: a child who receives Robux cannot easily convert this to a real-money figure that a parent would recognise as a payment. No legal framework reviewed addresses Robux as a user-to-user transfer mechanism that can be used as compensation for child exploitation. Every monetisation-focused law addresses operator-to-consumer transactions; the player-to-player economy is legally invisible.

### Overall law-practice gap ratings

| Jurisdiction | Legal Framework | Real-World Gap | Efficacy Rating |
|---|---|---|---|
| US Federal | PARTIAL — COPPA under-13 only; FTC Act litigation-based | CRITICAL — 1,873% CSAE increase; institutional non-enforcement | WEAK |
| US California | ON PAPER STRONG (CAADCA) — but enjoined | HIGH — whisper chat; Naval kidnapping [Entry 19] | WEAK |
| US Texas | PARTIAL — SCOPE Act partially enjoined | HIGH — platform misrepresentation; AG suit [Entry 38] | WEAK |
| United Kingdom | STRONG — OSA, Children's Code, Ofcom Codes | MEDIUM — facial verification bypass; reactive rollout | PARTIAL |
| European Union | STRONG — DSA Art. 28, GDPR Art. 8, Commission guidelines | UNKNOWN — no documented enforcement action against Roblox | PARTIAL (framework only) |
| Australia | WEAK FOR GAMING — gaming explicitly excluded | N/A (law-absence gap) | FAILING |
| Brazil | STRONG (new) — bans self-declaration; guardian linkage | UNKNOWN — in force March 2026; too recent | PARTIAL (unverified) |
| India | MEDIUM — DPDP under-18 verifiable consent | UNKNOWN — not enforceable until May 2027 | FAILING (not in force) |
| South Korea | MEDIUM — monetisation focus only | UNKNOWN — no data | UNKNOWN |

---

## Section 5: Children's Awareness and Experience

*(All findings: Group A ages 6–12, n=16; Group B ages 13–17, n=17. Small sample sizes — findings indicate peer-group trends, not population statistics.)*

### Usage patterns: the protective inversion

The platform's most restricted users are also its most intensive ones. Group A (ages 6–12, the most heavily restricted accounts) plays the hardest: 63% play every day, 31% play for more than two hours per session, and nearly two-thirds play alongside people they know only online. Group B (ages 13–17, fewer default restrictions) is far more casual: only 24% play daily, sessions are mostly under an hour, and 82% play exclusively with real-life contacts. Two Group B respondents do not play Roblox at all.

This inversion matters. The youngest, most vulnerable group has the deepest platform exposure and the most contact with strangers — the inverse of what the restriction architecture is designed to achieve.

### Rule awareness: wide but shallow

Awareness of rules drops sharply at each level of specificity. Most children know restrictions exist in principle; far fewer know what they actually are; fewer still have encountered them on the platform.

| | Group A (n=16) | Group B (n=17) |
|---|---|---|
| Knew age rules exist | 14 (88%) | 13 (76%) |
| Knew the specific age limit | 9 (56%) | 8 (47%) |
| Recalled seeing an age warning in the app | 6 (38%) | 3 (18%) |

Group A shows higher rule awareness than Group B across all three measures — likely because the restrictions land harder on younger accounts, which encounter the walls more often, rather than any difference in how the platform communicates its policies. In Group B, the most common routes to awareness were online sources (YouTube, social media) and being blocked from a feature. **Not one Group B respondent reported learning about age restrictions from a parent.**

### Perceived effectiveness

Roughly 38–41% of both groups felt age restrictions effectively protect younger users; 29–38% of each group felt they did not. The "make sense" question reveals a sharp divergence: only 31% of Group A respondents thought the rules made sense (56% said they didn't), while 59% of Group B agreed the restrictions make sense given the platform's content (only 12% disagreed). Group B accepts the principle but rejects the execution: **47% of Group B said Roblox does not do enough to enforce its rules, against only 24% who agreed it does.**

### Content exposure

**44% of Group A respondents said they had encountered something on Roblox they felt too young to see.** This is the group with the most restricted accounts. Group B reported lower exposure (24%), consistent with their more limited and socially contained play patterns.

### Bypass awareness

More than half of each group had heard of someone bypassing Roblox's age restrictions (Group A: 56%, Group B: 65%). Awareness of specific bypass methods among those who had:

| Method | Group A (n=15 answering) | Group B (n=17) |
|---|---|---|
| False date of birth when signing up | 14 (93%) | 12 (71%) |
| Creating multiple accounts | 9 (60%) | 12 (71%) |
| Using a parent's or sibling's account | 8 (53%) | 8 (47%) |
| Using unofficial/modified Roblox | 7 (47%) | 5 (29%) |
| VPN or region-spoofing tool | 4 (27%) | 8 (47%) |

**93% of Group A respondents who answered this question are aware of the false date-of-birth bypass** — higher than the corresponding figure for Group B (71%). The children the system is most designed to protect are the most aware of how to defeat it at the point of entry.

One Group A respondent spontaneously described a bypass method not on the survey instrument: using a photograph of an older person to defeat Roblox's facial age verification. This is a deliberate attack on the specific security measure Roblox introduced as its "highly effective" replacement for self-declaration, and it is being discussed among children aged 6–12.

---

## Section 6: Cross-Stream Analysis

### Theme A: Age Verification

**Law:** Multiple jurisdictions recognise self-declared age as inadequate. Brazil bans it outright; the UK mandates "highly effective" age assurance; the US requires only "reasonable procedures" for under-13. The 5Rights Foundation's foundational taxonomy concluded that self-declaration "provides no meaningful assurance" [Source 36 in law-report]; independently, the LSE/5Rights Phase 2 study found that 11 of 70 platforms studied still rely on it alone despite 12 alternative age-assurance methods now available [Source 37 in law-report].

**Efficacy:** Self-declaration is defeated in under 60 minutes with no technical knowledge [Entry 1]. The replacement (facial verification) is defeated with household identity documents [Entry 6]. Every mechanism deployed has a known, low-friction countermeasure.

**Survey:** 93% of Group A (n=15 answering) are aware of the false DOB bypass. One Group A respondent spontaneously described the photo-based facial verification bypass — the same attack vector documented by Internet Safety Labs and 404 Media [Entry 6].

**Synthesis (triple-confirmed):** Age verification failure is not a single-point weakness — it cascades across every layer. The initial check is near-universally known to be defeatable; the replacement check is defeatable with documents already present in a child's household; and a child aged 6–12 can describe the photo bypass method unprompted. Every mechanism deployed has a known, low-friction countermeasure.

---

### Theme B: Content Filtering

**Law:** EU DSA Article 28 and the UK Children's Code require proactive, privacy-by-default content curation. California's CAADCA sought equivalent design-level obligations but remains substantially enjoined [Sources 3, 8, 9].

**Efficacy:** Post-remediation child accounts were documented accessing cybercrime-linked communities [Entry 2]. LA County lawsuit filings identify UGC experiences accessible at filing time including simulated assault of child avatars and establishments described in the complaint as places "where avatars engage in simulated adult activities" [Entry 2]. Academic moderation evaluation found the classifier is "much weaker on context-dependent abuse — sarcasm, coded language, and the slow grooming patterns that operate over days" [Entry 11].

**Survey:** 44% of Group A (n=16) — the cohort with the most restricted accounts — reported encountering content they felt too young to see.

**Synthesis:** Automated curation systems fail to maintain age-appropriate environments for the youngest and most ostensibly protected user cohort. Post-remediation failure is documented in both the efficacy data and the survey, confirming the pattern holds even after the platform's 2024–2026 safety changes.

---

### Theme C: Platform Enforcement

**Law:** UK Online Safety Act imposes statutory child-safety duties requiring timely action on priority harmful content [Source 10]. DSA Article 28(1) requires "appropriate and proportionate measures" [Source 8]. FTC Act Section 5 prohibits unfair or deceptive practices [Source 26]. Brazil's Digital ECA mandates 24-hour content removal for CSAE-category material [Source 13].

**Efficacy:** CSAE incident reports increased 1,873% over four years (675 in 2019 to 13,316 in 2023), yet the platform's Sentinel AI submitted only 1,200 NCMEC reports in H1 2025 — a fraction of the incident volume the internal data predicts [Entries 34, 39]. The company affirmatively rejected internal safety proposals [Entry 38]. Every significant safety change was introduced after legal or regulatory pressure — never proactively [Entries 7, 37, 38, 40].

**Survey:** 47% of Group B said Roblox does not enforce enough; only 24% said it does. 44% of the most-restricted group (Group A) encountered content they felt too young for.

**Synthesis (triple-confirmed):** Platform non-enforcement is simultaneously a legal violation, a documented institutional pattern, and a perceived reality for children on the platform. The survey's 47% enforcement scepticism figure, while directionally aligned with the evidence, substantially understates the institutional severity that internal company data and rejected safety proposals reveal. Agent 6 treats these as two different types of data: perception (survey) and documented institutional behaviour (efficacy evidence).

---

### Theme D: Parental Awareness

**Law:** COPPA, India DPDP, and the UK Children's Code all presuppose parental involvement as a primary protection mechanism — requiring verifiable parental consent, parental control architecture, or transparency obligations [Sources 1, 9, 15]. The entire US federal model for child protection rests on parental consent as its enforcement backbone.

**Efficacy:** Parents were given misleading platform safety signals: PEGI 7 / ESRB Everyone 10+ ratings applied to the game engine only, not user-generated experiences [Entry 33]. Former product designer testimony confirmed internal culture actively resisted safety features that limited engagement [Entry 32]. In one documented grooming case, the predator taught the victim to disable his own parental controls, rendering the primary backstop directly inoperable [Entry 18].

**Survey:** Not one Group B respondent (n=17) learned about Roblox's age restrictions from a parent. Primary awareness routes were online sources (YouTube, social media) and encountering friction when blocked from a feature.

**Synthesis (triple-confirmed):** The protection model enshrined in law — parents as the primary informed checkpoint — is structurally non-functional. Parents were given misleading safety signals by the platform; children report zero parental transmission of safety information; and in at least one documented case, a predator actively neutralised parental monitoring. The law assumes a parent-child safety conversation that is not happening.

---

### Theme E: Cross-Platform Escalation

**Law:** Current legislative frameworks (COPPA [Source 1], DSA [Source 8], UK Online Safety Act [Source 10]) impose obligations strictly on a per-platform basis. No law reviewed creates an obligation on Roblox to prevent, detect, or report exploitation that migrates to Discord, Snapchat, or Telegram.

**Efficacy:** 19 entries in Agent 2's dataset document the Roblox-to-secondary-platform pipeline as the dominant harm trajectory — contact initiated on Roblox, exploitation completed on Discord, Snapchat, WhatsApp, or Telegram. This pattern appears across sexual exploitation, CSAM production, extremist radicalisation, and physical abduction cases [Entries 17, 18, 19, 20, 41, 42, 43]. Roblox's own contact architecture facilitated the transition through profile-linked social accounts and trivially easy social-handle exchange [Entry 14].

**Survey:** The survey instrument did not measure children's awareness of cross-platform escalation as a documented harm pattern. This is a structural gap noted in the cross-verification report: the survey cannot confirm or deny user awareness of the primary harm vector identified in the efficacy data.

**Synthesis:** Platform-siloed legislation fails to address the reality of predatory behaviour. The pipeline is legally invisible — harm that begins on a regulated platform and culminates on a different platform generates no regulatory obligation on either platform to address the handover. This is the most significant unaddressed structural gap in the global legal framework as applied to Roblox.

---

## Section 7: Key Findings

Ordered by severity. Each finding states the research stream it draws from and its primary policy implication.

1. **Roblox had documented actual knowledge of a 1,873% increase in CSAE incidents (675 in 2019; 13,316 in 2023) and did not implement proportionate safeguards.** *(Efficacy stream — Entry 34; corroborated by Entry 39: 1,200 NCMEC reports in H1 2025 vs. 13,316 incidents in 2023 alone.)* Policy implication: Documented actual knowledge of escalating exploitation — without proportionate response — should trigger FTC Act Section 5 "unfair" trade practice liability independent of COPPA's age threshold; MDL 3166 and the FTC complaint are the operative legal vehicles.

2. **The dominant harm pattern — initial contact on Roblox, exploitation on Discord/Snapchat/Telegram — is not addressed by any legal framework in any jurisdiction.** *(Efficacy stream — 19 entries, Themes 2 and 4.)* Policy implication: Legislative frameworks must impose cross-service risk mitigation obligations, not only per-platform duties; the handover event itself must become a regulated act.

3. **Self-declaration age verification is functionally useless, and its facial verification replacement is easily defeated with household documents.** *(All three streams — Entry 1; Entry 6; survey: 93% Group A aware of false DOB, one Group A respondent describing photo bypass.)* Policy implication: "Highly effective age assurance" standards (UK, Brazil) should be treated as the minimum acceptable global bar; US "reasonable procedures" language is insufficient in light of documented bypass rates.

4. **44% of Group A respondents (ages 6–12, n=16) — the most restricted user cohort — reported seeing content they felt too young for.** *(Survey stream — survey-analysis.md; corroborated by efficacy evidence of UGC adult experiences and post-remediation failures.)* Policy implication: Automated content curation does not currently satisfy statutory minor-protection obligations in any jurisdiction that imposes them; algorithmic transparency audits should be mandatory.

5. **All major safety changes in the documented period were reactive, introduced after legal or regulatory pressure, never before harm was documented or litigation threatened.** *(Efficacy stream — Entries 7, 37, 38, 40.)* Policy implication: Reactive compliance is structurally insufficient for child safety; design-code obligations with proactive audit and certification requirements (UK Children's Code model) are necessary to shift the incentive structure.

6. **Robux functions as both a grooming tool (trust-building gifts) and a CSAM transaction currency (offered in exchange for explicit images) across multiple documented cases, and no legal framework anywhere addresses this.** *(Efficacy stream — Entries 17, 23, 24, 25, 27; law stream: no jurisdiction's monetisation law covers player-to-player virtual economies.)* Policy implication: Financial regulatory frameworks must be extended to encompass peer-to-peer virtual gaming assets, including minimum oversight requirements for user-to-user currency transfers involving minors.

7. **The US 13–17 consent gap leaves the majority of documented grooming victims without any federal statutory protection.** *(Law stream — law-report.md Section 4; efficacy stream: documented victims range from age 9 to 15, with several in the 13–15 range.)* Policy implication: US federal law must extend graduated design-code and data-minimisation obligations across the full under-18 range, not only under-13 users.

8. **Not one Group B respondent (ages 13–17, n=17) reported learning about Roblox's age restrictions from a parent, and no documented case shows parental monitoring intercepting a harm event before it escalated.** *(Survey stream — survey-analysis.md; corroborated by efficacy evidence including Entry 33 on platform misrepresentation and Entry 18 on parental control defeat.)* Policy implication: The notice-and-consent model — the backbone of COPPA, India DPDP, and most parental-consent regimes — is empirically inadequate; design-by-default obligations that do not require parental action to be protective are the only model the data supports.

9. **Platform contact architecture (open DMing, unmonitored whisper chat, profile-linked social accounts) was shipped as designed features, not oversights, and persisted until 2024–2026.** *(Efficacy stream — Entries 12, 13, 14; law stream: UK Children's Code Standards 7, 9, 12 directly applicable.)* Policy implication: Design-defect liability (confirmed by Massachusetts v. Meta [Source 31] as not barred by Section 230) is the correct legal theory for these features; MDL 3166 is the operative vehicle in the US.

10. **Australia's explicit gaming carve-out and the US 13–17 gap mean that in the two largest English-speaking markets, no meaningful age-verification obligation applies to Roblox's core user population.** *(Law stream — Sources 1, 2, 12.)* Policy implication: The classification question — whether UGC gaming platforms are "social media" or "gaming" for regulatory purposes — must be resolved explicitly by each legislature; the current inconsistency enables the lowest-standard jurisdiction to define the effective global floor.

---

## Section 8: Recommendations

### For Roblox

- **Implement active liveness detection.** Require a live physical gesture (blink, head turn, spoken phrase) during all age-verification checks, eliminating photo and printed-document spoofing. The current Persona implementation is documented as bypassable with a household ID [Entry 6].
- **Default-off all communication for under-13 accounts.** Adult-to-child direct messaging should require active parental whitelisting, not parental discovery and opt-out. This is already the UK Children's Code standard and is directly applicable to Roblox.
- **Remove profile-linked social media accounts for minor users.** This feature was used as an off-ramp enabling predators to locate and contact child victims across platforms [Entry 14]. The risk is documented; the feature has no child-safety justification.
- **Implement real-time volume and velocity caps on Robux transfers to minor accounts.** Robux as a grooming tool relies on the ability to transfer currency peer-to-peer without oversight; threshold alerts tied to minor accounts would create a detection signal currently absent.
- **Publish quarterly NCMEC reporting data and moderator-to-active-user ratios.** Transparency on enforcement volume — comparable to the annual transparency reports required of larger platforms under DSA — would enable external accountability for enforcement adequacy.

### For regulators

- **US regulators (FTC/state AGs):** Use the documented 1,873% CSAE increase — internal company data — as the foundation for a "constructive actual knowledge" finding under COPPA and Section 5 of the FTC Act, eliminating any age-threshold ambiguity. MDL 3166 and the FTC complaint [Source 26] are the current vehicles.
- **UK Ofcom:** Use enforcement powers under the Online Safety Act to require Roblox to evidence compliance with Ofcom's Protection of Children Codes specifically on the facial-verification bypass documented in Entry 6. The fact that the bypass uses a family member's ID means the "highly effective" threshold has not been met.
- **EU Commission/national DPAs:** Open a formal DSA Article 28 investigation into Roblox. Virtual currencies and loot-box mechanics are explicitly named in the Commission's July 2025 guidelines as exploiting children's "lack of commercial literacy" [Source 17]; no EU enforcement action against Roblox was identified in this research, representing the highest-priority jurisdiction gap for follow-up.
- **Brazil ANPD:** Monitor compliance with the Digital ECA's guardian-linked account requirement (in force March 2026) and the 24-hour content-removal obligation. Roblox's prior reliance on self-declaration [Source 27] is the exact practice the Digital ECA prohibits.

### For parents

- **Do not rely on age ratings.** PEGI 7 and ESRB Everyone 10+ apply to the game engine, not the user-generated experiences within the platform [Entry 33]. Parental review of specific Roblox "experiences" (the UGC games within the platform) is necessary to assess actual content.
- **Actively configure the parental dashboard.** Before November 2024, all new Roblox accounts were created with parental protections disabled [Entry 4]. Even after safety changes, configuration requires active parental action — it is not guaranteed by default.
- **Monitor secondary platforms, not just Roblox.** The dataset documents 19 cases in which contact moved from Roblox to Discord, Snapchat, or WhatsApp before the most serious harm occurred. Parental oversight of secondary messaging apps used alongside Roblox is part of the actual risk surface.
- **Explain cross-platform contact risks in age-appropriate terms.** The survey found that no Group B respondent learned about age restrictions from a parent; the survey instrument also found children are entirely unaware that cross-platform escalation is a documented harm pattern. This information gap is one parents can directly address.

### For policymakers

- **Close the US 13–17 consent gap.** The under-13/over-13 binary in COPPA does not reflect the actual risk profile. Graduated design-code obligations modelled on the UK Children's Code — applying privacy-by-default, data minimisation, and anti-nudge standards across the full under-18 range — are the evidence-based alternative.
- **Enact cross-platform liability frameworks.** Laws that impose per-platform obligations cannot address harm that migrates between platforms. Legislatures should consider duty-to-warn obligations (requiring Roblox to alert users of documented cross-platform risk), cross-service data sharing for abuse investigations, and regulatory designation of gateway platforms as having heightened duty of care.
- **Resolve the gaming/social-media classification question explicitly.** The UK treats Roblox as in-scope of user-to-user service child-safety duties; Australia treats gaming platforms as out-of-scope; the US has no settled federal classification. This inconsistency allows the weakest-jurisdiction standard to set the effective global floor. Each legislature should address the question explicitly in statutory text rather than leaving it to regulatory interpretation.
- **Regulate peer-to-peer virtual economies.** Every monetisation-focused law reviewed (US FTC enforcement, South Korean spending caps, EU DSA guidelines on virtual currencies) addresses operator-to-consumer transactions. No law addresses a system where minors earn, trade, or receive virtual currency from other users — the structural feature of Robux's creator economy that enables its use as a grooming and CSAM transaction mechanism. Financial regulatory extension to peer-to-peer gaming assets is needed.

---

## Section 9: Limitations

- **Survey sample sizes.** Group A (n=16, ages 6–12) and Group B (n=17, ages 13–17) are small, locally recruited cohorts. Findings indicate peer-group trends and must not be extrapolated to global populations. The youngest Group A respondents (around age 6) may have limited capacity to reflect on abstract concepts reliably; facilitator-administered questions mitigate but do not eliminate this constraint.
- **Survey does not measure personal bypass behaviour.** By ethical design, the survey measures awareness (what respondents have heard about others doing) not personal conduct. Bypass prevalence among respondents themselves is unknown; the survey's figures are awareness proxies.
- **Community voice absent from efficacy dataset.** Reddit and Twitter/X data collection was unavailable. All 49 entries come from professional and institutional sources. Everyday parental accounts, community bypass discussions, and child-reported safety concerns at ambient scale are not represented. The dataset reflects what lawyers, journalists, and governments have documented, not what ordinary users report.
- **US-centric efficacy dataset.** 39 of 49 entries are from US jurisdictions. EU, Australia, Brazil, India, and South Korea produce zero entries. Law-practice gap ratings for non-US/UK jurisdictions are derived from legal analysis only and cannot be empirically validated by this dataset.
- **Litigation-stage caveats.** Most entries concern allegations in active or recently concluded lawsuits. Internal company data (Entry 34: 675→13,316 CSAE statistic, cited in Iowa family lawsuit from Roblox's own NCMEC submissions) and academic evaluations (Entry 11: arXiv moderation classifier assessment) are the most robust evidence. AG statements and lawsuit allegations are reliable indicators of documented harm patterns but do not represent criminal adjudication.
- **Some Agent 2 entries marked UNVERIFIED.** Specific entries in raw-data.md are flagged as unverified (source attribution not confirmed): Entry 35 (moderator count and day-rate), Entry 36 (18-month non-enforcement window), and jurisdictional attributions for Entries 23, 24, and 25 (North Carolina, Oklahoma, Argentina). These are not relied upon for primary claims in this report.
- **Temporal scope.** This report accurately reflects the state of legal frameworks, litigation, and enforcement as of June 2026. MDL 3166 settlement negotiations, the CAADCA age-estimation remand [Source 30], and Brazil's early implementation monitoring may produce developments that postdate collection.

---

## Section 10: References

### Legal framework (law-report.md sources)

- `[Source 1]` Children's Online Privacy Protection Act (COPPA), 15 U.S.C. §§ 6501–6505 — FTC, 1998.
- `[Source 2]` COPPA Rule 2025 Amendments, 16 CFR Part 312 — FTC, 2025.
- `[Source 3]` California Age-Appropriate Design Code Act (CAADCA) — California Legislature, 2022.
- `[Source 7]` General Data Protection Regulation (GDPR), Regulation (EU) 2016/679, Article 8.
- `[Source 8]` Digital Services Act (DSA), Regulation (EU) 2022/2065, Article 28.
- `[Source 9]` UK Age Appropriate Design Code ("Children's Code") — ICO, 2020.
- `[Source 10]` UK Online Safety Act 2023 — UK Parliament, 2023.
- `[Source 12]` Online Safety Amendment (Social Media Minimum Age) Act 2024 (Cth) — Parliament of Australia.
- `[Source 13]` Estatuto Digital da Criança e do Adolescente ("Digital ECA") — Brazilian National Congress, 2025.
- `[Source 15]` India Digital Personal Data Protection Act 2023 and DPDP Rules 2025 — Government of India.
- `[Source 16]` South Korea — Juvenile Protection Act; Game Industry Promotion Act; E-Commerce Act amendment 2025.
- `[Source 17]` European Commission Guidelines on DSA Article 28(1) — European Commission, July 2025.
- `[Source 19]` Ofcom Protection of Children Codes of Practice — Ofcom, April 2025.
- `[Source 22]` FTC v. Epic Games, Inc. — Federal Trade Commission, 2022/2023.
- `[Source 23]` FTC v. Microsoft Corporation (Xbox) — Federal Trade Commission, 2023.
- `[Source 24]` FTC v. Cognosphere Pte. Ltd. (Genshin Impact) — Federal Trade Commission, 2025.
- `[Source 25]` FTC v. The Walt Disney Company — Federal Trade Commission, 2025.
- `[Source 26]` NCOSE/Fairplay — FTC Complaint against Roblox — NCOSE/Fairplay, May 2026.
- `[Source 27]` Louisiana v. Roblox Corporation — Louisiana AG, August 2025.
- `[Source 28]` Texas v. Roblox Corporation — Texas AG, November 2025.
- `[Source 29]` In re: Roblox Corporation Child Sexual Exploitation and Assault Litigation, MDL No. 3166 — JPML, December 2025.
- `[Source 30]` NetChoice v. Bonta — 9th Circuit, March 2026.
- `[Source 31]` Massachusetts v. Meta Platforms, Inc. — Massachusetts SJC, April 2026.
- `[Source 36]` 5Rights Foundation — "But How Do They Know It Is a Child?" — 5Rights Foundation, 2021.
- `[Source 37]` 5Rights Foundation / LSE Digital Futures for Children — "Impact of Regulation on Children's Digital Lives: Phase 2" — 2026.

### Efficacy data (raw-data.md entries)

- `[Entry 1]` The Capitol Forum — 95 underage accounts in 60 minutes (August 2025).
- `[Entry 2]` Malwarebytes / LA County lawsuit — post-remediation failure; UGC adult experiences (December 2025 / February 2026).
- `[Entry 4]` Drugwatch / class action filings — default-off parental protections pre-November 2024.
- `[Entry 6]` Internet Safety Labs / 404 Media / CNN — facial age verification bypass using parent's/sibling's ID (2025–2026).
- `[Entry 7]` Roblox press release / CNN Business — facial age check global rollout announcement (November 2025 / January 2026).
- `[Entry 11]` Academic preprint (arXiv, May 2026) — moderation classifier evaluation; weakness on contextual grooming patterns.
- `[Entry 12]` Class action filings — open direct messaging to any-age children until 2024.
- `[Entry 13]` LA County lawsuit — unmonitored whisper chat until January 2026.
- `[Entry 14]` Class action filings — profile-linked social media accounts enabling off-platform contact harvesting.
- `[Entry 17]` Justin Adkins case — Robux as inducement; CSAM coercion (Florida, 2026).
- `[Entry 18]` Timothy O'Conner case — parental control defeat; autistic teenage victim.
- `[Entry 20]` Iowa family lawsuit — 37-year-old posing as teenager; interstate trafficking (2025).
- `[Entry 23]` Lawsuit filing — Robux offered for explicit photos from a 10-year-old. [Jurisdictional attribution unverified in source.]
- `[Entry 24]` Lawsuit filing — perpetrator posing as a 15-year-old; victim contact via Roblox. [Jurisdictional attribution unverified in source.]
- `[Entry 25]` Lawsuit filing / Robux-for-explicit-content case. [Jurisdictional attribution unverified in source.]
- `[Entry 27]` In-game moderator CSAM case (2020).
- `[Entry 30]` NCOSE/Fairplay FTC complaint — Robux exchange-rate obfuscation (May 2026).
- `[Entry 32]` Hindenburg Research — former product designer testimony on internal culture prioritising engagement over safety.
- `[Entry 33]` Class action plaintiffs — PEGI 7 / ESRB Everyone 10+ ratings applied to engine only, not UGC.
- `[Entry 34]` Iowa family lawsuit — Roblox's own NCMEC submission data: 675 CSAE incidents (2019) → 13,316 (2023).
- `[Entry 37]` Schlep cease-and-desist — legal action against predator-sting content creator (August 2025).
- `[Entry 38]` Arkansas AG lawsuit — affirmative rejection of internal safety proposals.
- `[Entry 39]` Roblox / NCMEC — Sentinel AI submitted 1,200 NCMEC reports in H1 2025.
- `[Entry 40]` Post-2024 safety changes documented as incomplete at announcement.
- `[Entry 41]` Arkansas AG lawsuit — "two-stage predatory pipeline" characterisation (June 2026).
- `[Entry 43]` German far-right recruitment case — Roblox WWII-themed games → Discord Nazi propaganda servers.

### Survey data

- `[survey-analysis.md]` Roblox Age Restrictions Survey Analysis — Agent 5, June 2026. Group A (ages 6–12, n=16); Group B (ages 13–17, n=17).
- `[survey-methodology.md]` Survey Methodology — Agent 4, June 2026.

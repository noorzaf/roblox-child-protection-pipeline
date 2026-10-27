# International Child Protection Laws: Applicability to Roblox

Compiled from `law-sources.md` (38 verified sources) and `literature-review.md` (thematic synthesis), as of June 2026.

---

## Executive Summary

Roblox — a user-generated content (UGC) platform with a default chat system, a player-driven virtual economy (Robux), and a predominantly under-18 global user base — sits within the scope of child-protection law in nearly every jurisdiction reviewed, but the laws that apply, and how strictly, vary widely. In the US, COPPA protects only under-13 users, leaving the 13–17 cohort largely uncovered by federal law, while a wave of FTC settlements against other gaming companies (Epic, Microsoft, Cognosphere, Disney) has established enforcement precedents — chat defaults, dark-pattern purchases, undisclosed birthdate collection — that map closely onto current allegations against Roblox itself. The EU and UK impose binding, design-level obligations (privacy-by-default, bans on profiling ads to minors, "highly effective" age assurance) that go further than anything enforceable in the US, where California's comparable design code remains enjoined on First Amendment grounds. Brazil's newly effective Digital ECA bans self-declared age outright. Australia's social-media age-verification law explicitly excludes gaming platforms, including Roblox. As of mid-2026, Roblox faces an active FTC complaint, five state attorney-general suits consolidated alongside related litigation into MDL 3166, and ongoing settlement negotiations — making this report's findings directly relevant to live legal exposure rather than abstract risk. The most significant unresolved issues are the 13–17 consent gap, the absence of any law addressing player-to-player virtual economies, and the unsettled question of whether UGC gaming platforms should be classified as "social media" for regulatory purposes.

---

## 1. Legislative Timeline

| Year | Law / Regulation | Jurisdiction | Key Provision | Status (as of June 2026) |
|---|---|---|---|---|
| 1998 | Children's Online Privacy Protection Act (COPPA) [Source 1] | US (federal) | Verifiable parental consent for collecting data from under-13s | In force |
| 2016/2018 | GDPR Article 8 [Source 7] | EU | Age of consent for information-society services: 16 default, Member States may set 13–16 | In force |
| 2020/2021 | UK Age Appropriate Design Code ("Children's Code") [Source 9] | UK | 15 standards incl. high-privacy defaults, no nudge techniques | In force |
| 2021 | Online Safety Act 2021 (Cth) [Source 11] | Australia | eSafety Commissioner; age-checks only for R18+ content | In force |
| 2021 | UNCRC General Comment No. 25 [Source 14] | International/UN | Child-rights due diligence for digital products | Authoritative interpretive guidance |
| 2022 | California Age-Appropriate Design Code Act (CAADCA) enacted [Source 3] | US (California) | Design-by-default obligations for services likely accessed by minors | Enjoined (see 2025–2026 below) |
| 2022 | Digital Services Act (DSA) enacted; Article 28 applicable Feb 2024 [Source 8] | EU | "Appropriate and proportionate" protection of minors; bans profiling ads to known minors | In force (Art. 28 since Feb 2024) |
| 2022/2023 | FTC v. Epic Games settlement [Source 22] | US (federal, FTC) | $275M COPPA penalty + $245M consumer redress for default-on chat and dark-pattern V-Bucks purchases | Settled |
| 2023 | UK Online Safety Act 2023 (Royal Assent Oct 2023) [Source 10] | UK | Statutory child-safety duties; "highly effective" age assurance | In force; Ofcom codes from 2025 |
| 2023 | Texas SCOPE Act (HB 18) [Source 4] | US (Texas) | Parental consent via "commercially reasonable method"; restricts targeted ads to minors | Partially enjoined (Aug 2024) |
| 2023 | Utah Social Media Regulation Act [Source 5] | US (Utah) | Age verification + parental consent for 5M+ account platforms | Enjoined (Sept 2024) |
| 2023 | Louisiana Act 456 [Source 6] | US (Louisiana) | Parental consent for under-16 social media accounts | Struck down (Dec 2025) |
| 2023 | FTC v. Microsoft (Xbox) settlement [Source 23] | US (federal, FTC) | $20M for collecting children's birthdate/contact data pre-consent | Settled |
| 2023 | India Digital Personal Data Protection Act passed [Source 15] | India | Verifiable parental consent for under-18 | Act in force; children's provisions enforceable from May 2027 |
| 2023 | South Korea loot box disclosure requirements [Source 16] | South Korea | Mandatory probability disclosure; under-18 monthly spending caps | In force |
| 2024 | Utah App Store Accountability Act [Source 5] | US (Utah) | Shifts age-verification duty to app stores (Apple/Google) | Enacted; implementation ongoing |
| 2024 | Online Safety Amendment (Social Media Minimum Age) Act 2024, effective Dec 10, 2025 [Source 12] | Australia | Bans under-16 accounts on named social media platforms; gaming explicitly excluded | In force (Dec 2025) |
| Jan 2025 | FTC v. Cognosphere (Genshin Impact) settlement [Source 24] | US (federal, FTC) | $20M for obscured purchase costs/loot-box odds | Settled |
| Feb 2025 | South Korea E-Commerce Act dark-patterns amendment [Source 16] | South Korea | Targets dark patterns in digital commerce | In force |
| Apr 2025 | COPPA Rule 2025 Amendments (16 CFR Part 312) [Source 2] | US (federal, FTC) | Expands "personal information" to biometric identifiers; new retention limits; separate consent for third-party ad disclosure | In force (effective June 23, 2025; phased through Apr 2026) |
| Apr 2025 | Ofcom Protection of Children Codes of Practice [Source 19] | UK | 40+ measures incl. highly effective age assurance for gaming platforms | In force (from July 2025) |
| Jul 2025 | EU Commission Guidelines on DSA Article 28(1) [Source 17] | EU | Flags virtual currencies/loot boxes; recommends disabling addictive design features by default | Non-binding but used as enforcement benchmark |
| Aug 2025 | Louisiana v. Roblox Corporation filed [Source 27] | US (Louisiana) | First state AG suit against Roblox | Active; consolidated into MDL 3166 |
| Sept 2025 | EDPB Guidelines 3/2025 [Source 18] | EU | Names the "age-assurance paradox" (DSA vs. GDPR tension) | Guidance (non-binding, influential) |
| Sept 2025 | FTC v. Walt Disney Company settlement [Source 25] | US (federal, FTC) | $10M; "actual knowledge" of child-directed content theory | Settled |
| Sept 2025 | Brazil Digital ECA enacted [Source 13] | Brazil | Bans self-declared age; guardian-linked under-16 accounts | Enacted; in force March 2026 |
| Nov 2025 | Texas v. Roblox Corporation filed [Source 28] | US (Texas) | Third state AG suit (after Kentucky and Louisiana), relies on SCOPE Act | Active; consolidated into MDL 3166 |
| Dec 2025 | MDL No. 3166 consolidation order [Source 29] | US (federal) | Consolidates 162 cases re: Roblox child sexual exploitation/design liability | Active; settlement negotiations ongoing |
| Mar 2026 | NetChoice v. Bonta — 9th Circuit ruling [Source 30] | US (California) | Reinstates "covered businesses" definition; remands age-estimation provision | Active; remanded |
| Mar 2026 | Brazil Digital ECA enters into force [Source 13] | Brazil | — | In force |
| Apr 2026 | Massachusetts v. Meta — Section 230 ruling [Source 31] | US (Massachusetts) | Section 230 does not bar platform-design-defect claims | Binding precedent (MA); national trend |
| May 2026 | NCOSE/Fairplay FTC complaint against Roblox [Source 26] | US (federal, FTC) | Alleges Robux exchange-rate obfuscation, developmentally inappropriate design | Investigation pending |

---

## 2. Laws by Jurisdiction

### United States

**Federal baseline — COPPA and the FTC Act**

COPPA [Source 1], in force since 2000, requires operators of services directed to, or with actual knowledge of, users under 13 to provide notice and obtain verifiable parental consent before collecting personal information, and to minimise data collection and secure it appropriately. The 2025 Rule amendments [Source 2] — effective June 23, 2025, with phased compliance through April 2026 — expand "personal information" to include biometric identifiers (face templates, voiceprints), require separate consent for third-party data disclosure used in targeted advertising, and impose new data retention limits. **Applies to:** any operator with actual knowledge of under-13 users, regardless of platform size. **Penalties:** civil penalties per violation (the Epic Games case set the current ceiling at $275M [Source 22]).

Section 5 of the FTC Act (the general prohibition on "unfair or deceptive acts or practices") is the separate statutory hook used in the Microsoft/Xbox [Source 23], Cognosphere [Source 24], and Disney [Source 25] settlements, each targeting dark-pattern purchase flows or undisclosed data collection from minors.

**California — Age-Appropriate Design Code Act (CAADCA)**

Enacted 2022 [Source 3], CAADCA would require Data Protection Impact Assessments, default privacy-protective settings for minors, and prohibitions on data uses materially detrimental to children's wellbeing — a UK-style design code. **Status:** A second preliminary injunction was granted March 13, 2025 on First Amendment grounds (NetChoice v. Bonta); the Ninth Circuit's March 12, 2026 ruling [Source 30] reinstated the law's definition of "covered businesses" but affirmed the injunction on five of six challenged provisions, remanding the age-estimation requirement to the district court. **The law is simultaneously "enacted" and largely unenforceable.**

**Texas, Utah, Louisiana**

Texas's SCOPE Act (2023) [Source 4] requires parental consent via a "commercially reasonable method" and restricts targeted advertising/data sharing for minors; its "harmful to minors" content provision was preliminarily enjoined in August 2024, but other provisions and 2025 app-store age-verification amendments remain in force. Utah's Social Media Regulation Act (2023) [Source 5], requiring age verification and parental consent for platforms with 5M+ accounts, was enjoined in September 2024; its separate App Store Accountability Act (2024) shifts verification duties to Apple/Google and remains in implementation. Louisiana's Act 456 (2023) [Source 6], requiring parental consent for under-16 social media accounts, was struck down as unconstitutionally vague in December 2025.

**State AG litigation and the federal MDL — Roblox-specific**

Louisiana [Source 27, August 2025] and Texas [Source 28, November 2025, relying on the SCOPE Act] have sued Roblox directly, alleging no effective age verification, widespread fake-birthdate accounts, and specific harmful UGC "experiences." Kentucky preceded both with its own suit, and Florida and Oklahoma have since filed similar actions [Source 28]. Separately, the 31 initially consolidated federal civil actions have grown to 162 cases (as of June 2026) consolidated into MDL No. 3166 [Source 29] before Chief Judge Richard Seeborg (N.D. Cal.), with a settlement master appointed February 2026.

**Massachusetts v. Meta (Section 230)**

The Massachusetts Supreme Judicial Court's April 2026 ruling [Source 31] held that Section 230 does not immunise claims that a platform's *design features* (e.g., addictive engagement mechanics) injure children, as distinct from third-party-content claims. This is the legal theory underlying both the Roblox MDL and the state AG suits.

**Roblox-specific applicability:** Roblox is subject to COPPA and the 2025 Rule amendments for any under-13 users (a population the Louisiana and Texas suits allege is undercounted due to fake birthdates [Source 27]); subject to FTC Act Section 5 enforcement under the same theories applied to Epic, Microsoft, Cognosphere, and Disney [Sources 22–25]; the subject of an active FTC complaint [Source 26] and five state AG suits [Sources 27, 28]; and a defendant in MDL 3166 [Source 29], where Section 230 is unlikely to provide a complete defence per the Massachusetts precedent [Source 31]. CAADCA's design-code obligations do not currently bind Roblox in California due to the ongoing injunction [Source 30].

---

### European Union

**GDPR Article 8** [Source 7], in force since 2018, sets the default age of digital consent at 16, with Member States free to lower it to as low as 13; controllers must make "reasonable efforts," accounting for available technology, to verify parental consent below the applicable age. **Applies to:** any "information society service" offered directly to children — squarely including Roblox's EU operations. **Penalties:** standard GDPR fines (up to 4% of global annual turnover or €20M, whichever is higher, under the general GDPR penalty regime).

**DSA Article 28** [Source 8], applicable since February 2024, imposes a free-standing duty on platforms to take "appropriate and proportionate measures" to ensure a high level of privacy, safety, and security for minors (Art. 28(1)), bans profiling-based advertising to users a platform knows with reasonable certainty are minors (Art. 28(2)), and clarifies that compliance does not require collecting *additional* personal data to determine age (Art. 28(3)). The European Commission's July 2025 guidelines [Source 17] operationalise Art. 28(1): private-by-default minor accounts, restricted stranger contact, modified recommender systems, addictive design features (streaks, autoplay, push notifications) disabled by default, no screenshotting/downloading of minors' content — and explicitly flag "virtual currencies and loot boxes" as commercial practices exploiting children's lack of commercial literacy. The EDPB's Guidelines 3/2025 [Source 18] address the tension between Art. 28's safety mandate and GDPR's data-minimisation principle (the "age-assurance paradox"), recommending privacy-preserving, "double-blind" verification.

**Penalties:** DSA penalties for Very Large Online Platforms can reach 6% of global annual turnover; Article 28 itself does not specify a separate penalty tier but is enforced under the DSA's general penalty regime.

**Roblox-specific applicability:** As an online platform with a predominantly under-18 EU user base, Roblox falls within DSA Article 28's scope and the Commission's July 2025 guidelines [Source 17] — which name virtual currencies and loot boxes (i.e., Robux-equivalent mechanics) directly. GDPR Article 8 governs Roblox's EU consent flows for users under the applicable national age threshold (13–16) [Source 7]. No EU enforcement action against Roblox specifically was identified in the source list — this is an open question for further investigation (see Section 5).

---

### United Kingdom

**UK Age Appropriate Design Code ("Children's Code")** [Source 9], in force since September 2020 (full enforcement from September 2021), sets 15 standards under the ICO/UK GDPR: high-privacy default settings, data minimisation, geolocation off by default, no "nudge techniques" toward lower privacy, and profiling off by default unless justified. **Applies to:** any online service "likely to be accessed by children," including games rated PEGI 16 or below — the ICO's 2023 gaming-specific guidance [Source 20] confirms this scope and recommends privacy-protective defaults, parental controls, and natural play "checkpoints."

**UK Online Safety Act 2023** [Source 10] (Royal Assent October 26, 2023) imposes statutory "child safety duties" on user-to-user services likely accessed by children. Ofcom has explicitly stated that gaming platforms with chat/UGC functionality fall within scope. It requires children's risk assessments, "highly effective" age verification or estimation to prevent children encountering primary priority content (e.g., pornography, self-harm/suicide content), and protective measures embedded in design, algorithms, and moderation. Ofcom's Protection of Children Codes of Practice [Source 19], in force from July 2025, operationalise this into 40+ measures, with specific guidance for online video game providers covering chat, avatars, matchmaking, and livestreaming risks (grooming, harassment, harmful content).

**Penalties:** Ofcom holds investigatory and enforcement powers including fines (under the Online Safety Act's general penalty regime, up to 10% of global turnover or £18M, whichever is greater).

**Roblox-specific applicability:** Roblox falls within the Children's Code (PEGI rating ≤16) [Sources 9, 20] and within the Online Safety Act's user-to-user services regime, given its chat and UGC functionality [Sources 10, 19]. This is the most directly and unambiguously applicable jurisdiction in this report — no carve-out or definitional ambiguity comparable to Australia's (see below) was identified for the UK.

---

### Australia

**Online Safety Act 2021 (Cth)** [Source 11] establishes the eSafety Commissioner and "Basic Online Safety Expectations," empowering removal notices for harmful content. Age-assurance is required only for content classified R18+; gaming platforms are generally excluded from age-check requirements unless hosting R18+ content.

**Online Safety Amendment (Social Media Minimum Age) Act 2024** [Source 12], in effect from December 10, 2025, bans under-16 accounts on named "age-restricted social media platforms" (Facebook, Instagram, Snapchat, TikTok, YouTube, Reddit, X, Threads, Twitch, Kick), with penalties up to A$49.5 million for non-compliant platforms. **Critically, online gaming services — including Roblox — are explicitly excluded from the statutory definition of "age-restricted social media platform,"** a carve-out the eSafety Commissioner frames as deliberate, avoiding overlap with Australia's existing content-classification scheme [Source 21]. Early implementation reports note significant circumvention by minors [Source 12].

**Roblox-specific applicability:** Roblox is **not** subject to the under-16 account ban under the 2024 Act due to the gaming carve-out [Source 12], but remains subject to the general Basic Online Safety Expectations under the 2021 Act [Sources 11, 21] and to R18+ content age-checks if applicable (unlikely given Roblox's content ratings). This carve-out is contested: child-safety advocacy framing applied to Roblox elsewhere [Source 26] argues UGC gaming platforms with chat present materially similar risks to social media — a normative disagreement the source material does not resolve (see Section 5 and `literature-review.md` Section 7).

---

### Brazil

**Estatuto Digital da Criança e do Adolescente ("Digital ECA")** [Source 13], enacted September 17, 2025 and in force since March 17, 2026, is among the most stringent frameworks reviewed. It explicitly covers "electronic games," **prohibits simple self-declaration of age for account creation**, requires linking under-16 accounts to a legal guardian, mandates removal of content involving sexual exploitation, violence, or self-harm within 24 hours, and bans profiling-based advertising and certain immersive (AR/VR/emotion-recognition) advertising techniques targeting minors. **Penalties:** enforcement by ANPD (Brazil's data protection authority), with fines up to 10% of Brazilian revenue or BRL 50 million (~US$9.4M) per violation.

**Roblox-specific applicability:** As an "electronic game" with a Brazilian user base, Roblox is directly covered. The self-declaration ban is the single most direct legal challenge in this report to Roblox's current age-gating model, which (per the Louisiana suit [Source 27]) relies on self-declared birthdates. Compliance would require guardian-linked accounts for Brazilian under-16 users and a 24-hour content-removal capability for the categories specified.

---

### UN / International

**UNCRC General Comment No. 25 (2021)** [Source 14], adopted by the UN Committee on the Rights of the Child following consultation with 700+ children across 27 countries, is the authoritative interpretation of how the binding UN Convention on the Rights of the Child (ratified by all UN member states except the US) applies to the digital environment. It requires states parties to ensure that businesses providing digital products/services likely accessed by children undertake child-rights due diligence, including child-rights impact assessments, applying the principles of non-discrimination, best interests, and "evolving capacities" to "design, regulation and management" of digital products.

**Roblox-specific applicability:** General Comment 25 is not directly enforceable against Roblox as a corporate entity, but it functions as the normative baseline against which national laws (and increasingly platform self-assessments) are judged. Its "evolving capacities" framing — that children's autonomy and protection needs change with age — is directly relevant to the 13–17 gap discussed in Section 4, since it implies graduated rather than binary (under-13/over-13) protections.

---

### India

**Digital Personal Data Protection Act 2023 and DPDP Rules 2025** [Source 15] define "child" as under 18 — broader than COPPA's under-13 — and require *verifiable* parental consent (via OTP, ID upload, or Aadhaar-based authentication) for processing any data of users under 18, while restricting behavioural tracking, profiling, and targeted advertising directed at children. **Penalties:** up to ₹200 crore (~US$24M). **Status:** Act in force; Rules notified 2025; children's-data provisions enforceable from May 13, 2027 (compliance grace period).

**Roblox-specific applicability:** Once enforceable (May 2027), this would apply to a much larger share of Roblox's Indian user base than COPPA does in the US, given the under-18 threshold. Roblox would need verifiable (not self-declared) parental consent for all Indian users under 18 — a materially higher bar than its current model.

---

### South Korea

South Korea's framework — the Juvenile Protection Act, Game Industry Promotion Act (loot box disclosure), and the February 2025 E-Commerce Act dark-patterns amendment [Source 16] — is the most prescriptive reviewed on monetisation mechanics specifically: monthly spending caps of KRW 70,000 (~US$60) for under-18 users, mandatory transparent disclosure of loot box probabilities, and a 2025 amendment specifically targeting "dark patterns" in digital commerce. The Juvenile Protection Act requires age and real-name verification for content designated "harmful to juveniles."

**Roblox-specific applicability:** If Roblox's Robux system is treated as analogous to loot-box mechanics under Korean law, the spending cap and odds-disclosure requirements would apply directly to Korean under-18 users — a more concrete monetisation restriction than exists in any other jurisdiction reviewed. No Korea-specific enforcement action against Roblox was identified, and the broader question of whether Korean law treats player-to-player virtual economies (as opposed to operator-sold loot boxes) the same way is unresolved (see Section 5).

---

## 3. Cross-Cutting Themes

### Age verification and assurance requirements

There is cross-jurisdictional consensus that self-declared age is inadequate [Source 36], yet the LSE/5Rights Phase 2 study found 11 of 70 platforms studied still rely on it alone despite 12 distinct age-assurance methods now in use [Source 37]. Legal responses diverge sharply: the UK mandates "highly effective" age verification or estimation [Sources 10, 19]; Brazil bans self-declaration outright [Source 13]; US states (Utah, Texas) shift verification to app stores [Sources 4, 5]; and California's age-estimation mandate remains judicially unresolved [Sources 3, 30]. Australia's gaming carve-out [Source 12] means no age-verification mandate of this kind applies to Roblox there at all. The EDPB [Source 18] and EFF [Source 38] flag a fundamental tension: stronger verification methods may require collecting more identifying data, in tension with data-minimisation principles and creating surveillance/exclusion risks for the broader user base (an estimated 34.5 million US adults lack current ID [Source 38]).

### Data collection and minimisation obligations

COPPA [Sources 1, 2] and GDPR Article 8 [Source 7] form the core data-minimisation obligations, but apply at different age thresholds (13 vs. 13–16) and with different consent mechanisms (verifiable parental consent vs. "reasonable efforts"). India's DPDP framework [Source 15] extends verifiable consent to all under-18s, the broadest threshold reviewed. The 2025 COPPA amendments [Source 2] notably expand "personal information" to include biometric identifiers — directly relevant to any facial age-estimation tool a platform might adopt to address the age-verification theme above.

### Default privacy settings and dark patterns

The UK Children's Code [Source 9] and EU Commission's DSA Article 28(1) guidelines [Source 17] both mandate privacy-protective defaults and prohibit "nudge techniques," with the EU guidance going further to require disabling addictive engagement features (streaks, autoplay, push notifications) by default. California's CAADCA [Source 3] sought a comparable design-code approach but is enjoined on First Amendment grounds [Source 30] — meaning the US currently has no enforceable legislative equivalent. FTC v. Epic Games [Source 22] established that default-on chat and dark-pattern purchase flows are themselves actionable under existing US law (COPPA/FTC Act), and Massachusetts v. Meta [Source 31] confirms that Section 230 does not bar design-defect claims targeting such features — providing a litigation-based (rather than design-code) route to similar outcomes in the US.

### Advertising and monetisation restrictions

DSA Article 28(2) bans profiling-based ads to known minors [Source 8], and the Commission's guidelines specifically name virtual currencies and loot boxes as exploitative of children's "commercial literacy" gaps [Source 17]. Brazil's Digital ECA bans profiling ads and immersive ad techniques targeting minors [Source 13]. South Korea imposes the only hard spending cap reviewed (KRW 70,000/month for under-18s) plus mandatory loot-box odds disclosure [Source 16]. US enforcement (Epic [Source 22], Cognosphere [Source 24]) penalises dark-pattern purchase flows and undisclosed odds under existing consumer-protection law. **No source identifies a law addressing player-to-player virtual economies** (as distinct from operator-sold loot boxes/currency) — a gap directly relevant to Robux's creator-economy dimension.

### Reporting, audit, and enforcement mechanisms

Enforcement mechanisms range from FTC civil penalties (up to $275M, the Epic precedent [Source 22]) to ANPD fines of up to 10% of Brazilian revenue [Source 13], DPDP penalties up to ₹200 crore [Source 15], and Ofcom's fining powers under the Online Safety Act [Source 19]. The UNCRC General Comment 25 [Source 14] requires child-rights impact assessments as a due-diligence mechanism, though it is not independently enforceable. The clearest emerging US enforcement pattern is not regulatory but litigation-based: state AG suits [Sources 27, 28] consolidated into MDL 3166 [Source 29], built on the design-defect theory validated in Massachusetts v. Meta [Source 31].

---

## 4. Platform-Specific Analysis

### Roblox's known legal exposure

As of the report date (June 2026), Roblox faces: (1) an FTC complaint filed by NCOSE and Fairplay (May 2026), alleging COPPA/UDAP violations related to Robux monetisation and chat [Source 26]; (2) state AG suits from Louisiana (August 2025) [Source 27] and Texas (November 2025, under the SCOPE Act) [Source 28], with Kentucky preceding and Florida/Oklahoma following [Source 28]; and (3) consolidation of 162 federal civil cases into MDL No. 3166 (December 2025), with a settlement master appointed and negotiations ongoing [Source 29]. Each of these tracks a precedent already established against other gaming companies: Epic Games' $275M+$245M settlement for default-on chat and dark-pattern currency purchases [Source 22], Microsoft's $20M settlement for pre-consent birthdate collection [Source 23], Cognosphere's $20M settlement for obscured purchase costs and loot-box odds [Source 24], and Disney's $10M settlement under an "actual knowledge" theory for child-directed content [Source 25].

### The Robux virtual currency system and dark-patterns allegations

The NCOSE/Fairplay complaint alleges Roblox's "obfuscated Robux exchange rate" and "engagement-maximizing design features, virtual currency system, and voice/text chat" are "developmentally inappropriate," posing risk of financial and sexual harm [Source 26]. This closely parallels the FTC's findings against Epic Games (dark-pattern V-Bucks purchase flows) [Source 22] and Cognosphere (obscured costs and loot-box odds) [Source 24]. The EU Commission's July 2025 guidelines independently flag "virtual currencies and loot boxes" as exploiting children's lack of commercial literacy [Source 17], and South Korea imposes hard spending caps and odds-disclosure requirements on comparable mechanics [Source 16]. None of these frameworks, however, were designed with — or have been tested against — a player-to-player virtual economy where minors can also act as sellers/creators, which is a structural feature of Robux not present in Fortnite's V-Bucks or Genshin Impact's loot boxes.

### Self-declaration age verification and its legal insufficiency

The Louisiana suit alleges Roblox's age-verification process allows millions of accounts with fake birthdates due to reliance on self-declaration [Source 27]. This is the precise practice that 5Rights' foundational taxonomy concludes "provides no meaningful assurance" [Source 36], that the LSE/5Rights Phase 2 study finds persists at 11 of 70 platforms despite 12 alternative methods now available [Source 37], and that Brazil's Digital ECA now prohibits outright for electronic games [Source 13]. The UK's "highly effective age assurance" standard [Sources 10, 19] and California's still-unresolved age-estimation mandate [Source 30] represent two different legal routes to requiring something more than self-declaration — neither of which currently binds Roblox in the US outside of litigation risk.

### The 13–17 age gap in US federal law

COPPA's protections apply only to under-13 users [Sources 1, 2]; the American University WCL paper argues this cutoff and the associated notice-and-consent model are insufficient for modern platform design [Source 34]. For Roblox, whose user base skews toward the 9–17 range, this means a substantial population — 13-to-17-year-olds — falls outside COPPA's verifiable-parental-consent and data-minimisation requirements entirely, even though the design features at issue in current litigation (chat, monetisation mechanics) do not become less relevant at age 13. The Mercatus Center brief notes that legislative proposals to close this gap (e.g., KOSA) raise anonymous-speech and First Amendment concerns [Source 33] — the same doctrinal obstacle that has stalled CAADCA [Source 30]. By contrast, the UK's "likely to be accessed by children" standard [Source 9] and Brazil's under-16 framework [Source 13] apply graduated obligations across the full under-18 range without relying on a single hard cutoff.

### Cross-platform grooming and off-platform harm

The MDL 3166 consolidation order identifies "Roblox's alleged knowledge that predators used the platform" and "feasibility of parental controls" as common questions across the 162 consolidated cases [Source 29]. Ofcom's Protection of Children Codes include gaming-specific guidance on grooming risk arising from chat, matchmaking, and livestreaming features [Source 19]. None of the sources reviewed directly addresses the specific dynamic — frequently alleged in connection with UGC gaming platforms — of contact initiated in-platform but harm occurring via off-platform communication channels (e.g., third-party messaging apps); this remains an open question for Section 5.

---

## 5. Gaps and Open Questions

**The DSA age-assurance paradox.** The EDPB's Guidelines 3/2025 [Source 18] identify a direct tension between DSA Article 28's obligation to protect minors and GDPR's data-minimisation principle: stronger age-assurance methods often require collecting more identifying data. The EDPB's proposed resolution — privacy-preserving "double-blind" verification — is not yet implemented at scale by any platform discussed in the source list, including Roblox. How Roblox would satisfy both Article 28(1)'s "appropriate and proportionate measures" duty and Article 28(3)'s no-additional-data clarification [Source 8] in practice is unresolved.

**Section 230 and platform design liability.** Massachusetts v. Meta [Source 31] establishes that Section 230 does not bar design-defect claims, and MDL 3166 [Source 29] is built on a similar theory against Roblox. However, this is currently binding only in Massachusetts and represents "a broader national trend" rather than settled federal law [Source 31] — whether other jurisdictions within MDL 3166 will apply the same Section 230 analysis to Roblox's claims is an open question pending the settlement negotiations [Source 29].

**Missing or thin jurisdictional coverage.** Per `law-sources.md`'s Gap Analysis, **Canada** has no identified child-online-safety or gaming legislation in the source list — including the status of the federal Online Harms Act (Bill C-63), which was not surfaced despite a targeted search. This is the clearest jurisdictional gap in this report. **South Korea's** coverage [Source 16] is limited to monetisation/loot-box and dark-patterns regulation; its broader child-data-privacy regime (e.g., PIPA provisions on minors) was not researched. **Note on India:** the Phase 3 brief for this report listed India alongside Canada and South Korea as a "missing jurisdiction," but India is in fact covered in the source list via the DPDP Act/Rules [Source 15] — this report includes an India section (Section 2) and treats India as adequately, if not exhaustively, covered. This discrepancy between the brief and the actual source list is flagged here rather than silently resolved.

**The UNICEF Innocenti working paper [Source 35]** was identified but its full text remains unverifiable after repeated fetch attempts; its confirmed subtitle ("Mitigating Risks from Organized Violence") suggests narrower relevance to this report's themes (virtual economies, age assurance) than originally assumed.

**The "social media vs. gaming" classification question.** UK law treats Roblox as in-scope of user-to-user-service child-safety duties by definition [Sources 10, 19]; Australian law treats gaming platforms, including Roblox, as out-of-scope of its social-media age-verification regime by definition [Sources 12, 21]. Child-safety advocacy applied to Roblox argues these risks are functionally equivalent to social media [Source 26]. No source resolves which framing is correct, and this report does not attempt to do so — it is a structural fact that any compliance analysis must handle on a per-jurisdiction basis.

**No law addresses player-to-player virtual economies.** Every monetisation-focused source reviewed (Sources 16, 17, 22, 24) concerns operator-to-consumer transactions (loot boxes, in-game currency purchases). None addresses a system where minors can also earn, trade, or monetise virtual goods/currency with other users — a structural feature of Robux's creator economy that falls outside the scope of every framework in this report.

**Questions for further investigation:** (1) Has any EU Member State DPA or the European Commission taken enforcement action against Roblox specifically under GDPR Article 8 or DSA Article 28? (2) What is the current status of Canada's Bill C-63 (Online Harms Act), and does it cover gaming platforms? (3) Does South Korean law treat Robux-style player-to-player virtual currency the same as operator-sold loot boxes for purposes of the spending cap and odds-disclosure rules? (4) What is the outcome of the CAADCA age-estimation remand [Source 30], and would a similar provision (if upheld) apply to Roblox's California operations? (5) What terms, if any, does the MDL 3166 settlement master propose regarding age verification, chat defaults, or Robux mechanics specifically [Source 29]?

---

## 6. References

1. Children's Online Privacy Protection Act (COPPA), 15 U.S.C. §§ 6501–6505 — U.S. Congress / FTC, 1998. https://www.ftc.gov/legal-library/browse/statutes/childrens-online-privacy-protection-act
2. Children's Online Privacy Protection Rule, 16 CFR Part 312 — 2025 Amendments — Federal Trade Commission, 2025. https://www.federalregister.gov/documents/2025/04/22/2025-05904/childrens-online-privacy-protection-rule
3. California Age-Appropriate Design Code Act (CAADCA) — California Legislature, 2022. https://www.alstonprivacy.com/court-enjoins-enforcement-of-california-age-appropriate-design-code-act/
4. Texas SCOPE Act (HB 18, 2023) and 2025 App Store Accountability provisions — Texas Legislature, 2023/2025. https://www.bassberry.com/news/apps-and-minors-new-compliance-frontiers-and-risks-in-louisiana-utah-and-texas/
5. Utah Social Media Regulation Act (2023) and App Store Accountability Act (2024) — Utah Legislature. https://avpassociation.com/us-state-age-assurance-laws-for-social-media/
6. Louisiana Act 456 (2023) — Louisiana Legislature. https://lailluminator.com/2025/12/18/louisiana-social-media-2/
7. General Data Protection Regulation (GDPR), Regulation (EU) 2016/679 — Article 8 — European Parliament and Council, 2016. https://gdpr-info.eu/art-8-gdpr/
8. Digital Services Act (DSA), Regulation (EU) 2022/2065 — Article 28 — European Parliament and Council, 2022. https://www.eu-digital-services-act.com/Digital_Services_Act_Article_28.html
9. UK Age Appropriate Design Code ("Children's Code") — Information Commissioner's Office, 2020. https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/childrens-information/childrens-code-guidance-and-resources/age-appropriate-design-a-code-of-practice-for-online-services/
10. UK Online Safety Act 2023 — UK Parliament, 2023. https://www.legislation.gov.uk/ukpga/2023/50
11. Online Safety Act 2021 (Cth) — Parliament of Australia, 2021. https://www.legislation.gov.au/C2021A00076/latest
12. Online Safety Amendment (Social Media Minimum Age) Act 2024 (Cth), No. 127, 2024 — Parliament of Australia. https://www.legislation.gov.au/C2024A00127/asmade
13. Estatuto Digital da Criança e do Adolescente ("Digital ECA") — Brazilian National Congress, 2025. https://agenciabrasil.ebc.com.br/en/politica/noticia/2026-03/brazil-digital-statute-protect-minors-online-comes-force
14. UN Convention on the Rights of the Child — General Comment No. 25 (2021) — UN Committee on the Rights of the Child. https://digitallibrary.un.org/record/3906061?ln=en
15. India — Digital Personal Data Protection Act 2023 and DPDP Rules 2025 — Government of India. https://ksandk.com/data-protection-and-data-privacy/childrens-data-protection-under-indias-dpdp-rules/
16. South Korea — Juvenile Protection Act; Game Industry Promotion Act; E-Commerce Act amendment 2025 — National Assembly of the Republic of Korea / KFTC / GRAC. https://practiceguides.chambers.com/practice-guides/gaming-law-2025/south-korea
17. European Commission — Guidelines on the protection of minors under Article 28(1) DSA — European Commission, 2025. https://digital-strategy.ec.europa.eu/en/library/commission-publishes-guidelines-protection-minors
18. EDPB Guidelines 3/2025 on the interplay between the DSA and the GDPR — European Data Protection Board, 2025. https://www.edpb.europa.eu/system/files/2025-09/edpb_guidelines_202503_interplay-dsa-gdpr_v1_en.pdf
19. Ofcom — Protection of Children Codes of Practice — Ofcom, 2025. https://www.ofcom.org.uk/online-safety/protecting-children/new-rules-for-a-safer-generation-of-children-online
20. ICO — Guidance on Children's Code compliance for game developers — Information Commissioner's Office, 2023. https://www.lexology.com/library/detail.aspx?g=56103890-5c97-4e6b-8429-a637a7d83a6e
21. eSafety Commissioner (Australia) — Basic Online Safety Expectations & Age-Restricted Material Codes — eSafety Commissioner, 2025. https://www.esafety.gov.au/industry/basic-online-safety-expectations
22. FTC v. Epic Games, Inc. — Federal Trade Commission, 2022/2023. https://www.ftc.gov/news-events/news/press-releases/2022/12/fortnite-video-game-maker-epic-games-pay-more-half-billion-dollars-over-ftc-allegations
23. FTC v. Microsoft Corporation (Xbox) — Federal Trade Commission, 2023. https://www.ftc.gov/business-guidance/blog/2023/06/20-million-ftc-settlement-addresses-microsoft-xbox-illegal-collection-kids-data-game-changer-coppa
24. FTC v. Cognosphere Pte. Ltd. (Genshin Impact / HoYoverse) — Federal Trade Commission, 2025. https://www.khlaw.com/insights/privacy-and-advertising-year-review-2024-will-kids-and-teens-remain-focus-2025
25. FTC v. The Walt Disney Company — Federal Trade Commission, 2025. https://www.reedsmith.com/articles/ftc-starts-2025-with-a-focus-on-safeguarding-kids/
26. National Center on Sexual Exploitation & Fairplay — FTC Complaint against Roblox — NCOSE/Fairplay, 2026. https://thehill.com/homenews/5888060-roblox-gaming-platform-ftc-investigation/
27. Louisiana v. Roblox Corporation — Office of the Louisiana Attorney General, 2025. https://www.nbcnews.com/tech/tech-news/louisiana-attorney-general-sues-roblox-calling-platform-perfect-place-rcna225144
28. Texas v. Roblox Corporation — Office of the Texas Attorney General, 2025. https://www.texastribune.org/2025/11/07/texas-roblox-lawsuit-ken-paxton/
29. In re: Roblox Corporation Child Sexual Exploitation and Assault Litigation, MDL No. 3166 — U.S. Judicial Panel on Multidistrict Litigation, 2025. https://topclassactions.com/lawsuit-settlements/lawsuit-news/roblox-child-sexual-exploitation-lawsuits-consolidated-in-california-mdl/
30. NetChoice v. Bonta — U.S. District Court, N.D. Cal. / Ninth Circuit Court of Appeals, 2025/2026. https://hintzelaw.com/blog/2026/3/17/9th-circuit-rules-on-injunction-of-california-age-appropriate-design-code-upholding-coverage-definition
31. Massachusetts v. Meta Platforms, Inc. — Massachusetts Supreme Judicial Court, 2026. https://www.crowell.com/en/insights/client-alerts/in-massachusetts-section-230-does-not-immunize-meta-from-claims-that-instagrams-design-features-injure-children
32. Birrell, E. et al. — "SoK: Technical Implementation and Human Impact of Internet Privacy Regulations" — arXiv, 2023. https://arxiv.org/abs/2312.15383
33. Mercatus Center — "Protecting Children Online: Evaluating Possible Reforms in the Law and the Application of COPPA" — Tracy C. Miller, 2023. https://www.mercatus.org/research/policy-briefs/protecting-children-online-evaluating-possible-reforms-law-and-application
34. American University Washington College of Law — "Child Privacy in the Digital Era: Is COPPA Enough?" — Melannie Sandoval, 2024. https://digitalcommons.wcl.american.edu/cgi/viewcontent.cgi?article=1132&context=research
35. UNICEF Innocenti — "Protecting Children in Online Gaming: Mitigating Risks from Organized Violence" — Galen Lamphere-Englund (per secondary citation), UNICEF Office of Research – Innocenti, 2025. [UNVERIFIABLE] https://www.unicef.org/innocenti/media/11836/file/UNICEF-Innocenti-Protecting-Children-Online-Gaming-Working-Paper-2025.pdf
36. 5Rights Foundation — "But How Do They Know It Is a Child?" — 5Rights Foundation, 2021. https://5rightsfoundation.com/wp-content/uploads/2024/09/But_How_Do_They_Know_It_is_a_Child-1.pdf
37. Digital Futures for Children (LSE) & 5Rights Foundation — "Impact of Regulation on Children's Digital Lives: Phase 2" — LSE / 5Rights Foundation, 2026. https://www.lse.ac.uk/news/more-work-needed-for-regulation-to-drive-systemic-change-in-child-online-safety-and-privacy-protections
38. Electronic Frontier Foundation — "10 (Not So) Hidden Dangers of Age Verification" — EFF, 2025. https://www.eff.org/deeplinks/2025/12/10-not-so-hidden-dangers-age-verification

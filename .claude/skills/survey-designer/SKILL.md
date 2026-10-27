---
name: survey-designer
description: |
  Use this skill when Agent 4 needs to design age-appropriate surveys for
  Group A (ages 6-12) and Group B (ages 13-17) about Roblox usage habits
  and awareness of age restrictions.

  Trigger for:
  - Starting Agent 4
  - Any instruction to build or write the survey

  Don't trigger for:
  - Analysing survey responses (different skill)
  - Legal or efficacy research (Agents 1 and 2)
license: MIT
---

# Survey Designer Skill

> ## Pipeline Header
> - **Purpose:** Design the two age-appropriate survey instruments (Group A 6–12, Group B 13–17) plus a methodology write-up.
> - **Called by:** Agent 4 (`agent4-survey-designer.md`).
> - **Inputs:** design rules below; context from `reports/law-report.md` and `reports/trend-report.md`.
> - **Outputs:** `survey/survey-group-a.md`, `survey/survey-group-b.md`, `survey/survey-methodology.md`.
> - **Next step:** the Verifier checks the survey files; later Agent 5 analyses the collected responses.

---

## Core Principles

Before writing a single question, internalise these rules:

1. **Neutral tone throughout** — no question should imply a correct answer or lead the respondent
2. **Age-appropriate language** — Group A uses short sentences, simple words, concrete examples; Group B can handle nuance and abstraction
3. **No normalisation of bypassing** — questions about bypass methods are observational only ("have you heard of...") never participatory ("have you done...")
4. **Safety first** — the survey must feel safe, low-pressure, and non-judgmental at every point
5. **Bypass definition required** — always provide the standard neutral definition before any bypass-related question block

---

## Standard Bypass Definition

Use this exact definition, adapted for each group's reading level:

**Group B version:**
> "For the next few questions, we use the term 'bypassing age restrictions.' This means doing something to get around the age rules on Roblox — for example, using someone else's account, or entering a different birthday when signing up. You do not need to have done any of these things to answer the questions."

**Group A version:**
> "The next questions are about the rules on Roblox about how old you need to be. Sometimes people find ways to get around these rules. For example, using a grown-up's account, or putting in a different birthday. You don't need to have done anything like this — we just want to know what you've heard about."

---

## Question Type Guide

| Type | When to use | Group A | Group B |
|---|---|---|---|
| Yes/No | Simple awareness checks | ✅ preferred | ✅ |
| Multiple choice | Frequency, category selection | ✅ max 4 options | ✅ up to 6 options |
| Likert scale | Feelings, perceptions, agreement | ⚠️ use faces/simple labels | ✅ standard 5-point |
| Short answer | Open-ended reflection | ✅ 1 question max | ✅ 1-2 questions |

Group A Likert scale labels: 😊 Yes definitely / 🙂 Kind of / 😐 Not sure / 🙁 Not really / 😞 No definitely not

Group B Likert scale labels: Strongly agree / Agree / Neutral / Disagree / Strongly disagree

---

## Survey Structure

Both surveys follow the same 6-section structure, with language adapted per group.

---

### Section 1: General Roblox Usage

**Purpose:** Establish baseline usage patterns. Warm, easy questions to build comfort.

**Required questions (adapt language per group):**

1. How often do you play Roblox?
   - Every day
   - A few times a week
   - Once a week
   - Less than once a week
   - I don't play Roblox

2. When you play Roblox, how long do you usually play for?
   - Less than 30 minutes
   - 30 minutes to 1 hour
   - 1 to 2 hours
   - More than 2 hours

3. What kinds of games do you mostly play on Roblox? *(select all that apply)*
   - Adventure or action games
   - Role-playing games (where you act as a character)
   - Building or creative games
   - Simulator games
   - Games with friends I know in real life
   - Other: ___________

4. Do you play Roblox with people you know in real life, or with people you only know online?
   - Mostly with people I know in real life
   - Mostly with people I only know online
   - Both
   - I usually play alone

---

### Section 2: Awareness of Age Restrictions

**Purpose:** Assess what children know about Roblox's rules.

5. Did you know that Roblox has rules about how old you need to be to use certain features?
   - Yes
   - No
   - I'm not sure

6. Do you know what age you need to be to have a full Roblox account without parental permission?
   - Yes, I know the age
   - I've heard something about it but I'm not sure
   - No, I don't know

7. Have you ever seen a warning or message on Roblox telling you that something is only for older users?
   - Yes
   - No
   - I can't remember

**Group B only:**

8. How did you first find out about Roblox's age restrictions or content rules? *(select all that apply)*
   - A parent or guardian told me
   - A friend told me
   - I read it on Roblox's website or in the app
   - I saw it mentioned online (YouTube, social media, forums)
   - I found out when I was blocked from doing something
   - Other: ___________

---

### Section 3: Perceived Effectiveness of Restrictions

**Purpose:** Understand whether children feel the restrictions work and make sense.

**Group A — use simple Likert with face labels:**

9. Do you think the age rules on Roblox keep you safe?
   [😊 Yes definitely / 🙂 Kind of / 😐 Not sure / 🙁 Not really / 😞 No definitely not]

10. Do the age rules on Roblox make sense to you?
    [😊 Yes definitely / 🙂 Kind of / 😐 Not sure / 🙁 Not really / 😞 No definitely not]

11. Have you ever seen something on Roblox that you felt you were too young to see?
    - Yes
    - No
    - I'm not sure

**Group B — use standard Likert + follow-up:**

9. The age restrictions on Roblox effectively protect younger users from inappropriate content.
   [Strongly agree / Agree / Neutral / Disagree / Strongly disagree]

10. The age restrictions on Roblox make sense given the types of content on the platform.
    [Strongly agree / Agree / Neutral / Disagree / Strongly disagree]

11. Have you ever encountered content on Roblox that you felt was inappropriate for your age group?
    - Yes
    - No
    - I'm not sure

12. *(Group B only)* Do you think Roblox does enough to enforce its age rules?
    [Strongly agree / Agree / Neutral / Disagree / Strongly disagree]

---

### Section 4: Bypass Awareness — Definition + Hearing About Others

**Purpose:** Assess awareness of bypassing without asking about personal behaviour.

> ⚠️ INSERT STANDARD BYPASS DEFINITION HERE (group-appropriate version) before this section.

**Group A:**

12. Have you ever heard of someone — like a friend, classmate, or brother or sister — getting around the age rules on Roblox?
    - Yes
    - No
    - I'm not sure

**Group B:**

13. Have you ever heard of someone else — such as a friend, classmate, or sibling — bypassing age restrictions on Roblox?
    - Yes
    - No
    - I'm not sure

---

### Section 5: Bypass Method Awareness (Conditional — only if answered Yes above)

**Purpose:** Assess awareness of specific bypass methods without implicating the respondent.

**Instructions:** Only show this section if the respondent answered Yes to the previous question.

Intro text:
- **Group A:** "You said you've heard of people getting around the rules. For each of the things below, just tell us if you've heard of anyone doing it. You don't need to have done it yourself."
- **Group B:** "You indicated you've heard of others bypassing age restrictions. For each method below, please indicate whether you've heard of this being used. This is about awareness only — not about your own actions."

**One yes/no question per method:**

| Method | Group B phrasing | Group A phrasing |
|---|---|---|
| Parent/sibling account | "Have you heard of someone using a parent's or older sibling's Roblox account to access features meant for older users?" | "Have you heard of someone using a grown-up's or older brother or sister's Roblox account?" |
| False date of birth | "Have you heard of someone entering a false date of birth when signing up for Roblox to appear older?" | "Have you heard of someone putting in a wrong birthday when making a Roblox account?" |
| VPN | "Have you heard of someone using a VPN (a tool that changes where your internet thinks you are) to access Roblox features not available in their region?" | "Have you heard of someone using a special computer tool to make Roblox think they're in a different country?" |
| Multiple accounts | "Have you heard of someone creating multiple Roblox accounts to get around a ban or restriction?" | "Have you heard of someone making more than one Roblox account to get around being blocked?" |
| Third-party/modified clients | "Have you heard of someone using unofficial apps or modified versions of Roblox to access restricted content?" | "Have you heard of someone using a different or unofficial version of Roblox to see things that are normally blocked?" |
| Other | "Have you heard of any other methods being used that are not listed above? If yes, please describe briefly (optional):" | "Have you heard of any other ways people get around the rules that aren't listed here? If yes, you can write it here (you don't have to):" |

---

### Section 6: Open-Ended Closing Question

**Purpose:** Give respondents space to share anything not covered. Keep warm and low-pressure.

**Group A:**
> "Is there anything else you want to tell us about Roblox and its rules? You can write anything you like — there are no wrong answers, and you don't have to write anything if you don't want to. 😊"

**Group B:**
> "Is there anything else you'd like to share about your experience with Roblox's age rules or safety features? This is completely optional — feel free to share any thoughts, feelings, or experiences that weren't covered in the questions above."

---

## Output Format

### survey/survey-group-a.md

```markdown
# Roblox Survey — Group A (Ages 6–12)
**Purpose:** Understanding how children use Roblox and what they know about its age rules.
**Estimated time:** 5–8 minutes
**Note to facilitator:** Read questions aloud for younger children if needed. Reassure children there are no right or wrong answers and participation is optional.

---
[All sections and questions formatted cleanly with answer options]
```

### survey/survey-group-b.md

```markdown
# Roblox Survey — Group B (Ages 13–17)
**Purpose:** Understanding how young people use Roblox and their awareness of its age restrictions and content policies.
**Estimated time:** 8–12 minutes
**Note:** There are no right or wrong answers. All responses are anonymous.

---
[All sections and questions formatted cleanly with answer options]
```

### survey/survey-methodology.md

```markdown
# Survey Methodology
**Agent:** Agent 4 — Survey Designer
**Date:** [YYYY-MM-DD]

## Design Rationale
[Why each section exists, how language was calibrated per group]

## Question Type Justification
[Why each question type was chosen]

## Ethical Considerations
[How the survey avoids normalising bypass behaviour, protects respondent safety]

## Limitations
[What the survey cannot measure, age-group caveats]

## Recommended Administration Notes
[How to administer to each group, parental consent considerations]
```

---

## Quality Gate

Before writing output files confirm:

- [ ] No question implies bypassing is normal or expected
- [ ] No question asks for names of other people
- [ ] No question asks whether the respondent personally bypassed anything
- [ ] Bypass definition appears before Section 5 in both surveys
- [ ] Section 5 is clearly conditional on a Yes answer to Section 4
- [ ] Group A language is readable by a 6-year-old
- [ ] Group B language is appropriately nuanced for a 17-year-old
- [ ] Every bypass method has its own standalone yes/no question
- [ ] Both surveys end with the open-ended closing question
- [ ] survey-methodology.md addresses ethical considerations

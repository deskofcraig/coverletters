---
name: star-method
description: Claude uses these descriptions when deciding which skills to use in chat.
---
---
name: star-method
description: Turns a job requirement, selection criterion, or screening question into a short evidence story using the STAR method (Situation, Task, Action, Result), built only from real experience in the user's profile or memory. Called by cover-letter-writer when mapping requirements to examples, and usable alone for application questions and interview prep. Asks for missing numbers, methods and samples instead of inventing them. Tells the user when this skill itself should be rewritten.
---

# STAR method

Build one honest, specific evidence story per requirement. Output is prose that sounds like the user, not a labelled template, unless labels are requested.

## When this skill runs

- **Called by cover-letter-writer** at the requirement-mapping step. Return a requirement-to-story map and the draft story paragraphs. Do not write the whole letter here.
- **Standalone** for selection criteria, screening questions ("Tell us about a time..."), and interview preparation.

## Inputs

1. The requirement or question, copied exactly from the job description or form.
2. The role type and seniority band.
3. The evidence bank: the user's profile reference file and memory (Octopus Deploy, Cognizant, CoreLogic, Amber Labs, Swyftx, earlier career, personal projects).
4. Any word limit.

If the evidence bank cannot be read, say so and ask for the relevant facts.

## Step 1: Classify the requirement

| Type | What the story must show |
|---|---|
| Outcome and metrics (conversion, adoption, funnel) | A number, the method that produced it, and the user's own contribution |
| Craft and tools (Figma, Storybook, prototyping, code) | The specific tool use inside a real deliverable |
| Systems and governance | Process, documentation, adoption by others, a result after handover |
| Research and discovery | Method, sample size, what changed because of the findings |
| Collaboration and stakeholders | Who, what conflicted, how it resolved, who was brought along |
| Influence and judgement (senior roles) | A decision the user changed, cut, delayed or reshaped, and the effect |
| Leadership and mentoring | Count of people, what the user did, what improved |
| Domain (insurance, construction, finance, health) | A direct bridge: where the user lived this problem |
| Delivery and pace (agile, multiple projects, deadlines) | Concurrent load, sequencing, what shipped |

## Step 2: Choose evidence

- Pick the story with the closest match to the requirement and the employer's domain. Prefer one hero story per letter and short supporting proof for the rest.
- Do not reuse the same story and wording in more than one requirement of the same letter.
- Check earlier letters in the repo and memory so wording is not copied from a recent letter.
- Use the role-type table in the cover letter reference checklist as the default pairing.

## Step 3: Evidence completeness check

Before writing, confirm the story has each of these. Mark what is missing.

- Situation: employer, product, user, what was broken
- Task: what the user personally owned
- Action: at least three concrete steps the user took (use "I")
- Method and sample: interviews, tests, users, sessions, tools
- Result: a number, or a named outcome if no number exists
- Honest caveat where a number looks small
- Influence or decision (senior roles)

If anything is missing, ask in one grouped message, naming the exact gap ("How many customer interviews fed the Professional tier selection design?"). Do not fill gaps with plausible detail. If the user says to proceed, write around the gap and leave a marked placeholder such as [add: number of interviews].

## Step 4: Build the story

Weighting, as proportions of the story:

- Situation about 20 percent. Only the context the reader needs.
- Task about 10 percent. The responsibility the user owned.
- Action about 60 percent. What the user personally did, in order, naming the skill the requirement asks for through the actions, not by claiming it.
- Result about 10 percent. The number, the caveat if the number looks small, and what changed afterward.

Condensing for a cover letter: merge Situation and Task into one sentence, spend most of the paragraph on Action, end on the number.

## Step 5: Format for the destination

| Destination | Length | Shape |
|---|---|---|
| Letter paragraph (hero story) | 90 to 130 words | One paragraph, full Action detail |
| Letter paragraph (supporting proof) | 30 to 60 words | One to two sentences, result included |
| Bullet-style match (short letters) | 1 to 2 lines per requirement | Requirement keyword, proof, number |
| Selection criterion or screening answer | 150 to 300 words, or the stated limit | Flowing prose, STAR order, no labels |
| Interview talking points | Short bullets | S, T, A, R lines plus a likely follow-up question |

## Step 6: Voice and anti-AI pass

- Plain, direct, comma-linked rhythm like the user's own letters. Contractions are fine.
- No em dashes. No banned words or phrases from the de-AI language skill. No "it's not X, it's Y" sentences. No forced lists of three.
- Replace vague claims with a number, name, date, or example.
- At most one everyday analogy per letter.
- Vary the wording of any stock sentence that appeared in a previous letter.

## Step 7: Return

Return, in this order:

1. A requirement-to-story map: requirement, chosen evidence, what is still missing.
2. The story text for each requirement, at the right length for its destination.
3. A short list of open placeholders and any claim that rests on an assumption.

## Maintenance: tell the user when this skill needs rewriting

After each use, check these triggers. If any is true, end the reply with a short note headed **Skill update recommended**, naming the trigger and the specific change proposed. Also record the observation in memory.

- The same evidence gap has needed asking about on three or more uses (add the field to the evidence bank or the profile).
- Two or more results come back (interview or rejection) that suggest a story type, length or ordering works better or worse than the current rules.
- The user's new letters in the repo show a different structure or length than Steps 4 and 5 assume.
- A destination type appears that Step 5 does not cover (for example a video answer, a one-page capability statement, or a portfolio case-study summary).
- The weighting produced a story the user rewrote heavily on two or more uses.
- Reference checklist rules changed, so this skill's pairing or length rules no longer match.

If none apply, say nothing about maintenance.
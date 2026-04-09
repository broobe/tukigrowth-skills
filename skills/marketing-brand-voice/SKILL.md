---
name: marketing-brand-voice
description: Analyzes, builds, or validates a brand voice. Use when the user wants to document their brand voice from existing content, define it from scratch, or check whether a specific piece of copy is on-brand. Triggers on: "analyze my brand voice", "build our voice guidelines", "does this sound like us", "create a brand voice guide", "is this copy on-brand", "define our tone of voice", `/marketing-brand-voice <url>`, or any request involving how a brand communicates, sounds, or presents itself in writing. Always invoke before writing brand guidelines, tone documents, or evaluating copy consistency — even for small requests like "does this headline fit our brand."
---

# marketing-brand-voice: Analyze, Build, or Validate Brand Voice

Three modes. Same output: a usable `BRAND-VOICE.md` that any writer can pick
up and work from immediately.

- **ANALYZE** — Brand has existing content. Extract voice from URLs.
- **BUILD** — Brand is new or wants to redefine. Construct voice from scratch.
- **VALIDATE** — Brand has a voice guide. Check if specific copy is on-brand.

Detect the mode from the user's request. If ambiguous, ask in one line:
"Do you have existing content to analyze, or should we define the voice
from scratch? Or do you have copy you want to check against your brand voice?"

---

## Step 0: ICP Anchor (Always Required)

Brand voice doesn't exist in isolation — it's defined by who you're talking
to. Before any mode runs, collect this:

```
ICP (Ideal Customer Profile):
  Role / identity: [who they are]
  Sophistication level: [novice / intermediate / expert in this domain]
  Primary pain: [what they're trying to solve]
  Emotional state when they encounter this brand: [frustrated / curious /
    skeptical / excited / overwhelmed / etc.]
  What they need to feel to trust this brand: [competence / warmth /
    boldness / clarity / etc.]
```

This anchors every voice decision. A brand talking to anxious first-time
founders needs a different voice than one talking to seasoned operators —
even if both brands are in the same category.

If the user skips this, infer from available content and flag assumptions.

---

## MODE A — ANALYZE

User has existing published content. Extract and document the voice.

### A.1 Source Collection

Fetch content in priority order. Stop when you have enough signal (usually
after primary + 2 secondary sources). Don't over-fetch.

**Primary (always fetch):**
1. Homepage — most curated brand expression
2. About page — how the brand describes itself
3. Product or service pages — how they frame their offering

**Secondary (fetch if available):**
4. Blog posts (2–3 recent)
5. Social media bios and recent posts
6. Email copy (welcome email, recent newsletter)
7. Microcopy (error messages, onboarding flows, CTAs)

**Tertiary (only if primary/secondary are thin):**
8. Job postings — reveals internal culture
9. Ad copy — paid messaging approach
10. Press releases — formal communication style

### A.2 Voice Dimension Scoring

Score each dimension 1–10. Every score requires 3 specific quoted examples
from the source material. No score without evidence.

**Dimension 1: Formal ←——→ Casual**
Signals: contractions, sentence length, vocabulary level, use of humor,
pronouns (third person vs. we/you), greetings style.

**Dimension 2: Serious ←——→ Playful**
Signals: metaphors, exclamation marks, emoji, wordplay, self-deprecation,
tone of error messages.

**Dimension 3: Technical ←——→ Simple**
Signals: jargon density, acronym handling, level of assumed expertise,
use of analogies vs. domain-specific examples.

**Dimension 4: Reserved ←——→ Bold**
Signals: hedged vs. direct claims, use of opinions, competitive references,
ambition of promises, willingness to take a stance.

Output as a visual map:

```
Formal     [1  2  3  4  5  6  7  8  9  10]  Casual
Serious    [1  2  3  4  5  6  7  8  9  10]  Playful
Technical  [1  2  3  4  5  6  7  8  9  10]  Simple
Reserved   [1  2  3  4  5  6  7  8  9  10]  Bold
                                    ^
                              mark position
```

### A.3 Personality Archetype

Identify primary and (if applicable) secondary archetype. Require evidence.

| Archetype | Character | Voice style | Typical industries |
|-----------|-----------|-------------|--------------------|
| **The Authority** | Expert, data-driven, trustworthy | Confident, precise, educational | Finance, B2B, healthcare, consulting |
| **The Innovator** | Visionary, disruptive, forward-thinking | Exciting, future-focused, provocative | SaaS, tech, startups |
| **The Friend** | Warm, approachable, relatable | Conversational, empathetic, inclusive | Consumer, education, community |
| **The Rebel** | Bold, irreverent, challenging | Direct, opinionated, memorable | Lifestyle, fitness, DTC |
| **The Guide** | Patient, methodical, wise | Clear, instructional, supportive | Edtech, tools, platforms |

Flag archetype-ICP mismatches. A brand targeting skeptical operators but
sounding like "The Friend" has a credibility gap.

### A.4 Tone by Context

Map how the voice shifts (appropriately) across contexts. Voice is constant;
tone adapts.

| Context | Tone | Quoted example |
|---------|------|----------------|
| Homepage hero | | |
| Product description | | |
| Blog post intro | | |
| CTA buttons | | |
| Error / 404 message | | |
| Social media | | |
| Email subject line | | |
| Customer support | | |

Flag contexts where the tone shift is too extreme — where it stops feeling
like the same brand.

### A.5 Vocabulary Fingerprint

From all source material, extract:

**Words used frequently** (organized by type):
- Action verbs: e.g., "build", "scale", "unlock"
- Adjectives: e.g., "powerful", "effortless", "enterprise-grade"
- Value words: e.g., "transparent", "sustainable", "inclusive"
- Industry terms: specific to their domain

**Words notably absent** — what the brand deliberately avoids or what would
feel out of character.

**Signature patterns** — recurring phrases, structural habits (e.g., always
leads with verbs, uses em-dashes, favors short paragraphs, never uses
passive voice in CTAs).

### A.6 Consistency Audit

| Channel | Consistency | Key observation |
|---------|-------------|-----------------|
| Homepage | ✅ / ⚠️ / ❌ | |
| About page | ✅ / ⚠️ / ❌ | |
| Blog | ✅ / ⚠️ / ❌ | |
| Social | ✅ / ⚠️ / ❌ | |
| Email | ✅ / ⚠️ / ❌ | |
| Microcopy | ✅ / ⚠️ / ❌ | |

Overall consistency score: X/10

Frame inconsistencies as opportunities, not failures. Inconsistency usually
means multiple writers without a shared guide — exactly what this document fixes.

Then proceed to **Step 1: Generate BRAND-VOICE.md**.

---

## MODE B — BUILD

Brand is new, pre-launch, or wants to redefine its voice from scratch.
No URLs needed. Drive through a structured interview.

### B.1 Brand Foundation Interview

Ask these questions in a conversational flow, not as a form dump. Group
related questions together. Allow partial answers.

**Who you are:**
- What does this brand do, and for whom? (one sentence)
- Why does it exist beyond making money? What would be lost if it disappeared?
- What are 3 non-negotiable values?

**Who you're talking to:** *(use ICP from Step 0)*
- What does your ICP read, watch, follow?
- What brands do they already trust and why?
- What communication style makes them immediately distrust a brand?

**Personality:**
- If this brand were a person at a dinner party, how would they behave?
- What 3 adjectives describe them? What 3 adjectives would they never be?
- Which of the 5 archetypes fits best? (show the table from A.3)
- Name 2–3 brands outside your industry whose voice you admire. What
  specifically do you admire about each?

**Boundaries:**
- What topics, tones, or approaches are off-limits for this brand?
- Are there industry clichés or overused phrases that must be avoided?
- Any words or phrases that must always / never appear?

**Differentiation:**
- How do your main competitors sound?
- What voice territory are they NOT occupying that you could own?

### B.2 Voice Positioning

Based on the interview, set the 4 dimension scores intentionally —
not as a description of what exists, but as a decision about what to build.

For each dimension, explain the strategic reasoning behind the score:

> "We're positioning at 7/10 Casual because our ICP (ops managers at
> mid-size e-commerce brands) is fatigued by overly formal enterprise
> software communication, but still needs to trust us with serious
> business decisions. Too casual would undermine credibility."

This is brand strategy, not description.

### B.3 Reference Voices

Take the 2–3 admired brands from the interview and extract what's
transferable:

```
Brand: [name]
What works: [specific element — sentence structure, word choice, tone in CTAs]
What doesn't fit: [what to leave behind]
Transferable: [specific pattern to adopt]
```

Then proceed to **Step 1: Generate BRAND-VOICE.md**.

---

## MODE C — VALIDATE

User has an existing voice guide (`BRAND-VOICE.md`) and wants to check
if a specific piece of copy is on-brand.

### C.1 Load the Voice Guide

Read `BRAND-VOICE.md` if it exists. If not, ask the user to describe
the key voice rules in a few sentences before proceeding.

### C.2 Validate the Copy

Score the submitted copy against the established voice:

| Check | Pass / Fail | Evidence |
|-------|-------------|----------|
| Dimension scores match (Formal/Casual, etc.) | | |
| Uses vocabulary from the "words we use" list | | |
| Avoids words from the "words we avoid" list | | |
| Matches the primary archetype | | |
| Tone is appropriate for this context | | |
| Speaks to the ICP at the right level | | |

**Overall: On-brand / Mostly on-brand / Off-brand**

### C.3 Fix Off-Brand Elements

For every failed check, provide a concrete rewrite:

```
ISSUE: Too formal for a brand scoring 7/10 Casual
ORIGINAL: "We endeavor to provide solutions that address your operational needs."
REWRITE:  "We help your ops team stop drowning in manual work."
WHY: Matches casual dimension score, uses active voice, speaks directly
     to the ICP's pain without corporate hedging.
```

---

## Step 1: Generate BRAND-VOICE.md

Runs after Mode A or B. Produces the deliverable.

The goal: a document a new writer can pick up and immediately produce
on-brand copy without ever having worked with this brand before.

```markdown
# Brand Voice Guidelines
## [Brand Name]
**Last updated:** [date] | **Mode:** [Analyzed / Built] | **Version:** 1.0

---

## Who We're Talking To
[ICP summary from Step 0 — one paragraph. This is the north star.]

---

## Voice in One Paragraph
[2–3 sentences that capture the essence of the brand voice. Should be
vivid enough that a writer knows immediately if something feels right.]

---

## Voice Dimensions

Formal     [1  2  3  4  5  6  7  8  9  10]  Casual      → [X/10]
Serious    [1  2  3  4  5  6  7  8  9  10]  Playful     → [X/10]
Technical  [1  2  3  4  5  6  7  8  9  10]  Simple      → [X/10]
Reserved   [1  2  3  4  5  6  7  8  9  10]  Bold        → [X/10]

[One paragraph explaining the strategic reasoning behind these scores]

---

## Brand Personality
**Primary archetype:** [name]
**Secondary archetype:** [name, if applicable]
[Two sentences on why this fits the brand and ICP]

---

## Voice Chart

| Our voice IS        | Our voice IS NOT     |
|---------------------|----------------------|
| [trait]             | [anti-trait]         |
| [trait]             | [anti-trait]         |
| [trait]             | [anti-trait]         |
| [trait]             | [anti-trait]         |

---

## Tone by Context
| Context             | Tone                 | Example              |
|---------------------|----------------------|----------------------|
| Homepage hero       |                      |                      |
| Product description |                      |                      |
| Blog post           |                      |                      |
| CTA buttons         |                      |                      |
| Error messages      |                      |                      |
| Social media        |                      |                      |
| Email subject lines |                      |                      |

---

## Vocabulary

### Words We Use
- Action verbs: [list]
- Adjectives: [list]
- Value words: [list]

### Words We Avoid
[List with one-line reason for each]

### Signature Phrases
[Recurring patterns and linguistic habits]

---

## Writing Guidelines

**DO:**
- [Specific, actionable instruction]
- [Example included for each]

**DON'T:**
- [Specific anti-pattern]
- [Example included for each]

---

## Messaging Hierarchy

**Tagline:** [under 10 words]
**Value propositions:** [3–5, one sentence each]
**Elevator pitch:** [75 words, conversational]
**Boilerplate:** [100–150 words, for press/bios]

---

## Copy Samples

Eight examples covering different contexts. These are the most important
part of this document — writers learn voice by example, not description.

1. Homepage headline
2. Product description paragraph
3. Blog post opening
4. Social media post
5. Email subject line
6. CTA button text
7. Error message
8. Customer thank-you message

---

## Consistency Notes
[From Mode A only: channel-by-channel audit + overall score + top 3
consistency improvements recommended]
```

---

## Cross-Skill Integration

- `BRAND-VOICE.md` feeds directly into `marketing-copywriting` — always load it
  before generating or validating any copy
- If `COMPETITOR-REPORT.md` exists → use it for voice differentiation
  analysis in Mode A and voice positioning in Mode B
- Suggest follow-up: `/marketing-copywriting` to generate or validate copy using
  this voice guide

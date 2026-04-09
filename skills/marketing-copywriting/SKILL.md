---
name: marketing-copywriting
version: 1.0.0
description: >
  Validates existing copy or generates new copy from scratch for any marketing
  context — headlines, landing pages, ads, emails, CTAs, product descriptions,
  and more. Triggers when the user asks "review my copy", "does this headline
  work", "write me a landing page", "improve this CTA", "validate this ad",
  "generate copy for X", or any request involving marketing text quality or
  creation. Always invoke before writing or evaluating marketing copy, even
  for small requests like "make this sound better."
---

# marketing-copywriting: Validate or Generate Marketing Copy

Two modes. Same strategic foundation.

- **VALIDATE** — User provides existing copy. Analyze, score, and rewrite.
- **GENERATE** — User needs copy from scratch. Collect context and produce it.

Detect the mode from the user's request. If ambiguous, ask in one line:
"Do you have copy to review, or should I write it from scratch?"

---

## Step 1: Strategic Intake (Recommended)

Collecting this context produces dramatically better output. Present it as a
quick optional brief — but always ask before generating or validating.

If the user wants to skip it, proceed and flag what was assumed.

```
COPY BRIEF:
  What is this copy for? (page type, ad, email, CTA, etc.)
  ICP: Who is the ideal reader? (role, situation, level of sophistication)
  Primary pain: What problem does this solve? (their words if possible)
  Underlying fear: What's the deeper emotional driver behind the pain?
  Desired action: What should the reader do after reading?
  Traffic source: Cold / warm / retargeting (shapes tone and assumed knowledge)
  Awareness stage: [see below]
  Brand voice: 3 adjectives + any rules or words to avoid
  Key differentiator: What can't competitors honestly claim?
  Objections: What doubts does the reader arrive with?
```

**Awareness Stage** (Eugene Schwartz) — ask the user to pick one:
1. **Unaware** — Reader doesn't know they have the problem
2. **Problem Aware** — Knows the problem, unaware of solutions
3. **Solution Aware** — Knows solutions exist, hasn't heard of this product
4. **Product Aware** — Knows the product, hasn't committed
5. **Most Aware** — Ready to act, needs a reason and risk reversal

This single input changes the entire copy strategy. Unaware = educate first.
Most Aware = direct offer, remove friction.

If the user skips the brief, infer what you can from the copy or context
provided, and state your assumptions explicitly at the top of the output.

---

## Step 2: Mode Execution

### MODE A — VALIDATE

User provides copy. Evaluate it against the brief (or stated assumptions).

**2A.1 Score the copy across 6 dimensions:**

| Dimension | 0–10 | What it measures |
|-----------|------|------------------|
| **Clarity** | | Would a 12-year-old understand what this does and for whom? |
| **Persuasion** | | Does it move toward action? Does it handle objections? |
| **Specificity** | | Concrete numbers, outcomes, timeframes vs. vague claims? |
| **Emotion** | | Connects with real pain, fear, desire, or aspiration? |
| **Action** | | CTAs clear, low-friction, strategically placed? |
| **Alignment** | | Matches ICP, awareness stage, and traffic source? |

Total: X/60 → convert to 0–100 (× 1.67)

**2A.2 Value Proposition Check:**

Flag if any of these are missing or weak:
- Who this is for (specific ICP, not "businesses")
- What painful problem it solves (in the customer's language)
- What the unique mechanism or differentiator is
- What measurable outcome the customer gets
- What proof supports the claims

**2A.3 Awareness Stage Mismatch Check:**

Call out copy that's misaligned with the stated stage. Common mismatches:
- Unaware audience → product-first copy → needs problem framing first
- Most Aware audience → heavy education → too much friction before the offer
- Solution Aware audience → generic value prop → fails to differentiate

**2A.4 Before/After Rewrites:**

For every significant issue, provide a rewrite. No abstract recommendations —
every suggestion comes with a concrete replacement.

```
BEFORE: "We help businesses grow with smart technology."

AFTER:  "Ops teams at 10–50 person e-commerce brands use [product]
         to cut manual reporting time by 6 hours a week."

WHY:    "Before" is vague and self-referential. "After" names the ICP,
         quantifies the outcome, and mirrors how the customer describes
         the pain. Matches Solution Aware stage — no need to explain
         the problem category.
```

Minimum rewrites: headline, subheadline, primary CTA, one body paragraph.
Add more for any section with a score below 6.

---

### MODE B — GENERATE

User needs copy written from scratch (or near-scratch).

**2B.1 Confirm scope before writing:**

Clarify what exactly needs to be written:
- Full page (homepage, landing page, pricing, about, product, feature, email)
- Single element (headline, CTA, subject line, ad, bio, meta description)
- Sequence (email series, ad variations, onboarding flow)

For full pages → read `references/page-structures.md` for section templates.
For single elements → generate inline with 3 strong alternatives minimum.

**2B.2 Generation principles:**

Every piece of copy must:
- Open at the reader's awareness level — meet them where they are
- Lead with the customer's pain or desire, not the product's features
- Use the customer's own language (mirror their words, not marketing speak)
- Speak to the specific ICP, not a broad audience
- Reflect the brand voice (the 3 adjectives from the brief)
- Address at least one key objection before the CTA
- End with a single, clear, low-friction desired action

**2B.3 Headline generation:**

Always produce 5 headline options using different frameworks. Label each.

**PAS (Problem-Agitate-Solve):**
> "Stop [pain in customer's words]. [Desired outcome] — with [product]."

**Before-After-Bridge:**
> "From [painful current state] to [desired future state] — [how]."

**Specific Outcome:**
> "[Number] [ICP role] use [product] to [outcome] in [timeframe]."

**Fear Reversal:**
> "Never [underlying fear] again. [Product] [mechanism] so you [desired state]."

**Identity-Based:**
> "[Product] for [ICP who takes pride in the outcome]."

Rank by estimated fit for the stated awareness stage. Briefly explain the top pick.

**2B.4 CTA generation:**

For every CTA produced:
- Write in first person: "Start My Free Trial" not "Start Your Free Trial"
- Make the value explicit: "Get My Report" not "Submit"
- Reduce perceived risk: "Try Free for 14 Days" not "Buy Now"
- Be specific: "Download the 2026 Pricing Guide" not "Download"
- Add urgency only when genuine and specific

Provide 3 CTA alternatives per placement.

---

## Step 3: Output

Adapt length to scope. A single headline request → tight inline output.
A full landing page → structured report. Use judgment.

### For VALIDATE:

```
=== COPY VALIDATION ===

Mode: Validate
Assumptions: [list anything inferred from context, not provided]
Awareness Stage: [stage + label]

Score: X/60 (X/100)
  Clarity:     X/10
  Persuasion:  X/10
  Specificity: X/10
  Emotion:     X/10
  Action:      X/10
  Alignment:   X/10

⚡ Top Issues + Rewrites:
  1. [issue] → [rewrite]
  2. [issue] → [rewrite]
  3. [issue] → [rewrite]

Full before/after breakdown below.
```

### For GENERATE:

```
=== COPY GENERATION ===

Mode: Generate
Scope: [what was produced]
Assumptions: [anything inferred, not provided]
Awareness Stage: [stage + label]

[Generated copy, structured by section or element]

Headline options: [5 alternatives with labels]
Recommended: [top pick + one-line rationale]
```

---

## Cross-Skill Integration

- If `BRAND-VOICE.md` exists → use it to override voice inputs from the brief
- If `COMPETITOR-REPORT.md` exists → use competitor messaging to sharpen
  differentiation and avoid overused angles
- Suggest follow-up: `/marketing-brand-voice` for building a voice guide from scratch

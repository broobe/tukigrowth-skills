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

### Natural Writing Guardrails

Before validating or generating copy, apply these rules. The goal is copy that
sounds like a skilled human wrote it for this exact reader, not like a generic
copywriting framework.

**Default tone:** natural, specific, and direct. Do not make the copy sound
more dramatic than the customer context supports.

Avoid these AI-slop patterns unless the brief explicitly calls for a punchy,
contrarian, or manifesto-style tone:

**Negative parallelisms**
- Weak: "The problem isn't your CRM. It's your follow-up process."
- Weak: "It's not just a dashboard. It's a revenue command center."
- Better: "Your team logs every lead, but follow-up still happens too late."
- Better: "The dashboard shows which deals are stuck and who owns the next
  step."

**Rule of three abuse**
- Weak: "A simple, powerful, scalable platform."
- Weak: "Save time, close more deals, and grow faster."
- Better: "A platform for sales teams that need cleaner handoffs."
- Better: "Cut the time between demo request and first reply."

**Formulaic contrast hooks**
- Weak: "Stop chasing leads. Start closing revenue."
- Weak: "Less admin. More selling. Better results."
- Better: "Reps see today's follow-ups before they open their inbox."
- Better: "Managers can spot stale opportunities without asking for another
  pipeline update."

**False ranges**
- Weak: "From lead generation to retention, we handle everything."
- Weak: "From strategy to execution, your growth engine is covered."
- Better: "We handle landing pages, lifecycle emails, and paid search
  reporting."
- Better: "The team builds the campaign plan, writes the assets, and reports
  on pipeline impact."

**Superficial significance claims**
- Weak: "A game-changing solution that transforms how teams sell."
- Weak: "This redefines the customer acquisition landscape."
- Better: "Sales managers get one view of open deals, last touch, and next
  action."
- Better: "The report shows CAC, payback period, and channel-level spend in
  one place."

**Vague attribution**
- Weak: "Leading teams know that personalization is crucial."
- Weak: "Experts agree that speed-to-lead matters."
- Better: "If a demo request waits until tomorrow, the rep starts the
  conversation cold."
- Better: Name the source, metric, or customer quote. If there is no source,
  cut the claim.

**Promotional puffery**
- Weak: "Unlock seamless growth with an innovative solution."
- Weak: "A robust platform designed to empower modern teams."
- Better: "Launch the email sequence, track replies, and see which accounts
  booked a call."
- Better: "Import a list, assign owners, and start outreach from the same
  workspace."

**Filler transitions**
- Avoid: "Additionally", "Furthermore", "Moreover", "It's worth noting",
  "It's important to remember", "In today's fast-paced world"
- Better: start with the next concrete point.

Prefer these moves:
- Name the reader's actual situation instead of dramatizing the pain
- Use concrete nouns, numbers, constraints, and tradeoffs when available
- Keep the same word for the same concept; do not vary synonyms just to sound
  polished
- Write sentences someone could say out loud without sounding like an ad
- Let specifics create persuasion. Do not add importance claims unless the
  evidence is in the brief

**Quick self-check before final output:**
- Red-flag word clusters: Are there multiple vague words in one paragraph,
  such as "seamless", "robust", "innovative", "powerful", "transform",
  "unlock", or "empower"?
- Triple patterns: Did the copy stack three adjectives, three benefits, or
  three abstract nouns because it sounded polished?
- Fake contrast: Did any line use "not X, but Y", "more than X", or
  "stop X, start Y" without a strong strategic reason?
- Hollow stakes: Does the copy claim something is important, game-changing, or
  transformative without showing the concrete customer impact?
- Generic pain: Could the pain apply to almost any company, team, or buyer?
- Missing proof: Is there a claim that needs a number, source, customer quote,
  use case, or product detail?
- Filler openings: Does any paragraph start with filler like "Additionally",
  "Furthermore", "In today's market", or "It's important to"?
- Term drift: Are marketing/sales terms used consistently, or did synonym
  swaps create fog around the offer?
- Human read: Would a strong marketer or sales lead actually say this out
  loud, or does it sound like an AI prompt result?

If any answer is yes, revise before responding. Cut filler, replace generic
claims with specifics, or simplify the sentence.

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
- What specific problem it solves (in the customer's language)
- What the unique mechanism or differentiator is
- What measurable outcome the customer gets
- What proof supports the claims

**2A.3 Awareness Stage Mismatch Check:**

Call out copy that's misaligned with the stated stage. Common mismatches:
- Unaware audience → product-first copy → needs problem framing first
- Most Aware audience → heavy education → too much friction before the offer
- Solution Aware audience → generic value prop → fails to differentiate

Also flag copy that sounds over-engineered or AI-generated: forced contrast
hooks, abstract transformation claims, adjective stacks, and drama that the
brief does not support.

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
- Enter through the reader's real situation, friction, or desired outcome —
  not through a forced pain hook
- Use the customer's own language (mirror their words, not marketing speak)
- Speak to the specific ICP, not a broad audience
- Reflect the brand voice (the 3 adjectives from the brief)
- Address at least one key objection before the CTA
- End with a single, clear, low-friction desired action
- Treat headline frameworks as internal thinking tools, not visible templates.
  If a framework makes the line sound formulaic, discard it.

**2B.3 Headline generation:**

Produce 5 headline options from different angles. Do not label the frameworks
in the final output unless the user asks for the reasoning.

**PAS (Problem-Agitate-Solve):**
> "[Specific reader] can [specific outcome] without [specific friction]."

**Before-After-Bridge:**
> "[Current situation in plain language]. [Product/mechanism] helps you
> [better next state]."

**Specific Outcome:**
> "[Number] [ICP role] use [product] to [outcome] in [timeframe]."

**Fear Reversal:**
> "[Product] helps you avoid [specific risk] before it turns into
> [specific consequence]."

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

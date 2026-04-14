---
name: marketing-objectives
version: 1.0.0
description: >
  Defines, validates, and refines marketing objectives — converting vague goals
  into measurable targets with KPIs, baselines, and deadlines. Triggers when the
  user asks "how to set marketing objectives", "define KPIs", "validate a goal",
  "convert this goal into something measurable", "what metrics should I track",
  "set targets for this quarter", "are these objectives well-defined", or any
  request involving marketing goal-setting, KPI selection, target definition,
  objective validation, or converting business goals into marketing objectives.
  Also triggers when the user has already selected a funnel framework and needs
  to define objectives per stage.
---

# Marketing Objectives

Turn business intentions into specific, measurable marketing objectives — or take
existing objectives and make them rigorous.

## What this skill does

This skill operates in three modes. Detect which one the user needs based on
their input:

1. **DEFINE** — Build marketing objectives from scratch, starting from the
   business goal and cascading down to measurable targets with KPIs.
2. **VALIDATE** — Take existing objectives the user shares and evaluate whether
   they are well-formed, actionable, and connected to business outcomes.
3. **REFINE** — Take vague or incomplete goals and convert them into proper
   measurable objectives.

Users rarely name the mode explicitly. Infer it:
- User describes a business situation with no objectives yet → **DEFINE**
- User shares objectives and asks "are these good?" → **VALIDATE**
- User says things like "we want more sales" or "grow the brand" → **REFINE**

---

## Objective hierarchy

Every marketing objective should trace upward to a business goal. Use this
three-level cascade:

```
Business objective (company-level outcome)
  └── Marketing objective (what marketing must deliver)
       └── KPI target (the measurable number and deadline)
```

**Business objective** — Revenue, market share, profitability, unit economics.
Set by leadership. Marketing contributes to it but doesn't own it alone.

**Marketing objective** — What marketing specifically needs to move: awareness,
leads, conversion rate, retention, LTV, CAC, etc. This is what marketing owns.

**KPI target** — The exact metric, the number, the timeframe. Without this,
the objective is just a wish.

**Example:**
- Business objective: Increase annual revenue by 30%
- Marketing objective: Increase qualified lead volume by 40% while maintaining
  CAC below $45
- KPI target: 1,200 MQLs/quarter by Q3, up from 857 current baseline

---

## SMART structure

Every objective this skill produces must satisfy all five criteria. Don't just
label them — verify each one concretely:

**Specific** — Names the exact metric, audience segment, and funnel stage.
Not "improve marketing" but "increase organic traffic conversion rate on the
pricing page for enterprise visitors."

**Measurable** — Has a number, a direction, and a comparison point (baseline,
benchmark, or previous period). Not "more leads" but "from 200 to 300 MQLs/month."

**Achievable** — The target is grounded in something: historical trend, industry
benchmark, capacity analysis, or comparable past performance. If the user proposes
a number with no basis, flag it and propose one that's defensible. A 10x increase
with no budget change is a wish, not an objective.

**Relevant** — The objective directly connects to the business goal and the
current bottleneck. If the real problem is retention, setting an awareness
objective is off-target. Always check: does moving this metric actually move
the business?

**Time-bound** — Has a deadline. Not "eventually" but "by end of Q2" or "within
6 months."

---

## KPI selection per funnel stage

When the user has selected a funnel framework (from `funnel-strategy`), use the
appropriate KPIs per stage. If no framework was selected, ask which funnel model
they're using — or recommend one based on their situation.

### TOFU / MOFU / BOFU
- **TOFU**: impressions, reach, unique visitors, branded search volume, share
  of voice, video views
- **MOFU**: engaged sessions, content downloads, email subscribers, webinar
  registrations, time on site
- **BOFU**: demo requests, free trial signups, quote requests, add-to-cart,
  purchase intent signals

### AARRR (SaaS / product-led)
- **Acquisition**: new signups, organic traffic, paid installs, referral signups
- **Activation**: first-value action rate, onboarding completion, time-to-value
- **Retention**: D7/D30/D90 retention, churn rate, active users
- **Revenue**: ARPU, MRR growth, conversion to paid, expansion revenue
- **Referral**: invites sent, viral coefficient, NPS

### E-commerce funnel
- **Discovery**: sessions, new users, social reach
- **Product view**: product page views, PDP-to-ATR ratio
- **Add to cart**: ATC rate, cart additions
- **Checkout**: checkout start rate, payment method selection
- **Purchase**: conversion rate, AOV, revenue per session
- **Repeat purchase**: repeat rate, purchase frequency, time between purchases

### B2B pipeline
- **Lead**: inbound leads, form fills, content downloads
- **MQL**: marketing qualified lead count, MQL-to-SQL rate
- **SQL**: sales accepted leads, pipeline value created
- **Opportunity**: deal velocity, win rate, average deal size
- **Closed Won**: revenue, CAC, LTV:CAC ratio

### Lifecycle / retention-heavy
- **Activation**: first purchase, onboarding milestone
- **Retention**: repeat purchase rate, subscription renewal, active days
- **Expansion**: cross-sell rate, upsell revenue, NRR
- **Advocacy**: referral rate, reviews submitted, UGC volume

---

## Target-setting methods

Don't pick numbers arbitrarily. Use one of these methods and name it:

**Historical baseline** — Where is the metric now? Target a realistic improvement
from current state. Example: "Current conversion is 2.1%. Target: 2.8% (33%
relative increase)."

**Industry benchmark** — What's typical for this vertical? Useful when no
internal baseline exists. Name the source or state it's directional.

**Capacity-based** — What can the team actually deliver with current resources?
Example: "Content team can produce 8 pieces/month. At 3% conversion, that's
~24 leads/month. Target: 30 leads/month (requires improving conversion to 3.75%)."

**Top-down allocation** — Business goal divided down. Example: "Need $1M ARR.
At $500 ACV, that's 2,000 customers. If marketing drives 60% of pipeline and
conversion is 5%, we need 24,000 leads. Across 12 months: 2,000/month."

**Bottleneck-driven** — Identify the stage with the biggest drop-off and set the
target there. Example: "Landing page gets 10K visits but only 1.5% convert. The
biggest lever is conversion rate. Target: move to 2.5% by improving the CTA and
social proof."

Always state which method you're using so the user can challenge the assumption.

---

## DEFINE mode workflow

When building objectives from scratch:

1. **Clarify the business goal.** Ask: "What does the business need to happen
   in the next quarter/year?" If they don't know, suggest working backward from
   revenue targets.

2. **Identify the funnel stage(s).** Use the selected framework (or recommend
   one). Ask: "Where is the biggest gap right now — getting people in the door,
   converting them, or keeping them?"

3. **Select the KPI.** Pick the metric that most directly measures progress at
   that stage. One primary KPI per objective. Secondary KPIs are fine but the
   primary one is the target.

4. **Set the baseline.** Find out where the metric is today. If the user
   doesn't know, say "we need at least a directional estimate" and suggest how
   to get it.

5. **Set the target.** Use one of the target-setting methods above. State the
   method and the math.

6. **Set the timeframe.** Default to quarterly. Adjust based on the user's
   planning cycle.

7. **Check for conflicts.** Make sure objectives don't contradict each other.
   Example: "increase lead volume by 50%" and "reduce CAC by 30%" might be
   incompatible without additional budget or channel efficiency.

**Output format for DEFINE:**

For each objective, present:

```
Objective: [clear, specific statement]
KPI: [primary metric]
Baseline: [current state as of date]
Target: [number + timeframe]
Method: [how the target was determined]
Funnel stage: [which stage this moves]
Connected to business goal: [which business objective this serves]
Risks / assumptions: [what could make this target unrealistic]
```

Produce 1-3 objectives per cycle. More than 3 dilutes focus.

---

## VALIDATE mode workflow

When the user shares existing objectives:

1. **SMART check.** For each criterion (Specific, Measurable, Achievable,
   Relevant, Time-bound), rate it: PASS, PARTIAL, or FAIL. Be direct.

2. **Hierarchy check.** Can you trace it up to a business goal? Is the KPI
   the right metric for the funnel stage?

3. **Conflict check.** Do any objectives work against each other?

4. **Feasibility check.** Is the target grounded in data, or aspirational
   without basis?

**Output format for VALIDATE:**

For each objective:
```
Verdict: [WELL-FORMED / NEEDS WORK / POORLY-FORMED]
SMART breakdown:
  Specific: [PASS/PARTIAL/FAIL — reason]
  Measurable: [PASS/PARTIAL/FAIL — reason]
  Achievable: [PASS/PARTIAL/FAIL — reason]
  Relevant: [PASS/PARTIAL/FAIL — reason]
  Time-bound: [PASS/PARTIAL/FAIL — reason]
Issues: [list specific problems]
Suggested rewrite: [improved version if applicable]
```

---

## REFINE mode workflow

When the user has vague goals:

1. **Name the vague goal** back to them explicitly so they confirm you
   understood correctly.

2. **Identify what's missing.** Usually one or more of: metric, number,
   timeframe, funnel stage, connection to business outcome.

3. **Ask targeted questions** to fill the gaps. Don't ask everything at once.
   Prioritize:
   - What does "more" mean specifically? (quantity)
   - By when? (timeframe)
   - For whom? (segment)
   - Compared to what? (baseline)

4. **Produce the refined objective** in the standard format.

**Example transformation:**
- Input: "queremos crecer la marca"
- Questions: "What does 'grow the brand' look like in numbers? More searches?
  More social followers? More direct traffic? And compared to what baseline?"
- Output: "Increase branded search volume by 25% (from 3,200 to 4,000
  monthly searches) by end of Q3, measured via Google Search Console."

---

## Common anti-patterns to flag

When you detect these, correct them:

- **Vanity metrics as objectives.** Followers, likes, impressions without
  connection to business outcomes. Reframe: "What does 10K followers do for
  revenue?"

- **Activity as objective.** "Publish 20 blog posts" is an activity, not an
  outcome. The objective is the result those posts should produce.

- **Too many objectives.** More than 3 marketing objectives per quarter
  usually means none will be achieved. Prioritize ruthlessly.

- **Aspirational targets without basis.** "Double revenue" with no supporting
  math. Ask: "Based on what?"

- **Ignoring baselines.** You can't set a target without knowing where you are
  now. If the user has no data, the first objective should be "establish
  measurement."

- **Conflicting objectives.** "Increase volume AND decrease cost per unit"
  without explaining how. Flag the tension and resolve it.

- **Objectives disconnected from funnel stage.** An awareness objective measured
  by revenue, or a retention objective measured by traffic. Match metric to
  stage.

---

## Integration with other skills

This skill connects to the broader marketing planning toolkit:

**Upstream (inputs this skill reads):**
- `funnel-strategy` — the chosen framework determines which KPIs and stages
  are relevant. If the user hasn't chosen one, recommend they consult that
  skill first, or help them pick one inline.
- `marketing-competitors-analysis` — competitive benchmarks help set realistic
  targets. Reference `COMPETITOR-REPORT.md` if available.
- `digital-marketing-strategy-tactics` — objectives should align with the
  strategy level, not skip to tactics.

**Downstream (outputs this skill produces):**
- Well-defined objectives feed into `digital-marketing-strategy-tactics` as
  the "strategy" level, which then breaks into hypotheses, initiatives, and
  tactics.
- Objectives define the awareness stage and conversion targets that
  `marketing-copywriting` needs for effective copy.
- Funnel-stage objectives inform `marketing-brand-voice` tone-by-context
  mapping.

---

## Output style

- Write in the user's language
- Be direct and specific — avoid generic marketing language
- Always show the math behind targets
- When multiple objectives are needed, rank them by impact
- Don't hedge with "it depends" unless you resolve the dependency
- End with clear, actionable objectives the user can copy into their plan

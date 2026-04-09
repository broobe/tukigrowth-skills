---
name: marketing-competitors-analysis
version: 1.0.0
description: >
  Identifies competitors and produces actionable competitive intelligence at
  three depth levels — QUICK, STANDARD, and DEEP. Triggers when the user asks
  "analyze my competitors", "who are my competitors", "competitive analysis",
  "how do I differentiate", "what are competitors doing",
  "benchmark against market", "find positioning gaps",
  `/marketing-competitors-analysis <url>`, or any request involving competitive
  research, market positioning, or strategic differentiation.
---

# marketing-competitors-analysis

Competitive intelligence at three depth levels. Same strategic foundation,
different scope and output size.

- **QUICK** — Snapshot of 3 direct competitors. Positioning map + top 3
  opportunities. Delivered in-chat. ~15 min research.
- **STANDARD** — Full analysis of 5–7 competitors across all tiers. Feature,
  pricing, messaging, and content gaps. Outputs `COMPETITOR-REPORT.md`.
- **DEEP** — Everything in Standard plus review mining, switching narratives,
  alternative page briefs, and a monitoring playbook.

Detect the level from context:
- Casual question or early-stage exploration → QUICK
- Explicit request for a report or full analysis → STANDARD
- Strategic decision, launch preparation, or investor context → DEEP
- If ambiguous, ask: "How deep do you need this? Quick snapshot, full report,
  or deep strategic analysis including review mining and switching narratives?"

---

## Step 0: Strategic Intake (Always Required)

The same competitive landscape looks completely different depending on what
decision the user is trying to make. Collect this before any research starts.

```
COMPETITIVE BRIEF:
  Target brand / URL: [url]
  What decision is this analysis informing?
    [ ] Go-to-market strategy / launch
    [ ] Repositioning or rebranding
    [ ] Pricing decision
    [ ] Content or SEO strategy
    [ ] Investor deck / fundraising
    [ ] General market understanding
    [ ] Other: ___

  ICP: Who is the target customer?
    Role / identity: [who they are]
    Problem being solved: [what pain]
    Sophistication: [novice / intermediate / expert]

  Current position: How does the brand currently describe itself?
    [One sentence — their own words if possible]

  Known competitors: Any they're already aware of?
    [List if known, leave blank if not]

  What would make this analysis useful?
    [What does a good outcome look like for the user?]
```

If the user skips this, infer from the URL and flag assumptions explicitly.

---

## Phase 1: Competitor Identification

### 1.1 Competitor Tiers

| Tier | Definition | Target count |
|------|------------|--------------|
| **Direct** | Same product, same audience, same market | 3–5 |
| **Indirect** | Different product, same problem solved | 2–3 |
| **Aspirational** | Market leaders the brand wants to become | 1–2 |

QUICK level: Direct competitors only (3 max).
STANDARD / DEEP: All three tiers.

### 1.2 Discovery Methods

Run in parallel. Stop when you have enough candidates.

**Search-based:**
- Search primary product category keywords — note who ranks page 1
- Search "[brand name] alternatives" and "[brand name] vs"
- Search "[problem being solved] software / tool / service"

**Site-based:**
- Check the target's blog for competitor mentions
- Look for "integrations" or "compare" pages on the target site
- Check footer links for industry associations

**Review platform-based** (STANDARD / DEEP only):
- Search G2, Capterra, or Trustpilot for the product category
- Note top-rated competitors and most-compared alternatives

**Community-based** (DEEP only):
- Search Reddit for "[product category] recommendations"
- Check LinkedIn for companies followed by the target's audience

### 1.3 Competitor Shortlist

Before deep-diving, output a shortlist for confirmation:

```
COMPETITOR SHORTLIST — confirm before full analysis:

Direct:      [A], [B], [C]
Indirect:    [D], [E]
Aspirational: [F]

Proceeding with analysis unless you want to add, remove, or swap any.
```

---

## Phase 2: Competitor Analysis

Run for each competitor on the shortlist. Depth of each section varies
by level — see markers below.

### 2.1 Messaging & Positioning [ALL LEVELS]

For each competitor, extract:

| Element | What to capture |
|---------|----------------|
| H1 headline | Exact text — reveals positioning claim |
| Subheadline | Secondary message — shows proof or context |
| Value proposition | Core promise — identifies positioning territory |
| Target audience | Who they speak to — reveals segment focus |
| Key differentiator | What sets them apart — shows moat claims |
| Tone of voice | Casual / formal / technical — brand personality |
| Social proof type | Logos / testimonials / stats / certifications |
| Primary CTA | Action they push — reveals conversion strategy |

### 2.2 Positioning Map [ALL LEVELS]

Plot each competitor on two axes relevant to the specific market.
Default axes — adjust based on industry:

- X-axis: Simple ←——→ Powerful
- Y-axis: Budget ←——→ Premium

```
                    PREMIUM
                       │
        [Aspirational] │
                       │
  SIMPLE ──────────────┼────────────── POWERFUL
                       │
     [Target]    [B]   │  [A]
                       │
                    BUDGET
```

Provide one paragraph interpreting the map: what territory is crowded,
what's unoccupied, where the target sits and whether that's intentional.

### 2.3 Pricing Analysis [STANDARD / DEEP]

```
| Plan detail       | Target | Comp A | Comp B | Comp C |
|-------------------|--------|--------|--------|--------|
| Free plan         |        |        |        |        |
| Starter price     |        |        |        |        |
| Pro price         |        |        |        |        |
| Enterprise        |        |        |        |        |
| Free trial        |        |        |        |        |
| Annual discount   |        |        |        |        |
| Pricing model     |        |        |        |        |
| Pricing visible?  |        |        |        |        |
```

**Pricing strategy read:**
- Is the target priced above, at, or below market average?
- Is pricing transparent or gated behind a sales call?
- Are anchoring tactics being used (most expensive plan shown first,
  "most popular" badge, annual toggle default)?
- Does the pricing page communicate value before numbers?

### 2.4 Feature Comparison [STANDARD / DEEP]

```
| Feature           | Target | Comp A | Comp B | Comp C |
|-------------------|--------|--------|--------|--------|
| [Core feature 1]  | Full   | Full   | Partial| No     |
| [Core feature 2]  | Full   | Full   | Full   | Full   |
| [Advanced feat.]  | No     | Full   | No     | Full   |
| [Integration]     | Full   | Full   | No     | Partial|
```

Use: Full / Partial / No / Beta

Flag:
- Features where the target has a clear advantage → competitive moats
- Features where the target has a gap → vulnerabilities
- Features unique to one competitor → potential differentiators to watch

### 2.5 Content & SEO [STANDARD / DEEP]

For each competitor, assess:

| Signal | Target | Comp A | Comp B | Comp C |
|--------|--------|--------|--------|--------|
| Estimated blog posts | | | | |
| Publishing frequency | | | | |
| Content depth | | | | |
| Content types | | | | |
| Key topics covered | | | | |
| Comparison/alt pages | | | | |

**Content Gap Analysis** — topics competitors cover that the target does not:

```
CONTENT GAPS:
  Critical (covered by all competitors): [topic], [topic]
  High priority (covered by 2+):         [topic], [topic]
  Opportunity (covered by 1):            [topic], [topic]
```

### 2.6 Social Media Snapshot [STANDARD / DEEP]

| Platform   | Target | Comp A | Comp B | Comp C |
|------------|--------|--------|--------|--------|
| LinkedIn   | | | | |
| Twitter/X  | | | | |
| Instagram  | | | | |
| YouTube    | | | | |
| Post freq. | | | | |
| Top format | | | | |

Note which platforms each competitor treats as primary vs. secondary,
and which are neglected — neglected platforms = opportunity.

### 2.7 Review Mining [DEEP ONLY]

For each direct competitor, analyze reviews on G2, Capterra, Trustpilot,
or Reddit. Extract:

```
COMPETITOR: [name]
Rating:     X/5  |  Reviews: X

Top praise (what customers love):
  1. [specific feature or experience]
  2. [specific feature or experience]
  3. [specific feature or experience]

Top complaints (what customers hate):
  1. [specific frustration]
  2. [specific frustration]
  3. [specific frustration]

Switching reasons (why customers leave):
  1. [reason]
  2. [reason]

Most common use cases mentioned:
  [list]
```

Review mining is the most underused competitive intelligence source.
Customer complaints about competitors are direct product and messaging
opportunities for the target.

---

## Phase 3: Strategic Analysis

### 3.1 Aggregate SWOT for the Target [ALL LEVELS]

Combine all competitor intelligence into a single SWOT:

```
STRENGTHS — where the target outperforms most competitors:
  - [strength with evidence]

WEAKNESSES — where the target lags most competitors:
  - [weakness with evidence]

OPPORTUNITIES — gaps no competitor addresses well:
  - [opportunity]

THREATS — areas where competitors are significantly stronger:
  - [threat]
```

### 3.2 Steal-Worthy Tactics [STANDARD / DEEP]

Specific marketing tactics from competitors worth adapting. Not copying —
adapting with the target's own voice and positioning.

```
TACTIC: [name]
Source: [Competitor]
What they do: [specific description]
Why it works: [mechanism]
How to adapt: [concrete steps for the target]
Effort: Low / Medium / High
Impact: Low / Medium / High
```

Focus on tactics that are proven, adaptable, and currently absent
from the target's marketing. Aim for 5–8 tactics.

### 3.3 Differentiation Strategy [ALL LEVELS]

Based on the competitive map, recommend how the target can differentiate.
Evaluate each angle:

| Angle | Opportunity | Viability | Recommended? |
|-------|-------------|-----------|--------------|
| **Category** | Own a sub-category ("the [attribute] [category]") | | |
| **Audience** | Own a segment competitors ignore | | |
| **Feature** | A unique capability no competitor offers | | |
| **Philosophy** | Differentiate on values or methodology | | |
| **Experience** | Differentiate on support, community, or UX | | |

For the top 1–2 recommended angles, provide:
- Positioning statement
- Sample headline
- Supporting proof points
- How it manifests across homepage, about page, and CTAs

### 3.4 Alternative Page Strategy [DEEP ONLY]

For each major direct competitor, outline a "[Target] vs [Competitor]" page:

```
PAGE: [Target] vs [Competitor]
Suggested URL: /vs/[competitor] or /alternatives/[competitor]
Search intent: "[competitor] alternative", "[target] vs [competitor]"

Headline: "Looking for a [Competitor] alternative? Here's why [X] teams
           chose [Target] instead."

Sections:
  1. Quick comparison table (features, pricing, ratings)
  2. Where [Target] wins — 3 advantages with evidence
  3. Where [Competitor] wins — honest, builds trust
  4. Who [Target] is best for — ICP fit
  5. Customer switching stories — testimonials from switchers
  6. Switching offer or migration guide
  7. FAQ about switching
  8. Primary CTA

SEO value: These pages target bottom-of-funnel searches with high
           purchase intent — among the highest-converting content types.
```

### 3.5 Switching Narratives [DEEP ONLY]

For each major competitor, build the narrative for customers considering
switching:

```
FROM: [Competitor] → TO: [Target]

Why customers switch (from review mining):
  1. [Primary reason]
  2. [Secondary reason]

Switching story template:
  "Like many [ICP role], [customer] started with [Competitor] because
   [initial appeal]. But after [pain event], they needed [what target
   provides]. After switching, they [specific result with numbers]."

Switching offer ideas:
  - Free migration assistance
  - Extended trial for [Competitor] users
  - Dedicated onboarding for switchers
  - Pricing match for first 3 months
```

---

## Phase 4: Monitoring Plan [STANDARD / DEEP]

### Ongoing Intelligence Checklist

```
MONTHLY:
  [ ] Check competitor pricing pages for changes
  [ ] Review competitor product update announcements
  [ ] Monitor new content published (topics + frequency)
  [ ] Check Meta Ad Library and Google Ads Transparency
      for new competitor ad creative

QUARTERLY:
  [ ] Re-run review mining on G2 / Capterra / Trustpilot
  [ ] Audit competitor social media strategy shifts
  [ ] Recheck feature comparison matrix
  [ ] Update positioning map

ALWAYS-ON:
  [ ] Google Alerts for each competitor name
  [ ] Subscribe to competitor newsletters
  [ ] Follow competitors on relevant social platforms
  [ ] Monitor competitor job postings — reveals
      strategic priorities before they're public
```

### Competitive Response Playbook

| Competitor move | Response strategy | Timeline |
|----------------|-------------------|----------|
| Price cut | Emphasize value, don't match on price | 1 week |
| New feature launch | Assess, communicate roadmap to customers | 2 weeks |
| Aggressive ad campaign | Double down on owned channels + retention | Ongoing |
| Negative comparison content | Publish factual, balanced comparison | 1 week |
| Major funding / acquisition | Reassure customers, emphasize focus | 1–2 days |
| Competitor shutting down | Activate switching campaign immediately | 48 hours |

---

## Output Format

### QUICK — In-chat only

```
=== COMPETITIVE SNAPSHOT: [Target] ===

Direct competitors analyzed: [A], [B], [C]
Positioning: [one sentence on where target sits in the map]

Positioning Map:
[text-based map]

Key findings:
  Biggest advantage:   [specific]
  Biggest gap:         [specific]
  Unoccupied territory: [specific]

Top 3 opportunities:
  1. [opportunity + one-line rationale]
  2. [opportunity + one-line rationale]
  3. [opportunity + one-line rationale]

Want a full report? Ask for STANDARD or DEEP analysis.
```

### STANDARD / DEEP — Save to COMPETITOR-REPORT.md

```markdown
# Competitive Intelligence Report: [Target Brand]
**URL:** [url] | **Date:** [date] | **Level:** Standard / Deep
**Competitors analyzed:** [count] | **Position:** Strong / Moderate / Weak

---
## Competitive Brief
[Confirmed intake from Step 0]

## Executive Summary
[3–4 paragraphs: landscape, target position, biggest advantage,
biggest threat, top 3 recommendations]

## Competitor Overview
[Summary table: name, URL, positioning, pricing tier, differentiator]

## Detailed Profiles
[One section per competitor: messaging, pricing, features, SWOT]

## Comparison Tables
[Feature matrix, pricing matrix, social presence, review ratings]

## Positioning Map
[Visual map + interpretation]

## Content & SEO Gap Analysis
[Gaps table + keyword opportunities]

## Strategic Recommendations
### Steal-Worthy Tactics        [5–8 tactics]
### Differentiation Strategy    [top 1–2 angles fully developed]
### Alternative Pages           [DEEP only]
### Switching Narratives        [DEEP only]

## Monitoring Plan              [STANDARD / DEEP]
[Checklist + response playbook]

## Next Steps
[Top 3 prioritized actions]
```

---

## Cross-Skill Integration

- If `BRAND-VOICE.md` exists → use competitor voice analysis to sharpen
  differentiation recommendations
- If `marketing-copywriting` has been run → use competitor messaging gaps to inform
  copy recommendations
- Output feeds into: `marketing-copywriting` (differentiated messaging),
  `marketing-brand-voice` (voice positioning relative to competitors)

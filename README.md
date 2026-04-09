# tukigrowth-skills

Claude Code skills for working with TukiGrowth and digital marketing planning.

## What are skills?

Skills are `SKILL.md` files that Claude Code loads automatically when the conversation context calls for them. Each skill gives Claude specific instructions on how to behave in a particular domain.

## Available skills

### `tukigrowth-api` — v1.0.0

Complete reference for the TukiGrowth REST API v1.

Triggers when the user asks how to consume the API, what endpoints exist, how to authenticate, what fields an endpoint accepts, how to integrate TukiGrowth with external systems, or requests curl examples.

Covers:
- Authentication via `X-API-Key`
- Response format and error codes
- Pagination
- Endpoints by module: Organizations, Clients, Business Context, Strategy, Content, E-commerce, Services, Ads, Email, PR & Speaking, CRM/Leads
- Required and optional fields for each operation (POST / PATCH)

---

### `funnel-strategy` — v1.0.0

Opinionated guidance for selecting and applying marketing funnel frameworks.

Triggers when the user asks which funnel to use, how models differ, how to structure growth, or how to map acquisition, conversion, retention, and revenue.

Covers:
- TOFU/MOFU/BOFU, extended lifecycle funnel, granular purchase funnel
- Flywheel, AARRR, e-commerce funnel, B2B pipeline
- Hybrid models
- Selection factors beyond business type (demand type, buying cycle, current bottleneck, etc.)
- Common anti-patterns

Responds in Spanish by default.

---

### `digital-marketing-strategy-tactics` — v1.0.0

Explains the difference between strategy, hypothesis, initiative, and tactic in digital marketing.

Triggers when the user asks about marketing planning, the difference between strategy and tactics, what a growth hypothesis is, or how to organize a digital marketing plan.

Covers:
- The 4 levels of marketing thinking and how they connect
- Structure of a testable hypothesis
- How to trace a tactic back to the strategy
- The most common mistake (confusing a tactic for a strategy)

---

### `marketing-copywriting` — v1.0.0

Validates existing copy or generates new copy from scratch for any marketing context — headlines, landing pages, ads, emails, CTAs, product descriptions, and more.

Triggers when the user wants to check if their copy works, improve it, or create it from zero.

Covers:
- Two modes: VALIDATE (score and rewrite) and GENERATE (from scratch)
- Copy brief with ICP, awareness stage, brand voice, objections
- 6-dimension scoring (Clarity, Persuasion, Specificity, Emotion, Action, Alignment)
- Headline generation using PAS, Before-After-Bridge, Specific Outcome, Fear Reversal, Identity-Based frameworks
- CTA generation with first-person voice and risk reduction
- Cross-skill integration with `marketing-brand-voice` and `marketing-competitors-analysis`

---

### `marketing-brand-voice` — v1.0.0

Analyzes, builds, or validates a brand voice from existing content or from scratch.

Triggers when the user wants to document their brand voice, define it from scratch, or check if specific copy is on-brand.

Covers:
- Three modes: ANALYZE (extract from URLs), BUILD (interview-based), VALIDATE (check copy against guide)
- ICP-anchored voice definition
- 4-dimension scoring (Formal/Casual, Serious/Playful, Technical/Simple, Reserved/Bold)
- Personality archetype identification
- Vocabulary fingerprint and tone-by-context mapping
- Generates a `BRAND-VOICE.md` deliverable
- Cross-skill integration with `marketing-copywriting` and `marketing-competitors-analysis`

---

### `marketing-competitors-analysis` — v1.0.0

Identifies competitors and produces actionable competitive intelligence at three depth levels.

Triggers when the user wants to understand the competitive landscape, find differentiation opportunities, or benchmark against competitors.

Covers:
- Three levels: QUICK (3 competitors, in-chat), STANDARD (5–7, report), DEEP (full intelligence)
- Competitor identification across direct, indirect, and aspirational tiers
- Messaging and positioning analysis
- Pricing and feature comparison
- Content and SEO gap analysis
- Review mining and switching narratives (DEEP)
- Differentiation strategy with positioning recommendations
- Generates `COMPETITOR-REPORT.md` (STANDARD/DEEP)
- Cross-skill integration with `marketing-copywriting` and `marketing-brand-voice`

---

## Skill dependencies

```
marketing-competitors-analysis
  ├── outputs COMPETITOR-REPORT.md → used by marketing-copywriting
  └── outputs COMPETITOR-REPORT.md → used by marketing-brand-voice

marketing-brand-voice
  ├── outputs BRAND-VOICE.md → used by marketing-copywriting
  └── reads COMPETITOR-REPORT.md → from marketing-competitors-analysis

marketing-copywriting
  ├── reads BRAND-VOICE.md → from marketing-brand-voice
  └── reads COMPETITOR-REPORT.md → from marketing-competitors-analysis
```

Standalone (no dependencies): `tukigrowth-api`, `funnel-strategy`, `digital-marketing-strategy-tactics`

---

## Repository structure

```
skills/
  tukigrowth-api/
    SKILL.md
  marketing-funnels/
    SKILL.md
  marketing-strategies/
    SKILL.md
  marketing-copywriting/
    SKILL.md
  marketing-brand-voice/
    SKILL.md
  marketing-competitors-analysis/
    SKILL.md
```

## Usage

To use these skills in Claude Code, add the skills directory to your `settings.json`:

```json
{
  "skillsDirectories": ["/path/to/tukigrowth-skills/skills"]
}
```

Or add this repository as a skills source in your project configuration.

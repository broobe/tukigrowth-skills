# tukigrowth-skills

Claude Code skills for working with TukiGrowth and digital marketing planning.

## What are skills?

Skills are `SKILL.md` files that Claude Code loads automatically when the conversation context calls for them. Each skill gives Claude specific instructions on how to behave in a particular domain.

## Available skills

### `tukigrowth-api`

Complete reference for the TukiGrowth REST API v1.

Triggers when the user asks how to consume the API, what endpoints exist, how to authenticate, what fields an endpoint accepts, how to integrate TukiGrowth with external systems, or requests curl examples.

Covers:
- Authentication via `X-API-Key`
- Response format and error codes
- Pagination
- Endpoints by module: Organizations, Clients, Business Context, Strategy, Content, E-commerce, Services, Ads, Email, PR & Speaking, CRM/Leads
- Required and optional fields for each operation (POST / PATCH)

---

### `funnel-strategy`

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

### `digital-marketing-strategy-tactics`

Explains the difference between strategy, hypothesis, initiative, and tactic in digital marketing.

Triggers when the user asks about marketing planning, the difference between strategy and tactics, what a growth hypothesis is, or how to organize a digital marketing plan.

Covers:
- The 4 levels of marketing thinking and how they connect
- Structure of a testable hypothesis
- How to trace a tactic back to the strategy
- The most common mistake (confusing a tactic for a strategy)

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
```

## Usage

To use these skills in Claude Code, add the skills directory to your `settings.json`:

```json
{
  "skillsDirectories": ["/path/to/tukigrowth-skills/skills"]
}
```

Or add this repository as a skills source in your project configuration.

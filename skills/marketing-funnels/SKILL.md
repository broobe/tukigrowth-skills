---
name: funnel-strategy
version: 1.0.0
description: >
  Select, compare, and apply marketing funnel frameworks — TOFU/MOFU/BOFU,
  AARRR, flywheel, e-commerce, B2B pipeline, and hybrid models. Triggers when
  the user asks "which funnel should I use", "how do funnels differ", "how to
  structure growth", "map acquisition and retention", or any request involving
  funnel selection, comparison, or stage mapping.
---

# Funnel Strategy

Provide clear, opinionated guidance on funnel frameworks. Focus on **selection, tradeoffs, application, and diagnosis**, not theory alone.

## Core behavior

- Default to **recommendation, not description**
- Assume the user wants to **choose or improve a model**
- Prefer **practical distinctions over textbook definitions**
- Recommend **hybrid models** when appropriate
- Tie every recommendation to:
  - business model
  - demand pattern
  - buying process
  - team structure
  - current growth constraint

## Separate these explicitly

Do not collapse these into synonyms:

- Marketing funnel → acquisition, awareness, consideration, messaging
- Sales funnel → qualification, pipeline progression, closing
- Product funnel → activation, usage, retention, monetization
- Lifecycle model → retention, loyalty, expansion, advocacy
- Growth model → system-level prioritization across teams

If the user mixes them, correct it directly.

---

## Supported frameworks

### TOFU / MOFU / BOFU
Use for:
- content strategy
- demand generation
- messaging by level of awareness and intent
- simple inbound planning

Strengths:
- intuitive
- useful for content mapping
- easy for non-specialists

Limitations:
- too abstract for detailed reporting
- weak for product analysis
- weak for retention-heavy businesses

### Extended funnel
Typical extension:
- TOFU
- MOFU
- BOFU
- Retention
- Loyalty
- Advocacy

Use for:
- lifecycle marketing
- subscription businesses
- repeat purchase businesses
- CRM and email automation strategy

Strengths:
- includes post-purchase economics
- better for LTV-oriented strategy

Limitations:
- still less precise than product or CRM models
- can become vague if stages are not operationalized

### Granular purchase funnel
Typical stages:
- Awareness
- Interest
- Consideration
- Intent
- Evaluation
- Purchase

Use for:
- diagnosing conversion drop-offs
- more precise stage-based messaging
- businesses with non-trivial purchase journeys

Strengths:
- more precise than TOFU/MOFU/BOFU
- useful for optimization and analysis

Limitations:
- may be overkill for small teams
- still focused mainly on acquisition-to-purchase

### Flywheel
Typical phases:
- Attract
- Engage
- Delight

Use for:
- customer-led growth
- referral-led growth
- retention and experience-driven businesses

Strengths:
- reframes growth as compounding customer value
- useful for aligning marketing, CX, and retention

Limitations:
- not a detailed KPI model by itself
- can become too conceptual without operational layers

### AARRR
Typical stages:
- Acquisition
- Activation
- Retention
- Revenue
- Referral

Use for:
- SaaS
- apps
- product-led growth
- startup growth systems

Strengths:
- includes activation and retention explicitly
- strong fit for product and growth teams

Limitations:
- does not map sales pipelines well
- may miss stakeholder complexity in enterprise sales

### E-commerce funnel
Typical stages:
- Discovery
- Product View
- Add to Cart
- Checkout
- Purchase
- Repeat Purchase

Use for:
- DTC
- retail ecommerce
- transactional conversion optimization

Strengths:
- highly operational
- behavior-based
- clear conversion metrics

Limitations:
- too narrow for complex consultative buying
- weaker as a content or education model

### B2B sales funnel
Typical stages:
- Lead
- MQL
- SQL
- Opportunity
- Closed Won

Use for:
- CRM pipeline management
- sales-led GTM
- long, multi-stakeholder deals
- revenue operations

Strengths:
- good for handoffs, pipeline visibility, forecasting
- clear ownership across marketing and sales

Limitations:
- weak for product usage
- weak for retention and lifecycle unless extended

### Hybrid model
Combine models when different teams need different views.

Common combinations:
- TOFU/MOFU/BOFU for content
- MQL/SQL/Opportunity for sales
- AARRR for product/growth
- retention/advocacy for lifecycle

Default to hybrid when the organization has multiple teams, multiple motions, or multiple bottlenecks.

---

## Funnel selection factors beyond business type

When the user asks which funnel to use, do not choose based only on company category. Evaluate these factors too.

### 1. Type of demand
Assess whether the business needs to create demand or capture existing demand.

- Low awareness / category education needed → prefer TOFU/MOFU/BOFU or granular educational funnel
- High existing intent / transactional demand → prefer ecommerce or conversion-oriented funnel

### 2. Complexity of the decision
Assess how much education, validation, and consensus the buyer needs.

- Low complexity / fast decision → prefer ecommerce or simpler conversion funnels
- High complexity / rational evaluation / multiple stakeholders → prefer granular funnel, B2B pipeline, or hybrid with content + sales

### 3. Length of the buying cycle
Assess how long it takes to move from awareness to purchase.

- Short cycle → prefer transactional or simplified funnel models
- Long cycle → prefer nurturing-oriented models with MOFU, qualification, or CRM stages

### 4. Role of the product
Assess whether growth depends on product usage or on human selling.

- Product-led or usage-led growth → prefer AARRR
- Sales-led or relationship-led growth → prefer B2B pipeline or hybrid

### 5. Importance of retention
Assess whether growth depends heavily on renewals, repeat purchase, expansion, or referrals.

- Retention is a key driver of economics → prefer extended funnel, AARRR, or flywheel
- Retention is secondary → acquisition/conversion funnel may be enough

### 6. Team structure
Assess who owns growth and whether there are specialized teams.

- Small generalist team → prefer simpler models
- Specialized teams across marketing, sales, product, CX → prefer hybrid model

### 7. Company maturity
Assess whether the organization needs speed or precision.

- Early stage → prefer a simpler funnel with fast learning loops
- Mature organization → prefer more specialized or layered frameworks

### 8. Quality of tracking and instrumentation
Assess what data the company can actually observe.

- Low instrumentation → prefer simpler, stage-based models
- Strong product analytics / CRM / lifecycle tracking → prefer AARRR, granular funnels, or hybrids

### 9. Main growth channel
Assess where growth comes from.

- Content / inbound → prefer TOFU/MOFU/BOFU
- Paid performance / CRO → prefer granular or ecommerce funnel
- Product usage / virality → prefer AARRR or flywheel
- Outbound sales → prefer B2B pipeline

### 10. Current objective
Assess what the company is trying to improve right now.

- More traffic / awareness → marketing funnel
- Better lead qualification → MOFU or B2B pipeline
- Better close rate → sales funnel
- Better activation → AARRR
- Better retention / LTV → extended funnel, flywheel, or AARRR

### 11. Bottleneck location
This is often the most important factor.

Choose the funnel based on where growth is breaking:
- acquisition bottleneck → marketing funnel
- conversion bottleneck → granular or ecommerce funnel
- qualification/sales bottleneck → B2B pipeline
- activation bottleneck → AARRR
- retention bottleneck → lifecycle, flywheel, or AARRR
- multiple bottlenecks → hybrid

---

## Decision logic

Apply these heuristics by default:

- Content / awareness problem → TOFU/MOFU/BOFU
- Education-heavy buyer journey → TOFU/MOFU/BOFU or granular purchase funnel
- Transactional conversion problem → ecommerce or granular funnel
- Product activation problem → AARRR
- Retention / expansion problem → extended funnel, AARRR, or flywheel
- Sales complexity problem → B2B pipeline
- Customer-led growth / referral emphasis → flywheel
- Multi-team org or mixed motion → hybrid

When two or more factors point to different answers, recommend a hybrid.

---

## Recommendation method

When answering, follow this sequence:

### 1. Infer context
If the user gives little context, infer the likely scenario:
- SaaS
- ecommerce
- B2B sales-led
- service business
- content-led business
- hybrid growth model

State assumptions briefly.

### 2. Identify the real decision variable
Do not anchor only on business type. Identify the most relevant factor:
- demand creation vs demand capture
- short vs long cycle
- activation vs closing vs retention
- team simplicity vs operational precision
- current bottleneck

### 3. Compare only relevant models
Do not list every framework. Usually compare 2 to 4 models maximum.

For each selected model, explain:
- what it solves
- where it fails
- what team benefits most

### 4. Recommend one model or hybrid
Always conclude with:
- best-fit funnel
- why it fits
- what not to use as the main framework
- what to layer on top if needed

### 5. Add implementation considerations
Include 2 to 4 practical considerations:
- metrics
- ownership
- instrumentation
- stage definitions
- common pitfalls

---

## Key distinctions to enforce

Always clarify these points when relevant:

- TOFU/MOFU/BOFU is a marketing abstraction, not a full operating system
- AARRR is a product/growth model, not a CRM pipeline
- Flywheel is a strategic framing, not a full measurement architecture
- B2B pipeline is a revenue tracking model, not a full customer journey
- Ecommerce funnels are behavioral and transactional, not conceptual awareness models
- Retention-heavy businesses should not stop at purchase
- One company can validly use several funnels at once

---

## Anti-patterns to flag

If detected, correct them explicitly:

- Using TOFU/MOFU/BOFU as the only funnel in SaaS with activation problems
- Ignoring retention in subscription or repeat-purchase businesses
- Mixing MQL/SQL stages with product usage stages without separating ownership
- Forcing one funnel across marketing, sales, product, and lifecycle teams
- Choosing the framework based on fashion instead of bottleneck
- Treating all customer journeys as linear
- Adding too many stages without operational definitions
- Using a granular funnel when the company lacks data to support it

---

## Output style

- Write in Spanish unless the user asks otherwise
- Be concise, structured, and practical
- Favor tradeoffs over generic advice
- Avoid filler and abstract marketing language
- Do not end with “depende” unless you resolve the dependency

Always end with a **clear recommendation**.

---

## Preferred answer format

Use this structure when the request is broad:

### Contexto asumido
State the likely business and the key deciding factors.

### Modelos relevantes
For each relevant model:
- qué resuelve
- cuándo conviene
- dónde falla

### Qué hace variar la elección
Mention the non-business-type factors that matter most in this case.

### Recomendación
State the best-fit funnel or hybrid and why.

### Riesgos o errores comunes
List the main mistakes to avoid.

---

## Example behaviors

If the user asks:
- "¿TOFU, MOFU y BOFU siguen vigentes?"
  Explain that they remain useful for content and messaging, but are often insufficient for product, retention, or sales operations.

- "¿Qué funnel conviene para un SaaS?"
  Compare AARRR versus TOFU/MOFU/BOFU and recommend based on whether the bottleneck is acquisition, activation, or retention.

- "¿Qué usamos en B2B enterprise?"
  Compare content funnel and CRM pipeline. Usually recommend a hybrid.

- "¿Qué conviene para ecommerce?"
  Prioritize ecommerce funnel and post-purchase retention layer.

- "Además del tipo de negocio, ¿qué hace variar la elección?"
  Focus on demand type, decision complexity, sales cycle, retention importance, team structure, tracking maturity, growth channel, objective, and bottleneck location.

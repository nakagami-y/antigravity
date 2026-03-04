---
name: brainstorm
description: Generates 5-7 unique content angles using 8 systematic ideation frameworks (SCAMPER, JTBD, Contrarian Angle, Time-Horizon Shifts, etc.). Each angle includes headline, source framework, target audience, and value proposition.
version: "1.0.0"
---

# Brainstorm — Systematic Ideation Skill

## Overview

Generates 5-7 differentiated content angles for a given topic using systematic design thinking frameworks. Each angle comes with a headline, which framework generated it, target audience segment, and a clear value proposition.

Works for: blog posts, newsletter editions, video topics, presentations, product ideas, or any creative exploration.

## Trigger

- `/brainstorm [topic]`
- "brainstorm angles for [topic]"
- "ideate on this topic"
- "find angles for [topic]"
- "切り口を考えて"

---

## Step 1: Classify the Input

| Input Type | Description | Frameworks to Prioritize |
|------------|-------------|--------------------------|
| **Specific topic** | "AI agents in customer support" | SCAMPER, Intersection, Stakeholder |
| **Trend** | "Everyone's talking about MCP servers" | Time-Horizon, Contrarian, First Principles |
| **Vague direction** | "Something about AI and productivity" | JTBD, Pain Mining, SCAMPER |

If the user doesn't specify, ask:

```
What are you starting with?

1. A specific topic (e.g., "AI agents in enterprise")
2. A trend you've noticed (e.g., "everyone's building MCP servers")
3. A vague direction (e.g., "something about AI costs")
```

---

## Step 2: Apply Frameworks (8 Total)

Run the topic through **at least 4 frameworks** (selected based on input type). Each framework must produce at least 1 distinct angle.

### Framework 1: SCAMPER

| Lens | Question |
|------|----------|
| **Substitute** | What if you replaced a core assumption? |
| **Combine** | What happens when you merge this with an adjacent domain? |
| **Adapt** | What model from another industry solves this? |
| **Modify** | What if you 10x or 1/10x a key variable? |
| **Put to another use** | Who else could benefit that nobody's talking about? |
| **Eliminate** | What if the thing everyone assumes is necessary... isn't? |
| **Reverse** | What if the opposite approach works better? |

### Framework 2: Jobs-to-be-Done (JTBD)

Structure: **"When [situation], I want to [action], so I can [outcome]."**

| Job Type | Example |
|----------|---------|
| **Functional** | "When my boss asks about AI, I want a clear framework so I can present a credible plan" |
| **Emotional** | "When I see everyone adopting AI, I want to know what works so I can feel confident" |
| **Social** | "When I'm with peers, I want a sharp take so I can contribute something original" |

### Framework 3: Contrarian Angle Generator

1. **List the consensus**: 3-5 things "everyone agrees" about this topic
2. **Challenge each one**: What evidence contradicts this? What hidden assumption does it rely on?
3. **Find the strongest reversal**: A contrarian take with real evidence (not shock value)

### Framework 4: Time-Horizon Shifts

| Horizon | Timeframe | Question |
|---------|-----------|----------|
| **H1: Now** | This week/month | What's the immediate tactical reality? |
| **H2: Transition** | 6-18 months | What's shifting? What's the messy middle? |
| **H3: Future state** | 2-5 years | What current assumptions will seem quaint? |

### Framework 5: Stakeholder Perspective Rotation

View the same topic through 4+ different roles (engineer, manager, customer, investor, etc.). Pick the most underrepresented perspective.

### Framework 6: Intersection Discovery

Combine the topic with an unexpected adjacent domain. Keep only intersections that produce genuine insight.

### Framework 7: First Principles Decomposition

1. Strip to fundamentals
2. Remove jargon — describe it to a smart 12-year-old
3. Rebuild from scratch with zero assumptions

### Framework 8: Audience Pain Mining

1. What frustrates them about this topic?
2. What have they tried that didn't work?
3. What question do they keep asking?

---

## Step 3: Compile & Filter

### Quality Filter

Before including an angle:

- [ ] **Distinct thesis**: Different from other angles?
- [ ] **Defensible**: Can be backed with evidence?
- [ ] **Not obvious**: Reader's reaction is "huh, interesting" not "yeah, I know"?
- [ ] **Actionable**: Reader walks away knowing something useful?
- [ ] **Clear audience**: Who specifically benefits?

If two angles are too similar, keep the stronger one and regenerate from a different framework.

---

## Step 4: Output Format

```markdown
# Brainstorm: [Topic]

**Input type**: Specific topic / Trend / Vague direction
**Frameworks applied**: [List]
**Date**: YYYY-MM-DD

---

## Angles

### Angle 1: [Headline]
- **Framework**: [Which framework]
- **Thesis (1 sentence)**: [Core argument]
- **Target audience**: [Who benefits most]
- **Value proposition**: [What the reader gains]
- **Key sections** (3-4 bullets):
  - ...
- **Hook**: [Opening line that pulls the reader in]

### Angle 2: [Headline]
...

(5-7 angles total)

---

## Recommendation

**Top pick**: Angle #[X] — "[Headline]"
**Why**: [2-3 sentences]

**Runner-up**: Angle #[X]
**Why**: [1-2 sentences]

---

## Differentiation Check

| Angle | Framework | Audience | Overlaps? |
|-------|-----------|----------|-----------|
| 1 | ... | ... | None |
| 2 | ... | ... | ... |
```

---

## Rules

1. **Minimum 5, maximum 7 angles**
2. **Each angle notes its source framework** — prevents clustering
3. **No two angles share the same core thesis**
4. **Every angle has a clear audience segment** — "everyone" is not an audience
5. **Headlines are specific and opinionated** — not "The State of X" but "Why X Will Kill Y Before It Kills Z"
6. **Prioritize angles with built-in tension** — the best pieces have a "wait, really?" moment

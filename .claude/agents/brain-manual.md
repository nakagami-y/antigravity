# Brain (Decision OS) — User Manual

> Your thinking OS — use it when you're stuck on a decision, need to validate a direction, or want someone to challenge your assumptions.

---

## In One Sentence

**A "copy of your best thinking" that you can consult anytime.**

- You (or team members) use it → Get a structured recommendation (Advisor Mode)
- You want to stress-test your thinking → Get your assumptions challenged (Sparring Mode)

---

## How to Invoke

In Claude Code, just describe what you need:

```
I need the Brain's advice: Should we write a blog post on this topic?
```

```
Brain sparring mode: Should we expand into YouTube Shorts?
```

Or use the Task tool directly with `subagent_type: "wado-brain"` (or whatever name you've given it).

---

## Two Modes

### Advisor Mode (Default)

**Who uses it**: Anyone who needs a decision clarified

**What you get back**:
1. Premise check (Is this connected to the actual goal?)
2. **One clear decision** (Yes / No / Conditional GO)
3. Reasoning (Which thinking principle was applied)
4. Trade-offs (What you gain, what you give up)
5. Next step (One specific action, doable today)
6. Confidence level (High / Medium / Low + reasoning)
7. Lateral expansion ideas

**Tip**: Provide as much context as possible. "What do you think?" is weak. "This topic, with these materials, targeting this audience" is strong.

### Sparring Mode

**Who uses it**: The project owner / decision maker

**What you get back**:
1. Premise challenge (Is the question itself correct?)
2. Attack on the weakest assumption
3. Unseen risks
4. Alternative frame (A different way to see the same problem)
5. If forced to decide (Recommendation despite challenges + alternative path)
6. Lateral expansion potential

**Tip**: Use when "I'm torn between two options", "Is this direction right?", or "Something feels off but I can't name it." Half-formed questions are fine — the Brain starts by examining the premise.

---

## 4 Consultation Domains

| Domain | When to Use | Example Questions |
|--------|-------------|-------------------|
| **Content** | What to write/create, which angle to take | "Should we write about this topic?" "Which hook is stronger?" |
| **Business & Product** | Product design, pricing, offers | "New product or improve existing?" "Is this price point right?" |
| **Team & Resources** | Time allocation, outsourcing, automation | "Should I outsource this?" "Which task should I automate first?" |
| **Strategy** | Direction, positioning, pivots | "Should we chase this trend?" "Is it time to pivot?" |

---

## Crafting Good Questions

### Provide Context (Most Important)

The Brain's accuracy scales directly with context quality. Include:

- **Target audience**: Which segment are you addressing?
- **Current numbers** (if available): Conversion rate, list size, revenue, retention, etc.
- **Options**: If deciding between A and B, describe both
- **Constraints**: Budget, time, resource limitations
- **Available material**: Do you have first-hand experience? Data? Customer testimonials?

### Question Templates (Copy and Customize)

**Content Decision**:
```
Brain advisor:
- Topic: [topic]
- Target: [audience segment]
- Material: [what you have — experience, data, testimonials, etc.]
- Medium: [blog / social / email / video]
- Stuck on: [specific dilemma]
```

**Business Decision**:
```
Brain advisor:
- Question: [what you're deciding]
- Current state: [numbers, situation]
- Options: A=[option A] / B=[option B]
- Constraints: [budget / time / resources]
```

**Strategy Sparring**:
```
Brain sparring:
- Current strategy: [what you're doing now]
- Doubt/concern: [what feels off]
- Context: [recent market changes, signals you've noticed]
```

---

## Reading the Output

### Confidence Levels

| Confidence | Meaning | Your Next Move |
|------------|---------|---------------|
| **High** | Information is sufficient, judgment is solid | Execute as-is |
| **Medium** | Direction is right but information gaps exist | Check "what additional info is needed" before executing |
| **Low** | Premises are uncertain or major info gaps | Gather information first. OK to defer the decision |

### "Next Step" Means Today

The Brain always closes with a concrete next step. This is not an abstract direction — it's **something you can do in the next 30 minutes**. When you get a recommendation, do this one thing first.

### Lateral Expansion = Your Idea Bank

Lateral expansion ideas always appear. You don't have to act on all of them. Bookmark the interesting ones — they become seeds for future content, products, or initiatives.

---

## What the Brain Does NOT Do

| Cannot Do | What to Do Instead |
|-----------|-------------------|
| Create content | Use a writer agent or content skills |
| Build websites/code | Use a developer agent or coding skills |
| Make legal/tax decisions | Consult a professional |
| Guarantee 100% correct answers | Use confidence level to calibrate your own judgment |
| Write to files | Take the Brain's output and act on it yourself or delegate |

---

## Common Usage Patterns

### Pattern 1: Morning Priority Setting

```
Brain advisor:
I have 3 things I could work on today.
A: Draft a blog post (topic: automation case study)
B: Create email sequence (webinar reminder)
C: Outline new product concept
Which should I do first?
```

### Pattern 2: Topic Go/No-Go

```
Brain advisor:
- Topic: "Why most productivity systems fail"
- Target: Small business owners
- Material: I have my own failed experiments + 3 client stories
- Medium: Newsletter + social posts
- Concern: Is this too negative? Will it attract the right audience?
```

### Pattern 3: Pricing Decision

```
Brain advisor:
Deciding on pricing for a new workshop.
- Content: 3-hour hands-on session
- Target: Established professionals ($100K+/year)
- Competitors: Similar events are $50-$300
- My existing product: $500/month membership
- Options: $200 / $400 / $700
```

### Pattern 4: Strategic Sparring

```
Brain sparring:
Currently focused on blog + newsletter, but considering YouTube Shorts.
- Current state: 3,000 newsletter subscribers, 5 posts/month
- Signal: Short-form video market is growing fast in my niche
- Worry: Will I spread too thin and do both poorly?
```

---

## File Structure

| File | Role |
|------|------|
| `.claude/agents/brain.md` | Agent definition (thinking tiers, decision frameworks, output protocol) |
| `.claude/agents/brain-knowledge.md` | Decision knowledge base (distilled judgment material) |
| `.claude/agents/brain-manual.md` | This file (user manual) |

---

## Troubleshooting

- **Recommendation is too abstract** → Add more context to your question and ask again
- **Confidence is always "Low"** → You likely need more data. Measure before asking
- **Not sure which mode to use** → Want an answer? Advisor. Want your thinking challenged? Sparring
- **Disagree with the recommendation** → That's fine. You make the final call. The Brain provides structured thinking material, not orders

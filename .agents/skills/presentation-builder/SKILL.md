---
name: presentation-builder
description: Transforms ideas, outlines, or documents into structured slide content with titles, bullets, visual placeholders, and speaker notes. Adapts structure to presentation type (pitch deck, business review, technical workshop, etc.).
version: "1.0.0"
---

# Presentation Builder Skill

## Overview

Transforms raw ideas, outlines, research, or documents into structured, presentation-ready slide content. Outputs clear slide titles, concise bullet points, visual direction, and optional speaker notes — ready to paste into Google Slides, Keynote, or any presentation tool.

## Trigger

- `/presentation-builder`
- "create slides for [topic/purpose]"
- "build a deck about [topic]"
- "make a presentation on [topic]"
- "プレゼン資料を作って"

---

## Step 1: Gather Context

Ask these targeted questions (skip any the user already answered):

```
1. **Purpose**: What is this presentation for?
   - Sponsor/investor pitch
   - Business review
   - Technical workshop / tutorial
   - Community talk / meetup
   - Research briefing
   - Other: ___

2. **Audience**: Who are you presenting to?

3. **Duration**: How long is your slot?
   - 5 min / 10 min / 15 min / 20 min / 30 min / 45+ min

4. **Key message**: If the audience remembers ONE thing, what should it be?

5. **Source material**: Do you have notes, an outline, or a previous deck?
```

---

## Step 2: Select Structure Template

Based on the presentation type, apply the appropriate structural flow:

### Pitch Deck (Sponsor / Investor)

| Slide # | Section | Purpose |
|---------|---------|---------|
| 1 | **Title + Hook** | One sentence that captures the opportunity |
| 2 | **Problem** | The pain point — make it visceral |
| 3 | **Solution** | What you do, in one clear statement |
| 4 | **How It Works** | 3-step visual explanation |
| 5 | **Traction / Proof** | Numbers, growth, social proof |
| 6 | **Market** | Size and opportunity |
| 7 | **Business Model** | How you make money |
| 8 | **Team** | Why this team wins |
| 9 | **The Ask** | What you want and what they get |
| 10 | **Contact / CTA** | Next step |

### Business Review

| Slide # | Section | Purpose |
|---------|---------|---------|
| 1 | **Title + Period** | What period this covers |
| 2 | **Executive Summary** | 3 key takeaways up front |
| 3 | **Key Metrics** | Dashboard view — numbers that matter |
| 4 | **What Worked** | Wins with evidence |
| 5 | **What Didn't** | Honest assessment with root causes |
| 6 | **Learnings** | What you now know |
| 7 | **Next Period Plan** | Priorities and targets |
| 8 | **Asks / Blockers** | What you need from the audience |

### Technical Workshop / Tutorial

| Slide # | Section | Purpose |
|---------|---------|---------|
| 1 | **Title + What You'll Learn** | Clear outcome promise |
| 2 | **Why This Matters** | Motivation and context |
| 3 | **Concepts** | Key mental models (2-3 max) |
| 4-N | **Step-by-Step** | One concept or action per slide |
| N+1 | **Demo / Live Example** | Show, don't tell |
| N+2 | **Common Mistakes** | What to watch out for |
| N+3 | **Resources + Next Steps** | Where to go from here |

### Community Talk / Meetup

| Slide # | Section | Purpose |
|---------|---------|---------|
| 1 | **Title + Hook** | Provocative question or bold claim |
| 2 | **Context / Story** | Set the scene |
| 3 | **The Insight** | The non-obvious thing you discovered |
| 4-6 | **Evidence / Examples** | 2-3 supporting points |
| 7 | **So What?** | Why this matters to the audience |
| 8 | **Takeaway + CTA** | One thing to do or think about |

### Research Briefing

| Slide # | Section | Purpose |
|---------|---------|---------|
| 1 | **Title + Research Question** | What you investigated |
| 2 | **Why It Matters** | Stakes and relevance |
| 3 | **Methodology** | How you approached it |
| 4-6 | **Key Findings** | 1 finding per slide, with evidence |
| 7 | **Implications** | What this means for the audience |
| 8 | **Open Questions** | What's still unknown |

---

## Step 3: Slide Count Guidelines

| Duration | Slide Count | Pacing |
|----------|-------------|--------|
| 5 min | 5-7 slides | ~45 sec/slide |
| 10 min | 8-12 slides | ~50-75 sec/slide |
| 15 min | 12-16 slides | ~55-75 sec/slide |
| 20 min | 15-20 slides | ~60-80 sec/slide |
| 30 min | 20-28 slides | ~65-90 sec/slide |
| 45 min | 25-35 slides | ~75-110 sec/slide |

**Hard rule**: If you have more than 5 bullets on a slide, you have 2 slides. Split them.

---

## Step 4: Write Each Slide

### Slide Content Format

```markdown
---

### Slide [#]: [Title — states the takeaway, not the topic]

**Bullets** (3-5 max):
- [Point 1 — one line, one idea]
- [Point 2]
- [Point 3]

**Visual direction**: [Chart type, image concept, diagram, or "text only"]

**Speaker notes**: [What you'd actually SAY — conversational, 2-4 sentences. Include transition.]

---
```

### Slide Title Rules

| Do | Don't |
|----|-------|
| "AI Agents Cut Support Costs 40%" | "AI Agents Overview" |
| "3 Steps to Production-Ready RAG" | "RAG Implementation" |
| "We Grew 3x in 6 Months" | "Growth Metrics" |

**The title should state the takeaway, not the topic.**

### Bullet Rules

- **One idea per bullet** — if it has a comma then a new thought, split it
- **Start with the insight, not the setup**
- **Parallel structure** — all bullets follow the same grammatical pattern
- **No sub-bullets** — if you need them, you need another slide
- **Maximum 5 bullets**

---

## Step 5: Output Format

```markdown
# Presentation: [Title]

**Purpose**: [Type]
**Audience**: [Who]
**Duration**: [X] minutes
**Slide count**: [N] slides
**Key message**: [One sentence]
**Date**: YYYY-MM-DD

---

## Slide-by-Slide Content

### Slide 1: [Title]
**Bullets**: ...
**Visual direction**: ...
**Speaker notes**: ...

---

(all slides)

---

## Presentation Summary

### Narrative Arc
[2-3 sentences describing the story from start to finish]

### Title-Only Readthrough
1. [Slide 1 title]
2. [Slide 2 title]
...

### Next Steps
- [ ] Add visuals in [tool of choice]
- [ ] Rehearse with timer
```

---

## Rules

1. **Slide titles state the takeaway, not the topic**
2. **Maximum 5 bullets per slide** — 6+ = split into 2 slides
3. **No walls of text** — tighten bullets to ~15 words max
4. **Every slide earns its place** — if removing it doesn't weaken the argument, remove it
5. **Visual direction is required** — even if it's "text only"
6. **Speaker notes are conversational** — write what you'd actually say
7. **Title-only readthrough must work** — titles alone tell the full story
8. **Match slide count to duration**
9. **End with a clear CTA**

---
name: first-principles-problem-solver
description: >
  First principles thinking: breaks problems into basic truths, strips assumptions, validates what’s actually true, and rebuilds solutions from scratch instead of copying best practices or analogies. Activates when user says “I’m stuck on [problem]”.
license: MIT
metadata:
  author: tejasashinde
  version: 1.0.0
  created: 2026-04-29
  last_reviewed: 2026-04-29
  review_interval_days: 90
---

# FIRST PRINCIPLES PROBLEM SOLVER

First principles thinking is basically the art of "breaking things down to the studs." Instead of looking at how everyone else is doing something (reasoning by analogy) and trying to improve it by 10%, you strip the problem of all assumptions until you’re left with only the undeniable truths—the basic physics or core facts of the situation.

Once you’ve identified those "atoms" of information, you start building a solution from the ground up. For example, if you're building a new product, you don't look at your competitors; you look at the raw materials and the fundamental human need, then ask, "Based on these facts alone, what is the best way to solve this?"

It’s mentally exhausting because you have to constantly ask "Why?" and challenge things that everyone else takes for granted. But by refusing to follow a "best practice" just because it’s the status quo, you open the door to true innovation and solutions that others completely miss.

## When to USE THIS SKILL

User invokes `/first-principles` followed by their stuck problem:

```
/first-principles I'm stuck on how to reduce server latency
/first-principles I can't figure out how to price this product
/first-principles My team is stuck on this architecture decision
/first-principles I'm stuck on [your actual problem here]
```

## METHODOLOGY

Follow this sequence strictly. Do not skip steps.

### 1. EXTRACT ALL ASSUMPTIONS
First list **every single unstated assumption** the user is making. These are things they are taking as given without questioning.
- List 7-12 assumptions minimum
- Separate explicit vs implicit assumptions
- Mark which are most likely to be wrong

### 2. VALIDATE EACH ASSUMPTION
For **every single assumption** ask these three questions:
- Is this actually true?
- How do we know this is true?
- What would happen if this was false?

Mark each assumption as:
- 🔴 Definitely false
- 🟡 Probably false / unproven
- 🟢 Actually true

### 3. DISMANTLE THE PROBLEM
Remove all false and unproven assumptions. Restate the problem from scratch using only what you actually know to be true.
- No analogies
- No best practices
- No "everyone does it this way"
- Only fundamental truths

### 4. REBUILD FROM SCRATCH
Start over from the fundamental truths. Build up possible solutions without carrying over any prior assumptions.
- Generate at least 3 completely different solution approaches
- Rank them by feasibility and impact
- Identify which solution was previously invisible because of bad assumptions

### 5. REVEAL THE HIDDEN SOLUTION
Explain:
- Exactly which assumption was blocking progress
- Why everyone (including the user) accepted this assumption
- What the actual solution is now that the assumption is removed
- First concrete action step to take today

## EXAMPLES
Read [references/examples.md](./examples.md) for detailed examples

## Rules
❌ Never reason by analogy
❌ Never improve existing things by 10%
❌ Never look at what competitors are doing
❌ Never use "best practices" as justification
✅ Always break things down to fundamental atoms
✅ Always build solutions from scratch
✅ Always challenge every taken for granted truth
✅ Always calculate what should be possible, not what currently is.

## Output Format
Present results in this exact structure:
```
## 🧠 Assumptions Identified
[list all assumptions with validation status]

## 🔴 False Assumptions Found
[the assumptions that are not actually true]

## ✅ Fundamental Truths Remaining
[only what we know for certain]

## 🔄 Restated Problem (without assumptions)
[clean problem statement]

## 💡 Solutions From First Principles
[3+ solution approaches]

## ⚡ Hidden Solution Revealed
[the actual answer that was being blocked]

## 🚀 First Action
[single concrete step to take right now]
---
name: identify-common-mistakes
description: >
  Identify the most common, high-impact mistakes in any new project (business, technical, analytical, etc.) and provide clear, actionable steps to prevent them before they become costly or difficult to recover from. Use when users ask about common mistakes or what to avoid.
metadata:
  author: tejasashinde
  version: 1.0.0
  created: 2026-04-30
  last_reviewed: 2026-04-30
  review_interval_days: 90
---

# IDENTIFY COMMON MISTAKES

## Contents

- [PURPOSE](#purpose)
- [WHEN TO USE THIS SKILL](#when-to-use-this-skill)
- [INPUT VALIDATION](#input-validation)
- [DOMAIN ADAPTATION](#domain-adaptation)
- [IMPORTANT CORE PRINCIPLES](#important-core-principles)
- [METHODOLOGY](#methodology)
- [SELECTION RULES](#selection-rules)
- [OUTPUT FORMAT](#output-format)
- [FOLLOW-UP SUPPORT](#follow-up-support)

## PURPOSE

Identify and surface the most common high-impact mistakes before the user starts. You are an expert failure analyst. Your job is to prevent predictable, high-cost mistakes that people repeatedly make when starting something new.


## WHEN TO USE THIS SKILL

User invokes `/identify-common-mistakes` followed by their project:
```
/identify-common-mistakes I'm about to start building a SaaS product
/identify-common-mistakes I'm about to start learning machine learning
/identify-common-mistakes I'm about to start a YouTube channel
/identify-common-mistakes I'm about to launch my startup
```
OR Natural Language trigger like:
```
I'm about to start [project]. What mistakes should I avoid?
What are the most common mistakes people make when doing this?
What do people always get wrong when they start [thing]?
```

## INPUT VALIDATION

If the project is vague or underspecified:
Either:
  - Ask 1–2 clarifying questions BEFORE generating output, OR
  - If proceeding without clarification, explicitly state assumptions first
  - If assumptions are made, briefly state them before the main output

## DOMAIN ADAPTATION

First classify the project into one of:
- Business / Startup
- Technical Product
- Skill Learning
- Content Creation
- Analytical / Research

Then tailor mistake types accordingly.

---

## IMPORTANT CORE PRINCIPLES

- Be realistic, not optimistic
- Be direct and honest, but not abrasive
- Avoid generic phrasing; all advice must be contextualized to the specific project
- Only include mistakes widely observed in real-world practice
- If uncertain, prefer fewer mistakes over speculative ones
- Prioritize clarity over harshness
- Focus on mistakes that are costly or difficult to recover from
- All recommendations must be actionable before significant time, money, or public commitment

---

## METHODOLOGY

Return 4–6 high-impact mistakes (default: 5).  
If fewer high-confidence mistakes exist, return fewer rather than adding weak or speculative ones

For EACH mistake provide:
1. **The mistake** — one clear sentence
2. **What happens** — concise explanation
3. **Why everyone does this** — cognitive bias or behavioral reason
4. **Point where recovery becomes difficult** — when fixing becomes disproportionately costly or unlikely
5. **How to avoid it BEFORE you commit** — 3 concrete actions
6. **Early warning sign** — what appears in early stage (2–6 weeks depending on project)
7. **Impact** — High / Very High / Existential
8. **Likelihood** — estimated % range

### SELECTION RULES:
- Prioritize mistakes that are commonly observed in this specific project type
- Focus on high-impact, hard-to-recover mistakes
- Avoid generic advice unless clearly contextualized
- Ensure each mistake is distinct and non-overlapping
- Order by impact (most destructive first)
- Each mistake must represent a distinct failure mode; overlapping or reworded mistakes are not allowed

---

## OUTPUT FORMAT

```
## Before you start [PROJECT]: The Mistakes You Cannot Afford To Make

---

### ❌ Mistake 1: [Mistake title]

**What happens**: [explanation]
**Why everyone does this**: [reason]
**Point where recovery becomes difficult**: [moment]
✅ **Do this BEFORE you commit**:
- [action 1]
- [action 2]
- [action 3]

⚠️ **Early warning sign (first 2–6 weeks)**: [signal]
🔥 **Impact**: [level]
📊 **Likelihood**: [e.g., 60–80%], not a single value

---

### ❌ Mistake 2: [Mistake title]

---

### ❌ Mistake 3: [Mistake title]

---

### ❌ Mistake 4: [Mistake title]

---

### ❌ Mistake 5: [Mistake title] (required unless fewer than 5 high-confidence mistakes exist)

---

## ✅ Final Check Before You Start

If you have done these 3 things, you are already ahead of most people:
1.
2.
3.

Good luck.
```

---

## FOLLOW-UP SUPPORT

Be ready to:
- Expand any mistake
- Provide real-world examples
- Adapt advice to user constraints
- Refine based on additional user context

---

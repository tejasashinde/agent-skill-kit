---
name: five-minute-summary
description: >
  Summarizes any topic into the most important points for quick understanding in under five minutes, using plain language and ending with one actionable takeaway. Use when user wants a five-minute-summary of certain topic.
---

# FIVE MINUTE SUMMARY

## Contents

- [Purpose](#purpose)
- [When to Use This Skill](#when-to-use-this-skill)
- [When Not to Use This Skill](#when-not-to-use-this-skill)
- [Instructions](#instructions)
- [Output Format](#output-format)
- [Style Guidelines](#style-guidelines)
- [Examples](#examples)
- [Notes](#notes)

---

## PURPOSE

Creates a short, clear summary of any topic so a reader can understand the essentials in under five minutes.
This skill is useful when:
- The input is long, complex, or detailed
- The user wants a quick understanding, not deep analysis
- Time is very limited

---

## WHEN TO USE THIS SKILL

Use this skill when:

- The input is long, dense, or hard to quickly understand
- The user asks for a summary, TL;DR, or quick explanation
- The goal is speed over depth
- The output must be easy to scan and beginner-friendly

## WHEN NOT TO USE THIS SKILL:

- The user explicitly asks for deep analysis or detailed breakdown
- The task requires step-by-step reasoning or problem solving
- The content must be fully preserved (e.g., legal or exact text)

## INSTRUCTIONS

Follow these steps:

1. **Understand the input**
   - Identify the main topic.
   - Detect the key ideas, facts, or arguments.

2. **Filter ruthlessly**
   - Keep only the most important 3–6 points.
   - Remove examples, fluff, repetition, and minor details.

3. **Rewrite simply**
   - Use plain language (no jargon, no technical terms unless necessary).
   - Prefer short sentences.
   - Explain ideas as if to a beginner.

4. **Structure the output**
   - Start with a **one-line overview** of the topic.
   - Then list key points as short bullets or brief paragraphs.

5. **Add one actionable takeaway**
   - End with exactly ONE clear action the reader can take.
   - Make it practical and specific.

---

## OUTPUT FORMAT

```
[One-line overview sentence (max 20 words, plain language, no jargon unless explicitly required)]
• Key point 1
• Key point 2
• Key point 3
(Up to 10-15 points max)

Actionable takeaway: [Exactly one specific, practical action the reader can take immediately from it]
```

---

## STYLE GUIDELINES

- Use everyday words (e.g., “use” instead of “utilize”)
- Avoid jargon unless absolutely necessary (and explain it if used)
- Be concise but complete
- Do not exceed what can be read in ~5 minutes (~150–300 words)
- Do not include multiple takeaways

---

## EXAMPLES

### Example 1

**Input:**
“Blockchain is a decentralized digital ledger that records transactions across many computers. It ensures that records cannot be altered retroactively without altering all subsequent blocks. It is used in cryptocurrencies like Bitcoin, but also in supply chain management, healthcare, and finance for transparency and security.”

**Output:**

```
Blockchain is a system for securely recording information across many computers.

• It stores data in blocks that are linked together in a chain  
• Once data is added, it is very hard to change  
• It does not rely on a central authority  
• It is best known for powering cryptocurrencies like Bitcoin  
• It is also used in industries like supply chains and healthcare for transparency  

Actionable takeaway: Learn one real-world use of blockchain in your field to understand its practical value.
```

---

### Example 2

**Input:**
“Time management is the process of planning and controlling how much time to spend on specific activities. Good time management enables an individual to work smarter, not harder, so that they get more done in less time. It involves setting priorities, eliminating distractions, and organizing tasks effectively.”

**Output:**

```
Time management is about using your time wisely to get more done with less stress.

• It involves planning how you spend your time  
• Helps you focus on important tasks first  
• Reduces stress by avoiding last-minute rush  
• Requires cutting down distractions  
• Makes you more productive without working longer hours  

Actionable takeaway: Start each day by listing your top 3 priorities and focus on completing them first.
```

---

### Example 3

**Input:**
“Artificial intelligence (AI) refers to the simulation of human intelligence in machines that are programmed to think and learn. AI systems can perform tasks such as speech recognition, decision-making, and language translation. Machine learning is a subset of AI that enables systems to learn from data and improve over time without being explicitly programmed.”

**Output:**

```
Artificial intelligence is technology that allows machines to think and learn like humans.

• AI can perform tasks like understanding speech and making decisions  
• It is used in tools like voice assistants and translation apps  
• Machine learning is a part of AI that learns from data  
• AI systems improve over time as they process more information  
• It helps automate tasks and solve complex problems  

Actionable takeaway: Try using one AI-powered tool (like a voice assistant or writing helper) to see how it improves your daily tasks.
```

---

## Notes

- If the input is already short, still simplify and refine it.
- If the topic is complex, prioritize clarity over completeness.
- Always include the actionable takeaway — this is mandatory.

---
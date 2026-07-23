---
name: checklist-builder
description: Turns any task, goal, project, workflow, routine, plan, process, or messy notes into a clear, ordered checklist with categories, dependencies, prerequisites, and completion-friendly steps. Use this skill whenever the user asks for a checklist, or says “turn this into steps,” even if they do not explicitly use the word checklist.
---

# Checklist Builder

Convert a user’s goal, task, process, workflow, project idea, or rough notes into a clear, ordered checklist that can be executed. Return the checklist itself, not a brainstorm or explanation, unless the user asks for reasoning. Always produce a usable checklist after careful thinking.

## Contents

- [When to USE this Skill](#when-to-use-this-skill)
- [Goal](#goal)
- [Build Process (Thinking)](#build-process-thinking)
- [Default Output Contract](#default-output-contract)
- [Checklist Modes](#checklist-modes)
  - [Simple Mode](#simple-mode)
  - [Detailed Mode](#detailed-mode)
  - [Dependency-first Mode](#dependency-first-mode)
  - [QA / Review Mode](#qa--review-mode)
- [Step-writing Rules](#step-writing-rules)
- [Ordering Rules](#ordering-rules)
- [Assumptions and Placeholders](#assumptions-and-placeholders)
- [Clarification Rules](#clarification-rules)
- [Edge Cases](#edge-cases)
  - [Vague Requests](#vague-requests)
  - [Messy Notes](#messy-notes)
  - [Multiple Goals](#multiple-goals)
  - [Simple Requests](#simple-requests)
  - [Detailed Requests](#detailed-requests)
  - [SOP or Workflow Requests](#sop-or-workflow-requests)
  - [QA, Review, or Audit Requests](#qa-review-or-audit-requests)
  - [Alternative Output Formats](#alternative-output-formats)
  - [Missing Files or Documents](#missing-files-or-documents)
  - [High-risk Domains](#high-risk-domains)
  - [Unsafe or Harmful Requests](#unsafe-or-harmful-requests)
- [Strict Output Rules](#strict-output-rules)
- [Final Quality Check](#final-quality-check)

## When to USE this Skill

Use this skill when the user asks for any of the following:

- checklist
- to-do list
- task breakdown
- step-by-step plan
- “turn this into steps”
- “break this down”

Also use it when the user gives messy notes and clearly wants ordered execution help.

## Goal

Produce a checklist that is:

- Ordered by dependency and execution flow
- Grouped into useful sections
- Written as Markdown checkboxes
- Actionable, specific, and completion-friendly
- As short as possible while still useful
- Detailed only when the task is complex, risky, technical, or multi-stage

## Default output contract

Use this structure unless the user requests another format:

```markdown
# Checklist: [Clear Goal]

## [Section]
- [ ] [Actionable step]

## Final Checks
- [ ] [Verification step]
````

Return only the checklist.

Do not include any commentary unless user explicitly asked for clarity.

## Build process (Thinking)

Before writing, always determine:

1. What outcome the user wants.
2. Whether the task is simple, detailed, dependency-heavy, or review/QA focused.
3. What must happen first.
4. What can happen in parallel.
5. What must be verified before completion.
6. Whether assumptions or placeholders are needed.

Then produce the checklist.

## Checklist modes

### Simple mode

Use for personal, daily, small, low-risk, or clearly simple tasks.

Rules:

* 5–15 items
* Short sections
* No sub-bullets unless necessary
* No “Why” or “Done when” lines unless they are asked

Template:

```markdown
# Checklist: [Goal]

## Prepare
- [ ] [Step]
- [ ] [Step]

## Do
- [ ] [Step]
- [ ] [Step]

## Finish
- [ ] [Step]
```

### Detailed mode

Use for projects, launches, development work, research, business workflows, planning, or multi-stage tasks.

Rules:
* Use phases
* Include dependencies when important
* Add completion criteria only where useful
* Add owners, dates, or placeholders only when they improve execution

Template:

```markdown
# Checklist: [Goal]

## 1. Scope
- [ ] [Define or confirm the goal]
  - Done when: [Clear completion condition]

## 2. Inputs
- [ ] [Collect required input]
  - Depends on: [Dependency, if any]

## 3. Execution
- [ ] [Action step]

## 4. Review
- [ ] [Validation step]

## 5. Handoff
- [ ] [Final delivery step]
```

### Dependency-first mode

Use when prerequisites, approvals, assets, permissions, blockers, or ordering constraints matter.

Template:

```markdown
# Checklist: [Goal]

## Prerequisites
- [ ] [Required item]
- [ ] [Required access, file, approval, or decision]

## Dependencies
- [ ] [A must be completed before B]
- [ ] [Approval or input needed before next phase]

## Execution
- [ ] [Ordered step]
- [ ] [Ordered step]

## Final Checks
- [ ] [Verify result]
- [ ] [Confirm handoff or completion]
```

### QA / review mode

Use when the user wants to verify quality, correctness, readiness, compliance, launch status, or bugs.

Template:

```markdown
# QA Checklist: [Thing Being Reviewed]

## Functionality
- [ ] [Check behavior]

## Content / Data
- [ ] [Check accuracy or completeness]

## UX / Accessibility
- [ ] [Check usability, readability, or access]

## Edge Cases
- [ ] [Check failure or unusual case]

## Final Approval
- [ ] [Confirm release/readiness condition]
```

## Step-writing rules

Every checklist item must:

* Start with a verb when possible
* Describe one clear action
* Be small enough to complete
* Avoid vague thinking words
* Include the object of the action
* Be testable or visibly complete

Prefer:

```markdown
- [ ] Collect staging server credentials from the project owner.
```

Avoid:

```markdown
- [ ] Think about setup.
```

Prefer:

```markdown
- [ ] Test the signup flow with a new user account.
```

Avoid:

```markdown
- [ ] Check everything works.
```

## Ordering rules

Order steps in this sequence unless the user’s process requires otherwise:

1. Goal / scope
2. Inputs / resources
3. Prerequisites / permissions
4. Setup
5. Core execution
6. Testing / review
7. Fixes
8. Final delivery / publishing / handoff
9. Follow-up / monitoring / maintenance

Put dependent steps after their blockers.

If a dependency is important but cannot be resolved inside the checklist, mark it:

```markdown
- [ ] Confirm API access with the admin before starting integration.
```

## Assumptions and placeholders

If the request is broad but workable, include a short assumptions section before the checklist.

Use assumptions sparingly.

```markdown
## Assumptions
- This checklist is for a one-time project, not a recurring process.
- The user wants a practical execution checklist, not a strategy document.
```

Use placeholders for minor missing details:

```markdown
- [ ] Confirm the deadline: [DATE]
- [ ] Assign the owner: [NAME]
- [ ] Add the final link or file path: [LINK]
```

Ask one clarifying question only if the checklist would be misleading without the answer. Ask only when missing information changes the whole structure, such as:

* Target audience
* Output format
* Platform/tool
* Deadline/risk level
* Missing source material
* Whether the checklist is for execution, review, or delegation

If the user wants speed or says not to ask questions, make reasonable assumptions and continue.

## Edge cases

### User gives only a vague request

If the user says only “make a checklist” without a task, always ask:

```text
What task or goal should the checklist cover?
```

### User provides messy notes

Preserve all important items, remove duplicates, infer order, and group related work.

### User gives multiple goals

Create one checklist with sections per goal unless the goals are unrelated. If unrelated, create separate checklists.

### User asks for “simple”

Use Simple mode. Do not add dependencies, completion criteria, or explanations unless essential.

### User asks for “detailed”

Use Detailed mode. Include phases, dependencies, final checks, and completion criteria.

### User asks for “SOP” or “workflow”

Include:

* Start condition
* Inputs
* Steps
* Decision points
* Output
* Completion condition

### User asks for “QA,” “review,” or “audit”

Use QA / review mode. Focus on verification, edge cases, and release readiness.

### User asks for CSV, JSON, table, or document format

Follow the requested format. Keep checklist logic intact.

### User asks for a checklist from a missing file, link, image, or document

Use available content if provided. If the source is unavailable and necessary, ask for it. Do not invent source-specific steps.

### High-risk domains

For medical, legal, financial, safety, security, compliance, hiring, or production deployment checklists:

* Include review/approval steps
* Avoid presenting the checklist as professional advice
* Add verification, documentation, and escalation steps
* Always include “consult qualified professional” or “obtain approval” only when appropriate

### Unsafe or harmful requests

Do not create checklists that enable wrongdoing, evasion, abuse, self-harm, weapons misuse, credential theft, fraud, or dangerous instructions. Provide a safer checklist when possible.

## Strict output rules

* Use Markdown checkboxes: `- [ ]`
* Use clear headings
* Keep wording concise and avoid over-explaination
* Do not include meta-commentary or internal build process
* Do not add examples in the final output unless the user asks

## Final quality check

Before responding, verify:

- Prerequisites come first with clear goal title
- Steps are specific and actionable
- Dependencies are shown when needed
- No unnecessary detail
- Detail level matches the user request

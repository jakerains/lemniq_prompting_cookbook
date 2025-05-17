# 2. Prompt Fundamentals

## Table of Contents
- [2.1 The lemnIQ Formula](#21-the-lemniq-formula)
- [2.2 When to Ask Follow-Up Questions](#22-when-to-ask-follow-up-questions)
- [2.3 Temperature & Top-p Crash Course](#23-temperature--top-p-crash-course)
- [2.4 Prompt Iteration Cycle](#24-prompt-iteration-cycle)

## 2.1 The lemnIQ Formula
```
ROLE + TASK + CONTEXT + STYLE + CONSTRAINTS (+ EXAMPLES)
```
![Diagram of the lemnIQ formula with Role, Task, Context, Style, Constraints, and optional Examples flowing into a final prompt box](lemniq-formula.svg)

* **ROLE:** “You are an empathetic copywriter …”
* **TASK:** “… draft a 2‑paragraph intro …”
* **CONTEXT:** “… for our monthly SaaS newsletter about churn …”
* **STYLE:** “… witty, no buzzwords …”
* **CONSTRAINTS:** “… ≤120 words, include ✨ emoji.”
* **EXAMPLES (optional):** Paste a paragraph you love and say “Match this tone.”

## 2.2 When to Ask Follow‑Up Questions
If ChatGPT might need info you haven’t provided (e.g., audience pain points), tell it to ask first:
> “Before answering, ask me any clarifying questions you need.”

## 2.3 Temperature & Top‑p Crash Course
* **Temperature 0.2 – 0.4:** Factual, deterministic.
* **Temperature 0.6 – 0.8:** Creative brainstorming.

*Tip:* Set **max_tokens** and **stop** if you need disciplined length.

### Temperature Examples
**Prompt (0.2):**
```
Summarize the core benefit of CRM software in one sentence.
```
**Output (GPT-4o, <120 words):**
CRM software centralizes customer data so teams can track and manage relationships efficiently.

**Prompt (0.8):**
```
Describe the future of CRM tools in a playful tone.
```
**Output (GPT-4o, <120 words):**
Imagine a dashboard that practically winks at you while juggling chatbots, predictive analytics, and friendly nudges so no lead slips away.

## 2.4 Prompt Iteration Cycle
The prompt iteration cycle turns a rough idea into a refined prompt through a simple four-step loop:
1. **Plan** – Decide the role, task, context, and constraints.
2. **Write** – Draft your prompt using the lemnIQ formula.
3. **Critique** – Examine the response for gaps or tone issues.
4. **Revise** – Adjust the prompt or add clarifications, then test again.

Repeat until the response matches your needs; two or three passes usually do the trick.

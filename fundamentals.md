# 2. Prompt Fundamentals

## 2.1 The lemnIQ Formula
```
ROLE + TASK + CONTEXT + STYLE + CONSTRAINTS (+ EXAMPLES)
```

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

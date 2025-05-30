# 5. Troubleshooting Guide

| Symptom          | Likely Cause             | Fix                                          |
| ---------------- | ------------------------ | -------------------------------------------- |
| Hallucination    | Missing context          | Add authoritative source or say “Cite URLs.” |
| Too verbose      | Temp high / vague prompt | Add word limit / lower temperature.          |
| Stops mid‑answer | Max tokens hit           | Ask “continue” or raise limit.               |
| Rate limits | API quota exceeded       | Retry after waiting; monitor usage.        |
| Policy refusal | Content violates policy  | Rephrase request within guidelines.        |
| Formatting loss | Markdown stripped        | Enclose sections in triple backticks.      |
| Instructions not followed | Prompt unclear or conflicting | Break complex requests into numbered steps and restate key points. |

## When to Escalate to Human
- Response seems legally or ethically risky
- Multiple attempts still yield nonsense
- You require domain expertise the model lacks

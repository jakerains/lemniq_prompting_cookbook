# 5. Troubleshooting Guide

| Symptom          | Likely Cause             | Fix                                          |
| ---------------- | ------------------------ | -------------------------------------------- |
| Hallucination    | Missing context          | Add authoritative source or say “Cite URLs.” |
| Too verbose      | Temp high / vague prompt | Add word limit / lower temperature.          |
| Stops mid‑answer | Max tokens hit           | Ask “continue” or raise limit.               |
| Rate limit errors | API quota exceeded       | Retry after waiting; monitor usage.        |
| Policy refusal   | Content violates policy  | Rephrase request within guidelines.        |
| Formatting lost  | Markdown stripped        | Enclose sections in triple backticks.      |

## When to Escalate to a Human
- Response seems legally or ethically risky
- Multiple attempts still yield nonsense
- You require domain expertise the model lacks

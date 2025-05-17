# 4. Advanced Techniques

1. **Role Stacking** – Give ChatGPT multiple hats:
   > “You are a product manager and a sarcastic pirate. Alternate voices.”

2. **Tool Calling (Actions)** – If using Assistants API, define:
```json
{
  "name": "search_web",
  "description": "Searches Google",
  "parameters": { "type": "object", "properties": { "query": {"type":"string"} } }
}
```

3. **Chain‑of‑Thought on Demand** – Ask:
   > “Show step‑by‑step reasoning *inside triple backticks* before final answer.”

4. **System‑Prompt Guards** – For client‑facing bots:
```text
You are a polite AI. If user request violates policy X, refuse with apology.
```

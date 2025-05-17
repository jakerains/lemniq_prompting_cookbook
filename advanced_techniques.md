# 4. Advanced Techniques

## Table of Contents
- [1. Role Stacking](#1-role-stacking)
- [2. Tool Calling (Actions)](#2-tool-calling-actions)
- [3. Chain-of-Thought on Demand](#3-chain-of-thought-on-demand)
- [4. System-Prompt Guards](#4-system-prompt-guards)
- [4.5 Multi-Agent Prompt Orchestration](#45-multi-agent-prompt-orchestration)

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

## 4.5 Multi-Agent Prompt Orchestration
```json
{
  "agents": [
    {"role": "Researcher", "goal": "Gather facts"},
    {"role": "Writer", "goal": "Draft post"}
  ],
  "handoff": "Researcher summarizes findings, Writer produces final text"
}
```
Example system prompt:
> "Agent 1 delivers a bullet list to Agent 2. Agent 2 writes a concise summary for our newsletter."

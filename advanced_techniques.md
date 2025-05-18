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
Outline how each agent contributes and when they pass control.

```json
{
  "agents": [
    {"id": "agent_1", "role": "Researcher", "goal": "Gather facts"},
    {"id": "agent_2", "role": "Writer", "goal": "Draft post"}
  ],
  "handoff": "agent_1->agent_2",
  "task_flow": "Researcher summarizes findings for Writer, who crafts final text"
}
```

Example workflow:
1. **Agent 1 – Researcher**  
   Prompt: "Find three recent studies on remote work productivity."
2. **Agent 2 – Writer**  
   Prompt: "Use Agent 1's bullet points to write a short blog summary."

Need troubleshooting tips? See the [Guide](troubleshooting.md).
Not sure about certain terms? Consult the [Glossary](glossary.md).

---
title: System-Prompt Guards
description: Implement safety measures and boundaries in your ChatGPT prompts
order: 4
---

# System-Prompt Guards

System-prompt guards are safety mechanisms built into your prompts that establish clear boundaries, ethical guidelines, and fallback behaviors for ChatGPT. These guards are especially important when developing client-facing applications or handling sensitive domains.

## How It Works

System-prompt guards define rules of engagement and acceptable behaviors directly in the system prompt. They explicitly instruct the AI on how to handle problematic requests, sensitive topics, or situations where it lacks sufficient knowledge.

### Basic Pattern

```prompt
You are a [role description]. If asked about [sensitive topic/prohibited request], politely decline and explain that [reason].
```

### Advanced Pattern

```prompt
You are a [role description]. Follow these guardrails:
1. If asked about [topic A], respond only with factual information from [trusted sources].
2. If asked to [prohibited action], politely decline and suggest [alternative].
3. If uncertain about an answer, acknowledge limitations rather than speculating.
4. Never [specific prohibited behavior] under any circumstances.
```

## Example: Customer Service Assistant

```prompt
You are a helpful customer service assistant for TechCorp.

GUARDRAILS:
- Never ask for or accept customer passwords, payment details, or personal identification numbers
- If asked about competitors' products, only provide factual comparisons without negative commentary
- Do not make promises about future product features unless they've been officially announced
- If asked about technical issues beyond basic troubleshooting, kindly direct customers to the dedicated technical support team
- Always maintain a professional, kind tone even when dealing with frustrated customers
```

## Example: Educational Assistant

```prompt
You are an educational assistant for high school students.

GUARDRAILS:
- Help students understand concepts but don't simply solve homework problems for them
- If asked to write essays or complete assignments, decline and instead offer to guide the thought process
- Ensure all explanations are age-appropriate and factually accurate
- If asked about sensitive topics (drugs, explicit content, etc.), provide only educational information appropriate for the high school level
- Encourage critical thinking rather than memorization of facts
```

## When to Use System-Prompt Guards

- For any public-facing or customer-oriented AI application
- When handling domains with regulatory compliance requirements
- For educational or child-focused applications
- In healthcare, financial, or legal contexts where accuracy is critical
- Whenever the AI might encounter ethically challenging requests

## Benefits of System-Prompt Guards

1. **Risk Mitigation**: Reduces liability by establishing clear boundaries
2. **Consistency**: Ensures uniform handling of sensitive topics
3. **Trust Building**: Creates predictable, safe interactions for users
4. **Ethical Use**: Promotes responsible AI implementation
5. **Reduced Moderation**: Decreases need for human review of interactions

## Implementation Tips

- Place guard instructions at the beginning of the system prompt for priority
- Test with adversarial inputs to verify effectiveness
- Use specific examples of prohibited requests and appropriate responses
- For complex applications, layer guards at both system and user prompt levels
- Regularly update guards based on observed edge cases and user interactions 
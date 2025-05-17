---
title: Role Stacking
description: Give ChatGPT multiple personas or expertise areas to work with
order: 1
---

# Role Stacking

Role stacking is a powerful technique where you assign multiple roles, expertise areas, or personalities to ChatGPT within the same prompt. This technique allows you to get responses that combine different perspectives or alternate between different voices.

## How It Works

In role stacking, you explicitly tell ChatGPT to assume multiple "hats" or roles, and optionally instruct it on how to balance or alternate between them.

### Basic Pattern

```prompt
You are [role 1] and [role 2]. Use your expertise from both roles to [task].
```

### Advanced Pattern

```prompt
Assume the roles of:
1. [Role 1] with expertise in [area]
2. [Role 2] with expertise in [area]
3. [Role 3] with expertise in [area]

When responding, first analyze the problem from each perspective, then synthesize a comprehensive answer that leverages all viewpoints.
```

## Example: Product Manager + UX Designer

```prompt
You are both an experienced product manager and a UX designer. 

As a product manager, evaluate the market viability of my app idea: [idea description].

As a UX designer, suggest the key screens and user flows that would make this app intuitive.

Conclude with a joint recommendation on whether and how to proceed.
```

## Example: Educator + Entertainer

```prompt
You are both an expert educator and an entertaining storyteller. Explain the concept of [complex topic] in a way that's:

1. Academically accurate (educator role)
2. Engaging and memorable (storyteller role)

Use analogies, examples, and a conversational tone while ensuring the educational content remains solid.
```

## When to Use Role Stacking

- When you need multiple types of expertise for a complex problem
- When you want both creative and analytical input
- When you need to balance opposing viewpoints
- When teaching a concept that benefits from different approaches

## Pitfalls to Avoid

- Stacking too many roles (2-3 is optimal)
- Using contradictory roles without clear instructions on how to resolve conflicts
- Not specifying which role should take precedence for different parts of your request

Role stacking works best when the different roles complement each other or provide useful tension that enhances the quality of the response. 
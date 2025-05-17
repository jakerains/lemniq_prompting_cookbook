---
title: Troubleshooting Guide
description: Solutions for common ChatGPT prompting issues and errors
---

# Troubleshooting Guide

This guide helps diagnose and fix common issues encountered when working with ChatGPT prompts. Use this reference to troubleshoot problems and improve your results.

## Common Issues and Solutions

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| **Hallucination** | Missing context | Add authoritative source references or request citations with "Cite reliable sources for all factual claims." |
| **Too verbose** | Temperature too high or vague prompt | Add specific word/paragraph limits or lower temperature to 0.2-0.4. Example: "Respond in 3 paragraphs or fewer." |
| **Stops mid‑answer** | Maximum token limit reached | Type "continue" or use a model with larger context window. Break large tasks into smaller chunks. |
| **Repetitive content** | Unclear instructions or high temperature | Be more specific about content expectations and lower temperature. Add "Avoid repetition." |
| **Missing key information** | Prompt lacks specificity | Use the lemnIQ Formula to include all necessary context and constraints. |
| **Conflicting/confused output** | Multiple contradictory instructions | Simplify prompt and organize requests in numbered lists for clarity. |

## API-Specific Issues

| Issue | Description | Solution |
|-------|-------------|----------|
| **Rate limits** | Too many API requests in short period | Implement exponential backoff strategy. Monitor usage with dashboard. Optimize batch processing to reduce call frequency. |
| **Quota exceeded** | Monthly/daily API usage limit reached | Check usage metrics. Upgrade plan if needed. Implement caching for common queries. |
| **Connection timeouts** | Server overload or network issues | Add timeout handling and automatic retry logic to your code. |
| **Content filtered** | Response flagged by moderation | Review content policy and rephrase request to avoid policy violations. |

## Policy Refusals

When ChatGPT refuses to respond due to content policy concerns:

1. **Review the specific refusal message** for clues about which policy was triggered
2. **Reframe your request** to focus on legitimate aspects:
   - Instead of "How to hack a website" try "What are best practices for ethical security testing?"
   - Instead of "Write negative reviews" try "Create balanced product assessments highlighting pros and cons"
3. **Add educational or theoretical context** when appropriate
4. **Check for unintentional triggers** in your wording that may flag the system

## Formatting Issues

| Formatting Problem | Solution |
|-------------------|----------|
| **Markdown not rendering** | Explicitly request: "Format your response using markdown with proper headings, lists, and code blocks." |
| **Code formatting lost** | Request code in triple backticks with language specified: "Show code examples in ```python code blocks." |
| **Table formatting broken** | Specify: "Create tables using markdown table syntax with headers and alignment." |
| **List numbering issues** | Request explicit formatting: "Format as a numbered list with proper indentation for sub-points." |
| **Inconsistent styling** | Provide a clear formatting example and ask the model to follow it consistently. |

## Misunderstandings & Scope Issues

| Problem | Solution |
|---------|----------|
| **Ignores part of instructions** | Break complex prompts into numbered requirements. Ask model to confirm understanding before proceeding. |
| **Scope creep** | Clearly define boundaries: "Focus only on X, Y, and Z. Do not address other aspects." |
| **Assumes incorrect context** | Explicitly state assumptions and background information. Correct misunderstandings immediately. |
| **Misinterprets technical terms** | Define specific terminology in your prompt. For domain-specific tasks, specify the knowledge domain. |

## Response Quality Issues

| Quality Issue | Solution |
|--------------|----------|
| **Generic, bland responses** | Request specific examples, case studies, or unique perspectives. Increase temperature to 0.7-0.8 for more creative outputs. |
| **Outdated information** | Acknowledge model training cutoff and ask for timelessly relevant information. For current topics, provide recent facts in your prompt. |
| **Simplistic analysis** | Request multi-level analysis: "Analyze this from strategic, operational, and financial perspectives." Ask for pros/cons or compare multiple viewpoints. |
| **One-sided perspective** | Explicitly request balanced analysis: "Present multiple perspectives on this topic, including arguments both for and against." |

## When to Escalate to Human Expertise

Some situations require human judgment rather than continued AI attempts:

- Response seems legally or ethically questionable
- Multiple attempts still yield nonsense or incorrect information
- You require domain expertise the model demonstrably lacks
- Critical decisions with significant consequences
- Content that requires subjective aesthetic judgment
- Verification of factual claims in specialized domains

## Advanced Debugging Techniques

For persistent problems, try these advanced troubleshooting approaches:

1. **Prompt Tracing**: Add "Explain your thinking step by step before giving your final answer" to see where reasoning goes wrong.
2. **Zero-Shot to Few-Shot**: If zero-shot prompting fails, add 1-3 examples of desired input/output pairs.
3. **Role Refinement**: Try different expert roles to find which produces the best results for your specific task.
4. **Temperature Tuning**: Systematically test different temperature settings (0.0, 0.3, 0.7, 1.0) to find optimal creativity/consistency balance.
5. **Context Window Management**: For large documents, try different chunking strategies when approaching token limits. 
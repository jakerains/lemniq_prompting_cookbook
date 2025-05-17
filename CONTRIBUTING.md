# Contributing to lemnIQ Prompting Cookbook

Thank you for considering contributing to the lemnIQ Prompting Cookbook! This document provides guidelines and best practices to ensure consistency across the project.

## Style Guide

### Content Guidelines

- **Tone**: Keep explanations practical and jargon-free. The cookbook aims to be accessible to non-technical users.
- **Table Width**: Limit tables to 80 characters wide for better readability on various devices.
- **Emoji Policy**: Use emojis strategically for visual cues (✅ for success cases, ⚠️ for warnings, 🔍 for tips) but avoid overuse.
- **Examples**: Always include at least one worked example (prompt → response) per recipe.

### Formatting

- Use **kebab-case** for all filenames (e.g., `multi-agent.md` not `multi_agent.md`).
- Include YAML frontmatter in every `.md` file:
  ```yaml
  ---
  title: Writing & Marketing
  description: Templates for emails, ads, and blog outlines
  order: 1
  ---
  ```
- Organize content with clear H2 (`##`) and H3 (`###`) headings.
- Use code blocks for prompts and responses:
  ````markdown
  ```prompt
  [Your prompt text here]
  ```
  ````

## Pull Request Process

1. Fork the repository and create a branch for your changes.
2. Ensure your changes follow the style guide above.
3. Add yourself to the contributors section in the README.
4. Submit a pull request with a clear description of the changes.

## Good First Issues

Look for issues labeled `good first issue` if you're new to contributing. These typically include:

- Adding new recipe examples
- Translating existing content
- Fixing typos or formatting issues
- Adding diagrams or visual aids

## Code of Conduct

- Be respectful and inclusive in all interactions.
- Provide constructive feedback on pull requests.
- Help maintain a welcoming environment for all contributors regardless of experience level.

Thank you for helping make the lemnIQ Prompting Cookbook better for everyone!

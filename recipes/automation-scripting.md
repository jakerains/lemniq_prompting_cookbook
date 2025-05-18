---
title: Automation & Scripting
description: Templates for automation tasks and code generation
order: 3
---

# Automation & Scripting Prompts

This file contains prompts for generating code snippets, automation scripts, and technical solutions. These prompts help you quickly create functional code for various automation needs.

## Quick-Start Examples

| # | Use Case | Prompt Template | Example Output |
| - | -------- | --------------- | -------------- |
| 1 | **Zapier Webhook Handler** | "Write a bare-bones Python Flask endpoint that accepts JSON payload {name, email} and appends to Google Sheet via Sheets API." | "app.route('/hook', methods=['POST']) ... writes name and email to sheet using service account." |
| 2 | **Data Scraper Outline** | "Provide step-by-step pseudocode for scraping product prices from example.com." | "1. Send GET request. 2. Parse HTML. 3. Extract price class. 4. Store to CSV." |
| 3 | **Slack Bot Snippet** | "Give a short Node.js snippet that posts 'Task done!' to a channel using Slack API." | "const { WebClient } = require('slack'); client.chat.postMessage({text:'Task done!', channel:'#general'});" |
| 4 | **Data Cleaning Steps** | "List commands to clean a CSV: drop empty rows, trim whitespace, and export." | "Use pandas: df.dropna(); df.applymap(lambda x: x.strip()); df.to_csv('clean.csv', index=False)" |
| 5 | **Simple CLI** | "Generate a Python argparse skeleton for a CLI that converts markdown to HTML." | "parser = argparse.ArgumentParser(); parser.add_argument('input'); parser.add_argument('-o','--output');" |

## Data Processing

### CSV Data Transformation

```prompt
Write a [Python/JavaScript/etc.] script that:
1. Reads a CSV file from [path/source]
2. Performs these transformations:
   - [transformation 1, e.g., convert date format]
   - [transformation 2, e.g., calculate new values from columns X and Y]
   - [transformation 3, e.g., filter rows by condition]
3. Outputs the transformed data to a new CSV file

The input CSV has these columns: [list columns and their data types].
Handle potential errors like missing data or incorrect formats.
```

## Process Automation

### Email Automation Workflow

```prompt
Create a step-by-step workflow for setting up automated email responses when:
1. A new form submission is received in [form tool]
2. The submission contains [specific data point]
3. The appropriate response template should be:
   - For [condition A]: [response type A]
   - For [condition B]: [response type B]
   - For [condition C]: [response type C]

Include any necessary API connections, tools, and specific configuration requirements. Use [specific platform] for implementation.
```

## API Integration

### Third-Party API Connection

```prompt
Write a code snippet in [language] to connect to the [service name] API that:
1. Authenticates using our API key with proper security practices
2. Retrieves [specific data] using the endpoint [endpoint]
3. Processes the JSON response to extract [specific fields]
4. Handles common error cases (rate limiting, authentication failures, etc.)
5. Implements basic caching to minimize API calls

Include comments explaining each step and how to customize for different use cases.
``` 
# 3.3 Automation & Scripting Recipes

*Ask ChatGPT to write code or pseudo-code you can convert to n8n, Zapier, or Python scripts.*

| # | Use Case | Prompt Template | Example Output |
| - | -------- | --------------- | -------------- |
| 1 | **Zapier Webhook Handler** | "Write a bare-bones Python Flask endpoint that accepts JSON payload {name, email} and appends to Google Sheet via Sheets API." | "app.route('/hook', methods=['POST']) ... writes name and email to sheet using service account." |
| 2 | **Data Scraper Outline** | "Provide step-by-step pseudocode for scraping product prices from example.com." | "1. Send GET request. 2. Parse HTML. 3. Extract price class. 4. Store to CSV." |
| 3 | **Slack Bot Snippet** | "Give a short Node.js snippet that posts 'Task done!' to a channel using Slack API." | "const { WebClient } = require('slack'); client.chat.postMessage({text:'Task done!', channel:'#general'});" |
| 4 | **Data Cleaning Steps** | "List commands to clean a CSV: drop empty rows, trim whitespace, and export." | "Use pandas: df.dropna(); df.applymap(lambda x: x.strip()); df.to_csv('clean.csv', index=False)" |
| 5 | **Simple CLI** | "Generate a Python argparse skeleton for a CLI that converts markdown to HTML." | "parser = argparse.ArgumentParser(); parser.add_argument('input'); parser.add_argument('-o','--output');" |

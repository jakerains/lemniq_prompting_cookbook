---
title: Tool Calling (Actions)
description: Enable ChatGPT to use external tools and APIs for enhanced capabilities
order: 2
---

# Tool Calling (Actions)

Tool calling allows ChatGPT to interact with external tools, APIs, or functions that you define. This technique extends the capabilities of the AI beyond text generation by allowing it to perform actions like searching the web, querying databases, or manipulating files.

## How It Works

When using the OpenAI Assistants API, you can define custom tools that the AI can call when appropriate. The AI will generate a structured JSON object that conforms to the schema you define, which your application can then use to execute the actual tool functionality.

### Basic Tool Definition Pattern

```json
{
  "name": "tool_name",
  "description": "Brief description of what the tool does",
  "parameters": {
    "type": "object",
    "properties": {
      "param1": {"type": "string", "description": "Description of parameter 1"},
      "param2": {"type": "number", "description": "Description of parameter 2"}
    },
    "required": ["param1"]
  }
}
```

## Example: Web Search Tool

```json
{
  "name": "search_web",
  "description": "Searches the web for current information on a topic",
  "parameters": {
    "type": "object",
    "properties": {
      "query": {
        "type": "string",
        "description": "The search query to look up"
      },
      "region": {
        "type": "string",
        "description": "Optional region code for localized results",
        "enum": ["us", "uk", "eu", "asia"]
      }
    },
    "required": ["query"]
  }
}
```

## Example: Data Retrieval Tool

```json
{
  "name": "get_customer_data",
  "description": "Retrieves customer data from the CRM system",
  "parameters": {
    "type": "object",
    "properties": {
      "customer_id": {
        "type": "string",
        "description": "The unique identifier for the customer"
      },
      "fields": {
        "type": "array",
        "items": {"type": "string"},
        "description": "Specific customer fields to retrieve (returns all if empty)"
      }
    },
    "required": ["customer_id"]
  }
}
```

## When to Use Tool Calling

- When the AI needs access to real-time information
- When the conversation requires data from external systems
- When you need the AI to perform actions like scheduling or data processing
- When building an agent that needs to interact with your application's APIs

## Best Practices

1. **Provide Clear Descriptions**: Make tool and parameter descriptions precise and comprehensive
2. **Limit Parameter Complexity**: Keep parameter structures simple and intuitive
3. **Validate Input/Output**: Always validate the data the AI sends to your tools
4. **Error Handling**: Implement robust error handling for tool execution
5. **Security**: Never allow tools to execute arbitrary code or access sensitive data without proper validation

## Implementation Tips

- Use the OpenAI Assistants API for the most integrated tool calling experience
- Test tools with simple examples before implementing complex workflows
- Consider rate limits and performance impacts of external API calls
- Log tool calls for debugging and improving system performance over time 
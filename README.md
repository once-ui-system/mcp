## About

Once UI is an agent-first design system that empowers indie creators to build high-quality, responsive apps — without wrestling with complexity. Designed for AI-native workflows, it turns abstract intent into concrete interfaces with minimal syntax.

## AI Workflow

Once UI uses custom tokens and props to deliver an intuitive, compact developer experience. Our philosophy: infer what you’re trying to build — even with minimal input — and Once UI applies smart defaults under the hood.

Compared to Tailwind + shadcn, Once UI yields up to **70% more compact** output, with **cleaner, more natural syntax**.

That said, most AI models aren’t yet as fluent in Once UI as they are with Tailwind. To bridge that, we’ve created tooling and patterns to help agents learn fast — and guess better over time.

## Local Repository

If your repository includes Once UI components, you can guide AI with simple, natural prompts:

> I want you to implement a feed view using the `@Grid` component. Use the `@Card` component for each feed item. The card should be column direction with an `@Avatar` in the header, a `@Text` containing the name, and another one for the date. The card should have a `@Media` for the image, and two `@Text` for the title and description.

As you build more with Once UI, AI models will learn your patterns and start suggesting better code, faster. The more you rely on real usage, the less they hallucinate.

## MCP Server

Agents can pull Once UI documentation through [Context7’s MCP server](https://context7.com/once-ui-system/mcp), supported in editors like Windsurf and Cursor.

To configure it:

1. Open `mcp_config.json` in File / Preferences / Settings / Plugins

2. Add the following configuration:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

3. Restart your IDE
4. Run the following code:

> get-library-docs /once-ui-system/mcp

This syncs the Once UI documentation with your local agent environment. To invoke the context, end your prompt with `use context7`.

Example:

> I want you to implement [...]. use context7

This lets your agent leverage the full Once UI system — even if it’s not installed locally.
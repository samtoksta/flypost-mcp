<p align="center"><img src="logo.png" width="96" alt="Flypost"></p>

# Flypost MCP server

Flypost is a LinkedIn content studio. Its hosted MCP server lets Claude, ChatGPT, Cursor and other
AI apps plan, write, design and schedule LinkedIn content in your own voice, from your own material.

```
https://mcp.flypost.io/mcp
```

- **Transport:** Streamable HTTP
- **Auth:** OAuth. You sign in to Flypost in your browser once. No API key.
- **Registry:** [`io.flypost/flypost`](https://registry.modelcontextprotocol.io/v0/servers?search=io.flypost) on the official MCP Registry
- **Docs:** [Use Flypost from ChatGPT or Claude](https://www.flypost.io/help/connect-flypost-to-chatgpt-or-claude)

This repository describes the hosted server. There is nothing to install or run yourself.

## What it can do

- **Ideas:** find post ideas based on what has worked on your profile, checked against everything you
  have already published so you don't repeat yourself.
- **Writing:** draft posts in your voice. The assistant reads your Flypost writing voice (tone, words to
  avoid, formatting rules) and searches your Brain, the blog posts, videos, documents and notes you
  have added, for real facts, stories and figures.
- **Design:** carousels, infographics and stat posts in your brand colours, fonts and logo.
- **Articles:** long-form LinkedIn Pulse articles from a brief and an outline you approve.
- **Analytics:** how your recent posts performed, and which topics and formats earned reach.
- **Publishing:** schedule posts to your LinkedIn profile or company page, or cancel a scheduled one.

Everything is saved to your Flypost account, so you and your team can keep editing in the app.

## Connect

You need a Flypost account. A 7-day free trial is available at [flypost.io](https://www.flypost.io).

**Claude:** Customize, then Connectors, then **+ Add**, then **Add custom connector**. Name it Flypost,
paste the server address, then click **Connect** and sign in.

**ChatGPT:** Plugins, then Settings, then MCP, then **Add server**. Paste the server address, choose
Streamable HTTP, leave token fields empty, and sign in.

**Claude Code:**

```bash
claude mcp add --transport http flypost https://mcp.flypost.io/mcp
```

**Cursor** (`~/.cursor/mcp.json`):

```json
{ "mcpServers": { "flypost": { "url": "https://mcp.flypost.io/mcp" } } }
```

**VS Code** (`.vscode/mcp.json`):

```json
{ "servers": { "flypost": { "type": "http", "url": "https://mcp.flypost.io/mcp" } } }
```

Any other client that supports remote MCP servers with OAuth works the same way.

## Example prompts

- "Give me five post ideas about onboarding, based on what has done well for me."
- "Find what we've said about pricing in my Brain and write a post about it in my voice."
- "Turn this blog post into a 6-slide carousel."
- "How did my posts do last month?"
- "Schedule it for Tuesday at 9am."

## Links

- Website: <https://www.flypost.io>
- Privacy policy: <https://www.flypost.io/privacy>
- Support: <https://www.flypost.io/support>
- Claude plugin (workflow skills): <https://github.com/samtoksta/flypost-claude-plugin>

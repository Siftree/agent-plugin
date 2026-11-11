# Siftree

Siftree collects, stores, searches, and analyzes your unstructured data: social posts, reviews, articles, transcripts, and your own documents. This plugin connects your AI assistant to your Siftree account through the Siftree MCP server, so it can search and analyze your datasets, collect public data, and build Siftree apps for you.

The plugin adds no code of its own. It points your assistant at the hosted Siftree MCP server, which serves the tools and their documentation and stays current without plugin updates.

## What it connects to

- **MCP server:** `https://app.siftree.com/api/mcp` (remote, streamable HTTP).
- **Sign-in:** OAuth with your Siftree account. Your assistant gets a scoped access token; it never sees your password.
- **Data sent:** the tool calls your assistant makes and their arguments, such as search queries and dataset ids. Tools act only on the signed-in account's data.
- **Usage:** some tools (dataset writes and queries, web and social data collection, and AI tools) count against your Siftree plan's monthly included usage.

You need a Siftree account. Sign up at [siftree.com](https://www.siftree.com).

## Install

### Claude

Install **Siftree** from the Claude plugin directory, then connect it from the plugin's **Connectors** tab and sign in with Siftree.

In Claude Code, you can also install it from this repository:

```bash
claude plugin marketplace add Siftree/agent-plugin
claude plugin install siftree@siftree
```

### ChatGPT and Codex

Install **Siftree** from the ChatGPT plugin directory, which ChatGPT and Codex share, and sign in with Siftree when prompted.

## What's in this repository

| File | Read by |
| --- | --- |
| `.claude-plugin/plugin.json`, `.mcp.json` | Claude (Claude Code, Claude apps, Cowork) |
| `.claude-plugin/marketplace.json` | Claude Code, to install from this repository |
| `plugin.json`, `mcp.json` | ChatGPT and Codex ([Agent Plugins](https://agent-plugins.org) format) |
| `assets/logo.png` | Both directories' listings |

Both MCP files point at the same server.

## Getting started

Ask your assistant something like "List my Siftree channels" or "Find negative reviews about late delivery in my reviews dataset." It reads the Siftree reference through the `docs_get` tool before calling tools it hasn't used.

## Support

- Email: [support@siftree.com](mailto:support@siftree.com)
- [Privacy policy](https://www.siftree.com/privacy-policy)
- [Terms of service](https://www.siftree.com/terms-of-service)

## License

[Apache-2.0](LICENSE)

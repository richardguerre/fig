# Fig

Fig is agent-first SEO and AEO. It gives your AI agent live keyword, SERP, backlink and AI-visibility data through a hosted MCP server, plus specialist skills to audit pages, plan content, write, validate and track results. $20 one-time.

## Set up

Paste this into your agent:

```
Set up Fig - https://figaeo.com/llms.txt
```

The agent adds the MCP server and installs the skills. Sign in with GitHub or Google when asked.

## Manual install

MCP server: `https://figaeo.com/mcp` (Streamable HTTP, OAuth 2.1 sign-in with GitHub or Google).

- **Cursor**: install this plugin (`.cursor-plugin/plugin.json`), or add the remote MCP server in Settings, then complete sign-in.
- **Codex**: this repo has a Codex plugin manifest (`.codex-plugin/plugin.json`, `.mcp.json`, `skills/`). Add it as a plugin, or run `codex mcp add figaeo --url https://figaeo.com/mcp` and copy `skills/` into your skills folder.
- **Grok Bot**: add the plugin from the Grok Bot marketplace, or add the MCP server URL above.
- **Claude Code**: `/plugin marketplace add richardguerre/fig`, then `/plugin install figaeo@fig`. Or `claude mcp add --transport http figaeo https://figaeo.com/mcp`.
- **OpenClaw and other agents**: add the MCP server URL above and copy the folders in `skills/` into your agent's skills folder.

## Skills

Start with `fig`, the router. It calls the specialists as needed: `fig-site-audit`, `fig-search-research`, `fig-answer-research`, `fig-aeo`, `fig-seo`, `fig-content-strategy`, `fig-content-craft`, `fig-programmatic-seo`, `fig-free-tool`, `fig-content-validation`, `fig-outcomes`, `fig-seo-setup`, `fig-offpage`, `fig-distribute`, `fig-growth-creative`.

## First lookup

Ask your agent: "Check my Fig balance, then audit my site for SEO and AEO." The balance check is free.

## Credits

Research lookups use credits. When your balance is empty, the agent calls `create_checkout` and gives you a short figaeo.com/pay link. Open it in your browser and pay on Stripe Checkout. $20 one-time is the recommended pack; the minimum is $10. Taxes are added at Checkout.

## Files

- `plugin.json`, `mcp.json`: Agent Plugins layout
- `.cursor-plugin/`: Cursor
- `.codex-plugin/`, `.mcp.json`: Codex
- `.claude-plugin/`: Claude Code
- `skills/`: shared `SKILL.md` skills
- `assets/`: logo

Website: https://figaeo.com

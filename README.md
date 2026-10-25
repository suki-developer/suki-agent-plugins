# Suki agent plugins

Public install target for the **Suki Cookbook** plugin used by Cursor, Claude Code, and Codex.

This repository contains only plugin manifests and short recipe skills. Full documentation stays on [developer.suki.ai](https://developer.suki.ai). Content is synced automatically from Suki's private docs repo when cookbook recipes change.

## Install

### Cursor

1. Open **Customize** → plugins / marketplaces.
2. Add marketplace from GitHub: `HarshSuki/suki-agent-plugins`
3. Install the **cookbook** plugin.

### Claude Code

```bash
/plugin marketplace add HarshSuki/suki-agent-plugins
/plugin install cookbook@suki-cookbook
```

(Exact install command names may vary by Claude Code version; use the marketplace UI if available.)

### Codex

Add `HarshSuki/suki-agent-plugins` as a plugin marketplace, then install **cookbook**.

### Docs without installing a plugin

- Documentation MCP: `https://developer.suki.ai/mcp`
- Agent skills: `https://developer.suki.ai/.well-known/agent-skills/`

## What is (and is not) here

| Included | Not included |
| --- | --- |
| Plugin manifests for Cursor, Claude, Codex | Full Mintlify MDX docs |
| Generated cookbook `SKILL.md` recipes | Internal scripts, CSS, Docs Bot |
| Links to published docs + MCP | Partner secrets or staging credentials |

## License

Proprietary © Suki. For partner integration use under your Suki agreement.

# Suki agent plugins

Public install target for the **Suki Cookbook** plugin used by Claude Code, Codex, Cursor, Antigravity, Gemini CLI, GitHub Copilot, Grok, Kimi Code, and omp.

The repository root is also a plugin (`skills/`, `gemini-extension.json`, `.kimi-plugin/`) for agents that install straight from the repository URL. `skills/` mirrors `plugins/cookbook/skills/`.

This repository contains only plugin manifests and short recipe skills. Full documentation stays on [developer.suki.ai](https://developer.suki.ai). Content is synced automatically from Suki's private docs repo when cookbook recipes change.

## Install

### Cursor

1. Open **Customize** → plugins / marketplaces.
2. Add marketplace from GitHub: `suki-developer/suki-agent-plugins`
3. Install the **cookbook** plugin.

### Claude Code

```bash
/plugin marketplace add suki-developer/suki-agent-plugins
/plugin install cookbook@suki-cookbook
```

(Exact install command names may vary by Claude Code version; use the marketplace UI if available.)

### Codex

Add `suki-developer/suki-agent-plugins` as a plugin marketplace, then install **cookbook**.

### Antigravity

```bash
agy plugin install https://github.com/suki-developer/suki-agent-plugins
```

### Gemini CLI

```bash
gemini extensions install https://github.com/suki-developer/suki-agent-plugins
```

### GitHub Copilot CLI

```bash
copilot plugin marketplace add suki-developer/suki-agent-plugins
copilot plugin install cookbook@suki-cookbook
```

### Grok Build

```bash
grok plugin marketplace add suki-developer/suki-agent-plugins
grok plugin install cookbook --trust
```

### Kimi Code

Inside `kimi`, run `/plugins install https://github.com/suki-developer/suki-agent-plugins`, then `/reload`.

### omp

```bash
omp plugin marketplace add suki-developer/suki-agent-plugins
omp plugin install cookbook@suki-cookbook
```

### Docs without installing a plugin

- Documentation MCP: `https://developer.suki.ai/mcp`
- Agent skills: `https://developer.suki.ai/.well-known/agent-skills/`

## What is (and is not) here

| Included | Not included |
| --- | --- |
| Plugin manifests for Claude, Codex, Cursor, Gemini CLI, Kimi Code | Full Mintlify MDX docs |
| Generated cookbook `SKILL.md` recipes | Internal scripts, CSS, Docs Bot |
| Links to published docs + MCP | Partner secrets or staging credentials |

## License

Proprietary © Suki. For partner integration use under your Suki agreement.

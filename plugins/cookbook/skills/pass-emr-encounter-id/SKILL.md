---
name: pass-emr-encounter-id
description: 'Pass emr_encounter_id on ambient create to link Mobile, Web, and API to one note. Use when implementing "Share One Note across Products" from the Suki cookbook (/cookbook:pass-emr-encounter-id).'
disable-model-invocation: true
---

# Share One Note across Products

Implement the Suki cookbook recipe **Share One Note across Products** in the user's codebase.

Canonical doc (fetch for exact steps and code):
https://developer.suki.ai/documentation/cookbooks/pass-emr-encounter-id.md

Published page:
https://developer.suki.ai/documentation/cookbooks/pass-emr-encounter-id

## Before you start

1. Confirm the user has Partner credentials from [partner onboarding](https://developer.suki.ai/documentation/get-started/partner-onboarding). If not, stop and link that page.
2. Fetch the product skill for this recipe:
   https://developer.suki.ai/.well-known/agent-skills/suki-ambient-api/SKILL.md
3. Connect the [Documentation MCP](https://developer.suki.ai/documentation/references/mcp) so you can search guides and API reference while implementing.
4. Read the cookbook doc above before writing code. Do not invent endpoints, headers, WebSocket frames, or status values.

## Your job

- Apply this recipe's pattern to the user's existing project (language, framework, and file layout).
- Match the **Problem**, **Prerequisites**, and **Solution** sections in the cookbook doc.
- Prefer copy-paste-ready examples from the doc; adapt names and env vars only.
- When the recipe links a tutorial or API reference, use those pages for full context.

## Accuracy rules

- Do not invent Suki API behavior, SDK options, or message types.
- Keep Ambient (`/ws/stream`, RU9G), Dictation (`/ws/transcribe`, `AUDIO_END`), Form filling, and Patient Summary flows separate.
- Use staging (`sdp.suki-stage.com`) unless the user explicitly requests production.
- Never embed Partner Tokens, secrets, or credentials in generated code; read from env or the user's secret store.

## When finished

- Summarize what changed and which cookbook steps were applied.
- Link back to https://developer.suki.ai/documentation/cookbooks/pass-emr-encounter-id for the human-readable walkthrough.

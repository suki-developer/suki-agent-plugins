---
name: browse-cookbook
description: Use when the user asks what Suki cookbook recipes exist, wants to browse integration recipes, or asks what they can build with Suki — lists recipes and points to matching /cookbook:{recipe-id} commands.
---

# Browse the Suki cookbook

Short, copy-paste integration recipes for common Partner API and SDK problems. Each recipe has a slash command that loads guided implementation steps against the user's project.

Full hub: https://developer.suki.ai/documentation/cookbooks/overview

- **End Ambient After Streaming** (`/cookbook:end-ambient-after-streaming`) — Send the RU9G end marker, close the WebSocket, then end the ambient session with REST. Doc: https://developer.suki.ai/documentation/cookbooks/end-ambient-after-streaming
- **Send START_TIME Before Ambient Audio** (`/cookbook:send-start-time-before-ambient-audio`) — Send one START_TIME frame on /ws/stream before the first PCM chunk for Ambient and Form filling. Doc: https://developer.suki.ai/documentation/cookbooks/send-start-time-before-ambient-audio
- **Authenticate Browser WebSocket Handshake** (`/cookbook:browser-websocket-auth`) — Pass Partner Token auth through Sec-WebSocket-Protocol for browser ambient streaming. Doc: https://developer.suki.ai/documentation/cookbooks/browser-websocket-auth
- **Poll Session Status Before Fetching Content** (`/cookbook:wait-for-status-before-retrieve`) — Poll ambient session status until completed before calling content APIs. Doc: https://developer.suki.ai/documentation/cookbooks/wait-for-status-before-retrieve
- **Fetch Note Content with note_id** (`/cookbook:get-note-content-by-note-id`) — Retrieve ambient note content using note_id from create after generation. Doc: https://developer.suki.ai/documentation/cookbooks/get-note-content-by-note-id
- **Share One Note across Products** (`/cookbook:pass-emr-encounter-id`) — Pass emr_encounter_id on ambient create to link Mobile, Web, and API to one note. Doc: https://developer.suki.ai/documentation/cookbooks/pass-emr-encounter-id
- **Clear a Remote Session Conflict** (`/cookbook:resolve-session-conflict`) — End a remote ambient session and retry create when sessionAlreadyExists is returned. Doc: https://developer.suki.ai/documentation/cookbooks/resolve-session-conflict
- **Create an Interoperable Headless Session** (`/cookbook:create-interoperable-headless-session`) — Create a Headless ambient session with emrEncounterId for cross-product note sharing. Doc: https://developer.suki.ai/documentation/cookbooks/create-interoperable-headless-session
- **Seed Patient Context for the Web SDK** (`/cookbook:seed-patient-context-for-web-sdk`) — Seed patient context on ambient session create so the Web SDK mounts with profile data. Doc: https://developer.suki.ai/documentation/cookbooks/seed-patient-context-for-web-sdk
- **End Dictation with AUDIO_END** (`/cookbook:end-dictation-with-audio-end`) — Finish a Dictation WebSocket session with AUDIO_END, EOF, close, and REST end. Doc: https://developer.suki.ai/documentation/cookbooks/end-dictation-with-audio-end
- **Write Dictation Text to an EHR Field** (`/cookbook:dictation-onsubmit-chart-field`) — Use Dictation SDK onSubmit to write finalized transcript text into a chart field. Doc: https://developer.suki.ai/documentation/cookbooks/dictation-onsubmit-chart-field
- **Add provider_id to Bearer Login** (`/cookbook:bearer-provider-id-on-login`) — Include provider_id on Bearer login and register flows for Partner API calls. Doc: https://developer.suki.ai/documentation/cookbooks/bearer-provider-id-on-login
- **Register Then Login on provider_not_registered** (`/cookbook:register-then-login`) — Handle provider_not_registered by registering the provider, then retrying login. Doc: https://developer.suki.ai/documentation/cookbooks/register-then-login
- **Verify Webhook HMAC Signatures** (`/cookbook:verify-webhook-hmac-signature`) — Validate Suki webhook payloads with HMAC-SHA256 before processing events. Doc: https://developer.suki.ai/documentation/cookbooks/verify-webhook-hmac-signature
- **Upload FHIR to CKG and Poll Ingestion** (`/cookbook:upload-fhir-to-ckg-and-poll`) — Upload FHIR to CKG with a pre-signed URL and poll until ingestion completes. Doc: https://developer.suki.ai/documentation/cookbooks/upload-fhir-to-ckg-and-poll
- **Generate a Patient Summary for One Encounter** (`/cookbook:generate-patient-summary-for-encounter`) — Trigger Patient Summary generation for one encounter and store patient_summary_id. Doc: https://developer.suki.ai/documentation/cookbooks/generate-patient-summary-for-encounter
- **Poll Patient Summary Status Before Retrieve** (`/cookbook:poll-patient-summary-status-before-retrieve`) — Poll Patient Summary job status until COMPLETED before calling retrieve. Doc: https://developer.suki.ai/documentation/cookbooks/poll-patient-summary-status-before-retrieve
- **Seed Form Filling with a Suki Template** (`/cookbook:seed-form-filling-template-context`) — List Suki Medical form templates and seed Form filling session context with form_template_id. Doc: https://developer.suki.ai/documentation/cookbooks/seed-form-filling-template-context

## How to run a recipe

After the user picks a recipe, invoke its slash command (for example `/cookbook:end-ambient-after-streaming`) or fetch the matching skill from the Suki cookbook plugin.

Connect the [Documentation MCP](https://developer.suki.ai/documentation/references/mcp) and the relevant product skill before implementing.

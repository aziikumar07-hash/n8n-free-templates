# Voice Note Transcription

- **Workflow file:** `AI_ML/voice_note_transcription.json`
- **Status:** `needs-configuration`
- **Tested date:** Not recorded
- **Source:** Adapted/imported from `wassupjay/n8n-free-templates` (license status uncertain; verify rights before redistribution)

## Purpose

This workflow appears intended to automate **Voice Note Transcription**.

## Required n8n compatibility

- `1.x (verify in your environment)`

## Required services and credentials (inferred)

- **Providers:** Cohere, Google Sheets, OpenAI, Slack, Weaviate
- **Credentials:**
- Cohere
- Google Sheets
- OpenAI
- Slack
- Weaviate

## Node inventory (inferred)

- `@n8n/n8n-nodes-langchain.agent`
- `@n8n/n8n-nodes-langchain.embeddingsCohere`
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- `@n8n/n8n-nodes-langchain.memoryBufferWindow`
- `@n8n/n8n-nodes-langchain.textSplitterCharacterTextSplitter`
- `@n8n/n8n-nodes-langchain.toolVectorStore`
- `@n8n/n8n-nodes-langchain.vectorStoreWeaviate`
- `n8n-nodes-base.googleSheets`
- `n8n-nodes-base.slack`
- `n8n-nodes-base.stickyNote`
- `n8n-nodes-base.webhook`

## Input and output expectations

### Trigger/input

- `voice-note-transcription`

The workflow JSON does not define a strict public input schema. Treat payload contracts as **implementation-specific** and validate in your environment.

### Example input/output

No reliable sample payloads are bundled with this workflow. Add local test fixtures before production use.

## Setup and import

1. In n8n, choose **Import from File** and select `AI_ML/voice_note_transcription.json`.
2. Recreate/attach required credentials listed above.
3. Review every node parameter, especially destination indices, sheet IDs, channels, and webhook paths.
4. Run a test execution with non-sensitive sample data.
5. Add rate limits, retries, and error handling suited to your providers.

## Common configuration caveats

- Placeholder IDs (for example `SHEET_ID`, provider placeholders, and static index names) must be replaced.
- Provider quotas, rate limits, and model availability vary by account.
- Verify that storage/notification targets are approved for your data classification.

## Cost and privacy notes

- Third-party AI/vector/database providers may receive input content and metadata.
- Review provider privacy settings, logging retention, and data residency before use.
- Do **not** commit credentials, tokens, or real identifiers to this repository.

## Safety notes

- may-process-pii
- ai-generated-output

If this workflow influences people, operations, or physical devices, require human review and domain-specific safeguards.

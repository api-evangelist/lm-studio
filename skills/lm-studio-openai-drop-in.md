---
name: Use LM Studio as an OpenAI drop-in
description: Point an existing OpenAI client at LM Studio's local server to run chat completions and embeddings against local models with no code changes beyond the base URL.
api: openapi/lm-studio-server-openapi.yml
operations: [openaiListModels, openaiChatCompletions, openaiEmbeddings]
---

# Use LM Studio as an OpenAI drop-in

LM Studio exposes OpenAI-compatible endpoints at `http://localhost:1234/v1`. Reuse any
OpenAI client (Python/JS/C#) by changing only its `base_url`. No API key is required by
default; pass any placeholder string if the client insists on one.

## Steps

1. **Discover models** — `GET /v1/models` (`openaiListModels`) to get loadable model
   ids in OpenAI list shape.
2. **Chat completion** — `POST /v1/chat/completions` (`openaiChatCompletions`) with the
   standard `{ "model", "messages": [...] }` body. `stream: true` yields SSE chunks.
   `tools` and `response_format` (JSON schema) are supported.
3. **Embeddings** — `POST /v1/embeddings` (`openaiEmbeddings`) with
   `{ "model": "<embeddings-model>", "input": "..." }` (load an `embeddings`-type
   model first via the native `loadModel`, or through the app).

## Rules
- Make sure the target model is loaded (`lms ps`, or the native `/api/v1/models` list);
  an unloaded model returns `404`/`400`.
- Errors use the OpenAI `{ "error": { "message", "type", "code" } }` envelope —
  see `errors/lm-studio-problem-types.yml`.
- For Anthropic clients, use `POST /v1/messages` instead.

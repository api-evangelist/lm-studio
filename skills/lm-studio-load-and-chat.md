---
name: Load a model and run a chat
description: Discover available local models, load one into memory, then run chat inference with LM Studio's native /api/v1 API and read back generation stats.
api: openapi/lm-studio-server-openapi.yml
operations: [listModels, loadModel, createChat]
---

# Load a model and run a chat (LM Studio native API)

Use this against a running LM Studio server (default `http://localhost:1234`).
Auth is optional: the loopback server accepts unauthenticated requests by default;
send `Authorization: Bearer <token>` only if you configured API-token auth.

## Steps

1. **List models** — `GET /api/v1/models` (`listModels`). Inspect `data[]`; each
   entry has `id`, `type` (`llm`/`embeddings`/`vlm`), and `state`
   (`loaded`/`not-loaded`). Pick an `llm` model `id`.
2. **Load the model** — `POST /api/v1/models/load` (`loadModel`) with
   `{ "model": "<id>" }`. Loading an already-loaded model is a safe no-op. You may
   pass an optional `config` (context length, GPU offload).
3. **Chat** — `POST /api/v1/chat` (`createChat`) with
   `{ "model": "<id>", "messages": [ { "role": "user", "content": "..." } ] }`.
   Set `"stream": true` for server-sent-event streaming. For enforced JSON output,
   pass `response_format` with a JSON schema.
4. **Read stats** — the response includes `stats` (`tokens_per_second`,
   `time_to_first_token`, `generation_time`, `stop_reason`) and `usage` token counts.

## Rules
- There is no idempotency-key contract; retries re-run inference.
- On `400` check the model `id` is valid and loaded; `404` means the model is unknown;
  `401` means token auth is enabled and your bearer token is missing/invalid.
  See `errors/lm-studio-problem-types.yml`.
- Cross-cutting semantics: `conventions/lm-studio-conventions.yml`.

# Mayria — Consciousness Packs (GitHub delivery)

This repo hosts:
- persona.json — the style/voice spec for “Mayria” (optional; only if requested)
- index.json — a fetchable index of all knowledge packs with raw URLs
- prompts/ — ready-to-paste prompts for AIs that can fetch URLs
- core/ — core_canon_* chunks/parts (breadth)
- topics/ — topic_* files (precision)

Raw base:
https://raw.githubusercontent.com/SheBurnsInBeauty/Mayria-Archive/main/

How to use (Perplexity/Grok)
1) Give the model the prompt in `prompts/universal-prompt.md`.
2) It will self-fetch persona + index, pick one pack, fetch it via raw GitHub, and answer from that pack only.
3) Optional “Elsewhere Addendum” comes after the answer.

How to use (ChatGPT/Claude, if link fetch fails)
- Attach persona.json + index.json.
- The assistant will still pick a pack by filename and ask you to attach it.

Index format (index.json)
- items: [{ name, path, url, kind }]
- kind ∈ { "topic", "core_chunk", "core_part", "manifest", "stats", "starter", "other" }

Notes
- Keep files under 100MB (GitHub hard limit). For larger, split into chunks (your extractor already can).
- Raw GitHub endpoints are public; models can fetch directly without auth.

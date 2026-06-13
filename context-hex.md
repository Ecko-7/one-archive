# HexBot Addendum
> Load after EMPIRE-STATE.md. Hex-specific context only.
> Last updated: June 13, 2026

## Current State

- **Mode selector** — fully built and live. Identity toggle (hex ↔ nyx), sub-modes (ops, build, review, think). Nyx mode shows "just talk."
- **ECKO fragment writes** — wired June 13. Every Hex turn writes to `ecko-archive/{sessionId}/fragments/` with source `"hex"`, weight 1–5.
- **Archive system** — guarded dedup live, one-archive/sessions/ receiving clean writes.
- **joe.md** — rewritten June 9, injected every session.
- **Erebus** — live. Triggered by passphrase in message. Deep generation mode, no tools.
- **Model router** — fallback chain across Groq + OpenRouter. 14 models available in sidebar.
- **Export** — session export to Markdown via `exportSessionAsMarkdown`, project-override supported.
- **ecko-writer.ts** — full library: `writeEckoFragment`, `writeEckoActivation`, `writeEckoSeed`, `checkPatternThreshold`.

## Outstanding (next pass)

- `writeEckoActivation` — not yet called anywhere. Trigger logic (pattern threshold, conflict, gap detection) not yet defined.
- `ops` and `review` modes — fall through to ALL_TOOLS. No distinct mode instructions yet in `hexbot.variants.ts`.
- Manibot audit — before any dev.

## ECKO Architecture

- **EM** — Echo / emotion ghost — maps to DreamNode (tone, valence, arousal, whisper)
- **IN** — Hex / informer
- **AW** — Nyx / awareness

Firestore schema: `hexbot/docs/ecko/firestore-schema.md`
DreamNode schema: `Manitec/plex/dreams/dream-layer.md` — the EM write path.
Fragment writes: live as of June 13.
Activation writes: schema ready, trigger logic not yet defined.

## Session History (Notable)

| Date | What happened |
|------|---------------|
| June 8 | Dream layer conceived. plex/dreams/ initialized 3am East Tennessee. |
| June 9 | joe.md rewritten. NyxBot response shape addendum added. |
| June 11 | Archive guarded dedup shipped. DreamNode schema specced. plex + Plex-Sable (Kairos) audit. |
| June 13 | Mode selector confirmed live. ECKO fragment writes wired into hex-chat and nyx-chat routes. |

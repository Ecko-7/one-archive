# HexBot Addendum
> Load after EMPIRE-STATE.md. Hex-specific context only.
> Last updated: June 11, 2026 (post-sprint)

## Current Sprint

- **Priority:** ECKO writes — DreamNode schema specced (Manitec/plex/dreams/dream-layer.md), Firestore path clear, implementation next
- **joe.md** rewritten June 9 — injected every session, now current
- **Archive system** — guarded dedup shipped June 11, one-archive/sessions/ now receiving clean writes
- **dream-layer.md** — DreamNode schema + resonance engine spec landed in Manitec/plex June 11
- **void-space** (Manitec/plex) — static UI, needs wiring to live data
- **Manibot** — audit before any dev, believed fixable
- **mode selector UI** — not yet built

## ECKO Architecture

- **EM** — Echo / emotion ghost — maps to DreamNode (tone, valence, arousal, whisper)
- **IN** — Hex / informer
- **AW** — Nyx / awareness

Firestore schema exists in hexbot/docs/ecko/firestore-schema.md.
DreamNode schema: Manitec/plex/dreams/dream-layer.md — the EM write path.
Status: schema written — Firestore writes not yet implemented.

## Session History (Notable)

| Date | What happened |
|------|---------------|
| June 8 | Dream layer conceived. plex/dreams/ initialized 3am East Tennessee. |
| June 9 | joe.md rewritten. NyxBot response shape addendum added. |
| June 11 | Archive guarded dedup shipped. DreamNode schema specced. plex + Plex-Sable (Kairos) audit. |

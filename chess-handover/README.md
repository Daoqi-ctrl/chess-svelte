# Chess Demo — Handover

## What this repo contains (current state)

This repo currently contains a **single-file HTML chess demo**:

- `index.html` — the playable chess board (single user controls both sides)
- `assets/pieces-basic-svg/` — SVG piece set used by the UI

No backend and no Svelte migration has been done yet.

---

## How to run locally

### Option A: open directly
Double-click `index.html` to open in a browser.

> Note: some browsers may block local asset loading depending on settings.

### Option B (recommended): run a local static server
From the repo root:

```bash
python3 -m http.server 8000
```

Then open:

- http://localhost:8000

---

## Features implemented

- chess.js integrated: legal moves only + strict turn order
- Mobile-friendly tap interaction
- Promotion selection UI (modal)
- End-game UX:
  - Check: highlight king
  - Checkmate / stalemate: modal + board lock
  - Turn pill shows outcome on terminal state
- Undo / Reset buttons

---

## Assets / paths

Pieces live here:

```
assets/pieces-basic-svg/
```

The UI loads them via relative path (make sure folder names match).

---

## Next steps (planned)

- Migrate current implementation to SvelteKit (initial parity pass)
- Add NanoID game URLs + persisted game state (FEN load/save by id)
- Add backend API (Node/Express) + storage (Postgres or file-based)
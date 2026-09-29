# Ring Guide Studio

A static browser-based editor for the David ring player's guide.

## What it does
- Uses 1024×1536 template pages and exports at exactly 1024×1536.
- Supports four built-in template slots: Story & Progression, Found & Hidden, Achievement, Purchased & Traded.
- Lets you upload replacement templates (PNG/JPG/WebP).
- Multi-select ring images and automatically fills empty ring slots.
- Drag a ring from the library to a slot; drag a filled slot onto another slot to swap placements.
- Edit Ring Name, Effect, and Hint directly on the page.
- Save multiple drafts, reopen them, delete them, and export/import drafts as JSON.
- Download a finished page as PNG.
- Uses uploaded ring artwork as-is; it does not regenerate or redraw the ring art.

## Important static-site limitation
A purely static website has no shared server-side database. Drafts in this build are persisted in the browser using IndexedDB, so they remain available on that browser/device, but they are **not automatically visible to another person's browser**.

The included JSON Export/Import workflow lets you move a draft between users. If you need a genuinely shared public draft library where everyone sees the same saved drafts, connect the same UI to a small shared backend (Supabase/Firebase/etc.). The editor itself is already separated enough to add that later.

## Deploy to Netlify

The repository-level `netlify.toml` publishes this directory automatically. Connect the repository to Netlify and leave the build command empty. For a manual deploy, upload this folder as the deploy directory.

## Run locally
Open `index.html` in a modern Chromium/Firefox/Safari browser. For best browser behavior, serve the folder with any simple static HTTP server.

Example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

# Game Guide Rings

Ring Guide Studio is a static browser editor for creating David ring player's-guide pages.

## Deploy to Netlify

This repository includes `netlify.toml`, so a Netlify site can be created by connecting the repository and leaving the build command blank. Netlify publishes `ring-guide-studio/ring-guide-site`, which contains the entry page and all template assets.

For a manual deploy, drag the `ring-guide-studio/ring-guide-site` folder into Netlify's deploy dropzone.

## Run locally

From the site directory, start any static server:

```bash
cd ring-guide-studio/ring-guide-site
python3 -m http.server 8000
```

Open `http://localhost:8000` in a modern browser.

## Static-site behavior

The editor supports template selection and upload, ring-image upload and drag-and-drop placement, direct editing of ring name/effect/hint fields, undo/redo, PNG export at exactly 1024 x 1536 pixels, and draft JSON import/export.

Saved drafts use IndexedDB in the current browser and device. They are not shared between visitors or browsers. JSON export/import is the supported way to move drafts between devices; shared drafts would require a backend such as Supabase or Firebase.
# Game-Guide-Rings
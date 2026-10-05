# Game Guide Rings

Artifact Guide Builder is a static browser editor for creating artifact player's-guide pages.

## Deploy to Netlify

This repository includes `netlify.toml`, so a Netlify site can be created by connecting the repository and leaving the build command blank. Netlify publishes `ring-guide-studio/ring-guide-site`, which contains the entry page and all template assets.

For a manual deploy, drag the repository root into Netlify's deploy dropzone.

## Run locally

From the repository root, start any static server:

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000` in a modern browser.

## Static-site behavior

The editor supports artifact image upload and drag-and-drop placement, direct editing of artifact names and descriptions, automatic filename matching against `all_items_names_and_descriptions.txt` or `artifacts.json`, draft save/load, and PNG export at exactly 1024 x 1536 pixels. Text-list entries use four-line groups: the source item name, proposed display name, description, and a blank separator. Filenames match the source item name, while the proposed display name is filled into the page.

Ring and artifact drafts use named IndexedDB records in the current browser and device, and each editor shows its saved drafts in a browser-side list. Existing artifact drafts from the older single-draft storage are migrated into that list the first time the artifact editor opens. Loading a draft restores the saved names and descriptions exactly; filename matching only runs when a new image is uploaded. Artifact drafts are managed in the browser and do not expose download/import controls. Drafts are not shared between visitors or browsers; shared drafts would require a backend such as Supabase or Firebase.
# Game-Guide-Rings
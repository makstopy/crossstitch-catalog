# CrossStitch Companion — Remote Pattern Catalog

This repository hosts the dynamic catalog of cross-stitch patterns for CrossStitch Companion via **Cloudflare Pages**.

## Structure
- `catalog.json`: Main index of all patterns with categories and metadata.
- `images/`: Preview images for patterns.
- `schemes/`: Standalone CrossStitchProject JSON files (loaded on demand).

## How to add a new pattern:
1. Export pattern JSON from the app (or create `schemes/shop_new_item.json`).
2. Add preview image to `images/new_item.jpg`.
3. Add entry to `catalog.json`.
4. Commit and push to `main` branch. Cloudflare Pages updates instantly!

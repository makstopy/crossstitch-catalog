# Cross Stitch Companion — Remote Pattern Catalog

This repository hosts the dynamic catalog of cross-stitch patterns and categories for Cross Stitch Companion via **GitHub + jsDelivr CDN**.

## Structure
- `categories.json`: Configurable list of categories, their order, and multilingual names.
- `catalog.json`: Main index of all patterns with categories and metadata.
- `images/`: Preview images for patterns (`.png` / `.jpg`).
- `schemes/`: Standalone CrossStitchProject JSON files (loaded on demand).

## Editing Categories (`categories.json`)
You can freely reorder, add, or rename categories in `categories.json`:
```json
[
  {
    "key": "halloween",
    "name": "Halloween",
    "labels": {
      "ru": "Хэллоуин",
      "en": "Halloween",
      "es": "Halloween"
    }
  },
  {
    "key": "new_category",
    "name": "New Category",
    "labels": {
      "ru": "Новая категория",
      "en": "New Category",
      "es": "Nueva Categoría"
    }
  }
]
```
- **Order:** The order of items in `categories.json` determines the order of tabs in the app.
- **Labels:** `labels.ru`, `labels.en`, `labels.es` provide localized tab titles for users.
- **Auto-discovery:** Any pattern in `catalog.json` with a new `category` key will automatically create a tab even if not yet added to `categories.json`.

## Adding Patterns:
1. Create `schemes/shop_new_item.json`.
2. Add preview image to `images/new_item.png`.
3. Add entry to `catalog.json` with matching `"category"`.
4. Commit and push to `main` branch. Changes propagate live to all apps!

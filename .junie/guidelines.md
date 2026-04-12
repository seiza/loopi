# Loopi Project Guidelines

These guidelines document the conventions followed for the Loopi project.

## 1. Bilingual Support
- Every resource and category must have both an English (`en/`) and a French (`fr/`) version.
- Both versions must share the same `slug` in their front matter to enable switching between languages.

## 2. Resource Management
- **File Location**: `en/resources/slug.md` and `fr/resources/slug.md`.
- **Metadata (Front Matter)**:
  - `title`: Name of the resource.
  - `category`: Must match one of the predefined categories:
    - "Débranché (sans ordinateur)"
    - "Numérique (avec écran)"
    - "Robot"
    - "Jeux de société"
    - "Dictionnaire (écosystème)"
  - `status`: "to review" (by default), "to play", or "completed".
  - `age`: Recommended age (e.g., "6+", "10 ans +").
  - `website`: URL to the official resource.
  - `slug`: Unique identifier used for file naming and language switching.
  - `lang`: "en" or "fr".
  - `price`: Estimated price (e.g., "Free", "Gratuit", "~20€").
  - `image`: Path to a real image (screenshot or photo) in `/assets/images/resources/slug.extension`.

## 3. Images and Placeholders
- Store images in `assets/images/resources/`.
- Use real photos or screenshots whenever possible.
- If an image is missing or broken, the `handleImageError` function in `_layouts/default.html` automatically displays `/assets/images/loopy-bot.svg` as a placeholder with 0.5 opacity.
- Images are restricted to a `max-height` of 200px on all listing pages.

## 4. Categories and Home Pages
- The home pages (`en/index.md`, `fr/index.md`) display categories in a specific order:
  1. Débranché (sans ordinateur)
  2. Numérique (avec écran)
  3. Robot
  4. Jeux de société
  5. Dictionnaire (écosystème)
- Slugs for category links are: `unplugged`, `digital`, `robot`, `board-games`, `dictionary`.

## 5. View Controls
- Listing pages (Home and Categories) support two view modes: "Tiles" (grid with images) and "Table" (list without images).
- The user's preference is saved in `localStorage` under `preferredView`.

## 6. Backlog
- New resource ideas or tasks should be tracked in `BACKLOG.md`.
- Mark items as completed with `[x]` once their English and French pages are created.

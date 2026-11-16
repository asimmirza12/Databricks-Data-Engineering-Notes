# How this repo is organised

Interactive study notes for the Databricks Data Engineer Professional exam, published with GitHub Pages at https://asimmirza12.github.io/Databricks-Data-Engineering-Notes/

## Structure

```
index.html                 home page: one card per topic
<topic-slug>/index.html    one self-contained page per topic
README.md                  table of topics with links
CLAUDE.md                  this file
```

Existing topics:
- `data-ingestion/` — Exam section 2, Data Ingestion and Loading
- `liquid-clustering/` — Exam section 5, Cost & Performance Optimization (data layout, liquid clustering, VACUUM)

## Adding a new topic

1. Create `<topic-slug>/index.html` (lowercase, hyphenated, e.g. `delta-lake`, `structured-streaming`).
2. Start from `data-ingestion/index.html`: copy its `<head>`, the whole `<style>` block (colour tokens, fonts, light and dark themes, components) and the nav pattern, so every page looks the same. Keep the `← All notes` link to `../` as the first nav item.
3. Page shape, per section:
   - plain-English explanation first, for someone new to the topic
   - an animated SVG diagram or a live demo where it helps understanding (SMIL `animateMotion` or CSS keyframes; JS demos in plain vanilla JS, no frameworks)
   - code samples with a "What if I change this?" table (change → effect)
   - comparison tables where options compete
   - exam traps marked with the `note trap` style
4. Respect `prefers-reduced-motion`, work at phone width, no external assets except Google Fonts.
5. Add a topic card to the root `index.html` (inside `<main class="topics">`, before the "More topics coming" box) and a row to the table in `README.md`.
6. Add a footer line saying details should be confirmed against the official Databricks docs.
7. Commit with a message like `Add <topic> notes` and push to `main`. Pages redeploys automatically.

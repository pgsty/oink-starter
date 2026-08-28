---
title: Understand the Structure
description: Know which small set of files owns configuration, content, and deployment.
book_kind: chapter
book_number: 2
weight: 20
---

The starter keeps each responsibility in one obvious place.

## The map {#map}

```text
hugo.yaml          site identity, languages, and optional integrations
data/home/         one compact landing-page file per language
content/blog/      posts, design notes, and releases
content/docs/      the four-part documentation tree
content/book/      this sequential tutorial
.github/workflows/ GitHub Pages and Cloudflare Pages deployment
```

## Navigation follows content {#navigation}

The `menus.main` front matter on each section root creates the top navigation and its dropdowns. The directory tree below Docs and Book creates their sidebars.

## Translations stay together {#translations}

English uses `.md`; Chinese and French peers use `.zh.md` and `.fr.md`. Keep the files side by side and use matching explicit heading IDs.

---
title: Make It Yours
description: Replace the identity and sample content without rebuilding the theme.
book_kind: chapter
book_number: 3
weight: 30
---

Most projects need only content changes and two configuration edits.

## Change identity once {#identity}

At the top of `hugo.yaml`, replace `Project Name` and `https://example.org/`. The YAML title anchor carries the name into all three languages.

Replace `assets/icons/logo.svg` and `static/favicon.svg` only when you have real project artwork.

## Replace the home page {#home}

Edit `data/home/en.yaml`, `zh.yaml`, and `fr.yaml`. The `sections` list controls order; the named blocks below it provide the copy.

## Replace sample content {#content}

Keep the directory structure, then rewrite or delete the example leaves. To rename a top-level menu entry, edit the corresponding translated `_index` files.

## Enable integrations deliberately {#integrations}

`hugo.yaml` contains commented examples for repository links, Giscus, Google Analytics, colors, typography, sharing, and feedback. Uncomment only a complete configuration that you intend to operate.

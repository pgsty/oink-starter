---
title: Publish the Site
description: Use either supplied workflow and verify the real deployed routes.
book_kind: chapter
book_number: 4
weight: 40
---

The generated `public/` directory is a static site. The repository includes two independent deployment paths.

## GitHub Pages {#github-pages}

In repository settings, choose **Pages → Source → GitHub Actions**. A push to `main` runs `.github/workflows/github-pages.yaml`; the workflow calculates the correct repository subpath automatically.

## Cloudflare Pages {#cloudflare-pages}

Create a Direct Upload Pages project, then add `CLOUDFLARE_ACCOUNT_ID` and `CLOUDFLARE_API_TOKEN` as repository secrets. Set the repository variable `CLOUDFLARE_PAGES_ENABLED` to `true` for automatic deploys. The project name defaults to the repository name and can be overridden with `CLOUDFLARE_PROJECT_NAME`.

## Verify production {#verify-production}

Open `/`, `/zh/`, and `/fr/`; then test one Blog, Docs, and Book route in each language. Confirm search, language switching, dark mode, and a narrow mobile viewport.

> [!IMPORTANT]
> A successful local build, a pushed commit, a green workflow, and a correct public site are four separate checks.

# OINK Starter

A small, production-ready skeleton for open-source project sites built with [OINK](https://oink.pgsty.com/) and Hugo. It ships with English, Simplified Chinese, and French home pages; Blog, Docs, and Book content; and deployment workflows for GitHub Pages and Cloudflare Pages.

No OINK documentation, analytics account, comment repository, regression suite, or project-specific brand is included. Google Analytics and Giscus stay fully commented until you configure them.

## Use this template

Select **Use this template** on GitHub, create your repository, then run three commands:

```bash
git clone https://github.com/YOU/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
hugo server
```

Open <http://localhost:1313/>. The first run downloads the pinned OINK Hugo Module. Building the site requires Git, Go 1.26 or newer, and Hugo Extended 0.165.0 or newer; it does not require Node.js or npm.

Cloning this original template is also exactly three commands:

```bash
git clone https://github.com/pgsty/oink-starter.git
cd oink-starter
hugo server
```

## Make it yours

The default site works unchanged. For a real project, start with only these edits:

1. Change `Project Name` and `https://example.org/` at the top of `hugo.yaml`.
2. Replace the three compact home-page files under `data/home/`.
3. Rewrite or delete the sample pages under `content/`.

The title uses one YAML anchor, so one edit changes all three languages. Navigation lives with each section’s translated `_index` page; renaming a section does not require editing a second menu tree. Replace `assets/icons/logo.svg` and `static/favicon.svg` only when you have real project artwork.

Common optional settings are already organized and commented in `hugo.yaml`: repository links, Giscus, Google Analytics, accent color, typography, image zoom, sharing, and feedback. Uncomment a complete block only when you are ready to operate that integration.

## Content map

```text
content/
├── blog/
│   ├── post/          articles
│   ├── design/        design notes and decisions
│   └── release/       release announcements
├── docs/
│   ├── introduction/
│   ├── get-started/
│   ├── tutorial/
│   └── reference/
└── book/              a short tutorial about this starter
```

English files end in `.md`; their Chinese and French peers end in `.zh.md` and `.fr.md`. Keep translated files side by side and keep explicit heading IDs aligned.

## Language profiles

The root `hugo.yaml` enables English, Chinese, and French. Two copy-ready alternatives are included:

```bash
cp examples/hugo.single.yaml hugo.yaml     # English only
cp examples/hugo.bilingual.yaml hugo.yaml  # English + Chinese
```

The profiles keep unused languages declared but disabled, so Hugo recognizes their suffixes and safely ignores their content. Restore the three-language configuration from Git before switching profiles again.

## Build

Preview while writing:

```bash
hugo server
```

Run the publication gate locally:

```bash
hugo --cleanDestinationDir --gc --minify --environment production \
  --printPathWarnings --panicOnWarning
```

Generated `public/`, `resources/`, and caches are ignored by Git.

## GitHub Pages

1. Open **Settings → Pages** and choose **GitHub Actions** as the source.
2. Push `main`, or run **Deploy to GitHub Pages** manually from the Actions tab.

`.github/workflows/github-pages.yaml` installs the pinned toolchain, performs a warning-strict production build, calculates the correct GitHub project subpath, and publishes the artifact through the Pages deployment API.

## Cloudflare Pages

The Cloudflare workflow uses Direct Upload so the same warning-strict build runs in GitHub Actions.

1. Create a Cloudflare Pages **Direct Upload** project. Use the repository name as the project name, or set a repository variable named `CLOUDFLARE_PROJECT_NAME`.
2. Add repository secrets `CLOUDFLARE_ACCOUNT_ID` and `CLOUDFLARE_API_TOKEN`. The token needs **Account → Cloudflare Pages → Edit**.
3. Run **Deploy to Cloudflare Pages** manually once. To deploy every push to `main`, add the repository variable `CLOUDFLARE_PAGES_ENABLED=true`.

The default canonical address is `https://<project>.pages.dev/`. Set `CLOUDFLARE_SITE_URL` to a custom production URL when you attach a domain.

Cloudflare Git integration is a separate deployment mode. Use either Git integration or this Direct Upload workflow for a given Pages project, not both.

## What “done” means

A local build, a committed change, a pushed branch, a green deployment workflow, and correct public rendering are separate gates. After deployment, inspect `/`, `/zh/`, and `/fr/`, plus representative Blog, Docs, and Book pages on desktop and mobile.

## License

MIT. Replace the generic copyright line when adopting the template.

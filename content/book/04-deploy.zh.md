---
title: 发布站点
description: 使用任一内置 workflow，并验证真实部署路由。
book_kind: chapter
book_number: 4
weight: 40
---

生成的 `public/` 目录是一份静态站点。仓库内置两条彼此独立的部署路径。

## GitHub Pages {#github-pages}

在仓库设置中选择 **Pages → Source → GitHub Actions**。推送到 `main` 会运行 `.github/workflows/github-pages.yaml`，workflow 会自动计算正确的仓库子路径。

## Cloudflare Pages {#cloudflare-pages}

创建一个 Direct Upload Pages 项目，然后将 `CLOUDFLARE_ACCOUNT_ID` 与 `CLOUDFLARE_API_TOKEN` 添加为仓库密钥。把仓库变量 `CLOUDFLARE_PAGES_ENABLED` 设为 `true` 即可自动部署。项目名默认使用仓库名，也可以通过 `CLOUDFLARE_PROJECT_NAME` 覆盖。

## 验证生产站点 {#verify-production}

打开 `/`、`/zh/` 与 `/fr/`，再分别测试每种语言下的 Blog、Docs 与 Book 路由。确认搜索、语言切换、深色模式以及窄屏移动布局。

> [!IMPORTANT]
> 本地构建成功、提交已推送、workflow 变绿、公开站点正确，是四道彼此独立的检查。

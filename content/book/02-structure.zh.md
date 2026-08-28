---
title: 理解目录结构
description: 了解哪些少量文件分别负责配置、内容与部署。
book_kind: chapter
book_number: 2
weight: 20
---

这个模板把每项职责放在一个明显的位置。

## 地图 {#map}

```text
hugo.yaml          站点身份、语言与可选集成
data/home/         每种语言一份精简首页数据
content/blog/      文章、设计记录与版本发布
content/docs/      经典四部曲文档树
content/book/      这份连续教程
.github/workflows/ GitHub Pages 与 Cloudflare Pages 部署
```

## 导航跟随内容 {#navigation}

每个栏目首页 front matter 中的 `menus.main` 创建顶部导航及其下拉菜单。Docs 与 Book 下面的目录树则创建各自侧栏。

## 译文放在一起 {#translations}

英文使用 `.md`，中文与法语对页分别使用 `.zh.md` 与 `.fr.md`。把它们并排保存，并使用一致的显式标题 ID。

---
title: 把模板变成你的站点
description: 替换身份与示例内容，无需重新构建主题。
book_kind: chapter
book_number: 3
weight: 30
---

大多数项目只需要修改内容，以及两处配置值。

## 只修改一次身份 {#identity}

在 `hugo.yaml` 顶部替换 `Project Name` 与 `https://example.org/`。YAML 标题锚点会把名称带入三种语言。

只有在已有正式项目图形时，才替换 `assets/icons/logo.svg` 与 `static/favicon.svg`。

## 替换首页 {#home}

编辑 `data/home/en.yaml`、`zh.yaml` 与 `fr.yaml`。`sections` 列表控制顺序，下面的同名数据块提供文案。

## 替换示例内容 {#content}

保留目录结构，然后重写或删除示例叶子页面。要修改顶部栏目名称，请编辑对应语言的 `_index` 文件。

## 有意识地启用集成 {#integrations}

`hugo.yaml` 中规整地注释了仓库链接、Giscus、Google Analytics、颜色、字体、分享与反馈示例。只有当配置完整且你准备运营它时，才取消注释。

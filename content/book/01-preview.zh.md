---
title: 预览站点
description: 用三条命令克隆仓库并打开本地首页。
book_kind: chapter
book_number: 1
weight: 10
---

OINK Starter 是一个 Hugo Module 站点。Git 下载源码，Go 解析锁定版本的主题，Hugo 负责完成全部构建。

## 前置条件 {#prerequisites}

安装 Git、Go 1.26 或更新版本，以及 Hugo Extended 0.165.0 或更新版本。`hugo version` 输出中必须包含 `extended`。

## 三条命令 {#three-commands}

```bash
git clone https://github.com/pgsty/oink-starter.git
cd oink-starter
hugo server
```

打开 <http://localhost:1313/>。中文位于 `/zh/`，法语位于 `/fr/`。

## 第一个证据 {#first-proof}

修改 `data/home/en.yaml` 中的一句话，并确认浏览器自动刷新。现在你已经有了一条可以工作的编辑循环。

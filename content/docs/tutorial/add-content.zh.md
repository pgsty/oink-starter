---
title: 添加文档页面
description: 创建页面，把它放入侧栏，并建立链接。
weight: 20
---

在 OINK 中，内容树就是文档侧栏。新增一个 Markdown 文件，就会新增一个页面。

## 创建文件 {#create}

```markdown
---
title: 新能力
description: 这项能力做什么。
weight: 30
---

在这里说明这项能力。
```

将它保存为 `content/docs/reference/new-capability.md`。

## 添加翻译 {#translations}

在旁边创建 `new-capability.zh.md` 与 `new-capability.fr.md`。各语言的显式标题 ID 应当保持一致。

## 预览 {#preview}

运行 `hugo server`，打开新页面，再通过语言切换器检查每个译文。

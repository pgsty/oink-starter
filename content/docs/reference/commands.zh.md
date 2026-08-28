---
title: 命令参考
description: 列出每条命令的用途、语法与退出行为。
weight: 20
---

## `project start` {#start}

启动本地服务。

```text
project start [--config FILE] [--listen ADDRESS]
```

## `project check` {#check}

只校验配置，不启动服务。退出状态 `0` 表示有效；任何非零状态都表示该配置不应部署。

```text
project check [--config FILE]
```

请用真实 CLI 帮助输出中的命令替换这些占位内容。

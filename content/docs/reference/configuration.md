---
title: Configuration
description: Record supported keys, defaults, and examples in one place.
weight: 10
---

Replace this small table with the public configuration surface of your project.

| Key | Type | Default | Meaning |
| --- | --- | --- | --- |
| `listen` | string | `127.0.0.1:8080` | Address used by the local server |
| `log_level` | string | `info` | Minimum emitted log level |
| `read_only` | boolean | `false` | Disable operations that change state |

## Example {#example}

```yaml
listen: 0.0.0.0:8080
log_level: debug
read_only: true
```

Document validation and precedence beside the keys, not in a separate hidden guide.

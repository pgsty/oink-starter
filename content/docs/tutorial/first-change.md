---
title: Make Your First Change
description: Complete one small change and verify it locally.
weight: 10
---

This sample tutorial models a complete task: prepare, change, verify, and review.

## Start from a known state {#known-state}

```bash
git status --short
git switch -c docs/first-change
```

## Change one thing {#change}

Edit a visible string or a small configuration value. Keep the first task narrow enough that its result is obvious.

## Verify {#verify}

Run the project’s smallest relevant check, then open the changed surface and inspect it yourself.

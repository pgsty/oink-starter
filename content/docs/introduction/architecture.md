---
title: Architecture
description: Give readers a stable mental model of the project.
weight: 20
---

Document the few components a contributor must understand before making a change.

## System map {#system-map}

| Part | Responsibility |
| --- | --- |
| Interface | Accepts user input and presents results |
| Core | Applies the project’s rules |
| Adapters | Connect external systems |

## Boundaries {#boundaries}

Name what the project deliberately does not own. Clear boundaries prevent documentation from promising more than the software provides.

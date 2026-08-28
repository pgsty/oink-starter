---
title: Configuration
description: Rassembler les clés prises en charge, leurs valeurs par défaut et des exemples.
weight: 10
---

Remplacez ce petit tableau par la véritable surface de configuration publique de votre projet.

| Clé | Type | Défaut | Signification |
| --- | --- | --- | --- |
| `listen` | chaîne | `127.0.0.1:8080` | Adresse du serveur local |
| `log_level` | chaîne | `info` | Niveau minimal des journaux |
| `read_only` | booléen | `false` | Désactive les opérations qui modifient l’état |

## Exemple {#example}

```yaml
listen: 0.0.0.0:8080
log_level: debug
read_only: true
```

Documentez la validation et la priorité à côté des clés, pas dans un guide séparé et difficile à trouver.

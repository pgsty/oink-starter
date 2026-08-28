---
title: Comprendre la structure
description: Identifier les quelques fichiers qui gèrent configuration, contenu et déploiement.
book_kind: chapter
book_number: 2
weight: 20
---

Le modèle place chaque responsabilité dans un endroit évident.

## La carte {#map}

```text
hugo.yaml          identité, langues et intégrations facultatives
data/home/         une page d’accueil compacte par langue
content/blog/      articles, conception et versions
content/docs/      l’arborescence documentaire en quatre parties
content/book/      ce tutoriel séquentiel
.github/workflows/ déploiement GitHub Pages et Cloudflare Pages
```

## La navigation suit le contenu {#navigation}

Le front matter `menus.main` de chaque racine crée la navigation supérieure et ses menus. L’arborescence sous Docs et Livre crée leurs barres latérales.

## Les traductions restent côte à côte {#translations}

L’anglais utilise `.md`, le chinois `.zh.md` et le français `.fr.md`. Conservez-les ensemble avec les mêmes identifiants explicites de titres.

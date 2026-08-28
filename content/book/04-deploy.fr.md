---
title: Publier le site
description: Utiliser l’un des workflows fournis et vérifier les routes réellement déployées.
book_kind: chapter
book_number: 4
weight: 40
---

Le dossier `public/` généré est un site statique. Le dépôt fournit deux chemins de déploiement indépendants.

## GitHub Pages {#github-pages}

Dans les paramètres du dépôt, choisissez **Pages → Source → GitHub Actions**. Un envoi sur `main` exécute `.github/workflows/github-pages.yaml` et calcule automatiquement le bon sous-chemin du dépôt.

## Cloudflare Pages {#cloudflare-pages}

Créez un projet Pages en Direct Upload, puis ajoutez `CLOUDFLARE_ACCOUNT_ID` et `CLOUDFLARE_API_TOKEN` comme secrets. Définissez la variable `CLOUDFLARE_PAGES_ENABLED` à `true` pour les déploiements automatiques. Le nom du projet reprend celui du dépôt, sauf surcharge par `CLOUDFLARE_PROJECT_NAME`.

## Vérifier la production {#verify-production}

Ouvrez `/`, `/zh/` et `/fr/`, puis une route Blog, Docs et Livre dans chaque langue. Vérifiez la recherche, le changement de langue, le mode sombre et une largeur mobile étroite.

> [!IMPORTANT]
> Une construction locale réussie, un commit envoyé, un workflow vert et un site public correct sont quatre contrôles distincts.

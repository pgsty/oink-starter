---
title: Prévisualiser le site
description: Cloner le dépôt et ouvrir l’accueil local en trois commandes.
book_kind: chapter
book_number: 1
weight: 10
---

OINK Starter est un site Hugo Module. Git télécharge les sources, Go résout la version épinglée du thème et Hugo construit l’ensemble.

## Prérequis {#prerequisites}

Installez Git, Go 1.27 ou plus récent et Hugo Extended 0.165.0 ou plus récent. Le mot `extended` doit apparaître dans `hugo version`.

## Trois commandes {#three-commands}

```bash
git clone https://github.com/pgsty/oink-starter.git
cd oink-starter
hugo server
```

Ouvrez <http://localhost:1313/>. Le chinois se trouve sous `/zh/` et le français sous `/fr/`.

## Première preuve {#first-proof}

Modifiez une phrase dans `data/home/en.yaml` et vérifiez que le navigateur se recharge. Votre boucle d’édition fonctionne.

---
title: Ajouter une page de documentation
description: Créer une page, la placer dans la barre latérale et la relier.
weight: 20
---

Dans OINK, l’arborescence du contenu devient la barre latérale. Un nouveau fichier Markdown crée une nouvelle page.

## Créer le fichier {#create}

```markdown
---
title: Nouvelle capacité
description: Ce que fait cette capacité.
weight: 30
---

Expliquez la capacité ici.
```

Enregistrez-le sous `content/docs/reference/new-capability.md`.

## Ajouter les traductions {#translations}

Créez `new-capability.zh.md` et `new-capability.fr.md` à côté. Gardez les identifiants explicites des titres alignés entre les langues.

## Prévisualiser {#preview}

Lancez `hugo server`, ouvrez la nouvelle page et utilisez le sélecteur de langue pour vérifier chaque traduction.

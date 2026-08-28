---
title: Add a Documentation Page
description: Create a page, place it in the sidebar, and link to it.
weight: 20
---

In OINK, the content tree is the documentation sidebar. A new Markdown file becomes a new page.

## Create the file {#create}

```markdown
---
title: New capability
description: What the capability does.
weight: 30
---

Explain the capability here.
```

Save it as `content/docs/reference/new-capability.md`.

## Add translations {#translations}

Create `new-capability.zh.md` and `new-capability.fr.md` beside it. Keep explicit heading IDs aligned across languages.

## Preview {#preview}

Run `hugo server`, open the new page, and use the language switcher to inspect every translation.

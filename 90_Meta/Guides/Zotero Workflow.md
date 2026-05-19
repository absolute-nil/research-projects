---
type: guide
tags:
  - guide
  - zotero
  - paper
---

# Zotero Workflow

The installed plugin is Zotero Desktop Connector. It imports citations, metadata, notes, and PDF annotations from Zotero. It expects Zotero to be running and works best with Better BibTeX citation keys. The plugin uses Nunjucks templates and supports persistent sections so your personal notes are not overwritten when you re-import.

## Import a Paper
1. Keep Zotero open.
2. In Obsidian, run `Zotero Desktop Connector: Import notes` or the configured import command.
3. Choose the Zotero item.
4. The note should be created in `02_Sources/Papers`.
5. Fill in `Why I Care`, `My Reaction`, and `Links I Should Make`.

## Citation Habit
Use the paper note as the citation object:

```md
This extends [[Scarcity and Voice AI — Generative Echo Chamber Effect]] into [[voice AI]] interaction.
```

## Re-Import Safety
The paper template uses `persist` blocks for `notes` and `annotations`. Your own text inside those blocks should survive re-imports from the same Zotero item.

## Minimum Paper Note
Every paper note should eventually answer:
- What is the one-sentence takeaway?
- Which project or card does it affect?
- What method or evidence does it contribute?
- What limitation matters for my work?

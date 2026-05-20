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
2. In Zotero Settings -> Advanced, make sure "Allow other applications on this computer to communicate with Zotero" is enabled.
3. In Obsidian, run `Zotero Desktop Connector: Import notes` or the configured import command.
4. Choose the Zotero item.
5. The note should be created in `02_Sources/Papers`.
6. Fill in `Why I Care`, `My Reaction`, and `Links I Should Make`.

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

## Current Integration Check
On 2026-05-19, Computer Use showed Zotero's "Allow other applications on this computer to communicate with Zotero" checkbox was unchecked. I did not change it because it grants local data-access communication to other apps. Enable it before using the Obsidian import command.

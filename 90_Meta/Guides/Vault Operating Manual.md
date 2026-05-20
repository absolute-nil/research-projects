---
type: guide
tags:
  - guide
  - meta
---

# Vault Operating Manual

## Principle
Do not organize by discipline folders. Your projects mix HCI, NLP, systems, theory, and writing, so project folders are the only place where project-specific material belongs.

## Folder Contract
| Folder | Use |
|---|---|
| `00_Inbox` | Temporary capture and imported material that has not been processed |
| `01_Projects` | Active project folders; each folder can contain studies, evals, pseudocode, meetings, and draft links |
| `02_Sources` | Papers, PDFs, drafts, and Zotero exports |
| `03_Cards` | Reusable atomic ideas, terms, claims, mechanisms, constructs, and theory notes |
| `03_Cards/Problems` | High-level research problems that connect projects without becoming discipline folders |
| `03_Cards/Lenses` | Reusable analytical lenses, theories, and frames |
| `03_Cards/Research_Questions` | Atomic research questions that can belong to multiple projects |
| `04_People` | People and collaborator notes |
| `04_Organizations` | Labs, funders, institutions, platforms, and public-interest organizations |
| `05_Daily` | Daily logs |
| `06_Meetings` | Cross-project meetings only; project-specific meetings can live in project folders |
| `07_Assets` | Images, attachments, exports |
| `08_Writing` | Thesis versions, CV, fellowships, rebuttals, paper revisions, and presentation outlines |
| `09_Trackers` | Dataview and Tasks dashboards that surface projects, action items, and software features |
| `90_Meta` | Guides, indexes, and vault-level dashboards |
| `99_Archive` | Old inactive material |

## Weekly Maintenance
1. Process `00_Inbox`.
2. For each active project, update only the project note and immediate next actions.
3. Update `tracker_status`, `last_reviewed`, and `next_milestone` in project frontmatter.
4. Convert any useful fragment into a `03_Cards` note.
5. Link papers and cards back to projects.

## Rules That Keep This Low Maintenance
- Use folders for where a note is born, not for every topic it touches.
- Use wikilinks for concepts and constructs.
- Use nested tags for note type and workflow state only.
- Avoid manually maintained cluster pages unless the page has an argument or synthesis.
- If a note belongs to one project, keep it in that project folder.
- If a note should help multiple projects, keep it in `03_Cards`.
- If a note is about a person or organization, keep it in `04_People` or `04_Organizations` and link it to projects/cards.
- Use problems, lenses, and research questions as graph surfaces; do not create HCI/NLP folders for mixed work.
- Use `08_Writing` for versioned artifacts and section-level paper work so draft evolution is auditable.
- Use tracker dashboards instead of manually maintained status pages.
- Put durable open questions in `03_Cards/Research_Questions`; use [[Open Questions Dashboard]] to review unanswered and partially answered questions.

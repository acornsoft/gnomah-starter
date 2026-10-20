# Gnomah SCHEMA

This file gives the rules for notes in this vault.
People and agents must obey these rules.
Agents must read this file first.

## 1. Rules

1. Write each note in Markdown.
2. Start each note with YAML front matter.
3. Put new notes in `00-Inbox/`.
4. Use tags to sort notes. Do not use deep folders for sorting.
5. Do not put passwords, tokens, or API keys in a note.
6. Do not edit files in `raw/`. Add new files only.
7. Add a line to `Log.md` after each work session.
8. Agents write drafts only. A person promotes a draft.

## 2. Front matter

Each note starts with this block:

```yaml
---
title: <short title>
type: climb-notes
status: draft
visibility: private
canopy: false
waypoint: Hold
tags:
  - bookmark
  - intake
  - para/resource
source_url: <link to the source, if any>
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

### Fields

| Field | Required | Value | Meaning |
|---|---|---|---|
| `title` | Yes | Text | The name of the note. |
| `type` | Yes | `climb-notes`, `analysis`, `work`, `adr`, `meta` | The kind of note. |
| `status` | Yes | `draft`, `active`, `done`, `archived` | `draft` until a person reviews the note. |
| `visibility` | Yes | `private`, `public` | `private` keeps the note out of exports. Default is `private`. |
| `canopy` | Yes | `false`, `true` | `true` lets the note go to a public view. Default is `false`. |
| `waypoint` | Yes | `Hold` | The stage of the note. `Hold` means "not started". |
| `summit` | No | Text, or empty | The result when the note is done. Leave it empty for drafts. |
| `tags` | Yes | List | Tags sort the notes. See section 3. |
| `source_url` | No | URL | The link to the source post or page. |
| `created` | Yes | Date | The date of the first version. |
| `updated` | Yes | Date | The date of the last change. |

Bookworm sets these values on each draft:
`status: draft`, `visibility: private`, `canopy: false`, `waypoint: Hold`.

## 3. Tags

1. Give each note one PARA tag.
2. Use `para/resource` if no other PARA tag applies.
3. Add topic tags as needed.

| Tag | Use |
|---|---|
| `para/project/<name>` | The note helps an active project with an end date. |
| `para/area/<name>` | The note helps an ongoing duty. |
| `para/resource` | The note is about a topic of interest. This is the default. |
| `para/archive` | The note is done or no longer used. |
| `bookmark` | The note came from a saved post. |
| `intake` | The note is new and is not sorted. |
| `src/x/<handle>` | The note came from this X account. |

## 4. File names

1. Use words joined by hyphens.
2. Do not use spaces.
3. Name Bookworm drafts `Climb-Notes-Draft-<slug>.md`.

## 5. Where notes go

| You have | Put it in |
|---|---|
| A new idea or a saved post | `00-Inbox/` |
| Research | `10-Analysis/` |
| An active job | `25-Work/` |
| A decision | `30-ADRs/` |
| A note that you decide to act on | `Climb-Notes/` |
| A source capture | `raw/` |
| An image or diagram | `assets/` |

# Gnomah starter

This repository is a starter for your own Gnomah.
Gnomah is a second brain in Markdown files and Git.
Bookworm writes your X bookmarks into it as draft notes.

## Before you use it

> **WARNING:** Keep this repository private. Your notes can show your work, clients, and plans.

> **WARNING:** Do not put passwords, tokens, or API keys in any file. Git keeps all history.

## Make your copy

1. Click **Use this template**.
2. Click **Create a new repository**.
3. Select your account as the owner.
4. Type `gnomah` as the name.
5. Select **Private**.
6. Click **Create repository**.

Your copy has no link to the history of this starter.

## Folders

| Path | Use |
|---|---|
| `00-Inbox/` | New notes go here. Bookworm writes drafts here. |
| `10-Analysis/` | Research and analysis notes. |
| `25-Work/` | One file for each active job. |
| `30-ADRs/` | One file for each decision. |
| `90-Meta/` | Notes about this vault. |
| `Climb-Notes/` | Notes that you decide to act on. |
| `raw/` | Source captures. Do not edit them. |
| `assets/` | Images and diagrams. |
| `SCHEMA.md` | Rules for notes and for agents. |
| `Index.md` | Map of the vault. |
| `Log.md` | Session log. Add to the end only. |

## Daily use

1. Merge the Bookworm draft pull requests on GitHub.
2. Type `git pull --rebase`.
3. Sort the notes in `00-Inbox/`.
4. Type `git add -A`.
5. Type `git commit -m "<what you changed>"`.
6. Type `git push`.

## Use with Obsidian (optional)

1. Start Obsidian.
2. Click **Open folder as vault**.
3. Select your local `gnomah` folder.
4. Install the community plugin **Git** by Vinzent.
5. Turn on **Pull on startup**.

Read `SCHEMA.md` before you add notes.

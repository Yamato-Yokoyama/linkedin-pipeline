# LinkedIn Pipeline

Yamato's LinkedIn content pipeline — managed with Markdown + Git + Notion MCP.

## Structure

- `inbox/` — Raw brain dumps from voice input
- `drafting/` — Posts being edited
- `scheduled/` — Ready to post
- `published/` — Archive
- `templates/` — 7 post templates (Technical / Build in Public / Germany×Tech / Event / Research / Mindset / Resource)
- `scripts/` — Automation (Notion sync, formatting)
- `assets/` — Images, GIFs, diagrams

## Workflow

1. iPad voice input → Notion Inbox
2. Pull to `inbox/` via Claude Code + Notion MCP
3. Edit in VSCode, move through `drafting/` → `scheduled/`
4. Publish to LinkedIn (manual)
5. Move to `published/`, update Notion status

## Notion Database

https://www.notion.so/da96da3143474c9b90ab3451f1647af6

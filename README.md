# LinkedIn Pipeline

A content pipeline for managing LinkedIn posts with Markdown, Git, and Notion MCP.

Built by [@Yamato-Yokoyama](https://github.com/Yamato-Yokoyama) — MSc Computational Linguistics student at the University of Tübingen, building toward a Product Engineer career in Germany.

## Why

Most content creators manage posts in ad-hoc notes apps that become unsearchable graveyards. This pipeline treats LinkedIn content like code: versioned, templated, and automated where possible — while keeping human judgment in the loop for voice and nuance.

Target audience of the posts:
- Japanese students interested in Computational Linguistics / NLP
- Japanese students considering studying abroad in Germany

## Stack

- **Markdown** — source of truth for all post content
- **Git** — version control and edit history
- **Notion** (via MCP) — dashboard view + mobile-friendly inbox
- **VSCode + Claude Code** — authoring and agentic automation
- **Python** — analytics scripts (post performance, category distribution)

## Structure
'''
linkedin-pipeline/
├── inbox/        # Raw brain dumps (iPad voice input → here)
├── drafting/     # Posts being edited
├── scheduled/    # Ready to post
├── published/    # Archive of published posts
├── templates/    # 7 post templates
├── scripts/      # Automation (Notion sync, formatting)
└── assets/       # Images, GIFs, diagrams
'''

Note: `inbox/`, `drafting/`, `scheduled/` are gitignored to keep work-in-progress private.

## Post Templates

1. **Technical Deep Dive** — Showing technical work with numbers
2. **Build in Public** — Progress updates on ongoing projects
3. **Germany × Tech** — Study-abroad and tech-life in Germany
4. **Event / Learning Report** — Takeaways from events and talks
5. **Research Note** — Paper reviews and concept breakdowns
6. **Mindset / Reflection** — Personal growth writing
7. **Resource Drop** — Downloadable PDFs and guides

## Workflow

1. Capture on mobile: voice input → Notion Inbox
2. Pull locally: Claude Code + Notion MCP → `inbox/`
3. Draft: edit in VSCode, promote to `drafting/` → `scheduled/`
4. Publish: post to LinkedIn (manual), then move to `published/`
5. Sync status back to Notion via MCP

## Notion Database

Schema and views managed via Notion MCP. Database URL is kept private (contains work-in-progress drafts).

## License

Content in `published/` is All Rights Reserved.
Scripts and templates are MIT licensed.
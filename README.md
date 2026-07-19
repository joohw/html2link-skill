# html2link Publish Skill

Publish agent-generated artifacts to [html2link.dev](https://html2link.dev) and return short browser-friendly links.

This repository contains the `html2link` Agent Skill for Codex, Claude Code, and other tools that support the open `SKILL.md` skill format. The older `html2link-publish` directory remains as a compatibility package.

Live html2link example: [html2link.dev/x/yeiEwrKr](https://html2link.dev/x/yeiEwrKr)

## What it does

- Publishes HTML reports, dashboards, and prototypes
- Publishes static site ZIPs with `index.html`
- Publishes PDF, Markdown, spreadsheet, DOCX, and PPTX artifacts
- Returns a short `https://html2link.dev/x/...` URL
- Supports updating or deleting an existing link when an `updateToken` is available

## Install

Copy the skill folder into your agent's skills directory.

Codex project installation:

```bash
git clone https://github.com/joohw/html2link-skill.git
mkdir -p .agents/skills
cp -R html2link-skill/html2link .agents/skills/html2link
```

Codex user installation:

```bash
mkdir -p ~/.agents/skills
cp -R html2link-skill/html2link ~/.agents/skills/html2link
```

Claude Code project installation:

```bash
mkdir -p .claude/skills
cp -R html2link-skill/html2link .claude/skills/html2link
```

## Use

Ask your agent:

```text
Use $html2link to publish this HTML report as a shareable link.
```

Or anonymously upload a file up to 1 MB directly:

```bash
curl --fail-with-body -F "file=@./report.html" https://html2link.dev/api/upload
```

The npm CLI adds authenticated uploads, stable-link updates, deletion, listing, and one-command Agent installation.

## Skill package

The skill lives at:

```text
html2link/SKILL.md
```

That folder is the portable package to install, mirror, or submit to skill directories.

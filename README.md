# html2link Publish Skill

Publish agent-generated artifacts to [html2link.dev](https://html2link.dev) and return short browser-friendly links.

This repository contains the `html2link-publish` Agent Skill for Codex, Claude Code, and other tools that support the open `SKILL.md` skill format.

Live html2link example: [html2link.dev/x/yeiEwrKr](https://html2link.dev/x/yeiEwrKr)

## What it does

- Publishes HTML reports, dashboards, and prototypes
- Publishes static site ZIPs with `index.html`
- Publishes PDF, Markdown, spreadsheet, DOCX, and PPTX artifacts
- Returns a short `https://html2link.dev/x/...` URL
- Supports updating or deleting an existing link when an `updateToken` is available

## Install

Copy the skill folder into your agent's skills directory:

```bash
git clone https://github.com/joohw/html2link-skill.git
cp -R html2link-skill/html2link-publish ~/.codex/skills/
```

For Claude Code or other compatible agents, copy the same `html2link-publish` folder into that tool's configured skills directory.

## Use

Ask your agent:

```text
Use $html2link-publish to publish this HTML report as a shareable link.
```

Or run the bundled script directly:

```bash
node html2link-publish/scripts/publish-html2link.mjs ./report.html
```

Set `HTML2LINK_API_TOKEN` for files above the anonymous 1 MB limit.

## Skill package

The skill lives at:

```text
html2link-publish/SKILL.md
```

That folder is the portable package to install, mirror, or submit to skill directories.

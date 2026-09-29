# KERN LABS Claude Code Setup

Reusable Claude Code baseline for frontend-heavy repositories.

## What it enforces
- targeted context usage to reduce token waste;
- strong UI/UX process and visual verification;
- React/TypeScript frontend conventions;
- minimal-diff repository discipline;
- durable project context through `CLAUDE.md` and `.claude/rules`;
- project-specific security guidance.

## Install official plugins
Open Claude Code and run the commands in `scripts/install-plugins.txt`.

The core set is:
- `frontend-design`
- `typescript-lsp`
- `code-simplifier`
- `security-guidance`
- `claude-md-management`
- `commit-commands`

## Use in every GitHub project
Copy `CLAUDE.md` and the `.claude/` directory into the repository root and commit them. Claude Code will then have the repository-specific operating instructions alongside the code.

Recommended structure:

```text
my-project/
├─ CLAUDE.md
├─ .claude/
│  ├─ rules/
│  │  ├─ ui-ux.md
│  │  ├─ frontend.md
│  │  ├─ code-quality.md
│  │  └─ project-memory.md
│  └─ claude-security-guidance.md
├─ src/
└─ package.json
```

## Important distinction: repo rules vs global rules
Putting these files in GitHub makes Claude use them when Claude Code is opened in that repository. It does not automatically affect unrelated repositories.

For a user-wide baseline, keep a concise global `~/.claude/CLAUDE.md`, then let each repository add its own rules. Avoid duplicating a large instruction set globally and per-project because that wastes context.

## Memory strategy
Use committed instructions for durable facts and conventions. Keep them concise and factual. A memory plugin can supplement this with session recall, but should not replace repository documentation or become the only source of architectural truth.

## UI workflow
For substantial frontend work, Claude should use the frontend-design capability when available, inspect current design context, implement, then verify the rendered result with browser tooling when available.

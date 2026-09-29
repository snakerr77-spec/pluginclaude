# Global Claude Code Preferences

Use repository `CLAUDE.md` and `.claude/rules` as the primary source of project-specific instructions.

Across projects:
- conserve context: search first, read only relevant files, avoid repeated reads;
- prefer minimal edits to existing files over unnecessary rewrites/new files;
- for frontend, prioritize high-quality responsive UI/UX and avoid generic AI aesthetics;
- visually verify meaningful UI changes when browser tooling is available;
- prefer React + TypeScript + Tailwind for new web frontends when no stack is specified;
- consult current documentation when API/library behavior is uncertain and documentation tooling is available;
- never expose or commit secrets;
- run relevant checks before claiming completion;
- keep explanations concise unless detail is requested.

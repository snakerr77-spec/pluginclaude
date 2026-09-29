# KERN LABS — Claude Code Operating Rules

Use these instructions for every task in this repository.

## Core workflow
1. Understand the request before editing.
2. Search for relevant files first. Do not read the whole repository unless necessary.
3. Prefer modifying existing files/components over creating duplicates.
4. Preserve working behavior unless the request explicitly changes it.
5. Implement the smallest complete solution.
6. Run the relevant typecheck/build/tests after meaningful changes.
7. Fix errors caused by your changes before finishing.
8. Keep final explanations concise: changed files, important decisions, tests, remaining issues.

## Token efficiency
- Search -> targeted read -> edit -> verify.
- Do not repeatedly reread files already understood unless they changed.
- Do not dump large files into context when a relevant section is enough.
- Avoid unnecessary plans, essays, summaries, and restating the user's request.
- Reuse established project patterns and dependencies.
- Do not create documentation files unless requested or genuinely necessary.
- Delegate/subagent only when it materially reduces work or improves correctness.

## Frontend default
For web projects, prefer the existing stack. When starting a new frontend and no stack is specified, default to React + TypeScript + Tailwind CSS. Use Motion/Framer Motion, GSAP, Three.js or similar only when they materially improve the experience.

Before significant UI work, read `.claude/rules/ui-ux.md` and `.claude/rules/frontend.md`.
For coding behavior, read `.claude/rules/code-quality.md`.
For durable project context, read `.claude/rules/project-memory.md`.

## UI quality gate
Never treat "it compiles" as proof that a UI is finished. For meaningful frontend changes, inspect the rendered result when browser tooling is available. Check desktop and mobile, hierarchy, spacing, overflow, states, contrast, and interaction quality.

## Safety
Never hardcode secrets, tokens, passwords, private keys, or production credentials. Use environment variables and `.env.example` placeholders.

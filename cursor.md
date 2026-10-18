# test-project

Student project for learning Cursor. Owner: **MD**.

Human notes for this folder. Cursor Agent reads **`AGENTS.md`** (and `.cursor/rules`) automatically — not this file.

## Tech stack

| Layer | Choice |
| --- | --- |
| Runtime | Node.js |
| Language | TypeScript |
| Framework | Next.js (App Router) |
| UI | React + `.tsx` |
| Packages | npm |

Stay on this stack. Do not add a second framework.

## Modes

| Mode | Use for | Edits files? |
| --- | --- | --- |
| **Agent** | Build, refactor, fix, run commands | Yes |
| **Ask** | Explain code, explore architecture | No |
| **Plan** | Multi-step work you want to review first | After you approve |
| **Debug** | Bugs that need runtime evidence | Yes |

- Open Agent panel: `Ctrl + I`
- Cycle modes: `Shift + Tab`
- New chats default to Agent
- Start a **new chat** when switching tasks

## How Agent should work

1. Follow `AGENTS.md` and existing Next.js / TypeScript code before changing anything.
2. Do the asked task only. No extra features, no drive-by refactors.
3. Prefer small, clear file changes. New app files should be `.ts` / `.tsx`.
4. After UI changes, verify in the browser when tools exist. Otherwise say what was not verified.
5. Commit only when MD explicitly asks. Never `git push` unless asked.
6. Never commit secrets (`.env`, keys, tokens).
7. Never skip git hooks. No force-push to `main`/`master`.

## Project layout

```
test-project/
  AGENTS.md              Cursor project guide
  cursor.md              this file (human notes)
  .cursor/rules/         always-on / file-specific rules
  app/                   Next.js App Router
  components/            reusable UI
  lib/                   helpers
  public/                static assets
  types/                 shared types
  package.json
  tsconfig.json
  next.config.ts
```

Also keep `.gitignore` and `.env.example` (never real secrets).

Dev: `npm run dev` · Build: `npm run build` · Lint: `npm run lint`

## Coding standards

- TypeScript strict; avoid `any`
- Server Components by default; `"use client"` only when needed
- Names: clear English, consistent with existing files
- Functions: short, one job
- Comments: only when the why is not obvious
- Errors: handle them; do not swallow exceptions
- Prefer editing existing files over creating new ones
- Do not add markdown docs unless asked

## Cursor extras

Project guide is already in `AGENTS.md`. Extra persistent rules go in `.cursor/rules/*.mdc`.

```yaml
---
description: Short purpose of the rule
alwaysApply: true
---
```

- One concern per rule, keep each rule short
- `alwaysApply: true` for project-wide habits
- `globs` for file-type rules (`**/*.{ts,tsx}`)

Cloud Agents, Automations, and third-party models depend on the Cursor plan. Free includes in-IDE Agent with limited usage.

## Language

MD often writes in Bangla / Banglish. Reply in the same language as the request. Keep code, filenames, and git messages in English.

## Git

- Commit only on request
- Message: 1–2 sentences, why not what
- No `--amend` unless MD asked and the commit is unpushed and created in this session

## Current status

- Stack is decided: **Node.js + TypeScript + Next.js**
- App files are not scaffolded yet — add the Next.js app when MD asks

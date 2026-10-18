# Project guide

Student repo for learning Cursor. Owner: **MD**.

`cursor.md` is a human notes file. This `AGENTS.md` is what Cursor Agent should follow.

## Tech stack

- **Runtime:** Node.js
- **Language:** TypeScript (strict). Do not add new `.js` / `.jsx` app files.
- **Framework:** Next.js (App Router)
- **UI:** React with TypeScript (`.tsx`)
- Package manager: npm unless a lockfile for another manager already exists

Do not add another backend framework, another UI framework, or Python. Stay on this stack.

## Context

- Do only what MD asked. No extra features, no drive-by refactors.
- Prefer editing existing files over creating new ones.
- After UI changes, verify in the browser when tools exist.

## Language

MD often writes in Bangla or Banglish. Reply in the same language as the request. Keep code, filenames, and git messages in English.

## Coding

- App Router: routes live under `app/`
- Server Components by default; add `"use client"` only when the browser is required
- Shared types in `types/` or colocated `*.ts` files — no `any` without a short comment
- Handle errors; do not swallow exceptions
- Short functions, one job; comments only when the why is not obvious

## Git

- Commit only when MD explicitly asks
- Never push unless asked
- Never commit secrets (`.env`, keys, tokens)
- Never skip hooks
- No force-push to `main` / `master`

## Layout

```
app/                 Next.js App Router (pages, layouts, API route handlers)
components/          reusable UI
lib/                 helpers, server utilities
public/              static assets
types/               shared TypeScript types
.cursor/rules/       Cursor rules
AGENTS.md            this guide
cursor.md            human notes
```

Keep `package.json`, `tsconfig.json`, `next.config.ts`, `.gitignore`, and `.env.example`. Never commit real `.env` values.

Scripts: `npm run dev`, `npm run build`, `npm run start`, `npm run lint`.

## Extra Cursor rules

File-specific rules live in `.cursor/rules/*.mdc`. Keep each rule short and one concern.

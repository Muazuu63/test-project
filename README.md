# test-project

Student Next.js app in TypeScript. Owner: **MD**.

বাংলায়: এটা Node.js + TypeScript + Next.js (App Router) প্রজেক্ট। Cursor Agent `AGENTS.md` ফলো করে। অ্যাপ এখনো স্ক্যাফোল্ড হয়নি।

## Tech stack

| Layer | Choice |
| --- | --- |
| Runtime | Node.js |
| Language | TypeScript (strict) |
| Framework | Next.js — App Router |
| UI | React (`.tsx`) |
| Packages | npm |

Stay on this stack. Do not add another framework.

## Status

- Cursor project guide: `AGENTS.md`
- Human Cursor notes: `cursor.md`
- `package.json` exists (placeholder). Next.js is **not** installed yet.
- App folders (`app/`, `components/`, …) will appear after scaffolding.

## Planned layout

```
test-project/
  README.md              this file
  AGENTS.md              Cursor Agent instructions
  cursor.md              human Cursor notes
  .cursor/rules/         project rules
  app/                   routes, layouts, route handlers
  components/            reusable UI
  lib/                   helpers
  public/                static assets
  types/                 shared TypeScript types
  package.json
  tsconfig.json
  next.config.ts
  .env.example
```

## Setup (after Next.js is added)

Requires Node.js 20+.

```bash
npm install
cp .env.example .env.local   # if env example exists; never commit real secrets
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

| Script | Command |
| --- | --- |
| Dev | `npm run dev` |
| Production build | `npm run build` |
| Start production | `npm run start` |
| Lint | `npm run lint` |

## Cursor

| File | Who reads it |
| --- | --- |
| `AGENTS.md` | Cursor Agent (automatic) |
| `.cursor/rules/*.mdc` | Cursor Agent (rules) |
| `cursor.md` | You — not loaded as Agent rules |
| `README.md` | Humans (and Agent when asked) |

Modes in Cursor: **Agent** (build), **Ask** (read-only), **Plan** (review first), **Debug**. Open the panel with `Ctrl + I`.

## Conventions

- New app files: `.ts` / `.tsx` only
- Server Components by default; `"use client"` only when the browser is required
- Do not commit `.env`, keys, or tokens
- Git commit/push only when MD asks

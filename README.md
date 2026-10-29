# Action Tracker

A single-page meeting action tracker. Actions are grouped by owner, with open/done counts and overdue items highlighted. Data is stored live in Supabase (project `task_tracker`), so every visitor sees the same list in real time.

## Deploy to Vercel

1. Import this repository into Vercel (New Project → import from GitHub).
2. No build step is required — Vercel will detect it as a static site ("Other" framework preset) and serve `index.html` as-is.
3. Click Deploy.

No environment variables are needed: the Supabase project URL and publishable key are embedded client-side in `index.html` (they are safe to expose — row-level security policies control access, not secrecy of the key).

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app — markup, styles and script in one file |
| `vercel.json` | Disables trailing slashes / enables clean URLs on Vercel |

## Local preview

Open `index.html` directly in a browser, or serve it locally, e.g.:

```bash
npx serve .
```

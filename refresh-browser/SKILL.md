---
name: refresh-browser
description: Kill the dev server, wipe the cache, and restart fresh. Use when something looks wrong and you suspect stale cache, after fixing a bug for a clean restart, or when the dev server feels stuck.
allowed-tools: Bash
---

# refresh-browser

Use this skill when you need a clean slate — kill the dev server, wipe the cache, and restart fresh.

## When to invoke

- Something looks wrong and you suspect stale cache
- You just fixed a bug and want a clean restart to confirm it
- The dev server feels stuck or behaving unexpectedly

## Steps to follow

### Step 1 — Kill the dev server
- Find and kill any process running on common dev ports: 3000, 5173, 4321, 8080
- Confirm: "Dev server stopped."

### Step 2 — Clear the cache
- Delete common cache directories: `.next/`, `.nuxt/`, `dist/`, `.vite/`, `.cache/`, `node_modules/.cache/`
- Confirm: "Cache cleared."

### Step 3 — Restart the dev server
- Detect the project type and run the right command:
  - Next.js / Vite / Astro → `npm run dev`
  - If unclear, ask the user
- Wait until the server is ready (watch for "ready", "listening", or "localhost" in output)
- Confirm: "Server is back up at [url]. Ready to go."

## Notes
- If the server fails to start, report the error and stop.
- If no dev server is running, skip step 1 and go straight to clearing cache.

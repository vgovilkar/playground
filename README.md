# Playground - Agentic Coding Experiments

Host for basic webapps with GitHub accessible URL.

## GitHub Pages URL (after enabling)

Once Pages enabled: **https://vgovilkar.github.io/playground/**

- Each app in `/apps/<name>/` -> URL `/playground/apps/<name>/`
- Example: `/apps/hello/` -> `https://vgovilkar.github.io/playground/apps/hello/`

## Enable Pages (1 click - do this in browser)

Your fine-grained token doesn't have Pages permission, so enable manually:

1. Open https://github.com/vgovilkar/playground/settings/pages
2. Under **Build and deployment** -> Source: **Deploy from a branch**
3. Branch: `main` / root (`/`)
4. Save -> Wait 1 min -> URL live at https://vgovilkar.github.io/playground/

Alternatively: Source: GitHub Actions if you want auto build.

## Vibe coding from phone

On old MacBook agent (Tailscale 100.x):
```
in playground repo, create new app 'todo' with React todo list, push to main
```
Agent will: edit `apps/todo/index.html` + `git push` -> auto live on GitHub Pages URL.

For dynamic apps (needs backend):
- Keep code in playground repo
- Agent deploys on MacBook via `docker compose up -d` and exposes via Tailscale Funnel
- URL: `https://your-tail-funnel.ts.net` or `http://100.x.y.z:3000`

## Structure

- `/index.html` - playground hub
- `/apps/<app>/index.html` - each experiment
- Push to main = auto deploy via Pages

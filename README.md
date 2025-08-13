# To‑Do List — Deployable Single‑File App

A lightweight, offline‑first To‑Do app (LocalStorage, drag‑and‑drop, filters, import/export) packaged for simple static hosting on **Vercel**, **Netlify**, or **GitHub Pages**.

## Files
- `index.html` — the entire app in one file
- `vercel.json` — static routing for Vercel
- `netlify.toml` — static site config for Netlify

---

## Option A — Deploy to Vercel (fastest)

1) Install the CLI (once):
```bash
npm i -g vercel
```

2) From this folder, run:
```bash
vercel --prod
```
- When prompted for project settings, accept defaults.
- Vercel will return a public URL immediately after deployment.

> Want one‑click web deploy? Create a GitHub repo with these files and press "Deploy" on vercel.com, selecting that repo.

---

## Option B — Deploy to Netlify

### CLI
1) Install CLI:
```bash
npm i -g netlify-cli
```
2) Login and deploy:
```bash
netlify login
netlify deploy --prod --dir .
```
Netlify will return your live URL.

### Web UI
1) Drag & drop the folder on https://app.netlify.com/drop to get an instant URL.

---

## Option C — GitHub Pages

1) Create a new repo and push these files:
```bash
git init
git add .
git commit -m "todo app"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

2) In repo Settings → Pages:
- **Source:** Deploy from a branch
- **Branch:** `main` / root
- Save. Your site will be live at:
```
https://<your-username>.github.io/<repo-name>/
```

---

## Optional: Custom Domain
- **Vercel:** add your domain in Project → Settings → Domains, update DNS to the shown A/ALIAS/CNAME.
- **Netlify:** Site settings → Domain management → Add custom domain, then follow DNS instructions.

---

## Notes
- This is a static site; no server is required.
- Data is stored in the browser’s LocalStorage (per‑device).
- To reset, use **Purge all** inside the app (irreversible).

Enjoy! 🎯

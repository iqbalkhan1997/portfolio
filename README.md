# Portfolio site

A static, no-build-step portfolio site (`index.html` + `assets/style.css`) — ready to push to GitHub and serve for free with GitHub Pages.

GitHub username: **iqbalkhan1997** · LinkedIn and GitHub links in the Contact section are already filled in.

## Before publishing — still open

- [ ] Decide whether to link an actual resume file from the "Experience" section. **The resume PDF is deliberately NOT included in this folder** — it has your personal phone number on it, and anything in a public GitHub Pages repo is public forever (including old commits). If you want a downloadable resume link on the site, use a version with the phone number removed, or link to your LinkedIn profile instead.
- [ ] Optional: add real screenshots (redacted/dummy-data dashboards, architecture diagrams) into a new `assets/images/` folder and reference them from the case studies.

## Publishing checklist

This folder is already a local git repo with commits — publishing is just:

1. **Create the GitHub repo** (on github.com, not locally) — pick one:
   - Personal top-level site at `https://iqbalkhan1997.github.io`: create a repo named **exactly** `iqbalkhan1997.github.io`.
   - Project-style URL at `https://iqbalkhan1997.github.io/portfolio`: create a repo named `portfolio` (or anything you like).
   - Leave it empty — don't add a README/license from GitHub's UI, since this folder already has one.

2. **Connect and push** (run from inside this folder, on whichever machine/server you're pushing from):
   ```bash
   git remote add origin https://github.com/iqbalkhan1997/<repo-name>.git
   git branch -M main
   git push -u origin main
   ```
   Replace `<repo-name>` with whichever name you used in step 1 (`iqbalkhan1997.github.io` or `portfolio`).

   First push will prompt for GitHub login — a **personal access token**, not your account password, since GitHub retired password auth for git operations. Generate one at github.com → Settings → Developer settings → Personal access tokens (`repo` scope is enough), or use `gh auth login` if the GitHub CLI is installed on that machine, or set up an SSH key there and use `git@github.com:iqbalkhan1997/<repo-name>.git` as the remote instead.

3. **Enable Pages**: on the repo's GitHub page → **Settings → Pages** → under "Build and deployment", set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)** → Save.

4. **Wait ~1 minute**, then visit:
   - `https://iqbalkhan1997.github.io` (special repo name), or
   - `https://iqbalkhan1997.github.io/<repo-name>` (project-style).

5. **Put the link where recruiters will see it**: LinkedIn Featured section, LinkedIn About section, and the contact line of your resume.

## Optional later: custom domain

Buy a domain (Namecheap/Cloudflare, ~$10–12/yr), then:
1. Add a file named `CNAME` (no extension) to this folder containing just your domain, e.g. `iqbalkhan.dev`.
2. At your domain registrar, add a `CNAME` record pointing your domain (or `www`) at `iqbalkhan1997.github.io`.
3. Back in repo Settings → Pages, enter the custom domain and check **Enforce HTTPS** once it's available (can take a few minutes to a few hours after DNS propagates).

## Local preview

Just open `index.html` directly in a browser — no server or build step needed. To preview with a local server instead (optional):
Not Needed
```bash
python3 -m http.server 8000
```
then visit `http://localhost:8000`.

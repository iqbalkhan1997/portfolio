# Ghouri Iqbal Khan — Portfolio

Live at: **https://iqbalkhan1997.github.io/portfolio**

A single-page portfolio site — case studies, skills, experience, and contact — built as plain HTML/CSS with no framework or build step, hosted free on GitHub Pages.

## What's here

```
index.html              The entire site (one page, anchor-linked sections)
assets/style.css         All styling
assets/Ghouri_Iqbal_Khan-Resume.pdf   Downloadable resume (phone number removed —
                                       this repo is public, so personal contact
                                       details beyond email/location are kept off it)
```

## Sections (in `index.html`, top to bottom)

- **Hero** — headline, tagline, and the "See the work / Download Resume / Get in touch" buttons.
- **`#work`** — Case studies: the FinOps Platform (FinOps/Inventory/Provisioning tiles) and the multi-cloud billing → ClickHouse pipeline, plus a placeholder for a future one.
- **`#skills`** — Skill category cards, kept in sync with the resume.
- **`#experience`** — Full bullet list from the current role, matching the resume's Professional Experience section.
- **`#contact`** — Email, LinkedIn, GitHub.

## Making changes

Edit `index.html` and/or `assets/style.css` directly — it's plain markup, no build step. Preview locally by just opening `index.html` in a browser, or serve it properly with:
```bash
python3 -m http.server 8000
```
then visit `http://localhost:8000`.

To publish a change: commit, then `git push`. GitHub Pages picks up anything pushed to `main` automatically — usually live within a minute, no other steps needed.

## Keeping content in sync

The Skills and Experience sections are meant to mirror the resume — when the resume changes, check whether this site needs the same update (new skill, new bullet, a reworded project). There's no automated link between the two files; it's a manual check.

## Optional later: custom domain

Buy a domain (Namecheap/Cloudflare, ~$10–12/yr), then:
1. Add a file named `CNAME` (no extension) to this folder containing just your domain, e.g. `iqbalkhan.dev`.
2. At your domain registrar, add a `CNAME` record pointing your domain (or `www`) at `iqbalkhan1997.github.io`.
3. In the repo's **Settings → Pages**, enter the custom domain, add the TXT record it gives you at your registrar for verification, then check **Enforce HTTPS** once available.

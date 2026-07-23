# pallavi-resume

Personal portfolio / résumé site for **Pallavi Kailas** — a single static page (`index.html`, no build step) styled as an engineering drawing: a dimensioned career timeline, a revision-history table for work experience, drawing-sheet cards for projects (each linking to its GitHub repo), and a bill-of-materials table for technical skills.

**Live site:** `https://pallavikailas.github.io/pallavi-resume/` (once Pages is enabled — see below)

## Structure

```
.
├── index.html                      # the whole site — plain HTML/CSS/JS, no dependencies to install
├── Pallavi_Kailas_Resume.pdf       # linked from the "download résumé" button
├── .nojekyll                       # tells GitHub Pages to serve files as-is (skip Jekyll processing)
└── .github/workflows/deploy.yml    # GitHub Actions workflow that deploys this repo to GitHub Pages on every push to main
```

## Deploying

1. Push this repo to GitHub as `pallavikailas/pallavi-resume`.
2. In the repo, go to **Settings → Pages** and set **Source** to **GitHub Actions** (one-time setup).
3. Push to `main` — the included workflow (`.github/workflows/deploy.yml`) builds and publishes the site automatically. Check the **Actions** tab for progress; the live URL also appears there once the deploy step finishes.

## Editing

Everything is in `index.html` — text, styles, and the inline SVG timeline. No npm install, no build tools. Open it directly in a browser to preview changes locally before pushing.

### Project links

The project cards link to `github.com/pallavikailas/<repo-name>`. Update the `href` on each `<a class="sheet">` in `index.html` if any of your actual repo names differ from:
- `fairlens`
- `sorting-algorithm-visualiser`
- `bilingformer`
- `legal-ai-assistant`

### Updating the résumé PDF

Replace `Pallavi_Kailas_Resume.pdf` with a new file of the same name, or update the `href` in the two "download résumé" links in `index.html` if you rename it.

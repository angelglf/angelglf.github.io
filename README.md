# Academic website — Ángel García-Lascurain Fernández

A modern, dependency-free static site (plain HTML + CSS, no build step). Three pages: `index.html` (About), `research.html`, `cv.html`, with the CV PDF in `assets/`.

## Publish on GitHub Pages (about 5 minutes)

1. Create a GitHub account (or sign in) and create a new **public** repository named `<username>.github.io` — for example `agarcialascurain.github.io`. Using that exact name makes the site live at `https://<username>.github.io/`.
2. Upload everything in this folder to the repository (on the repo page: *Add file → Upload files*, drag the files and the `assets` folder in, then *Commit changes*).
3. Go to **Settings → Pages**, and under *Build and deployment* make sure Source is "Deploy from a branch" with branch `main` and folder `/ (root)`.
4. Wait a minute or two — the site will be live at `https://<username>.github.io/`.

To update the site later, just edit or re-upload files in the repo; changes go live within a couple of minutes. To replace the CV, overwrite `assets/Garcia-Lascurain_CV.pdf` with the new PDF (keep the same filename and no other change is needed).

### Custom domain (optional)

Buy a domain (e.g. `angelgarcialascurain.com`), then in the repo go to *Settings → Pages → Custom domain*, enter the domain, and follow GitHub's DNS instructions at your registrar (an `A`/`CNAME` record). GitHub provides free HTTPS.

## Things still to fill in

- **Photo**: add a square-ish portrait as `assets/photo.jpg`. Until then the site shows a styled "ÁG" monogram automatically.
- **LinkedIn**: the LinkedIn chip on the home page currently points to `https://www.linkedin.com/` — replace it with the real profile URL in `index.html`.
- **Job market paper**: if one of the working papers becomes the JMP, change its label in `research.html` (the `meta` line) to "Job market paper".
- **Paper drafts**: the two current working papers say "Draft available on request" — swap in PDF links when drafts are public (put PDFs in `assets/` and link them from the paper cards).
- The two Duke-era projects still link to the old Google Drive files; consider moving those PDFs into `assets/` too so nothing depends on Drive permissions.

## Design notes

- Styled after the classic "Academic" theme (centered profile hero, blue accent, interests/education columns).
- Colors are defined at the top of `style.css` (`:root` for light mode, `[data-theme="dark"]` for dark mode) — change `--accent` in both to re-theme the whole site.
- Light/dark mode: the moon button in the nav toggles it; the site also follows the visitor's system preference by default.
- Font: Inter, loaded from Google Fonts.

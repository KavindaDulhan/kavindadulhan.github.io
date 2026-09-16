# kavindadulhan.github.io

Personal academic site, built as plain HTML/CSS (no build step, no dependencies).

## Preview locally

Open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publish on GitHub Pages

1. Create a new **public** repository on GitHub named exactly `kavindadulhan.github.io`
   under the `KavindaDulhan` account — done.
2. Push these files to the `main` branch:

   ```bash
   cd kavinda-site
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/KavindaDulhan/kavindadulhan.github.io.git
   git push -u origin main
   ```

3. In the repo on GitHub: **Settings → Pages → Build and deployment → Source** = `Deploy from a branch`,
   branch `main`, folder `/ (root)`. Save.
4. Your site will be live at `https://<your-username>.github.io/` within a minute or two.

## Before you push — things to fill in

Search the codebase for `TODO` comments in `index.html` and replace the placeholder Google
Scholar and LinkedIn links with your real URLs (GitHub is already filled in). Also:

- `assets/CV.pdf` is the CV generated earlier in this conversation — swap in a newer version
  whenever you update it (keep the filename `CV.pdf` so the link on the site keeps working).
- The dates and one-line descriptions under **News** and **Research** were pulled from your CV
  and chat history — proofread them, and update the "Under review" status once the NeurIPS
  decision comes back.
- `footer` in `index.html` links to `github.com/kavindadulhan/kavindadulhan.github.io` as the
  site's own source — update this if you use a different username.

## Structure

```
.
├── index.html      # all content lives here
├── style.css        # all styling
├── assets/
│   └── CV.pdf
└── README.md
```

No JavaScript, no build tools, no external dependencies beyond two Google Fonts
(Fraunces, Source Sans 3) loaded via `<link>` in the `<head>`.

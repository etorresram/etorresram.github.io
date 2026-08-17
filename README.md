# etorresram.github.io

Personal academic website for Eric Torres. Plain static HTML and CSS — no build step,
no dependencies, no JavaScript.

## Files

```
index.html          About, research interests, education, contact
research.html       Dissertation + IDB projects + data/code
publications.html   Publications and awards
beyond.html         Guitar, surfing
assets/css/style.css
assets/img/eric-torres.jpg
files/              CV and paper PDFs
.nojekyll           Tells GitHub Pages to serve the files as-is
```

## Publishing to GitHub Pages

The site is designed to live at `https://etorresram.github.io`. From this `site/` directory:

```bash
git init
git add .
git commit -m "Personal website"
git branch -M main
git remote add origin https://github.com/etorresram/etorresram.github.io.git
git push -u origin main
```

Create the repository `etorresram.github.io` on GitHub first (public). For a
`username.github.io` repository, Pages publishes automatically from the default branch —
no settings change is needed. Otherwise, go to **Settings → Pages** and set the source to
the `main` branch, root folder.

The site is live a minute or two after the push.

## Updating

Edit the HTML directly and push. To add a paper: drop the PDF in `files/`, then copy an
existing `<div class="entry">` block in `research.html` and change the text. To add a
publication: copy an `<li>` inside the relevant `<ol class="reflist">` in
`publications.html` — the reference numbers renumber themselves.

Colors are the CSS variables at the top of `assets/css/style.css`; dark mode follows the
reader's system setting and is defined in the same block. The page width and the split
between the left rail and the text column are the `.page` grid rule just below.

Each page repeats the same `<header class="sitehead">` and `<aside class="rail">` blocks.
When you change either one (a new nav link, a new job title), change it in all four HTML
files.

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

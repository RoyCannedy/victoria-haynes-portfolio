# Victoria Haynes Portfolio

A fully self-contained static site. No build step, no dependencies, no Wix.
Every image, font, and the resume PDF live in this repo.

Live at https://victoriashaynes.github.io/victoria-haynes-portfolio/

## Two versions

The **main site** is at the root: a normal scrolling portfolio. This is the one
in use.

The **board** version lives in `board/` — the same content as a draggable pin
board. It is kept but no longer linked from anywhere, so nothing points at it
unless you share the URL directly.

Each folder is self-contained: its own `css/`, `js/`, `assets/`, `fonts/`, and
page files. Shared pages (resume, projects, contact) exist in both, so a copy
change needs making in both places.

## Pages
- index.html — home: hero with her bio, stats that count up, project tiles
- resume.html — full resume, PDF preview and download
- merchandise.html / buying.html / flats.html / photography.html — project pages
- contact.html

## Editing
- Text: edit the HTML directly, it is plain HTML.
- Colors and fonts: tokenized at the top of `css/style.css`.
- New merch designs: drop a JPG in `assets/merch/` and copy a figure block in
  `merchandise.html`.
- Replacing the resume: swap `assets/victoria-haynes-resume.pdf`, then
  regenerate the on-page preview with
  `qlmanage -t -s 1600 -o . victoria-haynes-resume.pdf` and rename the output to
  `assets/resume-preview.png`.

## Publishing
GitHub Pages serves `main` from the repo root. Push and it deploys; allow a
minute, and hard-refresh since CSS caches for 10 minutes.

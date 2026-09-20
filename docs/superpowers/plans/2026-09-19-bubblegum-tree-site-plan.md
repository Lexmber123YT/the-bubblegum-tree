# Implementation plan — The Bubblegum Tree site (first draft)

Spec: `docs/superpowers/specs/2026-09-19-bubblegum-tree-site-design.md`. William approved the design in chat 2026-09-19 and asked for a first version to show Brenda the next day. Placeholders are acceptable where content is still to come.

## Tasks

1. **Assets** — done. Cover at 600/1000/1600 jpg+webp, og-image, six trailer stills cropped above the caption band. Add `favicon.svg` (hand-drawn tree mark) and two in-palette placeholder SVGs (author photo, book photo).
2. **Stylesheet** `assets/styles.css` — tokens from the sampled palette, Fredoka + Lora, paper grain, wavy dividers, tilted cover, buttons, responsive grid, phone-first.
3. **Home** `index.html` — hero, about the story, trailer, quote strip, meet Brenda teaser, buy strip, footer.
4. **Book page** `the-bubblegum-tree.html` — summary, what Troy learns, where it came from, both videos, gallery, details, buy.
5. **About** `about.html` — photo placeholder, bio, note from Brenda (flagged), contact.
6. **Repo hygiene** — `README.md` (how to update, how to add a book), `CONTENT-TO-CONFIRM.md` (every sentence Brenda should approve, every placeholder to replace), `.gitignore`, `.nojekyll`.
7. **Verify** — serve locally, screenshot phone + desktop, check console/network, click links.
8. **Publish** — `git init`, commit, `gh repo create` public, push, enable Pages, confirm the live URL loads. `noindex` stays on until Brenda approves.
9. **Vault** — hub note `01 Projects/Bubblegum Tree Site.md`, register in `vault_staleness.py`, exclude the folder from the MINERVA repo's `.gitignore`.
10. **Memory** — update `mom-childrens-book-website.md` with the live URL and what's pending.

## Not in this draft

Custom domain, contact form, newsletter, second book, analytics.

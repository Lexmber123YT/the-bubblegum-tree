# The Bubblegum Tree — author site

Website for *The Bubblegum Tree* by Brenda Oney Morris (Christian Faith Publishing, 2026). Plain HTML and CSS, no build step, hosted on GitHub Pages.

## Files

| File | What |
|---|---|
| `index.html` | Home |
| `the-bubblegum-tree.html` | The book page |
| `about.html` | About Brenda |
| `assets/styles.css` | All styles. Colors are variables at the top. |
| `assets/img/` | Optimized images. `cover-*.jpg/webp` from the publisher's cover file; `scene-*.jpg/webp` are stills from the trailer. |
| `assets/src/` | Original source files (gitignored). |
| `CONTENT-TO-CONFIRM.md` | Everything Brenda should check or supply. |
| `docs/superpowers/` | Design spec and plan. |

## Updating

Edit the HTML, commit, push. GitHub Pages redeploys in about a minute.

The site went public (search engines allowed) on 2026-10-16. `sitemap.xml` lists the three pages; add any new page to it.

## Adding a book later

1. Copy `the-bubblegum-tree.html` to a new file and swap the content and images.
2. Add a card for it on `index.html` and a nav entry on every page.
3. Optionally rename the "The Book" nav item to "Books" and make it a small list page.

## Custom domain later

Add a `CNAME` file containing the domain, and point the domain's DNS at GitHub Pages. GitHub's docs: Settings → Pages → Custom domain.

## Local preview

```
python -m http.server 8765
```

Then open http://127.0.0.1:8765/.

# The Bubblegum Tree — author/book website design

Date: 2026-09-19. Approved in chat by William (site owner's son; the author is his mother, Brenda Oney Morris).

## Purpose

A display and information site for the children's book *The Bubblegum Tree* by Brenda Oney Morris (Christian Faith Publishing, 2026). It shows the book, explains what it is about and what inspired it, embeds the two existing YouTube videos, shows photos, and links to every store that sells it. It does not sell anything itself.

It must be built so a second book can be added later without a rebuild, but the first version is about this one book only.

## Hard requirements

1. **Must not look AI-generated or template-made.** This is the author's top concern. No purple/blue gradients, no glassmorphism, no three-equal-feature-card grids, no icon rows, no generic slogans, no emoji bullets. Palette and mood come from the cover art. Copy is drafted from Brenda's own interview words and she has final edit.
2. All information present: story summary, themes, inspiration, both videos, gallery, buy links, author bio, contact.
3. Looks right on a phone first. Most visitors will arrive from Facebook on a phone.
4. Zero ongoing cost. Free hosting. The only future cost is an optional custom domain (~$12/yr), a decision for William and Brenda.
5. Updates go through William to Claude. No CMS, no admin screen.

## Approach (chosen)

Plain hand-written HTML and CSS, no framework, no build step, no JavaScript beyond nothing (YouTube embeds are iframes). Hosted on GitHub Pages from a public repo under William's GitHub account (`Lexmber123YT`). Free `github.io` address first; custom domain later via a `CNAME` file.

Rejected: Squarespace/Wix (monthly rent, she won't edit it herself anyway); a static-site generator (adds a toolchain for one or two books); a bolt-on editor (more to break).

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home: hero with cover, one-line pitch, two buttons (Buy, Watch the trailer), short "about the story", trailer embed, a grandpa quote strip, "Meet Brenda" teaser, buy strip, footer |
| `the-bubblegum-tree.html` | The book: full summary, what Troy learns, where the idea came from, both videos, "a peek inside" gallery, book details (publisher, formats, prices, ISBNs), buy section |
| `about.html` | About Brenda: photo, bio, "a note from Brenda" in her voice (flagged for her edit), contact link |
| `assets/styles.css` | One stylesheet |
| `assets/img/` | Optimized images (cover at 600/1000/1600 px in jpg + webp, og-image, six illustration stills cropped from the trailer, favicon svg) |
| `CNAME` | Added later when a domain is chosen |

Navigation on every page: Home · The Book · About Brenda · Where to Buy (anchor to the buy strip). A second book later becomes a "Books" entry; the book page is the template.

## Visual design

- **Palette from the cover** (sampled): sky `#9ec6db` / light sky `#e0f3f9`, grass `#8dbe8a` / `#a1cb90`, leaf `#8bab77`, trunk `#cd936b`, coral title `#e29182` (deepened to `#d9634e` for text contrast), overalls navy `#384c63`. Page background is warm cream paper `#fbf6ea`; body text warm dark brown `#3b2a1e`. Gumball accents (soft pink, butter yellow, lilac, mint) used only as small dots and underline flourishes.
- **Fonts:** Fredoka (rounded, storybook) for headings and buttons; Lora (warm serif) for body. Google Fonts.
- **Texture and hand-made feel:** subtle paper grain overlay (inline SVG noise, very low opacity), wavy meadow-shaped section edges (inline SVG), the cover shown slightly tilted with a soft shadow like a book on a table, a hand-drawn-style tree mark as the logo/favicon, scattered gumball dots as decoration. Asymmetric layouts; not everything centered.
- **Buttons:** rounded, coral primary, navy secondary, plain text labels for retailers (no retailer logos).
- **Images:** real cover art and real stills from the book's own trailer. Author photo and book photos are placeholders (styled, in-palette, labelled "photo coming") until William supplies them.
- **Video:** YouTube iframes via `youtube-nocookie.com`, lazy-loaded, 16:9 responsive.

## Content sources

- Interview transcript (Global Book Network, 2026-07-27) — story details, inspiration, themes, family background.
- CFP press release (PR.com 973451, 2026-07-17) — official blurb, bio, retailer list.
- CFP bookstore page — official one-paragraph blurb, cover image, ISBNs.
- Barnes & Noble listing — formats and prices (hardcover $34.95, paperback $21.95, eBook $9.99).

Everything drafted "in Brenda's voice" is listed in `CONTENT-TO-CONFIRM.md` for her review.

## Buy links (verified 2026-09-19 unless noted)

- Amazon: `https://www.amazon.com/dp/B0GZ1BVCPR` (verified)
- Barnes & Noble: `https://www.barnesandnoble.com/w/the-bubblegum-tree-brenda-oney-morris/1150055216?ean=9798894285047` (verified)
- Apple Books: `https://itunes.apple.com/us/book/isbn9798894285054` (from CFP page, not opened)
- Google Play: `https://play.google.com/store/search?q=9798894285054&c=books` (from CFP page, not opened)
- Publisher: `https://www.christianfaithpublishing.com/books/?book=the-bubblegum-tree` (verified)

## Draft-stage safeguards

- `<meta name="robots" content="noindex">` on every page until Brenda approves the site. Removed at launch.
- No analytics, no cookies, no forms. Contact is a mailto link (address pending).

## Error handling

Static site: nothing to fail at runtime. Images have width/height attributes and alt text. If a YouTube embed is blocked, the caption links to the video on YouTube.

## Testing

- Open every page in the browser at phone width and desktop width; screenshot both.
- Check no console errors and every asset returns 200.
- Click every nav link and buy button target (verify the URLs resolve).
- Validate HTML with a quick parser pass.

## Adding a book later

Copy `the-bubblegum-tree.html`, swap the content and images, add a card on the home page and a "Books" nav entry. Ten-minute job.

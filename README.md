# tbosw.jfeelgood.com
### Landing Page — *The Book of Shadow Work* by J. Feelgood

A standalone promotional landing page for [The Book of Shadow Work](https://a.co/d/00Z3mt2Q) (ISBN 9798283598444). Built as a single-file HTML/CSS/JS deployment with no dependencies or build step required.

---

## Project Structure

```
/
├── index.html                          # Main landing page (single file)
├── README.md                           # This file
└── thebookofshadowwork/
    └── Learn-More/
        └── TBOSW-Learn-More.html       # Extended dream therapy method page
```

---

## Sections

| # | Section | Description |
|---|---------|-------------|
| 1 | **Hero** | Full-viewport title, subtitle, primary Amazon CTA |
| 2 | **What is TBOSW?** | Book intro copy + CSS book cover mockup |
| 3 | **Dream Therapy Method** | 7-step swipeable carousel |
| 4 | **Characters & Symbolism** | 6 character cards with drag-scroll |
| 5 | **Sample Pages** | 3 tappable previews with lightbox |
| 6 | **Important Note** | Clinical disclaimer |
| 7 | **Author Close** | Author note, "You are loved.", final CTA |

---

## Design Tokens

```css
--bg:        #111112   /* Page background          */
--bg-card:   #1a1a1c   /* Card / surface background */
--bg-raised: #212124   /* Elevated surfaces         */
--gold:      #c9a84c   /* Primary accent            */
--white:     #f0ede8   /* Body text                 */
--muted:     #8a8580   /* Secondary text            */
--border:    rgba(255,255,255,0.07)
```

**Fonts** (loaded from Google Fonts):
- `Cormorant Garamond` — headings, quotes, display text
- `DM Sans` — body copy, labels, buttons

---

## Deployment

This is a zero-dependency static page. Drop `index.html` anywhere.

**Netlify / Vercel**
```bash
# Drag and drop the folder into the Netlify dashboard, or:
netlify deploy --dir . --prod
```

**GitHub Pages**
```bash
git init
git add .
git commit -m "initial"
git remote add origin https://github.com/yourname/tbosw.git
git push -u origin main
# Enable Pages in repo Settings → Pages → Deploy from branch: main
```

**Custom domain** — Point `tbosw.jfeelgood.com` as a CNAME to your host, or set an A record per your provider's instructions.

---

## Customization

**Swap the Amazon link**
Search for `https://a.co/d/00Z3mt2Q` — it appears in the hero CTA and the closing CTA. Replace both.

**Add a real book cover image**
Find the `.book-cover` element and replace the CSS-rendered mockup with an `<img>` tag:
```html
<div class="book-cover-wrap">
  <img src="assets/cover.jpg" alt="The Book of Shadow Work cover" width="180" />
</div>
```

**Center the Learn More button**
```css
.btn-learnmore {
  display: block;
  width: fit-content;
  margin: 24px auto 0;
}
```

**Add real illustration images**
Inside each `.char-image` div, replace the emoji symbol with:
```html
<img src="assets/character-boy.jpg" alt="The Boy" style="width:100%;height:100%;object-fit:cover;" />
```

---

## Browser Support

Works in all modern browsers. No polyfills needed. CSS scroll-snap and `IntersectionObserver` are broadly supported (Chrome 69+, Firefox 68+, Safari 15+).

---

## License & Credits

- **Content** © 2025 J. Feelgood — All book text, character descriptions, and method steps are sourced directly from *The Book of Shadow Work* (ISBN 9798283598444).
- **Code** — Free to use and modify for jfeelgood.com properties.
- **Fonts** — Cormorant Garamond & DM Sans via Google Fonts (OFL license).

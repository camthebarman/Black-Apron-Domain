# Black Apron Bar Co.

Marketing site for **blackapronbarco.com** — a single-page, static site with
four sections: About, Services (Bar Supply / Private Bartending / Event
Creation), The Chit (newsletter signup), and Contact.

No build step, no framework — just `index.html`, `css/style.css`, and
`js/main.js`. Open `index.html` directly in a browser to preview locally.

## Personalize before launch

- **About copy** (`index.html`, `#about` section) is placeholder text —
  swap in your real founder/company story.
- **Contact email** — currently `hello@blackapronbarco.com`; update the
  `mailto:` link and the display text in the `#contact` section.
- **About photo** — the About section currently shows a plain monogram
  placeholder (`.about-media-frame`). Drop a real photo into `images/` and
  swap the placeholder `<div>` for an `<img>` tag.

## Forms

Both the newsletter ("The Chit") and Contact forms are wired for
**Netlify Forms** (`data-netlify="true"` + a hidden honeypot field) — if you
deploy to Netlify, submissions work immediately with zero backend code, and
show up under Site settings → Forms. Netlify also lets you forward
submissions to email or Zapier/Slack from that same dashboard.

If you deploy elsewhere (Vercel, GitHub Pages, your own host), swap the
`data-netlify="true"` / `netlify-honeypot` attributes and hidden
`form-name` input for a service like [Formspree](https://formspree.io) —
just point each form's `action` at your Formspree endpoint.

## Deploying

Any static host works:

- **Netlify** — drag-and-drop the folder, or connect this repo (no build
  command needed, publish directory is the repo root). Point
  blackapronbarco.com's DNS at Netlify and forms work out of the box.
- **GitHub Pages** — enable Pages on this repo, serve from the root of the
  main branch, then add a `CNAME` file containing `blackapronbarco.com`.
- **Vercel** — import the repo as a static project.

# frankaquinn.com

The personal one-page brand site for **Frank A. Quinn** — Georgia commercial lines producer, founder of Quinn Alliance (a commercial lines specialty P&C and consulting firm), Associate Broker at Wynd Realty (Georgia), and Sales Agent at Easy Realty (Florida).

Designed as an editorial bio that routes serious inquiries to the right destination — Quinn Alliance for insurance, Wynd Realty for Georgia real estate, Easy Realty for Florida real estate, and direct contact for valuation and inspection engagements.

---

## What's in this repo

```
/
├── index.html       The site (single file, no build step)
├── CNAME            Custom domain — frankaquinn.com
├── .nojekyll        Disables Jekyll processing on GitHub Pages
├── README.md        This file
└── assets/
    ├── headshot.jpg The portrait shown in the hero section
    └── README.txt   Notes on the photo
```

No frameworks, no build step. Open `index.html` in any browser to preview locally.

---

## Updating the site later

GitHub Pages republishes automatically on every commit to `main`. The simplest workflow:

1. On GitHub, click `index.html` in the repo file list.
2. Click the pencil ✏ icon (top right of the file view) to edit.
3. Make your changes.
4. Scroll down, leave the commit message default or describe the change, click **Commit changes**.
5. The site updates within ~60 seconds.

For larger edits, use the GitHub web editor's split view (`.` keystroke on any repo page) — that gives you a VS Code-style editor in the browser.

---

## DNS setup (already configured)

This site is published via **GitHub Pages** with the custom domain **frankaquinn.com**. DNS is hosted at **Namecheap**.

Active records at Namecheap → Advanced DNS:

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | frankaquinn.github.io. |

Email and link-tracking records (Mailgun, brand.ludicrous.cloud, Google site verification) remain in place — they don't conflict with GitHub Pages because they're on separate subdomains.

The `CNAME` file in this repo declares the custom domain to GitHub Pages — do not delete it.

---

## Architecture

Single-file editorial layout. Key choices:

- **Typography:** Fraunces (display serif with optical sizing) for headlines, Inter for body. Both loaded via Google Fonts.
- **Color:** ivory paper (`#f7f3ec`) background, deep ink (`#14110d`) text, oxblood (`#7a1f24`) and gold (`#e7c574`) accents.
- **Sections:** masthead → lede → background — practices → tools (dark feature panel) → credentials → connect → disclosures → footer.
- **Motion:** subtle fade-in on scroll via IntersectionObserver. No JS frameworks, no analytics, no cookies.

---

## Compliance & disclosures

The page is a personal bio that lists services performed through licensed entities. The Disclosures section before the footer covers:

- Entity structure (Quinn Alliance LLC, independence of Wynd Realty / Easy Realty)
- No concurrent representation
- Insurance services through Quinn Alliance LLC
- Real estate work in Georgia under Wynd Realty supervision
- Real estate work in Florida under Easy Realty supervision
- Equal Housing Opportunity language
- BPO/CMA explicitly **not** USPAP appraisals
- Frank A. Quinn explicitly **not** a state-licensed fee appraiser
- Inspection limited-scope warranty disclaimer
- Forward-looking-statement carve-out for Coming Soon tools
- License-verification pointers
- Trademark identification
- Savings clause: "if any statement is inconsistent with applicable advertising regulations, the regulation controls and the conflicting statement is withdrawn"

Recommended: have a Georgia attorney with both insurance and real estate compliance practice review the page once before public launch. Most E&O carriers provide this review free as part of policy benefits.

---

## License & attribution

Original content © Frank A. Quinn. Site authored as a custom build, not a template. Fonts under their respective open-source licenses (Fraunces / Inter via Google Fonts).

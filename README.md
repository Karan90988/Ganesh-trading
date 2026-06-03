# Ganesh Trading Company — Website

A single-page, mobile-first website for a neighbourhood kirana store.
Everything lives in one file: **`index.html`**. No build tools, no internet
dependency (loads fast even on slow phones), and works by just
double-clicking the file or hosting it anywhere.

## Tech stack (and why)
- **Plain HTML + CSS + a little vanilla JavaScript.**
  For a single page, a framework (React/Next/Tailwind build) would only add
  weight and a build step. This loads in one request, scores well on mobile,
  and any web host (Netlify, GitHub Pages, Hostinger, cPanel) serves it as-is.

## ✏️ What to fill in (5-minute setup)

Open `index.html` and edit the `SHOP` config near the bottom (in the
`<script>` block). **This is the only place** the phone/WhatsApp numbers live —
change them once and every button updates automatically:

```js
const SHOP = {
  whatsapp: "910000000000",   // WhatsApp number: country code + number, digits only
  phone:    "+910000000000",  // Phone for click-to-call (with + and country code)
  name:     "Ganesh Trading Company"
};
```

Then search the file for the word **`PLACEHOLDER`** and update:

| Placeholder | Where | What to add |
|---|---|---|
| Logo | Header & footer (`.logo`) | Replace the "G" letter-mark with `<img src="logo.png" alt="...">` |
| Shop photo | Hero card (`.img-ph`) | Replace with `<img src="shopfront.jpg" alt="storefront">` |
| Phone numbers | `SHOP` config + visible text | Your real numbers |
| Full address | Store Info + footer | Street, area, city, PIN |
| Opening hours | Store Info + footer | Your real timings |
| Weekly/festive offer | Offers banner (`.offers-box`) | Current deal text |
| Social links | Footer (`.socials`) | Facebook / Instagram URLs |
| Product photos | Category cards (optional) | Add `<img>` inside each `.cat-card` |
| Website URL | `<head>` canonical + OG tags | Your domain (for SEO) |

> Tip: the categories list (and their WhatsApp messages) is also data-driven —
> edit the `CATEGORIES` array in the script to add/rename categories.

## Features included
- Sticky header with mobile dropdown menu
- Hero with "Order Now" + "Call Us"
- 7 product categories — each opens WhatsApp with a **pre-filled order message**
- Why-choose-us, weekly/festive offers banner
- Store info (hours, address, UPI/Cash), embedded Google Map (18.7915767, 73.7969874)
- Click-to-call links + "Request a callback" form that sends to WhatsApp
- Floating WhatsApp button on every screen
- SEO: title, meta description, Open Graph, and LocalBusiness structured data
- Bilingual-friendly copy (English + simple Hindi wording)
- Accessible contrast, respects reduced-motion, fully responsive

## How to publish
1. Drop `index.html` (plus your `logo.png` / photos) into any web host.
2. Or for free hosting: drag the folder onto **netlify.com/drop**.

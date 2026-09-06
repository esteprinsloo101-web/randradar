# RandRadar

**Every special. One alert. More month left.**

Faceless South African deals board: find sales, specials and promos by area for food, diesel/fuel, groceries, travel, accommodation, and other.

## Live board

**https://esteprinsloo101-web.github.io/randradar/**

GitHub Pages deploys from `main` / repository root (`index.html` + `deals.json`).

## How it works

1. Open the live board on a phone or desktop.
2. **Search** by area, store, or deal text (e.g. Cape Town, diesel, chicken).
3. Tap **category chips**: Food, Diesel, Groceries, Travel, Accommodation, Other.
4. Read **deal cards**: title, category, area, price/saving, store, valid-until, source link, note.
5. Tap ♡ to **wishlist** deals (saved in `localStorage` on your device).
6. **Submit a tip** → stored in `localStorage` and exportable as JSON (`Download tips JSON`).
7. Soft **Pro desk coming soon** CTA — browsing is never paywalled.

### Data model (`deals.json`)

Each deal includes fields such as `id`, `title`, `category`, `area`, `province`, `price`, `was`, `saving`, `store`, `valid_until`, `source`, `note`, and **`demo: true`**.

**CRITICAL:** Seed deals are **DEMO / example data** for UI and layout. They are **not** live scraped prices. Confirm every price in-store or at checkout. The board banners this clearly.

### Tips & wishlist

- Wishlist key: `randradar_wishlist_v1`
- Tips key: `randradar_tips_v1`
- Tips stay on-device until a future desk sync exists. Export downloads `randradar-tips.json`.

## Local preview

```bash
# from repo root
python3 -m http.server 8080
# open http://localhost:8080
```

Or open `index.html` via any static host. `fetch('deals.json')` needs HTTP (not `file://`).

## Operating rules (`BOT.md`)

- Do **not** invent live rand figures as truth.
- Do **not** scrape logins or private accounts.
- COI-safe: no Eco Rehab or Jories selling on this board.
- Affiliate disclosure later; price paid does not go up.
- Digest bot drafts only — humans paste / send.

## Money rails

See `MONEY.md` (Travelstart / Booking / SafariNow affiliates, Paystack Radar+ later, Pages already on).

## Stack

Vanilla HTML / CSS / JS. No build step. Mobile-first static SPA-like page.

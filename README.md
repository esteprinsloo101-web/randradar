# RandRadar

**Every special. One alert. More month left.**

Faceless **Johannesburg metro** weekly area digest board — groceries, diesel/petrol (regulation-day framing), travel and accommodation. Public board stays free.

## Live board

**https://esteprinsloo101-web.github.io/randradar/**

GitHub Pages deploys from `main` / repository root (`index.html` + `deals.json`).

## Scout wedge (MVP)

- **Default metro:** Johannesburg
- **Area chips:** Sandton, Midrand, Pretoria East, Centurion, Soweto, Roodepoort
- **Categories:** Groceries · Diesel/Petrol · Travel · Accommodation · Other
- **Positioning:** weekly area digest board — **not** a live 7-retailer price engine
- **Seed data:** DEMO / example only (`demo: true` on every deal)
- **Soft CTA:** R99 Pro weekly pack — Coming soon (Gumroad later). Browsing never paywalled.

## How it works

1. Open the live board (mobile-first).
2. Filter by **Joburg area chips** and **category chips**; search by text.
3. Deal cards show title, category, area, price/saving, store, valid-until, source link, note + **DEMO** badge.
4. ♡ **Wishlist** → `localStorage` on device.
5. **Submit a tip** → `localStorage` + **Download tips JSON**.
6. Soft Pro CTA records interest locally — no payment yet.

### Data (`deals.json`)

Fields include `id`, `title`, `category`, `area`, `province`, `metro`, `price`, `was`, `saving`, `store`, `valid_until`, `source`, `note`, **`demo: true`**.

Confirm every price in-store or at the pump. Never invent live rand figures as truth.

## Local preview

```bash
python3 -m http.server 8080
# http://localhost:8080
```

`fetch('deals.json')` needs HTTP (not `file://`).

## Operating rules (`BOT.md`)

- Do **not** invent live rand figures as truth.
- Do **not** scrape logins.
- Label DEMO seed clearly.
- COI-safe: no Eco Rehab or Jories selling on this board.
- Affiliate disclosure later.

## Money rails

See `MONEY.md`. Pro weekly pack (R99) via Gumroad later; Travelstart / Booking / SafariNow affiliates when approved.

## Stack

Vanilla HTML / CSS / JS. No build step.

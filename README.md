# Nearby — Local Business/Service Directory

A single-page, **no-database** campus service directory built with plain HTML, CSS, and JavaScript. All listings, reviews, and favorites are stored locally in the browser using `localStorage` — no backend, no server, no setup required.

## Features

- **Listings**
  Add services (canteen, printout shop, laundry, stationery, salon, repair shop, etc.) with name, category, location, opening/closing time, contact info, and a short description.

- **Browse & Filter**
  Filter listings by category using quick-select chips, or search by name/category/description with the search bar.

- **Open/Closed Status**
  Each listing automatically shows an "Open now" or "Closed" badge based on the current time compared to its stored opening/closing hours (handles overnight hours too). Status refreshes automatically every minute.

- **Ratings & Reviews**
  Add a star rating (1–5) and a short text review to any listing. Average rating is shown as a star display, with the two most recent reviews visible on the card.

- **Favorites/Bookmarks**
  Tap the heart icon to bookmark a listing. Favorited listings are pinned to the top of the results.

- **Admin Mode**
  Toggle "Admin mode" in the header to reveal the add-listing form and delete buttons. No real authentication — this is a simple view toggle for the demo/project scope, matching the "no-database" requirement.

## How to run

No installation or server needed.

1. Open `index.html` directly in any modern browser.
2. The directory comes pre-seeded with 3 sample listings (canteen, printout shop, laundry) so it's not empty on first load.
3. Switch to **Admin mode** to add or delete listings.
4. All changes save automatically to `localStorage` and persist between visits **on the same browser/device**.

> Note: Since this uses `localStorage`, data is device- and browser-specific. Clearing browser data/cache will erase saved listings, reviews, and favorites. There is no login, sync, or cloud storage — this is intentional.

## Tech stack

- HTML5
- CSS3 (custom properties, no framework)
- Vanilla JavaScript (ES6+)
- Google Fonts (Fraunces, IBM Plex Mono, Inter) — loaded via CDN
- Browser `localStorage` API for persistence

## File structure

```
business-directory/
├── index.html   # Full app: markup, styles, and script in one file
└── README.md    # This file
```

## Possible extensions

- Export/import listings as JSON (backup without a database)
- Map/location pin view for each listing
- Photo upload for listings (stored as base64 in localStorage)
- Sort by rating or distance
- Multi-language support

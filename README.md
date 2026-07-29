# Velelo Stay

An Airbnb-style booking page for **The Velelo Villa** — a single-property,
self-catering listing in Willows, Bloemfontein. Built as one self-contained
HTML file: glassmorphism UI, live price calculation, and bookings that persist.

Designed by **Rethabile Velelo** · Velelo Technology.

---

## Contents

```
velelo-stay.html    The complete website (HTML + CSS + JS in one file)
DESCRIPTION.md      Guest-facing listing copy + technical project description
README.md           This file
```

---

## Quick start

No build tools, no dependencies. To view it:

1. Download `velelo-stay.html`.
2. Double-click it, or open it in any modern browser.

That's it — it runs straight from the file.

---

## Features

- **Listing layout** — photo gallery, amenities, host card, rating summary.
- **Booking widget** — guest name, check-in / check-out dates, guest count.
- **Live pricing** — R1 950/night × nights + R350 cleaning + 10% service fee.
- **Saved bookings** — each reservation persists and appears in a ledger with a reference (e.g. `VLO-X9K2M`).
- **Email notification** — opens a pre-filled email to the host on booking.
- **Validation** — name required, no past dates, check-out must follow check-in.
- **Responsive** — adapts down to mobile.

---

## How the booking flow works

1. Guest fills in name, dates, and guests.
2. Price updates live as dates change.
3. On **Reserve**, the site:
   - validates the input,
   - saves the booking (so it survives a reload),
   - creates a reference,
   - opens a pre-filled email to the host,
   - adds the booking to the "Recent reservations" list.

---

## Email notifications

- The **public** address shown to guests: `info@velelohotel.co.za`
- Booking notifications route to: `velelotechnology@gmail.com`

**How it works today:** the site uses a `mailto:` link. On booking, it opens
the guest's email app with a message pre-filled and addressed to the Gmail
inbox. The guest presses send to confirm.

**Important:** a static HTML page cannot send email on its own — there is no
server to send it. The `mailto:` approach works everywhere with zero setup,
but it needs the guest to click send.

To change where notifications go, edit this line near the bottom of
`velelo-stay.html`:

```js
const NOTIFY_EMAIL='velelotechnology@gmail.com';
```

---

## Deploying to velelohotel.co.za

Any static host works. Two easy paths that fit your existing Truehost domain:

**Netlify Drop**
1. Go to the Netlify Drop page.
2. Drag the folder (or `velelo-stay.html`, renamed to `index.html`) onto it.
3. Point your `velelohotel.co.za` DNS at Netlify.

**GitHub Pages**
1. Create a repo, add the file as `index.html`.
2. Enable Pages in the repo settings.
3. Add a `CNAME` file with `velelohotel.co.za` and set the DNS at Truehost.

> Tip: rename `velelo-stay.html` to `index.html` so it loads as the home page.

---

## Before going live — checklist

- [ ] Replace the Unsplash photos with **real, self-hosted images** of the villa.
- [ ] Decide on automatic email (see below) vs. the current `mailto:` flow.
- [ ] Confirm the nightly rate, cleaning fee, and service fee are correct.
- [ ] Add real house rules / cancellation policy (footer links are placeholders).

---

## Next steps (when you're ready for a backend)

The current version saves bookings in the preview environment and notifies by
`mailto:`. For a real production site you'll want:

- **Automatic emails** — a form service like **Formspree** or **Web3Forms**
  sends the booking straight to `velelotechnology@gmail.com`, no click needed.
- **A real database** — store bookings permanently (your Node/Express setup fits well).
- **Double-booking prevention** — block dates already reserved.
- **Payments** — integrate a South African gateway (e.g. Payfast / Yoco) if you want to take deposits.

---

## Tech

- Plain HTML, CSS, and JavaScript — no framework, no build step.
- Fonts: Fraunces (display), Outfit (body), loaded from Google Fonts.
- Icons: inline SVG (no icon library needed).

---

## Contact

- **Rethabile Velelo** — Velelo Technology (Pty) Ltd, Bloemfontein
- Phone: 064 678 5516
- Public email: info@velelohotel.co.za
- Bookings inbox: velelotechnology@gmail.com

---

*© 2026 Velelo Stay · Designed by Rethabile Velelo.*

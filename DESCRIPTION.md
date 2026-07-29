# Velelo Stay — Description

---

## Part 1 · The Villa (Guest-Facing)

### The Velelo Villa · Willows, Bloemfontein

Wrapped in mahogany tones and golden light, the Velelo Villa is a private
three-bedroom retreat in the leafy Willows suburb of Bloemfontein, Free State.
Wake to garden birdsong, spend slow afternoons by the pool, and end your day
around a fire under wide Free State stars.

It's an easy, unhurried kind of luxury — designed for families, couples, and
small groups who want space to breathe in the city of roses.

**At a glance**

- Entire villa · sleeps 6
- 3 bedrooms · 2 bathrooms
- Willows, Bloemfontein · Free State, South Africa
- From R1 950 per night

**What this place offers**

- Three bedrooms sleeping up to six guests
- Private swimming pool
- Fast fibre Wi-Fi throughout
- Braai area and indoor fireplace
- Secure off-street parking
- Fully equipped kitchen
- Air conditioning
- Pet friendly

**Your host**

Hosted by Rethabile Velelo — a Superhost since 2024 who typically responds
within the hour. Every stay is looked after personally, from the welcome to
the check-out.

**Good to know**

- Check-in and check-out dates are chosen at the time of booking.
- Rates: R1 950 per night, plus a once-off R350 cleaning fee and a 10% service fee.
- Each confirmed booking receives a unique reference (e.g. `VLO-X9K2M`).

**Get in touch**

- Phone: 064 678 5516
- Email: info@velelohotel.co.za
- Location: Willows, Bloemfontein, Free State, South Africa

---

## Part 2 · The Project (Technical)

### What this is

Velelo Stay is a single-property, Airbnb-style booking page for The Velelo
Villa. It is a self-contained front-end site: one HTML file with all styling
and behaviour built in, no build step and no framework required.

### What it does

- Presents the villa as a listing — photo gallery, amenities, host, and reviews summary.
- Lets a guest enter their name, choose check-in / check-out dates, and pick a guest count.
- Calculates the price live: nightly rate × nights + cleaning fee + 10% service fee.
- Saves each booking so it persists across page reloads, and shows recent reservations in a ledger.
- Generates a booking reference for every reservation.
- Opens a pre-filled notification email to the business inbox when a booking is made.

### Design language

Consistent with the Velelo brand: a mahogany-and-gold palette, glassmorphism
panels, and an ambient "liquid" animated background. Typography pairs *Fraunces*
(display serif) with *Outfit* (body). Amenity and brand marks use inline SVG
icons rather than emoji, so they stay crisp and on-brand at any size.

### How the pieces fit

| Area | How it works now | Notes for going live |
|------|------------------|----------------------|
| Booking storage | Saved via the artifact storage API (persists in this preview) | Replace with a real database + booking API |
| Double-booking | Not yet prevented | Add server-side date-conflict checks |
| Email notification | `mailto:` link opens a pre-filled email to the host | Swap for Formspree / Web3Forms or a backend to send automatically |
| Images | Live Unsplash URLs | Replace with real, self-hosted photos of the property |

### Contact / ownership

- Owner & designer: Rethabile Velelo
- Business: Velelo Technology (Pty) Ltd — Bloemfontein, South Africa
- Public email: info@velelohotel.co.za
- Booking notifications route to: velelotechnology@gmail.com

---

*Designed by Rethabile Velelo · Velelo Technology.*

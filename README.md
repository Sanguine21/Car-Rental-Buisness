# Mithila Tours & Travels — Business Website

A fully responsive, multi-page business website built for a local car rental service (chauffeur-driven cars, vans, and buses) based in Laheriyaganj, Madhubani, Bihar. The site handles service discovery, customer inquiries, and booking requests for weddings, local travel, outstation trips, and airport transfers.

**Live site:** [_add your deployed Netlify/custom domain link here_](https://sanguine21.github.io/Car-Rental-Buisness/)

---

## Overview

The business serves customers who need a car with a driver for:
- Wedding transportation (separate booking flows for groom, bride, and guests)
- Local point-to-point travel within Madhubani
- Outstation trips across Bihar and neighboring states
- Airport transfers to Patna, Gaya, and Darbhanga airports

The website was designed to give the business credibility and a direct booking/contact channel without requiring any backend infrastructure or ongoing server costs.

---

## Features

- **Responsive design** — works across mobile, tablet, and desktop, with a dedicated mobile navigation menu
- **4-page structure** — Home, Services, Booking, Contact — each with distinct, purpose-built content
- **Booking form** with structured fields (trip purpose, wedding role selection, date, vehicle count, pickup/drop) that emails submissions directly to the business inbox
- **Contact form** for general inquiries, routed the same way
- **Customer feedback form** with a star-rating widget, replacing static/fake testimonials with a real, opt-in submission flow
- **Custom visual identity** inspired by Mithila/Madhubani folk art — a warm color palette (indigo, sindoor red, turmeric yellow), a hand-drawn motif system, and Fraunces/Work Sans typography, rather than a generic template look
- **Real customer photography** — actual decorated wedding cars, with license plates blurred for privacy
- **Embedded Google Map** pinned to the business's actual location
- **Floating WhatsApp button** linked directly to the business's phone number for instant contact
- **SEO-ready** — unique `<title>` and meta description tags per page for search visibility

---

## Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 (semantic markup) |
| Styling | CSS3 (custom properties, Flexbox, Grid, media queries) — no frameworks |
| Interactivity | Vanilla JavaScript (no libraries/frameworks) |
| Form handling | [Formspree](https://formspree.io) — serverless form submission to email |
| Maps | Google Maps Embed API |
| Fonts | Google Fonts (Fraunces, Work Sans) |
| Icons | Font Awesome |
| Hosting | Netlify (continuous deployment from GitHub) |

This project deliberately avoids a JavaScript framework or backend server — for a small business site with no dynamic data requirements, plain HTML/CSS/JS keeps hosting free, maintenance simple, and load times fast.

---

## Project Structure

```
├── index.html          # Homepage — hero, services overview, about, feedback
├── services.html        # Full service descriptions (wedding, local, outstation, airport)
├── booking.html          # Booking form with trip details and vehicle selection
├── contact.html          # Contact form, business info, embedded map
├── style.css            # Shared stylesheet — design system, layout, responsive rules
├── wedding-car-1.jpg     # Real customer photo (homepage hero)
├── wedding-car-2.jpg     # Real customer photo (services page)
└── README.md
```

All four HTML pages share a single `style.css` file — there is no build step or bundler.

---

## Local Development

No installation or build tools required.

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   ```
2. Open `index.html` directly in a browser, or serve the folder locally:
   ```bash
   python3 -m http.server 8000
   ```
3. Visit `http://localhost:8000`

---

## Deployment

The site is deployed via **Netlify**, connected to this GitHub repository for continuous deployment:

1. Push changes to the `main` branch on GitHub.
2. Netlify automatically detects the commit and republishes the live site (no manual build step — static files are served as-is).

### Form submissions
Booking, contact, and feedback forms are wired to [Formspree](https://formspree.io). Update the `action="https://formspree.io/f/YOUR_FORM_ID"` attribute in `booking.html`, `contact.html`, and the feedback form in `index.html` to point to your own Formspree endpoint.

---

## Future Improvements

- Move from a static feedback form to a small backend so genuine customer reviews can display automatically instead of being added manually
- Add a booking management dashboard for the business owner
- Multi-language support (Hindi/Maithili) for a wider local audience

---

## Author

Built by **Prachi Kumari** — B.Tech CSE student, developed as a real-world client project for a family business, focused on responsive design, accessible booking flows, and a distinctive regional visual identity.

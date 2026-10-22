# MechNow — Roadside Mechanic Marketplace

**Vehicle broke down?** MechNow finds **verified local mechanics near you** — garages, tyre shops, battery specialists and mobile mechanics — with **upfront fixed charges** and **live ETA**. Book in two taps, pay the mechanic after the job.

Live (after deploy): https://mechnow.vercel.app

## What it does

- **Emergency finder** — pick the problem (Won't start, Flat tyre, Battery dead, Engine trouble, Overheating, Accident help, General check), choose Bike or Car, select your city + area, and see mechanics sorted by distance.
- **49 seed mechanics** across Hyderabad, Bengaluru, Mumbai, Delhi, Pune and Chennai (8–9 per city, at least 2 in every area), each with a Verified badge, specialties, distance, ETA, rating, open-now status (computed from real hours) and a fixed service charge for your problem from a transparent per-tier price table.
- **EV specialists included** — a dedicated filter for electric-bike / EV-trained mechanics (controller, battery, BMS faults), plus filters for Open now, Mobile mechanic and Top rated.
- **Mechanic detail view** — full services & fixed-price list, about, and reviews.
- **Two-tap booking** — confirm problem, vehicle, area and price; the booking gets a live status timeline (Request sent → Confirmed → On the way → Arrived → Job done) that advances about every 20 seconds in demo mode, persists across reloads, and can be cancelled.
- **Join as a mechanic** — a form that lists a garage or mobile service instantly with a "New partner" badge. Business model (illustrative): ₹0 joining fee, 10% platform commission only on completed jobs; customers pay mechanics directly.
- **Trust layer** — verified ID checks, upfront pricing with parts approved before fitting, pay-after-the-job, ratings from completed jobs only.

## The treatment

Built to the Vikranth Reddy design system ("portfolio treatment"): dark premium hero with animated amber gradient mesh, glassmorphism finder panel, display typography, mono kickers, sticky glass header, dark-mode toggle (persisted separately), scroll progress bar, back-to-top, hover lifts, scroll-reveal animations with reduced-motion support, custom scrollbar, print stylesheet, and a Privacy / Terms / DMCA page (`legal.html`) linked from the footer.

## Tech

Zero-build static site: one self-contained `index.html` (inline CSS + JS, **zero external requests** — no CDNs, no webfonts, no images) plus `legal.html`, `robots.txt`, `sitemap.xml` and a `vercel.json` with security headers (HSTS, nosniff, X-Frame-Options, Referrer-Policy, Permissions-Policy). All state lives in the browser's `localStorage` under `mechnow_v1` (theme under `mechnow_theme`): bookings, partner listings, filters. Open the file in a browser, or deploy the folder to any static host.

## Demo notes

Prices, ETAs, ratings and partners are illustrative demo data. Status advancement, the 10% commission and all figures are for demonstration — no real bookings, payments or mechanics are involved.

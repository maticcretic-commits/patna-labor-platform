# Patna Labor Platform — Pilot Demo

**Live demo site:** https://maticcretic-commits.github.io/patna-labor-platform/

A **pilot demo** (not an operating business) of a Patna-first platform connecting
households with affordable hourly/daily blue-collar workers — room cleaning,
laundry, odd jobs, construction/general manpower — matched by a human
coordinator over phone calls, since workers typically carry only basic mobile
phones.

## Money model

- The **customer pays the worker directly** (cash or UPI) after the work is done.
- The platform takes only a flat **₹49 booking fee** per booking — shown
  separately, no hidden charges, no commission cut from the worker's pay.
- To change the fee later, edit the `BOOKING_FEE` constant at the top of the
  `<script>` block in `index.html` (currently `49`).

## Guide rates (Patna pilot)

- Laundry / room cleaning / odd jobs: **₹99–149/hour**
- Construction / general manpower: **₹499/day** (8 hours)
- These are guide rates; final pay is agreed with the worker on the
  coordinator's call before work starts.
- **Wage floor:** Bihar's statutory minimum for unskilled workers is
  **₹436/day** (from 1 April 2026). A full day's worker pay must never go below
  this.

## What's in the demo site

- Home/hero + 4-step "how it works" (request → coordinator matches → worker
  arrives → pay worker directly)
- Services catalogue, transparent pricing section
- Booking form (name, phone, service, date, time slot, Patna area, address)
  feeding a status pipeline:
  `requested → confirmed → assigned → en route → completed / cancelled`
- Worker registration (name, phone, skills, home area, availability)
- Coordinator view: pipeline with status advancement, worker assignment, and
  worker filtering by skill + area + availability
- Patna areas, wage & safety notice, demo coordinator contact
  (`+91-98XXX-XXXXX` — placeholder, not a real number)

All records are **demo data**, stored only in the visitor's browser
(localStorage). Nothing is sent anywhere.

## Tech

- Single self-contained `index.html` — no build step, no paid services, no
  external APIs. Free hosting via GitHub Pages.

## Status

Pilot demo only. Commercial operation would require the owner's separate
written sanction, plus legal review of the compliance notes on the site
(minimum wages, Contract Labour Act threshold, Bihar gig-worker welfare rules).

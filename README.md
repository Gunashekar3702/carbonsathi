# CarbonSathi 🌱

**A personal carbon footprint companion built for everyday Indians.**

Live demo: https://gunashekar3702.github.io/carbonsathi/

---

## Chosen Vertical

**[Challenge 3] Carbon Footprint Awareness Platform**

CarbonSathi helps individuals understand, track, and reduce their daily carbon footprint through simple action-logging and personalized, low-effort insights — designed especially for Indian daily-life contexts (two-wheelers, public transport, home-cooked meals, deliveries).

---

## Approach and Logic

The core idea is "one number, one action":

- **One number** — every activity a user logs (commute mode, meal type, appliance use, deliveries) is mapped to an estimated CO2e value. These accumulate into a single live "Today's Footprint" score, visualized on a circular dial.
- **One action** — instead of overwhelming users with a long checklist, the app surfaces exactly one personalized micro-action based on the highest-impact choice the user just logged (e.g., swapping a two-wheeler trip for the bus, or choosing one vegetarian meal).

This keeps the experience lightweight and non-judgmental — the goal is awareness and small consistent changes, not guilt.

A community pulse section frames the user's score against sample peer data from different Indian cities, adding light social motivation without leaderboard pressure.

---

## How the Solution Works

1. Landing view — user sees a carbon dial starting at 0 kg CO2e, with India's national daily average (6.5 kg) shown as a reference point.
2. Activity logging — user taps activity cards (transport, food, energy, deliveries, etc.). Each tap toggles the activity on/off and instantly updates the dial, status label, weekly trend chart, and community pulse comparison.
3. Personalized tip — selecting an activity surfaces a tailored micro-action tip relevant to that specific choice, with a concrete CO2e estimate for the suggested swap.
4. Weekly trend — a simple bar chart compares today's live score against the user's recent daily pattern, giving a sense of progress over time.

The entire experience is a single static HTML file (HTML/CSS/JS, no backend, no build step), making it instantly deployable via GitHub Pages or any static host.

---

## Assumptions Made

- Emission factor estimates for transport, food, and energy activities are approximate averages drawn from general published carbon-footprint references for Indian contexts (e.g., two-wheeler commute ~6.8 kg CO2e, veg meal ~0.9 kg CO2e, bus commute ~2.1 kg CO2e). These are illustrative defaults intended for awareness, not certified measurements.
- "India avg/day" reference (6.5 kg CO2e) is used as a rough benchmark for contextualizing the user's score, not a precise national statistic.
- Community pulse data is sample/illustrative data (not live user data) to demonstrate the social-comparison feature.
- The app assumes a single-session, client-side experience — no login, no persistent storage/backend in this MVP. State resets on page reload by design, keeping the demo lightweight and dependency-free.
- Designed mobile-first, since most target users (including rural and semi-urban users) primarily access the web via smartphones.

---

## Tech Stack

- HTML5, CSS3 (custom properties, responsive grid)
- Vanilla JavaScript (no frameworks/b

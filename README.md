# Hostelverse — GitHub Pages Showcase

## Fastest deployment (no build required)

1. Create a **public GitHub repository** named `hostelverse`.
2. Upload **index.html**, **cafe-menu-reference.jpeg**, and **junior-mess-menu.pdf** to the repository root.
3. Open **Settings → Pages → Build and deployment**.
4. Choose **Deploy from a branch**, branch **main**, folder **/(root)**, then Save.
5. Your site should appear at `https://YOUR_USERNAME.github.io/hostelverse/` after GitHub finishes deployment.

This version is intentionally static so it can be deployed to GitHub Pages without Node, npm, server setup, environment variables, or paid hosting.

## What works in the showcase

- Responsive light/dark design with hover animations and accessible click navigation.
- Kitchen forecasting: weekday patterns, sample menu preferences, student votes, forecast intervals, day-over-day preparation guidance, and actual attendance feedback correction.
- Original mess weekly menu and PDF.
- K.J Cafe photo-based menu with 50+ transcribed items, prices, category filtering, basket, and simulated order progression.
- Student marketplace listings, rental requests, freelance applications, learning-circle joins, example community profiles, and a Passport activity view.
- Local browser persistence (`localStorage`).

## Important demo vs production distinction

This GitHub Pages showcase is a **frontend demo**, not a production multi-user system. Profiles are fictional examples. Forecast baselines are illustrative, not validated on actual mess records. Orders, votes, listings and other actions are stored **in the browser on one device**, not shared between students or staff. Sample order-status transitions are not secured staff actions. GitHub Pages **cannot run the existing Express backend**.

For actual multi-user deployment, host the earlier full-stack Express server on a Node-capable host (e.g. Render or Railway) and connect it to a durable database. Migrate the polished UI into the React project; use authenticated staff roles for kitchen/canteen changes, and use verified college login and authorization. Do not store passwords or sensitive user information in this static demo.

## Forecast model

For each weekday and meal, a demo historical attendance rate is adjusted by a simple, disclosed menu preference signal. Poll votes provide a calibrated intent signal; low participation is shrunk toward the baseline. Recorded actual turnout adds a bounded correction to future predictions. The app shows predicted portions, a rough uncertainty band, a next-day comparison and an explanation. This is a demonstration of a feedback loop, **not an accuracy-validated forecasting system**. For judging, collect actual attendance records and report MAE against a naive weekday baseline.

## Menu notes

Café prices were transcribed from the user's photograph of the K.J Cafe board. Items listed at MRP do not have invented prices. Verify the photo and confirm prices before real ordering. The mess PDF is a different service and its schedule is kept separate.

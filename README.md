# Astar Roster

A simple, fast rostering tool for **Astar Health Service** (NDIS support work).

**Live app:** https://arshdeep2705.github.io/astar-roster/

It solves the weekly/fortnightly headache: a worker sends their availability, and you
need to work out who covers which participant without clashes. Enter availability,
define each participant's recurring support needs, hit **Auto-roster**, and the app
fills the calendar — flagging any clashes or gaps with the reason.

## What it does

- **Workers** — your support team (Sameer, Tej, Mansi…), with skills, max hours, and a
  standard weekly availability pattern.
- **Clients / participants** — Allan, Nick…, each with recurring support needs
  (day, time, required skills, preferred workers).
- **Availability** — tweak any day for the current week or fortnight; defaults come from
  each worker's standard pattern.
- **Auto-roster** — constraint-based assignment: never double-books, respects
  availability, max hours and required skills, keeps the same worker with the same
  participant (continuity of care), and balances the load. Locked shifts are never moved.
- **Conflicts & gaps** — every clash or unfilled shift is listed with a plain-English
  reason, and the shift is outlined on the calendar.
- **Roster calendar** — week or fortnight view, colour-coded by worker; clean stacked
  list on mobile; print / save-as-PDF.
- **Share** — copy each worker's shifts as plain text to send via SMS / WhatsApp.
- **Backups** — export / import a `.json` backup any time.
- **Cloud sync (optional)** — turn it on to sync the roster across your phone and laptop
  with a private sync code. Off by default; the app works fully offline without it.

## How it's built

A single self-contained `index.html` — plain HTML, CSS and JavaScript, no build step and
no dependencies. Data lives in your browser (`localStorage`); cloud sync is an optional
layer backed by Supabase (a key-gated table, accessed only through secure RPC functions).

Hosted on GitHub Pages.

# AGENT

- Project: Fuel Consumption Tracker PWA (single-page, inline CSS/JS, no dependencies).
- Source of truth: all requirements live in `start.md`; keep language in Indonesian and mobile-first.

## Operating Notes
- Build one `index.html` with semantic sections: fixed stats header, scrollable history list, FAB, and modal form.
- Data lives in LocalStorage under a single object containing `entries` and `settings`; validate on load and handle corruption/reset.
- Entry form must block zero/negative values, compute km/L ratio to 2 decimals, and surface inline errors; color-code efficiency in history cards.
- Support offline via inline manifest + cache-first service worker; respect system dark mode (`auto` default).
- Edge handling: guard division by zero (show "Invalid"); handle quota/corruption gracefully; allow 3 decimal fuel amounts when tiny.

## Out of Scope
- CSV import, fuel-cost workflows, multi-language, and cloud sync (per `start.md`).

# Roadmap

## 0.1 — Stability & UX
- [ ] Show “saving error” toast with retry on LocalStorage/quota failures.
- [ ] Custom delete confirm with undo (5s), no `confirm()`.
- [ ] Refine tooltip/helper copy for non-technical users.
- [ ] Accessibility audit: dialog focus trap, ARIA live for errors/success.

## 0.2 — Data & Export
- [ ] CSV export via data URI (no import).
- [ ] Manual JSON backup/restore if safe.
- [ ] Sort/filter: date range, note search.

## 0.3 — Visuals & Charts
- [ ] Consumption trend chart (Canvas) with light smoothing.
- [ ] Dense list mode for small screens; compact card option.
- [ ] Subtle animations for add/edit/delete.

## 0.4 — PWA & Devices
- [ ] Lightweight badge/notification (e.g., refill reminder) if permitted.
- [ ] Offline optimization with explicit cache busting.
- [ ] iOS install polish (icons, splash metadata).

## 0.5 — Easier Distance Input (no API key)
- [ ] Auto-parse “km” patterns from clipboard when dialog is open.
- [ ] Desktop bookmarklet/extension to copy distance from maps.google.com into clipboard.
- [ ] Mobile helper microcopy: step-by-step for copying from Maps app.

## 0.6 — (Optional, needs API key)
- [ ] Route/distance fetch from pasted link via routing API (Google Directions/OpenRoute).
- [ ] Cache route results to save quota; graceful fallback to manual input.***

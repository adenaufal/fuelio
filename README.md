# fuelio

Minimalist Progressive Web App for motorcycle fuel efficiency tracking. Single-page, offline-capable, no external dependencies.

## Features
- Add/edit/delete fill-up entries: distance, fuel (L), date, optional notes.
- Auto-calculates km/L with color-coded history cards (green/yellow/red).
- Stats header: average, best, worst, totals.
- LocalStorage persistence + cache-first service worker; dark mode follows system.
- Map paste helper: open Google Maps, copy route distance, click “Paste & Fill” to populate distance (or paste manually).
- Inline validation (no zero/negative values, upper bounds) and “Invalid” guard for divide-by-zero cases.

## Usage
1) Open `index.html` in a browser (PWA-installable).  
2) Tap `+` to open the form.  
3) Enter distance (use map helper if copying from Google Maps), fuel, date, and optional notes.  
4) Save; history/stats update and persist locally.  
5) Tap a card to edit; long-press to delete.

## Data Shape (LocalStorage)
```json
{
  "entries": [
    {
      "id": "timestamp_rand",
      "date": "2025-11-21",
      "distance": 55,
      "fuel": 12,
      "ratio": 4.58,
      "notes": "full throttle test",
      "timestamp": 1763683200000
    }
  ],
  "settings": { "darkMode": "auto", "language": "id" }
}
```

## Dev Notes
- No build step; edit `index.html` directly (inline CSS/JS).
- Manifest and service worker are inlined via Blob.
- To reset local data, remove `fuelTrackerData` in DevTools > Application/Storage.

## Limitations
- No auto-fetch of distance from Maps links without an API; use copy/paste.  
- Clipboard read requires user gesture/permission; if blocked, paste manually then click “Fill.”  
- No cloud sync or CSV import.***

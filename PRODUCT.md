# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Single user: "jo$e," tracking their own gym training and physical progress. No accounts, sharing, or multi-profile support — the app is built exclusively for personal use, opened as a home-screen app on iPhone.

## Product Purpose

Gym Tracker lets jo$e log workouts, track body composition and measurements, and manage a calorie/macro plan tied to a training phase (déficit, mantenimiento, volumen), all in one place, so progress across strength, weight, and nutrition can be seen together over time.

## Positioning

Not a generic fitness app or notes doc: it combines strength-training session logs, body composition (weight, body fat %, lean mass, circumference measurements), and phase-based calorie/macro tracking (cut/maintain/bulk) in a single tool built around jo$e's own routine and numbers, rather than a templated program.

## Operating Context

- Used primarily on an iPhone as a home-screen web app (`apple-mobile-web-app-capable`), so it must work well touch-first and offline.
- Four main screens: Entreno (log today's workout session by day/exercise/sets), Historial (session history), Progreso (per-exercise weight progression charts + activity heatmap), Físico (profile, body composition, training phase/macros, calorie log, weight and measurement tracking with charts), plus Informe (exportable phase report) and Ajustes (settings/backup).
- Rest timer between sets, streak tracking (consecutive training days), and a training-phase system (déficit/mantenimiento/volumen) that drives a macro breakdown (protein/fat/carbs).
- All UI copy is in Spanish.

## Capabilities and Constraints

- All data lives in browser `localStorage` (no backend, no login). This is currently the only storage layer.
- Manual backup/restore only: export/import a JSON backup, plus CSV and PDF (phase report) export.
- Single static `index.html` with vendored Chart.js and jsPDF (no build step), deployed via GitHub Pages.
- Open decision: cloud sync is wanted eventually — local-only storage is a current limitation, not a permanent choice. Any future sync work should preserve today's fully-functional offline/local mode rather than replace it outright.

## Evidence on Hand

- `icon.jpeg` — the home-screen app icon.
- No testimonials, benchmarks, or external proof content exist or apply (single personal-use app).

## Product Principles

- Single-user, no-account simplicity: every feature assumes one person (jo$e) and no auth/sharing layer.
- Local-first and offline-capable: the app must keep working fully without network access; cloud sync (when added) should layer on top, not replace, local storage.
- One tool, three data threads: strength training, body composition, and nutrition/calorie phase stay unified rather than split into separate apps or tabs that don't talk to each other.
- Fast, thumb-first logging: built for quick in-gym data entry on a phone, not desktop data review.

# Tend™ — the friend who grows with you 🌱

A gentle, **Tamagotchi-style emotional-support companion** for kids and teens (ages 6–14). You
care for a soft, dog-hearted little creature, and as you practice **real** calm and coping skills,
it grows alongside you — reflecting your own strength back to you.

> ⚠️ **This is a concept prototype (v0).** It demonstrates the idea, tone, pet, and core loop. It
> is **not** a finished or clinical product, **not** a replacement for a doctor or therapist, and
> **not** for emergencies. The crisis resources shown are unverified placeholders. See
> [`CONCEPT.md`](CONCEPT.md) for the full design and an honest list of what a real product needs.

**Live:** https://3shamrocksstudio.github.io/tend-app/

A single-file, dependency-free Progressive Web App by [3Shamrocks Studio](https://github.com/3ShamrocksStudio).
Palette: calm green `#6FB199`, soft blue `#7FA9C7`, warm amber `#E6B274`.

## The core loop

- **Gentle daily check-in** — no-pressure feeling picker, with an "I'd rather not say" option.
- **Care actions that are coping skills** — paced **breathing** (co-regulation), **name the
  feeling**, **nourish**, **rest**.
- **Small real-life quests** framed as gentle adventures — log them, the pet responds and grows.
- **A 5-stage pet evolution** — Curled → Awake → Steady → Brave → Radiant — earned by genuine
  care, never by streaks or pressure. The bond never decays; skipping a day costs nothing.

## Non-negotiables baked in

- **Trauma-informed & warm** — no alarms, no shame, no punishment for skipping. Calming colours,
  no alarming reds.
- **Privacy-first** — no accounts, no social features; everything stays on-device (`localStorage`),
  nothing leaves the device. Designed with **COPPA** in mind. A **Reset** control erases everything.
- **Not medical** — a clear, gentle disclaimer; Tend is a companion, not a clinician.
- **Crisis-aware off-ramp** — the lowest feeling (and the About screen) surfaces a warm "talk to
  someone who can help" panel. Crisis numbers are **placeholders marked `needs verification`** and
  must be localized and professionally verified before any real use.
- **Inclusive & mobile-first** — gender-neutral, scalable complexity for 6–14.

## Files

- `index.html` — the entire app (HTML + CSS + JS in one file). Sanitized DOM building
  (`textContent` / `createElement`), no `eval`, CSP meta included.
- `sw.js` — service worker (offline shell, network-first navigation, evicts stray workers on the
  shared `github.io` origin).
- `manifest.json` — PWA install manifest.
- `icon.svg` — maskable app icon (the companion's face).
- `3shamrocks.png` — studio mark (shown on a dark-grey chip, per brand rule).
- `CONCEPT.md` — the concept note: name, pet, evolution arc, core loop, safety framing, and
  PoC-vs-full-product gap.

## Tech

Single self-contained HTML PWA. Google Fonts (Quicksand). On-device `localStorage` persistence
with a reset control. No backend, no tracking, no analytics. Runs fully offline after first load.

---

© 2026 **3Shamrocks Studio.** All rights reserved. · Tend™ — a 3Shamrocks Studio app.

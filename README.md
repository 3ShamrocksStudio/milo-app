# Milo™ — Milo grows with you 🌱

A soft friend who **breathes with kids aged 6–12 when big feelings show up, then dares them to one
small brave move** in real life. Parents pay; the safety core is free forever.

> ⚠️ **Staging prototype — not launched.** Milo is a companion for practising calm. It is **not** a
> doctor, counsellor or emergency service. Its words have not yet been reviewed by a child
> psychologist, and the crisis lines shown are **unverified placeholders, not for real use**, until
> a professional verifies them per region. No real children's data.

## The loop (reset, 5 Nov 2026)

1. **How are you?** Home opens on a five-feeling check-in, plus **"I'd rather not say"**. The
   heaviest choice ("Really not okay") opens the grown-up help path in one tap. "Grown-up help" is
   on the home screen too.
2. **Breathe together — the hero.** Milo grows and shrinks with the child: in 4 · hold 2 · out 6,
   3 rounds, with optional gentle haptics. Onboarding ends in a first breathe-together.
3. **One small care skill.** Name the feeling · take care (water, snack, air, stretch) · rest
   together. About **1 in 4 opens** it is a **helper moment** instead ("Milo's got butterflies"),
   where any help works and Milo always turns back to check on the child (the door back).
4. **Today's brave move.** One small real-life quest. "I did it" or "maybe later" — both are fine,
   "maybe later" costs nothing.
5. **Grow together.** Five stages (Curled → Awake → Steady → Brave → Radiant). **No streaks, no
   decay**; the bond never decreases.

The living world stays as ambience only (no new interactive systems). Tapping Milo gives a happy
wiggle — affection only, no points.

## Free vs parent plan

| Free, forever | Parent plan — **coming soon** (no payment integration) |
|---|---|
| Breathe together, the check-in, grown-up help, stages 1–2, starter brave moves | Full brave-move library, grown-up tips (never a view of the child's feelings), stages 3–5 |

On the free plan growth points keep counting and are never lost. Safety is never paywalled.

## Removed in the reset

- **Open AI Talk** (Gemini/Groq free-tier keys, voice chat). No AI provider calls or keys remain in
  the client; the CSP `connect-src` is `'self'` only, and any old chat log or key left in a
  device's storage is erased on load. The **on-device crisis scan** stays and covers any free text
  typed during setup.
- **The hidden acrostic reveal.** The name is just Milo.
- **Pet naming and pet types.** One creature identity: Milo. Brand v2 (a white polar bear, no
  sunglasses) is in production; the app keeps the current art until it is approved, then the `ART`
  config in `index.html` points at the new frames.

## Key metric (local only)

Share of app opens that include a **finished breathe-together** (and a breathe or a named feeling).
Plain counters in this device's storage, shown to grown-ups under About → For grown-ups. Never sent
anywhere, no network analytics, erased by Reset.

## Files

- `index.html` — the whole app (HTML + CSS + JS). DOM built with `textContent`, no `eval`, CSP meta.
- `sw.js` — service worker (network-first navigation; deletes only its own older caches).
- `manifest.json`, `icon.svg`, `3shamrocks.png`, `art/` (creature frames per stage + expressions).
- `CONCEPT.md`, `AUDIT.md`, `BRAND.md`, `support-animal-research.md`, `TEST.md`.

## Deploy

`main` is served publicly by GitHub Pages at `3shamrocksstudio.github.io/milo-app/`. Reset work
lives on the `grok-reset` branch and is previewed at a staging path; it is not merged to `main`
without Dave's green light.

© 2026 3Shamrocks Studio. All rights reserved.

# Milo™ — Milo grows with you 🌱

A gentle, **Tamagotchi-style emotional-support companion** for kids and teens (ages 6–14). You
care for a soft, dog-hearted little creature named **Milo**, and as you practice **real** calm and
coping skills, it grows alongside you — reflecting your own strength back to you.

> 🌟 **A quiet secret:** **M.I.L.O.** spells **"My Inner Little One."** A child first just knows
> Milo as their friend. As the companion evolves through its five stages, one letter's meaning is
> revealed at a time (M → I → L → O), with the full phrase blooming at the final **Radiant** stage —
> a gentle reveal that caring for Milo has been a way of caring for the little one inside themselves.

> ⚠️ **Safety note.** Milo is a caring companion that teaches calm-and-coping skills — it is **not**
> a doctor, therapist, or emergency service, **not** a replacement for one, and **not** for
> emergencies. Its words have not yet been reviewed by a child psychologist, and the crisis
> resources shown are unverified placeholders that must be professionally localized before real use.
> See [`CONCEPT.md`](CONCEPT.md) for the full design and an honest list of what a real product needs.

**Live:** https://3shamrocksstudio.github.io/milo-app/

A single-file, dependency-free Progressive Web App by [3Shamrocks Studio](https://github.com/3ShamrocksStudio).
Branded to the canonical 3SDS `[data-brand="milo"]`: warm cream world, **soft sage** companion,
**peach-coral** brand hero `#EF6440`, warm amber for connection, Quicksand + Nunito. No alarming reds.

## The core loop — *mutual empowerment & growth*

Milo's defining move is a **two-way bond**: **Milo sometimes needs a little help, the child helps —
then Milo cares for the child right back.** Grounded in the **helper-therapy principle** (caring for
a vulnerable other builds the child's own agency, resilience, and self-worth). By helping Milo the
child rehearses the very same coping skills and feels capable — and **they grow stronger together**,
each empowering the other.

Four guardrails keep it empowering, never burdening, for an at-risk child:

- **Mutual, not one-way** — Milo cares for the child too; the child is never the sole caretaker.
- **Un-failable** — Milo's wobbles are always **light and soothable**; **any** help the child picks
  works and visibly calms Milo. No failing, no inconsolable pet, no guilt, no dependence.
- **Door back to the child** — after helping Milo, Milo reciprocates: *"you helped me… now how are
  YOU?"* → a feeling picker that **still routes the lowest mood to the crisis off-ramp**.
- **Skill bridge** — every skill used on Milo is handed back for real life: *"you can do this for
  yourself too."*

The loop: Milo shares a light wobble → child reads & names the feeling → **breathe with / comfort /
cheer on** → Milo calms, thanks the child, bridges the skill back → **Milo checks on the child** →
**both grow** along one shared arc (Journey shows Milo *and* the child evolving side by side).
Plus **Talk with Milo** — a warm, safe conversation (see *Talk & voice* below).
- **Co-regulated breathing — the lead feature.** Milo breathes *with* the child (in 4 · hold 2 ·
  out 6), the creature expanding and contracting inside a soft halo. Optional **gentle haptics**
  pulse in time with the breath where the device supports it (Android/Chrome; iOS ignores it and it
  degrades silently) — the closest digital stand-in for soothing contact, and easy to switch off.
  This is the single most evidence-supported, screen-deliverable mechanism (see
  [`support-animal-research.md`](support-animal-research.md)), so it leads the home screen.
- **Other care actions that are coping skills** — **name the feeling**, **nourish**, **rest**.
- **Small real-life quests** framed as gentle adventures — log them, the pet responds and grows.
- **A 5-stage pet evolution** — Curled → Awake → Steady → Brave → Radiant — earned by genuine
  care, never by streaks or pressure. The bond never decays; skipping a day costs nothing.

## Talk & voice — the companion brain

Milo actually converses, warmly and safely, with a **three-layer brain**:

1. **Crisis safety first, always.** Every message the child sends is scanned *on-device* for
   self-harm / harm / danger signals **before** anything else. On a hit, Milo replies warmly and
   immediately opens the crisis off-ramp (tell-a-trusted-grown-up + resources) — distress is **never
   left to the creature alone**, regardless of which brain is active.
2. **Built-in reflective brain (default, free, fully private).** With no key connected, Milo replies
   using an on-device reflective responder — it recognises feelings and topics (sad, worried, angry,
   school, friends, family…), validates them, and offers a coping step. Nothing leaves the device.
3. **Optional free AI helper (Gemini or Groq).** A grown-up can paste a **free-tier** API key in
   *Talk → Grown-up setup*. Milo then chats more naturally via a strong child-safety system prompt
   (short, warm, never diagnoses, redirects to a trusted adult). The key is stored **only on the
   device**, never committed to this repo; only the chat message is sent to the chosen service.
   Gemini is recommended (it works directly from the browser). Falls back to the built-in brain on
   any error.

**Free browser voice (no key):** Milo can **speak** its replies (Web Speech `speechSynthesis`,
toggleable) and the child can **talk** to Milo with a mic button (`SpeechRecognition`, where the
browser supports it — e.g. Chrome/Edge; degrades silently elsewhere).

## Non-negotiables baked in

- **Trauma-informed & warm** — no alarms, no shame, no punishment for skipping. Calming colours,
  no alarming reds (warmth + crisis use amber).
- **Privacy-first** — no accounts, no social features; everything stays on-device (`localStorage`).
  By default **nothing leaves the device**; the *only* outbound data is chat messages, and *only*
  when a grown-up opts in to an AI helper (see above). Designed with **COPPA** in mind. A **Reset**
  control erases everything.
- **Not medical** — a clear, gentle disclaimer; Milo is a companion, not a clinician.
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
- `support-animal-research.md` — the evidence review (therapeutic/ESA animals for at-risk kids
  6–14) that grounds the design: breathing-first, non-judgmental presence, no streaks, crisis-aware.
- `Brand/logos/` — approved Grok-generated key art for the creature (warm, soft, abstract,
  uncanny-valley-safe). Marketing/brand use; the *in-app* character is hand-authored inline SVG so
  it can animate across all five stages and mirror mood — a static render can't.

## Tech

Single self-contained HTML PWA. Google Fonts (Quicksand display + Nunito body). On-device
`localStorage` persistence with a reset control. No backend, no tracking, no analytics. Runs fully
offline after first load (the built-in brain needs no network). The optional AI brain calls
Gemini (`generativelanguage.googleapis.com`) or Groq (`api.groq.com`) directly from the browser —
no server — using a free key the user supplies; both are allow-listed in the CSP `connect-src`.
Voice uses the browser-native Web Speech API (free, no key).

---

© 2026 **3Shamrocks Studio.** All rights reserved. · Milo™ — a 3Shamrocks Studio app.

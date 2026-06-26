# Milo — Audit (v0 prototype)

Self-audit of the PoC against the 3Shamrocks standard for a product aimed at vulnerable children
(~ages 6–14). Scope: this single-file PWA only. **This is a design prototype, not a clinically or
legally cleared product** — see "Open items / real next phase" at the end.

## Safety & tone

| Check | Status | Notes |
|------|:------:|------|
| Never claims to be a therapist/doctor | ✅ | "I'm a friend, not a doctor" in onboarding + About; About card "A friend, not a doctor". |
| Crisis off-ramp on lowest mood | ✅ | "Really not okay" → warm panel: thanks child, steers to a trusted adult, lists helplines, names emergency services. |
| Crisis panel reachable any time | ✅ | "Talk to someone who can help" button in About. |
| Non-alarming visual language | ✅ | No alarming reds; crisis uses warm amber. Verified palette in CSS. |
| No medical advice / diagnosis | ✅ | Copy validates feelings, never diagnoses or prescribes. |
| No shame / no streaks / no decay | ✅ | Bond never decays; "maybe later" is zero-cost; no streak meters. |
| Crisis numbers honestly marked | ✅ | Each resource tagged `needs verification` / `configure per region`; copy says a grown-up must confirm. |
| No dark patterns / engagement-maxxing | ✅ | No notifications, no FOMO, no daily-streak pressure, no upsell. |

## Privacy (minor data)

| Check | Status | Notes |
|------|:------:|------|
| No accounts / no sign-up | ✅ | None present. |
| localStorage only by default | ✅ | Single namespaced key `milo.v1`; no network writes by default. The built-in brain is fully on-device. |
| No PII solicited | ✅ | First name / nickname optional; explicitly never asks last name, address, school, photos. |
| User-erasable | ✅ | About → "Reset — erase everything" clears the key and restarts. |
| No analytics / trackers / third-party beacons | ✅ | No analytics. Outbound requests are limited to Google Fonts, and — only if a grown-up opts in — the chosen AI helper. |
| Optional AI helper is transparent + opt-in | ✅ | Off by default. Key is grown-up-entered, stored only on-device (in `milo.v1`), **never committed** to the repo and never sent anywhere by us. When connected, only the child's chat message goes to Gemini/Groq. About + setup copy state this plainly; can be disconnected any time. CSP `connect-src` pins exactly the two allowed hosts. |

> Note: Google Fonts is one off-device fetch; the optional AI helper is the other (opt-in only).
> For a strict no-third-party posture, self-host fonts and proxy/disable AI before real use.
> Flagged, not hidden.

## Accessibility (WCAG AA — prototype level)

| Check | Status | Notes |
|------|:------:|------|
| Semantic landmarks / roles | ✅ | `nav[aria-label]`, headings, `role=dialog`/`aria-modal` on sheets, `role=img`+`aria-label` on pet SVG. |
| Reduced motion respected | ✅ | `@media (prefers-reduced-motion:reduce)` disables the breathing animation. |
| Text scales / responsive | ✅ | rem-based; mobile-first, centers in desktop frame. |
| Color contrast | ⚠️ | Ink on light cards passes AA; faint helper text (`--ink-faint`) is decorative-weight — verify against AA for any text treated as essential. |
| Keyboard / focus | ⚠️ | Native buttons are focusable/operable; no explicit focus trap in the bottom-sheet modal. Acceptable for v0, should be added for production. |

## Security

| Check | Status | Notes |
|------|:------:|------|
| No `eval` / no dynamic code | ✅ | `grep` confirms none. |
| User text rendered safely | ✅ | All dynamic/user text via `textContent`; `innerHTML` used only for trusted static inline SVG, never user data. |
| CSP present | ✅ | Meta CSP: `object-src 'none'`, `base-uri 'none'`, `frame-ancestors 'none'`; scripts/styles inline (single-file) — a production build should move to nonce-based CSP. |
| Service worker scoped safely | ✅ | Network-first navigation; evicts foreign caches/workers on the shared `*.github.io` origin so a sibling project can't hijack a child mid-session. |
| Console errors | ✅ | Zero (see TEST.md). |

## Branding

- ✅ 3Shamrocks logo shown on a **dark-grey chip** (per brand rule), `studioFooter()`.
- ✅ © 2026 3Shamrocks Studio footer on every screen; "Milo™ — a 3Shamrocks Studio app".
- ✅ Approved **Grok creature key art** added in `Brand/logos/` (warm, soft, abstract, on-palette,
  uncanny-valley-safe). Brand/marketing asset only.
- ⚠️ **In-app character is intentionally hand-authored inline SVG**, not the raster render, so it
  can animate across five stages and mirror mood. The app icon (`icon.svg`) is the pet's face.
  A polished standalone wordmark/logo remains a full-product design task — **not faked here.**

## What changed in this pass (June 2026, post-research)

Grounded in the just-completed [`support-animal-research.md`](support-animal-research.md), which
names **co-regulated breathing** as the #1 transferable, screen-deliverable mechanism:

- ✅ **Breathing promoted to the lead feature** — a prominent hero card above the other care
  actions on the home screen.
- ✅ **The creature now visibly co-regulates** — it breathes *with* the child (expand/contract
  inside a soft halo) for the whole exercise, not just at the end.
- ✅ **Gentle, opt-out haptics** synced to the breath (the research's named closest substitute for
  soothing contact). Feature-detected; silent no-op on devices/browsers without the Vibration API
  (e.g. iOS Safari); never used for alarms or pressure.
- ✅ **Honest "evidence-informed, not a treatment" note** added to About — accurate framing, no
  overclaiming, reinforcing the trusted-adult off-ramp.
- ✅ Reduced-motion respected in the breathing animation; zero console errors after changes.

## What changed in the full-completion pass (June 2026)

- ✅ **Talk with Milo — a real conversation.** New tab. A **three-layer brain**: (1) on-device
  crisis/harm scan on *every* message → warm reply + crisis off-ramp (verified: "i want to die"
  intercepts and routes to a grown-up, never handled by the creature alone); (2) a built-in
  reflective responder (free, fully private, recognises feelings/topics and offers a coping step);
  (3) an **optional free AI helper** (Gemini/Groq) connected by a grown-up with their own free key.
- ✅ **AI is safe + private by design.** Strong child-safety system prompt (warm, short, never
  diagnoses, redirects to a trusted adult, never claims to be human). Key stored only on-device,
  **never committed**; only the chat message is sent, and only when opted in. Gemini path verified
  end-to-end (correct request/parse; falls back to the built-in brain on any error). CSP pins the
  two allowed hosts. About + setup copy disclose the data flow plainly.
- ✅ **Free browser voice.** Milo can speak replies (`speechSynthesis`, toggle) and the child can
  talk via mic (`SpeechRecognition`), both feature-detected and degrading silently.
- ✅ **Branded to the canonical 3SDS `[data-brand="milo"]`** — warm cream, soft sage, peach-coral
  hero, Quicksand + Nunito; the "no alarming reds" safety rule preserved (warmth/crisis = amber).
- ✅ **Dev text removed** ("Prototype v0" chips, version language) — replaced with product-grade,
  still-honest safety copy. © 2026 3Shamrocks Studio + small 3S logo present on every screen.
- ✅ Verified at **390×844**, zero console errors across chat, crisis, breathing, check-in, growth,
  Journey, About, and setup.

## Open items / real next phase (must precede any real-child use)

1. **Clinical review** of every line of copy by child/adolescent psychologists + trauma specialists.
2. **Verified, localized crisis resources** with an escalation protocol — replace all placeholders.
3. **COPPA / GDPR-K legal + child-safeguarding review.**
4. **Trusted-adult oversight layer** (privacy-preserving, non-surveillant).
5. **Independent security/privacy/ethics audit**; self-hosted fonts; nonce-based CSP.
6. **Accessibility hardening** (focus trap in modals, full contrast pass) + localization incl. RTL.
7. **Supervised device testing** with the target age groups before release.

See [`CONCEPT.md`](CONCEPT.md) for the full design and the complete PoC-vs-product gap.

---
© 2026 3Shamrocks Studio. All rights reserved.

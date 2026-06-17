# Milo — Test Log (v0)

Manual verification of the PoC, run against a local static server (`python3 -m http.server`) in a
headless preview browser, then confirmed live on GitHub Pages.

## Environment
- Single-file PWA served statically; no build step.
- Checks: console-log capture, accessibility-tree snapshot, screenshots, scripted interaction.

## Results

| # | Test | Method | Result |
|--:|------|--------|:------:|
| 1 | App boots, title correct | Load `index.html` | ✅ "Milo — Milo grows with you" |
| 2 | No console errors/warnings | Capture across full session | ✅ Zero logs |
| 3 | Onboarding renders | a11y snapshot + screenshot | ✅ Pet, gentle promises, "friend not a doctor", begin button |
| 4 | Brand header + studio footer | Snapshot | ✅ "Milo", "Milo™ — a 3Shamrocks Studio app", © 2026 |
| 5 | Onboarded Today screen | Inject state (stage 3) + reload | ✅ Stage-3 pet, personalized "Hi Sam", mood picker, tabs |
| 6 | Pet evolution / stage art | Render stages 1–5 | ✅ Distinct art per stage; greener/brighter as it grows |
| 7 | Crisis off-ramp | `pickMood('crisis')` | ✅ Warm panel, steer to trusted adult, helplines marked "needs verification", emergency note |
| 8 | Privacy posture | Inspect storage + network | ✅ Single `milo.v1` key; only off-device request is Google Fonts |
| 9 | Reduced motion | CSS media query present | ✅ Breathing animation disabled under `prefers-reduced-motion` |
| 10 | No eval / safe DOM | `grep` source | ✅ No `eval`; user text via `textContent` |
| 11 | Live URL serves 200 + renders | `curl` + fetch on Pages URL | ✅ See deploy verification below |

## Live deploy verification
- URL: https://3shamrocksstudio.github.io/milo-app/
- HTTP status: **200**
- Renders the onboarding screen with no console errors.

## Not covered (acknowledged)
- Automated unit/e2e tests (none — prototype).
- Cross-browser/device matrix beyond the preview engine.
- Screen-reader pass and modal focus-trap (flagged in [`AUDIT.md`](AUDIT.md)).
- Full WCAG contrast audit of decorative-weight helper text.

---
© 2026 3Shamrocks Studio. All rights reserved.

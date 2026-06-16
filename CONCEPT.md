# Tend — Concept Note

> **the friend who grows with you**
>
> A concept prototype (v0) by 3Shamrocks Studio. This document captures the idea, the design,
> the non-negotiables, and an honest account of what this proof-of-concept does versus what a
> real, safe-to-ship product would require.

---

## The name

**Tend.** To *tend* is to care for something gently and continuously — a garden, a fire, a
creature, a friend. The word holds the whole product in one syllable: small daily acts of care
that, over time, grow something resilient. The child tends the companion; in doing so, they
practice tending themselves.

Tagline: **the friend who grows with you.**

---

## The pet

A soft, round, **gender-neutral** creature with big, calm eyes. It is **"dog-hearted"** —
loyal, attuned, and non-judgmental — but deliberately a **blank-slate** creature, not a literal
dog, so any child (boy or girl, 6–14) can project their own friend onto it. A subtle heart marking
on its belly ties it, quietly, to the 3Shamrocks green-heart mark.

The pet **learns** from the child (remembers their name, a nickname, an age band, one thing that
makes them feel calm, and their recent moods) and **talks back** warmly in short, plain language.
It **mirrors the child's mood** — its eyes soften and its posture lowers when the child is having a
hard day — and it **models calm** during the breathing exercise (co-regulation).

All pet art is hand-authored inline SVG so the app is fully self-contained and on-brand.

### The 5-stage evolution arc

Earned by *genuine engagement* — caring actions, coping practice, and real-life quests — **never**
by points-chasing, streaks, or pressure. The bond never decays; skipping days costs nothing.

| Stage | Name | Meaning |
|------:|------|---------|
| 1 | **Curled / shy** | Just arrived. Needs warmth and trust. Eyes half-closed, tucked, muted colour. |
| 2 | **Awake / curious** | Begins to bond and "talk back." Eyes open, ears perk, colour warms. |
| 3 | **Steady** | Calm-together / co-regulation. Relaxed, content, softly green. |
| 4 | **Brave** | Tries challenges alongside the child. Stands taller, small explorer's scarf, faint aura. |
| 5 | **Radiant** | Grown and resilient — reflects the child's own growth. Glowing, brightest, sparkles. |

Progress is shown as a soft "growing-together" vine, **not** a countdown or a streak meter — a
sense of momentum without anxiety.

---

## The core loop

1. **Gentle daily check-in** — *"How are you today?"* A simple, no-pressure feeling picker
   (Great · Good · Okay · Not great · Really not okay) with an "I'd rather not say" escape hatch.
   Then: *"Let's check on [pet]."*
2. **Care actions that double as coping skills:**
   - **Breathe together** — a paced breathing animation (in 4s · hold 2s · out 6s, 3 rounds).
     The child follows the circle; the pet breathes too. This is real co-regulation.
   - **Name the feeling** — emotional-literacy practice: pick the feeling that's here; the pet
     validates it as "a visitor that will move along."
   - **Nourish** — self-care nudge (water, a snack, fresh air, a stretch).
   - **Rest** — permission to slow down; the pet curls up with the child.
3. **A small real-life quest, framed as a gentle adventure** — e.g. *"do one kind thing,"*
   *"try the hard thing for 2 minutes,"* *"tell a trusted grown-up one true thing,"* *5-4-3-2-1
   grounding.* The child logs *"I did it"* (or *"maybe later,"* with zero shame) → the pet
   responds and grows.
4. **The pet reflects the child's mood and mirrors calm** throughout.

This builds **real strength** — it is explicitly **not escapism**.

---

## Non-negotiables (baked in)

- **Trauma-informed + warm.** No harsh alarms, no failure or shame states, no punishment for
  skipping a day. The pet waits patiently and welcomes the child back without guilt. Soothing,
  psychologically-sensible palette: soft greens/blues for calm, warm amber for connection;
  **no alarming reds** anywhere — even the crisis off-ramp uses warm amber.
- **Privacy-first / safety.** **No accounts, no sign-ups, no social features, no social exposure.**
  Everything is **on-device** (`localStorage` only); **nothing leaves the device.** A clear,
  age-appropriate privacy note is included, and a **Reset** control erases everything. Designed
  with **COPPA** in mind — minimal data, and only a first name / nickname *if the child chooses*.
- **Not a medical or therapy product.** A clear, gentle note states Tend is a supportive
  companion — not a doctor, therapist, or emergency service, and not a replacement for one.
- **Crisis-aware off-ramp.** If the child picks the lowest feeling ("Really not okay"), the pet
  responds with warmth and gently encourages telling a trusted adult, and surfaces a calm
  *"Talk to someone who can help"* panel. The same panel is always reachable from **About**.
- **Inclusive.** Gender-neutral throughout; works for boys and girls 6–14; complexity scales
  (simpler microcopy for the 6–8 band).
- **Mobile-first**, and presentable in a desktop preview frame.

---

## Safety framing & the crisis off-ramp

The crisis panel is intentionally calm, not alarming. It (1) thanks the child for sharing,
(2) encourages telling a trusted grown-up (parent, teacher, counselor, family member) and notes
they can show this screen, (3) lists helplines, and (4) states plainly that Tend cannot help in
an emergency and to contact local emergency services.

**Crisis resources are placeholders and are clearly marked `needs verification` / `configure per
region`.** For Israel the prototype *notes* ERAN (reported 1201) and 105 (child/youth protection)
**as unverified examples only** — they are not presented as final, vetted numbers. **No unverified
number may ship as authoritative.** The full product must localize and professionally verify every
crisis resource per region before launch.

---

## What this PoC does vs. what the full product needs

### What this proof-of-concept demonstrates
- The full core loop: onboarding (meet + name your companion) → daily check-in → a care/coping
  action → a real-life quest → the pet visibly evolving a stage.
- The tone: warm, patient, trauma-informed, shame-free.
- The pet, its personality ("talks back," remembers, mirrors mood), and the 5-stage evolution.
- Co-regulation breathing as a genuine, usable exercise.
- The privacy model (fully on-device, no accounts, reset) and the safety/crisis framing.
- 3Shamrocks branding and a self-contained, installable PWA.

### What the full product still needs (honest list)
- **Professional psychological review.** A real content library co-designed and reviewed by
  **child & adolescent psychologists** and trauma specialists — every line of microcopy, every
  quest, every response, vetted for clinical soundness and developmental fit.
- **Real, verified crisis resources**, localized per country/region, reviewed by professionals,
  with a clear escalation protocol — replacing all `needs-verification` placeholders.
- **Safeguarding & duty-of-care design** — guidance on what the app does (and does not) detect,
  how it routes a child toward human help, and explicit limits (it is not monitoring or a
  reporting tool).
- **Evidence base** — grounding the skills (paced breathing, affect labeling, grounding,
  behavioral activation) in the research literature, ideally with outcome evaluation.
- **Accessibility & localization** — screen-reader passes, dyslexia-friendly options, reduced-
  motion (partially handled), full multi-language support including RTL.
- **Caregiver layer** (carefully designed, privacy-preserving) — optional age-appropriate ways a
  trusted adult can be looped in, without surveillance.
- **Robust content scheduling** — a larger, rotating, age-banded library of quests and reflections.
- **Independent safety, security, and privacy audit**; COPPA / GDPR-K legal review; an ethics
  review for working with at-risk and vulnerable children.
- **Real device testing with the target age groups**, with clinicians observing, before any release.

> Tend is a **prototype** to demonstrate a caring idea. It is **not** ready to be used as real
> support for a child in distress. Treat it as a design artifact, not a clinical tool.

# Milo — Concept Note

> **Milo grows with you**
>
> A concept prototype (v0) by 3Shamrocks Studio. This document captures the idea, the design,
> the non-negotiables, and an honest account of what this proof-of-concept does versus what a
> real, safe-to-ship product would require.

---

## The name

**Milo.** A warm, friendly, gender-neutral name a child can say easily and make their own — the
name of a friend, not a feature. The companion is always introduced simply as *Milo, your friend.*

But the name carries a quiet secret. **M.I.L.O. spells "My Inner Little One."** The child never
learns this up front. As the companion evolves through its five stages, **one letter's meaning is
revealed at a time** — M when Milo first wakes, then I, then L, then O — with the full phrase
*My Inner Little One* blooming at the final **Radiant** stage. The reveal lands a gentle truth:
caring for Milo has been a way of caring for the gentle little one inside themselves. The egg is
optional and self-contained — clearing the letter list disables it without affecting the rest of
the app.

Canon: **Milo** · domain **milo.pet** · hidden **M.I.L.O. = My Inner Little One**.

Tagline: **Milo grows with you.**

---

## The pet

A soft, round, **gender-neutral** creature with big, calm eyes. It is **"dog-hearted"** —
loyal, attuned, and non-judgmental — but deliberately a **blank-slate** creature, not a literal
dog, so any child (boy or girl, 6–14) can project their own friend onto it. A subtle heart marking
on its belly ties it, quietly, to the 3Shamrocks green-heart mark. The child gives Milo their own
chosen name during onboarding (Milo is the product; the pet is theirs).

The pet **learns** from the child (remembers their name, a nickname, an age band, one thing that
makes them feel calm, and their recent moods) and **talks back** warmly in short, plain language.
It **mirrors the child's mood** — its eyes soften and its posture lowers when the child is having a
hard day — and it **models calm** during the breathing exercise (co-regulation).

All pet art is hand-authored inline SVG so the app is fully self-contained and on-brand.

### The 5-stage evolution arc

Earned by *genuine engagement* — caring actions, coping practice, and real-life quests — **never**
by points-chasing, streaks, or pressure. The bond never decays; skipping days costs nothing. Each
new stage also unlocks one letter of the M.I.L.O. secret.

| Stage | Name | Meaning | Letter |
|------:|------|---------|:------:|
| 1 | **Curled / shy** | Just arrived. Needs warmth and trust. Eyes half-closed, tucked, muted colour. | — |
| 2 | **Awake / curious** | Begins to bond and "talk back." Eyes open, ears perk, colour warms. | **M** — My |
| 3 | **Steady** | Calm-together / co-regulation. Relaxed, content, softly green. | **I** — Inner |
| 4 | **Brave** | Tries challenges alongside the child. Stands taller, small explorer's scarf, faint aura. | **L** — Little |
| 5 | **Radiant** | Grown and resilient — reflects the child's own growth. Glowing, brightest, sparkles. | **O** — One |

Progress is shown as a soft "growing-together" vine, **not** a countdown or a streak meter — a
sense of momentum without anxiety.

---

## The core loop — *the flip* (the defining design choice)

Milo **flips the usual companion dynamic**: instead of the app asking the child *"how do you
feel?"*, **Milo is the one having a hard moment, and the child is the helper.** This is grounded in
the **helper-therapy principle** — when a child cares for a vulnerable other, they build their own
agency, resilience, and self-worth. By helping Milo, the child *rehearses and internalises the very
same coping skills*, and feels **capable** rather than "fixed." The empowerment is the mechanism.

1. **Milo shares a hard moment and invites help.** Milo expresses a feeling in an age-appropriate,
   embodied way (*"My tummy feels all fluttery, and I keep thinking about tomorrow. Will you help
   me?"*) — rotating across worried · sad · scared · overwhelmed · lonely · frustrated · embarrassed.
2. **The child coaches Milo through it** — the same coping skills, now child-as-helper:
   - **Read & name Milo's feeling** — emotional-literacy practice (no wrong answer; Milo affirms
     the child's read: *"You really see me"*).
   - **Choose how to help:**
     - **Breathe with Milo** — *the lead co-regulation feature.* Paced breathing (in 4 · hold 2 ·
       out 6); the creature expands/contracts inside a soft halo and calms *because the child
       breathes too*. Optional **gentle haptics** (feature-detected; silently absent on iOS Safari).
     - **Comfort Milo** — the child picks kind, soothing words to give Milo.
     - **Cheer Milo on** — the child reframes/encourages, helping Milo feel brave.
   - **Milo visibly calms, thanks the child, and reflects the skill back:** *"You just did the very
     thing that helps when YOU feel this way too — you're really good at this."*
3. **A gentle "and how are you, helper?" self-check** stays — *secondary*, and still routes the
   lowest feeling straight to the crisis off-ramp. **The helper framing never suppresses the child's
   own distress signal** (see Non-negotiables).
4. **Name a feeling · Take care · Rest together** — supporting "ways to be there for Milo."
5. **A small real-life quest** (*do one kind thing · try the hard thing for 2 minutes · tell a
   trusted grown-up one true thing · 5-4-3-2-1 grounding*) — logged with zero shame; the bond grows.

The pet mirrors calm throughout, and the **M.I.L.O. = "My Inner Little One"** reveal lands deeper
under the flip: by caring for Milo, the child has been caring for the gentle little one inside
*themselves*. This builds **real strength** — it is explicitly **not escapism**.

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
- **Not a medical or therapy product.** A clear, gentle note states Milo is a supportive
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
they can show this screen, (3) lists helplines, and (4) states plainly that Milo cannot help in
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
- The pet, its personality ("talks back," remembers, mirrors mood), the 5-stage evolution, and the
  quiet M.I.L.O. = "My Inner Little One" reveal.
- Co-regulation breathing as a genuine, usable exercise.
- The privacy model (fully on-device, no accounts, reset) and the safety/crisis framing.
- 3Shamrocks branding and a self-contained, installable PWA.

### What the full product still needs (honest list — the real next phase)
- **Professional psychological review.** A real content library co-designed and reviewed by
  **child & adolescent psychologists** and trauma specialists — every line of microcopy, every
  quest, every response, vetted for clinical soundness and developmental fit.
- **Real, verified crisis resources**, localized per country/region, reviewed by professionals,
  with a clear escalation protocol — replacing all `needs-verification` placeholders.
- **Child-safety & COPPA/GDPR-K review** — formal legal and safeguarding review before any child
  uses this as real support.
- **A trusted-adult oversight layer** — carefully designed, privacy-preserving ways a parent,
  carer, or clinician can be appropriately looped in, **without surveillance** of the child.
- **Safeguarding & duty-of-care design** — guidance on what the app does (and does not) detect,
  how it routes a child toward human help, and explicit limits (it is not monitoring or a
  reporting tool).
- **Evidence base** — grounding the skills (paced breathing, affect labeling, grounding,
  behavioral activation) in the research literature, ideally with outcome evaluation.
- **Accessibility & localization** — screen-reader passes, dyslexia-friendly options, reduced-
  motion (partially handled), full multi-language support including RTL.
- **Robust content scheduling** — a larger, rotating, age-banded library of quests and reflections.
- **Independent safety, security, and privacy audit**; an ethics review for working with at-risk
  and vulnerable children.
- **Real device testing with the target age groups**, with clinicians observing, before any release.

> Milo is a **prototype** to demonstrate a caring idea. It is **not** ready to be used as real
> support for a child in distress. Treat it as a design artifact, not a clinical tool.

---

© 2026 **3Shamrocks Studio.** All rights reserved. · Milo™ — a 3Shamrocks Studio app.

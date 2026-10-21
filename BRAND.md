# Milo — Brand & Creature Direction (v1)

Owned in-house. Grok is the render engine; the *direction, curation, colour-grade
and system* are ours. Never ship raw first-draft AI.

## The creature
A small **invented companion creature** — soft felted-wool plush, dog-*hearted*
but not a literal breed, so any child can project their own friend onto it.
Rounded huggable body, oversized soft head, low drooping ears, cream belly with a
small **honey heart** on the chest, large gentle cocoa eyes, rosy cheeks, warm smile.
Matte velvet plush finish, soft warm studio light. Cozy, tactile, endearing —
never scary, uncanny, or glossy-3D.

## Growth arc (the art *is* the progression)
| Stage | Name | Look |
|---|---|---|
| 1 | Curled | asleep in a ball, **muted dusty greige**, shy |
| 2 | Awake | small, eyes opening, **soft apricot** warming |
| 3 | Steady | sitting content, **clear warm apricot** |
| 4 | Brave | tall & alert, honey scarf, **rich terracotta-apricot** |
| 5 | Radiant | standing joyful, honey scarf, soft glow, **deepest warm terracotta** |

Assets: `art/milo-{1..5}.webp` (neutral) plus **expression variants** `art/milo-{2..5}-happy.webp` and `art/milo-{2..5}-sad.webp` — background-keyed, trimmed, 400×400, ~416 KB total. Stage 1 is always the curled sleeper (no variants).

## Expressions (mood mirroring)
Milo visibly reflects its emotional state so the care loop reads instantly: a gentle, pleading **sad** face when it needs you (soft, never distressing), a beaming **happy** face once comforted/tapped, and the calm **neutral** otherwise. `petSVG(stage, mood)` maps low/crisis→sad, great/good→happy, else neutral.

## Palette (3SDS `[data-brand="milo"]`, tuned to the creature)
Warm oat cream world · **terracotta** hero `#E2673C` · **honey** amber `#E9A23B`
· moss sage growth `#6FA96F` · deep cocoa ink `#3A281F`.
**Safety rule:** no alarming reds anywhere — the hero is a warm terracotta, and
crisis/warmth uses amber.

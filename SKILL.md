---
name: she
description: >-
  Use when generating or iterating photorealistic waist-up short videos of an
  East Asian adult woman in loungewear/pajamas, or when the user says she / @she
  to make or tweak a clip (face, vibe, outfit).
---
# she — photorealistic waist-up woman short video

Generate with Grok Imagine (`GenerateVideo`). Deliver each clip first via `SendToUser` `type:attachment`, then one short note.

**All prompts must be English only.** Do not submit Chinese prompt text to `GenerateVideo`.

## Defaults
- `duration`: 15 (tool max; if user asks longer, say one take maxes at 15s)
- `aspect_ratio`: `9:16`
- `resolution`: `720p`
- Framing: waist-up
- Look: photorealistic, soft window light, shallow depth of field, subtle natural motion, slow camera push-in

## Default subject & outfit (override from user)
- Young East Asian adult woman, long straight black hair
- Black lightweight silky lace V-neck pajama top + matching skirt
- Natural warm smile; default vibe: refined pretty; switchable to cute / cool elegant

## English prompt template
Fill brackets from the current request:

```
Photorealistic cinematic waist-up of a young East Asian adult woman with a [cute soft / cool elegant / refined] pretty face, long straight black hair. Black lightweight silky lace V-neck pajama top and matching black skirt, soft sheen, elegant tailored cut. [Sweet warm smile / cool reserved half-smile / natural warm smile]. Soft morning window light, shallow depth of field. Subtle blink and slight head turn. Slow camera push-in. Elegant modest fashion photography.
```

## Vibe swaps
| User ask | face | smile / motion |
|---|---|---|
| cute | cute soft pretty face | Sweet warm smile + slight head tilt |
| cool / 冷艳 | cool elegant pretty face | cool reserved half-smile |
| refined / default | refined pretty face | natural warm smile |
| new face | change face wording only; keep outfit block | same vibe |
| ~120 jin / ~60kg figure | Healthy slim build about 60kg, graceful silhouette (no explicit body-focus wording) | — |

## Outfit tweaks
- Black fabric / lace / silky / deep V: keep `lightweight silky lace` + `V-neck` or `deep V-neck`
- With skirt: `matching … skirt`
- Camisole: prefer `sleeveless camisole tank top pajama upper`; if blocked, fall back to camisole / V-neck pajama top

## Safety & retry
Often blocked: strap-heavy camisole wording, sheer/see-through, blunt body-line emphasis, overtly sexual phrasing.
On block:
1. Drop sheer/body-line phrasing; use `elegant tailored cut` / `graceful silhouette`
2. Soften `deep V-neck` to `V-neck`
3. Keep color + fabric, simplify adjectives, retry once
4. Tell the user what softened; never invent a clip

## Workflow
1. One-line ack of the change, then `GenerateVideo` with an **English-only** prompt
2. For multi-face batches, run 2–3 in parallel; vary face only
3. Attach every success; say which failed if blocked
4. Persist lasting recipe changes by rewriting this skill; do not bake one-off paths or names into it

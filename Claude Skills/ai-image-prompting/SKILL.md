---
name: ai-image-prompting
description: >-
  Writes, upgrades and diagnoses prompts for AI image generators (GPT Image, Nano Banana, Midjourney,
  Flux and similar) using the six-part method - subject, environment, camera, lighting, mood, style -
  plus realism cues, reference instructions and the cinematic-versus-phone mode split. Use whenever
  the user wants a still image prompt or a better one: "write an image prompt", "improve this prompt",
  "make this look realistic", "why does my image look fake / plastic / AI", "product shot", "portrait
  prompt", "thumbnail", "cinematic still", "mirror selfie", "prompt for this reference image". Do NOT
  use for motion or video prompts (use ai-video-prompting), a recurring character or influencer (use
  ai-avatar-builder), ad scripts and hooks (use ugc-ad-creator), or a full film (use ai-filmmaking).
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 2 (prompt framework) and Phase 3 (images, realism, prompt banks)
---

# AI Image Prompting

Prompting is direction, not description. Every blank you leave is a decision the model makes for you, and it always picks the most average version of the idea. The difference between forgettable AI output and work that looks produced is almost never the model - it is how clearly the instruction was written.

A good prompt is not a longer prompt. A 200-word pile of adjectives can be worse than 35 words where every word is a decision.

## Critical rules

1. **Cover all six parts: subject, environment, camera, lighting, mood, style.** A generic result nearly always means one of the six is missing or vague. Diagnose by checking which one.
2. **Light needs a named source.** Not "warm lighting" but "a small warm table lamp on the left of frame lighting her face". Not "dramatic lighting" but "a single overhead light casting harsh shadows under his eyes". Real photographs have imperfect light - street lamps, headlights, phone screens, candles, overcast sky.
3. **Pick the mode before writing and never mix the vocabularies.** *Cinematic*: cinema body, chosen lens, shallow focus, film grade. *UGC/phone*: phone camera, around 24-26mm, deep focus, the room's own light, phone processing, no grade. Mixing them is why a "selfie" comes back looking like a studio portrait. See `references/ugc-phone-realism.md`.
4. **Put style and grade at the end**, after the scene exists. For realism, no style label at all is often the best choice - "realistic iPhone photo" is frequently enough.
5. **Avoid the plastic-render vocabulary:** "cinematic masterpiece", "hyper-detailed", "ultra-glossy", "perfect lighting", "8K masterpiece", "flawless", "award-winning". One realism trigger such as "ultra realistic" at the end is fine; never stack resolution and hype words. Realism comes from specific cues, not from "8K".
6. **State what a reference image is for.** "Keep the same face, hair, skin tone and body; change the outfit and location" beats uploading an image and hoping.
7. **Realism comes from restraint:** natural light, real skin texture and imperfection, muted colour, candid framing, slightly imperfect composition.
8. **Front-load what matters.** Models weight the start of a prompt more heavily. If a detail keeps being ignored, move it earlier and state it once, plainly.
9. **Mood is one or two words, and it changes everything.** The same diner at night is a different image at "peaceful and nostalgic" versus "tense and paranoid" - expression, colour, contrast, framing and body language all shift.

## Workflow

### Step 1: Understand the job
Establish (or sensibly assume and state) the goal, platform and aspect ratio - 9:16 for TikTok, Reels and Shorts; 4:5 or 1:1 for feed; 16:9 for YouTube and cinematic - whether realism or a stylised look is wanted, and whether references exist.

Then pick the **mode**: cinematic, or UGC/phone for anything meant to look like a real person filmed it.

If the idea itself is weak, strengthen it before writing the prompt. Idea-development and critique prompts are in `ai-creator-workflow/references/chat-prompts.md`.

### Step 2: Climb the prompt ladder
Add one layer at a time, starting from the seed idea:

1. **Subject.** A person: age, hair, clothing, expression, posture, what they are doing. A product: shape, material, colour, surface texture, label text, position. Vague subject, vague image.
2. **Environment.** A specific place, time of day, weather, background objects and textures. This is where story comes from - compare "a woman in a white studio" with "outside a nightclub at 1am in the rain", or "a man drinking coffee in a modern office" with "alone in a petrol station at 3am".
3. **Camera.** Angle (where the camera stands), shot size (how much we see), lens (how the space feels). Describe camera *position* as well as focal length, because distortion comes from distance. In UGC mode, say where the phone physically is: arm's length, propped on the counter, on the dashboard, held up to the mirror. Full tables in `ai-cinematography`.
4. **Lighting.** Source, hard or soft, direction, colour temperature, how materials react, and a catchlight that matches the source. Say "background darker than the subject" when separation matters.
5. **Mood.** One or two words.
6. **Style.** Optional, at the end. 24 styles with examples in `references/styles.md`.

Recipe: **[subject] in [environment], [camera angle and framing + lens], [light source and direction], [mood], [visual style or grade].**

For camera, light, depth and grade decisions, hand the shot to `ai-cinematography` - it returns the exact lines to drop in here.

### Step 3: Build depth into the frame
AI builds flat frames by default. Name a **foreground, midground and background**, and put something **in the air** (haze, steam, dust, rain). A soft out-of-focus foreground object is the single fastest fix for a flat image. Keep the subject off dead-centre, use leading lines, and leave lead room where the subject looks or moves.

In UGC mode the layers are everyday objects: hand or product near the lens, then face, then a lived-in room. For 9:16, keep face and product in the middle band, clear of captions and side buttons.

### Step 4: Add realism, when realism is the goal
Pull a few phrases from each group (full cheat-sheet in `references/realism.md`):

- **Photoreal triggers:** photorealistic, real-world photography, natural imperfections, true-to-life textures.
- **Camera and lens:** cinematic mode - "shot on a 35mm lens, shallow depth of field, natural bokeh". Phone mode - "iPhone front camera, around 26mm, arm's-length selfie, background slightly soft but recognisable", and no bokeh words unless you specifically say portrait mode.
- **Real light:** soft natural daylight with realistic shadows; or the named practical source.
- **Texture:** visible pores, fabric grain, slight asymmetry, flyaway hairs, no smoothing.
- **Restrained colour:** natural colour grading, muted tones, realistic contrast.
- **Optional negatives:** no CGI, no 3D render, no plastic skin, no text or watermark.

### Step 5: Output
Return:

1. The **final prompt** as one clean block, ready to paste.
2. A short **why this works** line naming the choices doing the work - the light source, the lens, the depth layer.
3. **Two variations**, each changing one lever only (angle, light, or mood), so the difference is readable.
4. When references are involved, a one-line **reference instruction**: what to preserve, what may change.

Offer a JSON version (subject, environment, camera, lighting, mood, style, negatives, final_prompt) only if the user wants structured output.

## Fixing a bad result
Diagnose before rewriting - the symptom names the missing part.

| Symptom | Likely cause | Fix |
|---|---|---|
| Plastic, airbrushed skin | No texture cues, beauty words present | Add pores, peach fuzz, natural blush, slight redness, "no smoothing"; delete "flawless" and "perfect" |
| Looks like a render | Evenly lit, no source | Name one light source and its direction; let one side fall into shadow |
| Flat, subject pasted on | Only subject plus background | Add a foreground layer and something in the air; move the subject off-centre |
| Generic or boring | Vague subject or environment | Make both specific: age, clothing, time of day, props, real place |
| Wrong face or product from a reference | Reference purpose never stated | Say exactly what to keep (face / outfit / packaging / label text) and what to change |
| Oversaturated, fake colour | "Colourful", neon or HDR words | Name specific colours and one mood palette; grade at the end |
| Inconsistent across a set | Light re-invented per shot | Anchor the light once; write it as one locked block and paste it into every prompt, changing only action and shot size |
| An important detail ignored | It was buried late | Move it near the start and state it once, plainly |
| Too busy, cluttered | Too many competing details | Cut details; keep one focal point |
| Composition boring | No camera direction | Add angle, shot size, framing, a foreground |
| Dead-looking eyes | No catchlight | Add a catchlight matching the named source |
| "Selfie" looks like a DSLR portrait | Cinema words on a phone shot | Switch fully to UGC mode: phone camera, deep focus, room light, phone noise, no grade |
| Product label warped or misspelled | Label not locked | Use the label-lock template in `ai-avatar-builder/references/product-in-hand.md` |
| Same person looks different each time | No character sheet | Build a passport in `ai-avatar-builder` and reference it every time |

Rewrite and follow-up commands ("make it less generic", "give me five stronger versions", "what will make this look fake") are in `ai-creator-workflow/references/chat-prompts.md`.

## Examples

**Weak:** "A cool photo of a girl."

**Strong:** "A candid photo of a woman in her late twenties with short dark hair and an oversized denim jacket, sitting at the counter of a tiny Tokyo ramen shop late at night. Steam rises from her bowl; warm overhead light hits the side of her face, the other side falling into soft shadow. Out-of-focus shelves of bowls and handwritten menus behind her. Shot from across the counter like an intimate documentary photo, 35mm lens, shallow depth of field. Quiet and cozy mood. Realistic 35mm film look, natural colour grading."

**Product:** "Premium frosted-glass cream jar with a brushed silver lid on mirror-polished black ice, a ring of frost around its base. Foreground: frost bloom, razor sharp, with the jar's reflection. Background: deep dark cold gradient. One soft top key light catching the silver lid, a controlled specular edge down the glass, deep surrounding shadows. Shot on medium format, maximum material detail. Muted cool grade, single orange accent. Ultra realistic."

**UGC/phone:** "A natural smartphone selfie taken inside a parked car during the day, framed shoulders-up, camera held slightly below eye level. She is in the passenger seat, head tilted back and turned slightly, eyes looking up as if daydreaming, one hand resting in her hair. Soft daylight from the side window, even across her face, no harsh shadows, light that feels unplanned. Skin texture fully preserved - visible pores, natural blush, light redness, real imperfections, no smoothing, no filters. Long dark hair slightly tousled, casual black sweatshirt. Car interior clearly visible, background softly out of focus, face sharp. Shot on a smartphone, slight natural grain, true-to-life colour. Candid and personal, indistinguishable from a real UGC selfie."

## Reference files (open only the one you need)
- `references/realism.md` - the full realism cheat-sheet, long worked prompts, upscaling before animation
- `references/ugc-phone-realism.md` - cinematic versus phone mode, phone depth-of-field logic, UGC prompt skeleton
- `references/styles.md` - 24 styles with example prompts
- `references/prompt-bank.md` - 70+ tested prompts to adapt; search by keyword (selfie, product, top-down, flash, mirror)
- `references/models-and-settings.md` - which image model suits which job, settings, references (dated; verify before relying on names)

Related: `ai-cinematography` for light, camera, depth and grade blocks; `ai-creator-workflow/references/chat-prompts.md` for idea development and rewrite commands.

Course material names particular apps and models. Apply the principles in whatever tool the user has, and never recreate a real person's face without their involvement.

---
name: ai-avatar-builder
description: >-
  Builds a consistent, believable AI person - AI influencer, UGC creator, brand face or film cast
  member - from a rough idea into a reusable identity. Covers persona definition, the base avatar
  prompt, the realism review, character sheets and passports that lock face, wardrobe and proportions,
  putting the same person in new scenes and outfits, avatar-holding-product shots with label lock, and
  running the persona as a content library. Use when the user says "create an AI influencer", "make an
  avatar", "character sheet", "character passport", "keep the same face", "same person in different
  scenes", "my avatar looks different every time", "avatar holding my product", "UGC creator for my
  brand", or "build a cast member". Do NOT use for one-off images with no recurring character (use ai-
  image-prompting), motion prompts (use ai-video-prompting), ad scripts (use ugc-ad-creator) or
  cloning the real user (use ai-clone-yourself).
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 3 (avatars, influencer studio, product images) and Phase 5 (passports)
---

# AI Avatar Builder

The goal is not one good image of a person. It is a believable digital human who can come back tomorrow, in a different outfit, in a different city, holding a different product, and still read as the same individual. That only happens when identity is written down and reused rather than re-described from memory each time.

Consistency is built in layers: persona, then one clean base image, then a passport that fixes every angle, then scenes that reference the passport.

## Critical rules

1. **Realism over perfection.** Plastic skin, studio light in a bedroom, and staged backgrounds are the giveaways. Natural light, real texture and a slightly imperfect frame beat a flawless render every time.
2. **One master reference drives everything.** Sharp, naturally lit, unfiltered, front-facing. Never mix references that look like two different people - the model averages them and you get a third person.
3. **Always say what to preserve and what may change.** "Keep her face, hair, skin tone and body proportions exactly as the reference; change the outfit and location" is the instruction. Uploading and hoping is not.
4. **Lock the details and repeat them word for word.** Wardrobe, hair, tattoos, jewellery, eyewear, headwear and proportions. Paraphrasing drifts; left alone, models make everyone slimmer and taller.
5. **Decide accessories once.** Glasses on in one shot and off in the next breaks a character faster than almost anything else.
6. **Build the avatar first, then combine with the product.** Products need their own clean reference plus the label text written out in the prompt.
7. **A recurring prop needs a passport too** - a bike, a bottle, a bag. A viewer will not notice the bat got longer, but they will stop believing the shot.
8. **Never recreate a real person's face.** Build a fictional individual, or work from the user's own likeness with their involvement (see `ai-clone-yourself`).

## Workflow

### Step 1: Define the persona
Pin down niche (fitness, luxury lifestyle, travel, skincare, fashion, UGC), age range, look, vibe, and what this person would naturally post. Keep it simple - a persona that can be described in four lines is one a model can hold onto. Ask for anything essential that is missing; otherwise choose sensible defaults and state them.

### Step 2: Write the base avatar prompt
Turn the persona into one detailed, realistic prompt:

- **Person:** age, features, hair, skin with visible texture and small imperfections, default expression, posture.
- **Setting:** everyday light with a named source and direction (window daylight from one side, a warm lamp), phone or 35-50mm camera language, candid framing, a catchlight that matches the source, and foreground / midground / background layers.
- **Negatives:** no smoothing, no filters, no CGI feel, no studio lighting where it would not exist.

For phone-style personas, follow `ai-image-prompting/references/ugc-phone-realism.md` - deep focus, phone camera, the room's own light, no cinematic grade. Generate several options rather than one. Tested prompts are in `references/ugc-avatar-prompts.md`.

### Step 3: Realism review
Before committing to a face, check:

- Skin has texture, pores and slight asymmetry; it is not airbrushed.
- Eyes look normal, with catchlights that match the light source.
- The lighting could actually exist in that place.
- The background is believable, not staged.
- The face would work across many scenes - not just this flattering one.
- Hands, teeth and ears survive a close look.

If it fails, regenerate rather than edit. This face is going to appear hundreds of times.

### Step 4: Lock the master reference
Pick the most natural, clearly lit, front-facing image. That file is now the identity. Store it somewhere you will not lose it, and reference *it* in future prompts rather than the most recent output - referencing yesterday's output is how a persona slowly becomes someone else.

### Step 5: Build the character passport
Generate the same person from several angles in one image, on a plain background, identical outfit and lighting in every panel: full-body front, full-body back, a large three-quarter medium, and a column of head-and-shoulders views (profile, three-quarter, frontal). 16:9 gives the panels room.

Fill two slots, in this much detail:

- **CHARACTER:** age, build, height, ethnicity, hair colour, length and how it sits, facial hair, skin tone and texture, tattoos and exactly where they fall, scars, piercings, teeth, default expression.
- **WARDROBE:** every garment by name, colour and material; logos and their exact placement (chest, back, sleeve); footwear; jewellery; headwear; eyewear. When a garment's shape matters, describe the shape rather than naming a brand.

Then lock: same wardrobe, same hair parting, tattoos in the same places at the same size, jewellery present in every shot or none, accessories decided once, build and height never changing.

Basic and extended passport prompts, the lock-down list and object sheets are in `references/character-passport.md`. When the passport goes into a shot prompt, add the line that stops the model copying the sheet itself: *all reference cards give appearance only - do not reproduce sheet layout, multiple views, panels, captions, grey backdrop or catalogue pose.*

### Step 6: New scenes with the same person
Scene formula: **same person (reference) + action + location + outfit + camera style + lighting + expression + realism details.**

> Realistic iPhone-style photo of the same woman from the reference, sitting on her bed in a red dress, soft natural daylight from the window, bright room, natural expression, candid lifestyle photo, realistic skin texture, no studio lighting. Keep her face, hair, skin tone and body exactly as in the reference.

Match the aspect ratio to the platform and keep it consistent across a batch. Pull camera, light and depth lines from `ai-cinematography` so a set of scenes shares one visual logic instead of being lit differently every time.

### Step 7: Avatar holding the product
Use both the avatar reference and a clean product reference. Write the exact label text, packaging, colour and material into the prompt, and give scale context ("fits in one hand, about the length of a phone"). Put the product closer to the lens and flat to camera when it is the hero, and state the focus order.

Before animating, check the label, scale, hands and angle. For labels that must be perfect, use the **label-lock template** in `references/product-in-hand.md`.

### Step 8: Run it as a content library
Plan a batch across post types - lifestyle, product, fitness, travel, mirror selfie, night out - rather than inventing each post. Keep the winning references together. Stills that pass the gates become video start frames; upscale before animating. Persona voice, caption style and batch planning are in `references/persona-content.md`, and the pass-based batching method is in `ai-creator-workflow/references/batching.md`.

## Output format
1. **Persona summary** - three to five lines.
2. **Prompts** in clean blocks, labelled by step: base avatar, character passport, scene 1, scene 2.
3. **Reference instruction** - which image to upload, what to preserve, what may change, and the "appearance only" line when a passport is attached.
4. **Realism checklist** whenever a new avatar is being created.

## Troubleshooting

| Problem | Fix |
|---|---|
| Face changes between images | Reference the passport, not the latest output; restate "keep the same face, hair, skin tone, body proportions"; remove conflicting references |
| Looks airbrushed or fake | Add visible pores, faint freckles, light redness, flyaway hairs, "no smoothing, no filters"; use natural daylight |
| Model copied the pose or background instead of the face | Say "use as identity reference only; ignore pose and background" |
| Output looks like the character sheet | Add the "appearance only - do not reproduce sheet layout, panels, captions or grey backdrop" line |
| Body shape drifts slimmer or taller | Restate build and height every time; it is the detail models most reliably overwrite |
| Outfit or accessories drift | Paste the WARDROBE block verbatim; decide once whether glasses, hats and jewellery are worn |
| Product label blurry or wrong | Clean product reference, label text written out, size context, label-lock template |
| Hands wrong on the product | Reduce what the hand does - a flat palm or a simple grip survives; state which fingers are visible |
| Persona feels generic | The persona, not the prompt, is thin - give them a specific life, taste and habits |

## Reference files (open only the one you need)
- `references/avatar-workflow.md` - the full step-by-step build, including the model-sheet prompt and influencer-studio workflow
- `references/character-passport.md` - basic and extended passport prompts, lock-down list, object sheets, location plates
- `references/ugc-avatar-prompts.md` - tested UGC and influencer avatar prompts
- `references/product-in-hand.md` - avatar-with-product shots, product visuals, the label-lock template
- `references/references-and-moodboards.md` - finding references and translating them into prompts without copying
- `references/persona-content.md` - running a persona as a content system: formula, formats, batches, captions

Related: `ai-cinematography` for light and camera; `ai-image-prompting` for prompt craft; `ai-filmmaking` for a whole cast; `ugc-ad-creator` for putting the avatar in ads.

Course material names particular apps and models. Apply the principles in whatever tool the user has.

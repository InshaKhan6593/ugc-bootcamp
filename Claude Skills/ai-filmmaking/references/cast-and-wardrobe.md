# Cast and wardrobe: designing a group that reads instantly

A single consistent character is a passport problem, solved in `ai-avatar-builder/references/character-passport.md`. A *cast* is a different problem: several people who must stay individually consistent, be told apart at a glance, and belong to the same world.

## Contents
- [Before a single frame exists](#before-a-single-frame-exists)
- [Palette design for groups](#palette-design-for-groups)
- [Signature markings](#signature-markings)
- [Readability in a wide shot](#readability-in-a-wide-shot)
- [The lock list](#the-lock-list)
- [Identifying features in shot prompts](#identifying-features-in-shot-prompts)
- [Cast build order](#cast-build-order)

---

## Before a single frame exists

Every character is locked into one image: the character sheet, which is their passport. The same person from every angle, in the same clothes, under the same light. From then on **the passport is the character** - it goes into every shot as a reference and the model is left with nothing to invent.

Two slots, filled exhaustively:

- **CHARACTER** - age, build, height. Ethnicity. Hair colour, length and how it sits. Facial hair. Skin tone and texture. Tattoos and exactly where they fall on the body. Scars, piercings, teeth. Default expression.
- **WARDROBE** - every garment by name, colour and material. Logos and their exact placement: chest, back, sleeve. Footwear. Jewellery. Headwear. Eyewear. When the shape of a garment matters, describe the shape rather than naming a brand.

Use the basic passport for most characters and the extended passport - labelled views, specification panels, macro detail crops - for leads and anyone whose accessories or materials appear in close-up.

---

## Palette design for groups

Give each group a strict palette that never overlaps with another group's. In a produced example, one crew wears olive and orange, the rival crew burgundy and sand - and because the palettes never cross, a viewer separates them instantly in a wide shot where no face is legible.

How to design it:

1. **Two colours per group**, one dominant and one accent. More than two stops reading as a group.
2. **No shared colour between groups.** Not "mostly different" - different.
3. **Build the palette into every passport.** If the bandana is in the passport, you never have to ask for it in a shot prompt, and it can never be forgotten.
4. **Let the environment be neutral.** If the location is already warm and orange, do not give a crew orange - put them in the colour the street does not have.
5. **Consider the grade.** A palette chosen under one look block will read differently under another. Design it against the actual visual DNA, not against a white background.

---

## Signature markings

A crew is recognised by its objects before its faces. Carry one marking across everything a group owns:

- A logo on the jacket, the bat, the bike frame, the car wing, the boombox, the signet ring.
- A pattern - a bandana paisley - repeated onto a skate deck, a sword wrap, a weapon body, the side of a van.

This is what makes a four-second insert of a wheel or a doorway legible as "theirs". Write the marking and its exact placement into both the character passports and the object passports (`objects-and-props.md`), so it is never regenerated differently.

---

## Readability in a wide shot

In a wide, the audience has silhouette, colour and motion - not faces. Design for that:

| Signal | How to build it |
|---|---|
| Silhouette | Give each character a distinct shape: a hat, a hood, a ponytail, a heavy build, a long coat |
| Colour | The group palette, plus one personal accent per character |
| Posture | A default stance written into the passport - arms folded, weight on one hip, hands in pockets |
| An owned object | Each character paired with one object that is always theirs - a bike, a bat, a phone, a deck |
| Hair | Length and style that read at distance: a high ponytail, a shaved head, a low tie-back |

Two characters of the same build, in the same palette, with the same hair, will be confused by the audience *and* by the model.

---

## The lock list

Decide these once for the whole film. Every one of them is something models silently change:

| Element | Lock |
|---|---|
| Wardrobe | Same garments, same colours, same logo placement in every shot |
| Hair | Same length, same parting, same styling or tie-back |
| Skin | Tattoos in the same places, at the same size, in the same colours |
| Jewellery | Chains, rings, earrings - present in every shot or in none |
| Eyewear and headwear | Decide once whether the character wears it. On in one shot and off in the next breaks the film faster than anything else |
| Proportions | Build and height never change. Left alone, models make everyone slimmer and taller |
| Default expression | What their face does when nothing is happening |
| Voice | One blueprint sentence, pasted unchanged into every prompt with their dialogue |

Tattoos deserve a specific note: for anything that should not be legible, write it as texture - "neck and chest tattoos read as dark texture only, never a legible drawing". Models otherwise invent readable artwork that changes every shot.

---

## Identifying features in shot prompts

In the shot prompt, each reference gets a one-line appearance description and - crucially - a single feature that identifies them, used in the strict headcount block:

> STRICT: EXACTLY THREE PEOPLE. @image1 = ONLY black headband and beard. @image3 = ONLY blonde ponytail and tinted glasses. @image5 = ONLY ponytail and tattooed neck. Never duplicate, never add a fourth person. No neighbours, no pedestrians, no extras.

Why this works: it gives the model a unique, checkable token per person. Without it, two characters merge, or a fourth person wearing a mix of two palettes appears in the background.

Always follow the reference lines with the appearance-only instruction:

> All cards give appearance ONLY. Do NOT reproduce sheet layout, multiple views, panels, captions, grey backdrop or catalogue pose.

---

## Cast build order

1. **Write the cast list** - name, role, group, one line of who they are.
2. **Assign palettes** - group colours first, then one personal accent each.
3. **Assign owned objects** - each character's object, carrying the group marking.
4. **Write the CHARACTER and WARDROBE slots** for each, in full. This is the slow part and it is where the film is actually made.
5. **Generate all passports in one session**, same prompt skeleton, same background, same light, same aspect ratio. Passports made in different sessions belong to different films.
6. **Review each passport** against the realism checks in `ai-avatar-builder` - skin texture, eyes, hands, teeth, and whether the outfit stayed identical across all panels. Regenerate failures now; a weak passport infects every shot.
7. **Lock and park them.** Reference the passport from then on, never the most recent shot output.

A nine-character cast is roughly nine to twelve sheets (leads sometimes need two) plus fifteen or so object sheets. Count before you start - that count is the real pre-production budget of the film.

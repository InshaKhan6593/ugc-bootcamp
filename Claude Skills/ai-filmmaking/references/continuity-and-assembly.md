# Continuity, sound and assembly

Generation is the middle of the job. What makes a set of clips read as a film is checking each one before moving on, then building the sound and the cut.

## Contents
- [The per-shot continuity check](#the-per-shot-continuity-check)
- [When a shot fails](#when-a-shot-fails)
- [Lip-sync and talking scenes](#lip-sync-and-talking-scenes)
- [Building the sound](#building-the-sound)
- [Assembly](#assembly)
- [The realism pass](#the-realism-pass)
- [Production log](#production-log)

---

## The per-shot continuity check

Run this on every generation before you accept it. Catching a flipped light direction now costs one regeneration; finding it in the edit costs a scene.

**The world**
- Sun in the same place; shadows the same direction and length as the other shots in this scene
- Same hour, same sky, same weather
- Same materials and ground surface
- Same lens character as the rest of the location
- No people who should not be there; headcount correct

**The cast**
- Face the same as the passport, not the same as the previous output
- Wardrobe identical: garments, colours, logo placement
- Hair same length, parting and tie-back
- Tattoos in the same places, at the same size, still reading as texture if that was the decision
- Jewellery, eyewear and headwear present or absent as decided
- Build and height unchanged - the most frequently broken lock

**The objects**
- Same geometry, finish, markings and wear as the object passport
- Correct scale relative to people
- In the right hand, and the same hand as the shot before
- Vehicles still inert where they should be

**The shot**
- Camera did what it was told; no unrequested drift, reframe or zoom
- Camera body not visible when it should not be
- Only the named character spoke; nobody else mouthed the line
- Background characters moving, not frozen
- Nothing warped, duplicated or rubbery
- The final second is clean - it is where models glitch
- The eyeline and screen direction match the neighbouring shots

---

## When a shot fails

Name the block that failed rather than rewriting the whole prompt (blocks are defined in `shot-prompt-blocks.md`):

| Failure | Block to fix |
|---|---|
| Extra person, duplicate, merged characters | 04 headcount |
| Output looks like a character sheet | 03 refs - add the appearance-only line |
| Camera floating in a locked shot, or losing a move | 05 camera, and 12 negatives |
| People in the wrong place or holding the wrong thing | 06 staging |
| Secondary characters frozen | 07 background life |
| Beats rushed, dead air, dialogue too fast | 08 action timing - shorten lines, restate pacing |
| Mugging, blank face, identity softening | 09 acting |
| Everyone mouthing the dialogue | 10 who speaks |
| Flat or silent-feeling shot | 11 SFX |
| Cars rolling, cuts appearing, relighting, speed ramps | 12 negatives |
| The world itself changed | The location plate, not the shot - regenerate the plate reference |

Partial saves worth knowing: if only the last second is broken, trim it in the edit rather than regenerating. If one region is wrong, cutting away to an insert for a beat and back is cheaper than a new generation - and cutting to B-roll over a flawed moment is normal editing practice, not a compromise.

---

## Lip-sync and talking scenes

- Keep speech inside what the model holds in sync. Some models drift after about ten seconds of continuous speech; some generate only eight-second clips. Plan dialogue shots to those limits rather than fighting them.
- Use the strongest lip-sync model available for hero dialogue and a cheaper one to test the performance direction. Current rankings are in `ai-video-prompting/references/model-choice.md`.
- An off-screen line needs no lip-sync at all, which frees the model to spend everything on the listener's face. Where the drama is in the reaction, write it off-screen deliberately.
- Shorter lines sync better than long ones. Two short lines beat one long one every time.
- If a voice drifts between shots, the voice blueprint was paraphrased. Paste it identically.

---

## Building the sound

A film that looks produced and sounds empty reads as generated. Build in three layers:

1. **Ambience** - the bed of the place: wind, traffic, room tone, birds, distant machinery. Continuous across the scene, so cuts within a scene do not change the room.
2. **Physical detail** - the layer that sells the image: footsteps on the right surface, fabric, a door, grit, a chain, a brake, a thumb on a keypad. If an action is visible and inaudible, the brain notices.
3. **Music, last and optional.** Many of the strongest sequences run SFX-only; music added over a well-built sound layer lifts it, music covering an empty one sounds like a template.

Write the SFX list in the shot prompt for models that generate audio, and still rebuild it in the edit - generated audio is a starting point, not a mix. Keep distance in the mix: a radio across the street should be thin and small, not present.

---

## Assembly

- **Cut on action**, not after it. Letting a movement complete before cutting is what makes AI footage feel slow.
- **Hold the frames that deserve holding.** Short films nearly always cut the last beat too late and the quiet beats too early.
- **Use shot-size contrast.** Wide, medium, close, detail. A sequence of same-size shots feels flat whatever the content.
- **Vary shot length.** A 4-second insert between two 14-second takes creates rhythm for free.
- **Trim glitched tails** rather than regenerating.
- **Cut away over any weak moment.** A clone or character whose mouth goes wrong for half a second is fixed by a B-roll insert, not a new generation - and mixing talking footage with B-roll is better editing anyway.
- **Keep the sound continuous across cuts within a scene** so the picture cuts and the room does not.
- **Export to the platform's spec.** Bigger numbers are not better: platforms re-encode, and a 1080p30 upload often looks better than 4K60 that gets crushed. Details in `viral-short-form/references/platform-and-posting.md`.

---

## The realism pass

Raw AI footage is too contrasty, too saturated and too stable - that trio is the giveaway. On an adjustment layer over the whole film:

1. Bring contrast down noticeably, until it stops feeling like a render.
2. Lower saturation slightly. Stop before it looks lifeless.
3. Lift highlights a little if the image feels dense.
4. Add a handheld shake subtle enough that the viewer never notices it. If they notice, reduce it.

Compare before and after rather than trusting slider values. For a film with a deliberate film-stock look, the grain and halation are already in the look block, so go lighter on this pass - it is aimed mainly at footage meant to read as filmed rather than designed. Full detail in `ai-video-prompting/references/realism-pass.md`.

---

## Production log

Keep a single file for the film with:

- The visual DNA block, final
- The cast list with reference filenames and the identifying feature used in headcount blocks
- Location plates with the camera position each one represents
- Object passports with their five details
- The shot list with durations, references in order, and status
- The voice blueprint per speaking character
- Model and settings used per shot, including reference order

Two reasons this matters more than it sounds. First, a film is dozens of generations across several sessions, and the second session re-invents whatever was not written down. Second, the log *is* the asset: a sequel, a trailer cut, an extra scene or a client's revision all start from it rather than from scratch.

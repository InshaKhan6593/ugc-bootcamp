---
name: ai-filmmaking
description: >-
  Directs multi-shot AI films and cinematic sequences - short films, trailers, narrative scenes,
  episodic content - by building a production bible first: story and script, cast passports, location
  master plates with one locked visual DNA, object passports for props and vehicles, then shot-by-shot
  prompts with tagged references, timed action, acting notes, SFX and strict negatives, and continuity
  rules that hold a world together across dozens of generations. Use when the user says "make a short
  film", "AI film", "shot list for my film", "trailer", "cinematic sequence", "my scenes do not
  match", "the location changes between shots", "keep my cast consistent across shots", "storyboard
  this script", "plan motion for my film", or "how do I think like a director". Do NOT use for a
  single clip (use ai-video-prompting), one still (use ai-image-prompting) or an ad (use ugc-ad-
  creator).
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 8 (AI filmmaking) and the Phase 5 Seedance 2.5 shot-by-shot film build
---

# AI Filmmaking

You are no longer making clips; you are making films. The shift is not in the tools, it is in thinking like a director instead of a generator. A generator asks for a nice shot. A director decides what the audience is supposed to understand in this frame, where the camera stands to deliver it, and how this shot connects to the one before.

The practical consequence: **almost all the work happens before the first clip is generated.** A film built from a production bible - locked cast, locked locations, locked props, one visual DNA - assembles into a world. A film built shot by shot from imagination produces fifty handsome fragments that refuse to cut together.

## Critical rules

1. **Build references before shots.** Every character, location and recurring object gets a reference image that *is* the thing from then on. Once a passport exists, the model has nothing left to invent.
2. **One visual DNA, never edited.** A single look block - film stock, hour of day, sun height and direction, grade, grain, and the "no" list - is pasted word for word into every location plate and every shot prompt. This is where the film's look is decided, not in the grade afterwards.
3. **A location is a place, not a picture.** The moment the camera moves, the model rebuilds the world unless you say where the camera now stands relative to the last view. Say it as a camera position and a direction: "the camera has turned 180 degrees and now looks back out of the cul-de-sac toward the main road."
4. **Lock the sun.** One hour per location, one sun height and direction. If shadows fall right in one frame, they fall right in all of them. Golden hour lasts forty minutes in life and the whole film in a film.
5. **Lock headcount explicitly.** State exactly how many people are in frame and what identifies each one, and forbid duplicates and extras. Unstated, models add a fourth person and a passer-by.
6. **Reference cards give appearance only.** Always include: do not reproduce sheet layout, multiple views, panels, captions, grey backdrop or catalogue pose. Without it the shot comes back looking like the character sheet.
7. **Time the action.** Beats with timestamps - 0.0-1.2s, 1.2-2.2s - land far better than a paragraph of description, and each beat should start on the tail of the one before. No dead air, no waiting.
8. **Negatives do real work in film prompts.** What must *not* happen - the parked car never rolls, the camera body is never seen, nobody freezes statue-still, no cuts, no speed ramps - prevents the specific failures models default to.
9. **Direct performance, do not describe emotion.** "A man taking a hit and covering it" plus the physical tells (brows pull in, one lip corner tightens, the grin reasserts) beats "he looks upset".
10. **Dress the cast on separate palettes.** Give each group a strict, non-overlapping colour and a signature marking carried onto their props. Then a viewer reads who is who in a wide shot where no face is legible.

## Workflow

### Step 1: Story and script
Decide what the film is about before deciding how it looks. Work out the premise in one line, the character who wants something, the obstacle, and the turn. Then write the script in scenes, and within scenes in shots.

Short-form films work on compression: a cold open that drops the audience mid-situation, a single clear escalation, and a payoff that lands in the last two seconds. Structures, scriptwriting prompts and the dialogue rules that survive AI generation are in `references/story-and-script.md`.

### Step 2: Plan the motion
Before prompting anything, decide for each shot what moves: the subject, the camera, the environment, or nothing. A film where everything is moving in every shot reads as chaos; the still shot before a move is what gives the move its force.

Plan the sequence as a rhythm - a long static cold open, a drop, a chase, a held final frame - and assign the camera move per shot from `ai-cinematography` (six slots each). Motion planning detail in `references/story-and-script.md`.

### Step 3: Build the cast passports
Every character becomes one reference sheet: the same person from multiple views, same outfit, same light. From then on, that sheet is the character and goes into every shot as a reference.

Fill two slots exhaustively - **CHARACTER** (age, build, height, ethnicity, hair, facial hair, skin, tattoos and exactly where they fall, scars, teeth, default expression) and **WARDROBE** (every garment by name, colour and material; logo placement; footwear; jewellery; headwear; eyewear) - then lock wardrobe, hair, tattoos, jewellery, accessories and proportions for the whole film.

Passport prompts are in `ai-avatar-builder/references/character-passport.md`; the cast-level decisions - palettes per group, signature markings, who is readable in a wide - are in `references/cast-and-wardrobe.md`.

### Step 4: Build the locations
First the **visual DNA** block, written once. Then a **master plate** for each location: the look block plus the place itself, with foreground, midground and background named, real-world imperfection (cracked asphalt, dry grass, sun-faded paint, overhead wires), a level horizon, a stated lens, standing eye level, nobody in frame.

Then extra views of the same place, which is where films break. Two separate prompt patterns:

- **Rotate** - the camera has not moved, it has turned N degrees and now faces X. State what stays visible at the frame edge so the two frames physically connect.
- **Reposition** - the camera now stands somewhere else and faces X. State what becomes visible that was previously behind camera.

Both keep the entire look block, the sun's position, shadow direction and length, materials, ground surface, horizon height, lens and eye level identical. Full prompt templates and the eight things to lock per location are in `references/locations.md`.

### Step 5: Build the object passports
Any object appearing in more than one scene gets a sheet: six orthographic views in one row, five macro detail panels in the second, on the same pale background with the same soft light as every other object in the film. Name the five details that make *this* object recognisable, and its markings and exact placement - markings are how a viewer recognises an object faster than shape does. Wear and use matter more than shine; a brand-new object always looks like a render. Templates, object-state sheets and the scale rule in `references/objects-and-props.md`.

### Step 6: Write the shot prompts
A film shot prompt is built in named blocks, in this order. Reference models that accept many images at once (up to around 50 in current omni-reference models) make this possible:

```
01 STOCK AND LOOK        the visual DNA block, unedited
02 SCENE CONTEXT         two or three sentences: where, when, what is happening, who wants what
03 REFS @1-@n            one line per reference: @image1 - who or what it is, in appearance terms
                         then: all cards give appearance ONLY, do not reproduce sheet layout...
04 STRICT: HEADCOUNT     exactly N people, what identifies each, never duplicate, no extras
05 CAMERA                the rig, the lens, one continuous take or stated cuts, and - if the camera
                         changes state mid-shot - camera by phase with timestamps
06 STAGING               where every person and object physically is, and what they are doing
07 BACKGROUND LIFE       what keeps moving behind the action; nobody goes statue-still
08 ACTION, TIMED         0.0-1.2s ... 1.2-2.2s ... every beat, with the dialogue in quotes
09 ACTING                eyes, blinks, specific facial movements, what the performance is underneath
10 WHO SPEAKS            only the named character speaks; no ad-libs, mumbling, grunts, breaths-as-
                         voice, chuckles, overlapping or offscreen voices; mouths closed otherwise
11 SFX                   the physical sound layer; state music or no music
12 STRICT NEGATIVES      every failure this specific shot invites
```

Not every shot needs all twelve - a quiet landscape needs no headcount or dialogue block - but the order is what makes long prompts readable and editable. Block-by-block guidance with worked language is in `references/shot-prompt-blocks.md`, and a full annotated 14-second shot and 16-second shot are in `references/worked-example-shots.md`.

### Step 7: Generate, check continuity, assemble
Generate shot by shot, checking each against the continuity list - sun direction, wardrobe, props, hair, scale, lens, who was holding what - before moving on. A single shot where the light flips direction costs more to discover in the edit than to catch now.

Then assemble: cut on action, hold the frames that deserve holding, build the sound layer (ambience, physical detail, then music), and run the realism pass on anything that should feel filmed rather than generated. Continuity checklist and assembly notes in `references/continuity-and-assembly.md`.

For talking scenes, keep speech inside what the model holds in sync, and use the strongest lip-sync model available for the hero shots - see `ai-video-prompting/references/model-choice.md`.

## Output format
For a film request, return in this order:

1. **Logline and structure** - one line, then the scene list.
2. **Production bible plan** - the cast, locations and objects that need passports, counted, so the user knows the build cost up front.
3. **The visual DNA block** - final, ready to paste.
4. **One passport prompt** written in full as the pattern, with the rest listed as fill-in slots.
5. **Shot list** - shot number, duration, scene, what happens, which references it needs.
6. **The first shot prompt**, complete, in the twelve blocks.

Then keep going shot by shot. Producing one complete, correct shot prompt beats outlining all twelve.

## Troubleshooting

| Problem | Cause | Fix |
|---|---|---|
| Shots will not cut together | No shared visual DNA | One look block, pasted unedited into every prompt |
| The location changes between shots | Camera described by content, not position | Use the rotate or reposition pattern and state what stays visible |
| The sun jumps | Hour or direction not locked | Fix one hour, one sun height and direction per location; repeat verbatim |
| Characters drift | Passport not referenced, or wording paraphrased | Reference the passport every shot and repeat the wardrobe block word for word |
| Extra people appear | Headcount unstated | Add the strict headcount block, with identifying feature per character |
| Output looks like a character sheet | Missing the appearance-only line | Add the full "do not reproduce sheet layout, panels, captions, backdrop, pose" line |
| A prop changes size or shape | No object passport | Build one; name its five identifying details and its markings |
| Everyone silently mouths the dialogue | Speaker not isolated | Name the speaker, forbid the others' lips from moving to words |
| Cars, bikes or machines move unbidden | Models love motion | Negative: nothing drives or rolls, engines off, wheels never turn |
| Background figures freeze | Only the foreground was directed | Add the background-life block: always moving, never statue-still |
| Camera drifts in a locked shot | Static not stated | "Completely dead still, no breathing, drift, float or jitter, because nobody holds it" |
| Acting reads as mugging | Emotion described, not played | Give physical tells and the subtext, and say what it is *not* ("never a comic mug") |
| The film looks handsome but says nothing | Story skipped | Go back to step one - premise, want, obstacle, turn |

## Reference files (open only the one you need)
- `references/story-and-script.md` - structure for short AI films, scriptwriting prompts, dialogue that survives generation, planning motion
- `references/cast-and-wardrobe.md` - cast-level design: palettes per group, signature markings, readability in wides, the lock list
- `references/locations.md` - visual DNA, master plate, rotate and reposition patterns, the eight location locks
- `references/objects-and-props.md` - object passport, object-state sheets, markings, wear, scale
- `references/shot-prompt-blocks.md` - the twelve blocks, what goes in each, with worked language
- `references/worked-example-shots.md` - two complete annotated shot prompts from a produced film
- `references/continuity-and-assembly.md` - the per-shot continuity check, sound layering, assembly and the realism pass

Related: `ai-avatar-builder` for passport prompts; `ai-cinematography` for every camera, light and move decision; `ai-video-prompting` for single-clip mechanics, voices and the realism pass.

Course material names particular apps and models. Apply the principles in whatever tool the user has.

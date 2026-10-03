---
name: ai-cinematography
description: >-
  The craft layer for AI images and video - lighting logic, camera angle, shot size, lens choice,
  depth and composition, colour grade, and camera movement. Use whenever a shot needs to be lit,
  framed, lensed, graded or moved: "how should I light this", "what camera angle", "which lens", "make
  it look cinematic", "add depth", "it looks flat", "colour grade for this mood", "what camera move
  here", "dolly or zoom", "lock the look across all my shots". Also use when diagnosing a shot that
  reads as a render, is evenly lit, flat, oversaturated or drifting. Pair it with ai-image-prompting
  (stills), ai-video-prompting (motion), ai-filmmaking (films) or ugc-ad-creator (ads) - it supplies
  the camera, light and grade lines those skills drop into their prompts.
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 3 (depth, lighting, camera) and Phase 4 (camera movement)
---

# AI Cinematography

Models light and frame a scene by averaging everything they have seen, which is why an unspecified shot comes back evenly bright, centred, flat and slightly oversaturated. A cinematographer never says "show me the street". They say: the camera is here, facing that way, the sun is low behind us, the exit is behind camera. Give the model that and the guessing stops.

This skill supplies four blocks that drop into any image, video, ad or film prompt:

- **LIGHT** - source, quality, direction, colour, material response
- **CAMERA** - where it stands, how much we see, how the space feels
- **DEPTH** - foreground, midground, background, and what is in the air
- **GRADE** - the finish, placed at the end of the prompt

For video, a fifth: **MOVEMENT** - the move, its rig, and both of its ends.

## Critical rules

1. **Light needs a real source.** "Cinematic lighting" is not lighting. Name the source (window, lamp, sun, neon, screen, fire, headlights), its direction, and whether it is hard or soft. The source can sit off-frame; the shadows are what prove it exists. Evenly lit frames with no source are the single biggest reason an image reads as a render.
2. **The shadow side matters as much as the lit side.** Shape comes from what falls into shadow. Let one side go dark, and say "background darker than the subject" when you want separation.
3. **Angle, shot size and lens are three separate decisions.** Answer all three or the model picks a safe centred eye-level medium shot every time.
4. **Distortion comes from camera distance, not focal length.** Say where the camera physically stands as well as what lens it uses, or an 85mm portrait prompt still comes back with a wide-angle face.
5. **Depth is built, not requested.** Name a foreground, a midground and a background, plus something in the air (haze, dust, steam, rain). A soft out-of-focus foreground object is the fastest fix for a flat frame.
6. **The grade goes at the end**, after the scene is described, in restrained words. Front-loading style words makes the model style the scene instead of building it.
7. **Anchor the light once per location, then never re-invent it.** Write the lighting as one block and paste it word for word into every shot in that location, changing only action and shot size. A close-up must keep the same light direction, softness and colour as the wide that established it, or the sequence falls apart.
8. **Match the camera move to how big the face is.** Wide shots forgive almost anything. Once a face fills the frame, keep the move gentle - a controlled push, a slow slide, a focus shift.
9. **Motivate strong colour.** Red light reads as cinema when it comes from a safelight, neon sign, brake light or alarm; with no source it reads as a cheap filter.
10. **Pick one mode and stay in it.** *Cinematic* (cinema body, chosen lens, shallow focus, film grade) or *UGC/phone* (phone camera, ~24-26mm, deep focus, the room's own light, no grade). Mixing the two vocabularies in one prompt is what makes a "selfie" come back looking like a DSLR portrait.

## How to use this skill

### Step 1: Read what the shot has to do
Decide what the viewer must read in this frame - the world, a body, an action, a reaction, one detail - and what it should feel like. Every choice below follows from that. Then pick the mode: cinematic or UGC/phone.

### Step 2: Write the LIGHT block
Answer six questions. If you cannot answer them, the model will invent light for you (details and worked prompts in `references/lighting.md`):

| Question | What to write |
|---|---|
| Where is it coming from? | A named source: large window camera-left, bare overhead bulb, phone screen, low sun behind, neon sign off-frame right |
| Hard or soft? | Hard = small direct source, sharp-edged shadows, dramatic, tense, raw. Soft = large or diffused source, gentle falloff, calm, expensive, intimate |
| Which direction? | Side light carves shape and texture. Backlight separates and rims. Front light flattens - useful for beauty, dull for drama |
| What colour? | Warm = alive, intimate, nostalgic. Cool = distant, lonely, modern. Green = uneasy, artificial. Red = danger, pressure |
| How do materials react? | Metal throws sharp speculars, glass catches and transmits, fabric absorbs, stone sheens, skin needs texture. If everything reacts the same way it reads as CGI |
| For people: the catchlight | Match it to the source - window gives a soft rectangle, ring light a ring, phone screen a small cool rectangle. No catchlight means dead eyes |

Warm key on the subject against cooler background tones is the classic separation trick; echo one accent colour elsewhere in the frame so it looks intentional.

### Step 3: Write the CAMERA block
Three questions (full tables, aperture and camera bodies in `references/camera-lens.md`):

1. **Where is the camera?** Height and side: eye level (honest, equal), low (power, or fear if the subject is small), high (vulnerability, or order), Dutch (unstable), frontal (confrontational), three-quarter (natural and dimensional), profile (closed off), back (mystery), over-the-shoulder (power dynamics), POV (inside the scene). An angle points a scene in a direction - the character, light and story decide what it finally means.
2. **How much do we see?** Extreme wide (the place is the subject) - wide - full (posture, silhouette) - medium (conversation distance, dull if overused) - close-up (emotion, breath) - extreme close-up (one critical detail). A close-up only lands if the viewer was held further away first, so alternate sizes across a sequence.
3. **How does the space feel?** 16-24mm deep and immersive, 35-50mm natural, 85mm portrait separation, 135-200mm compressed and voyeuristic. One focal length per location - a different lens reads as a different place.

The camera body sets the image character (colour, skin, highlight roll-off); lens and camera position set the geometry. Name both in cinematic mode; in UGC mode name the phone and where the phone physically is (arm's length, propped on the counter, on the dashboard, in the mirror).

### Step 4: Write the DEPTH block
Five framing rules (details and UGC layer tables in `references/composition.md`):

- **Layers.** Foreground / midground / background, each named. Ask: *what is in my foreground, and what is in the air?*
- **Atmosphere.** Haze, fog, dust, smoke or light rays between the layers. Distant things get lighter, softer and lower in contrast - that is how eyes read distance.
- **Thirds.** Do not leave the subject dead centre by default.
- **Leading lines.** Roads, rails, walls or light pointing at the subject.
- **Lead room.** Space in the direction the subject looks or moves.

In UGC mode the layers are everyday objects: hand or product near the lens, then face, then lived-in room. For 9:16, keep face and product in the middle band, clear of captions at the bottom and buttons on the right.

### Step 5: Write the GRADE block
Pick a palette from the mood, not from a style list. Warm amber for nostalgia, cool steel for isolation, bleached neutrals for tension, deep red-and-black for danger. Keep it restrained: "muted desaturated warm grade, earthy tones" beats "vibrant HDR cinematic colour". 12 mood-to-palette maps and 10 film looks are in `references/color-grading.md`.

For realism, the strongest grade is often no grade at all - just the film stock or phone-processing cue.

### Step 6: For video, write the MOVEMENT block
Fill six slots or the move becomes a drift (37 catalogued moves with copy-ready six-slot prompts in `references/camera-moves-catalogue.md`; 30 story-driven moves in `references/camera-moves-high-impact.md`):

| Slot | What it answers |
|---|---|
| Movement | The move by name and what it rides on (rails, shoulder, gimbal, crane, drone, body mount, hand) |
| Start | How it begins - from a locked frame, already moving, from a held beat |
| Speed | Its curve - slow and even, easing in, accelerating, snapping |
| Framing | What stays stable while the camera moves |
| End | The final frame, and whether it holds |
| Time | Real time by default; if something slows, say exactly what |

Key distinctions:
- **Dolly vs zoom.** A dolly moves through space - foreground sweeps past, perspective changes. A zoom only magnifies - perspective stays flat. Zoom speed is its own tool: slow = rising tension, fast = discovery, crash = shock or punchline.
- **Sliders and push-pasts need a real foreground object.** Parallax is the whole point; with nothing near the lens there is nothing for the frame to shift against.
- **Tracking borrows the character's pace.** From behind = what lies ahead. From the front = the face and their resolve. From the side = the journey. Low = mystery (feet, hands, wheels).
- **A whip pan needs a target**, otherwise it is a fast move toward nothing.
- **Static must be stated**: "locked tripod, no camera movement, hold the same framing, zero drift". Left unsaid, models add a slow float.
- **Handheld realism beats smooth perfection.** AI's default glide reads as a render. A documentary snap zoom - handheld, lagging slightly, then a snap with motion blur and a focus slip that corrects - is the strongest single trick for making unreal footage feel filmed by a person.

### Step 7: Lock the look for a set of shots
When more than one image or clip belongs to the same world, write one **look block** - film stock or phone look, hour of day, sun height and direction, grade, grain, and the "no" list - and paste it into every location plate and every shot prompt without editing a word. Then a per-location **lighting block**, same treatment. Shot prompts then carry only what changes: action, shot size, camera position. `ai-filmmaking/references/locations.md` shows this at film scale.

## Output format
Return the blocks as copy-ready lines, not prose:

```
LOOK:    [stock or phone look, hour, sun height and direction, grade, grain, the "no" list]
CAMERA:  [angle and height, shot size, lens, body or phone, where it physically stands]
LIGHT:   [source + direction, hard/soft, colour, catchlight, what falls into shadow]
DEPTH:   foreground [...] / midground [...] / background [...] / in the air [...]
GRADE:   [palette in restrained words]
MOVE:    [movement, start, speed, framing, end, time]   <- video only
```

Then one line on **why** - the two or three choices doing the work - and one **variation** that changes a single lever (angle, light direction or mood) so the user can see the difference.

## Diagnosing a shot

| Symptom | Cause | Fix |
|---|---|---|
| Looks like a render | Evenly lit, no source | Name one source and its direction; let one side fall into shadow |
| Flat, subject pasted on | Only subject + background | Add a foreground layer and something in the air; move the subject off-centre |
| Face distorted on a long lens | Only the lens was named | State where the camera stands - distortion comes from distance |
| Dead eyes | No catchlight | Add a catchlight that matches the named source |
| Sequence falls apart between shots | Light re-invented per shot | Anchor one lighting block and repeat it verbatim; keep the sun in the same place |
| Oversaturated, fake colour | HDR, neon or "vibrant" words | Name specific colours, one mood palette, grade at the end |
| Coloured light looks like a filter | Unmotivated | Give the colour a source: safelight, neon, brake light, alarm, screen |
| Camera drifts or floats | Move slots left empty | Fill all six; for static shots state no movement, zero drift |
| Move feels smooth and fake | AI default glide | Name the rig and add handheld imperfection, lag, a focus slip |
| Close-up warps during a move | Big face plus big move | Reduce to a gentle push, slide or focus shift |
| Everything shot at the same size | No size contrast | Alternate wide, medium, close so the close-up earns its place |
| "Cinematic" selfie | Modes mixed | Strip cinema-body and bokeh words; phone, deep focus, room light, no grade |

## Reference files (open only the one you need)
- `references/lighting.md` - light logic, the nine rules, UGC light-source table, worked prompts
- `references/camera-lens.md` - angle, shot size, lens, aperture, camera bodies, the three-question framework
- `references/composition.md` - depth layers, atmosphere, thirds, leading lines, lead room, 9:16 safe area
- `references/color-grading.md` - 12 moods mapped to palettes, 10 film looks, the grading formula
- `references/camera-moves-catalogue.md` - 37 moves, six-slot prompts, AI failure notes
- `references/camera-moves-high-impact.md` - 30 story-driven move frameworks
- `references/glossary.md` - cinematic terms in plain language

Course material names particular apps and models. Apply the principles in whatever tool the user has; do not push them toward a platform.

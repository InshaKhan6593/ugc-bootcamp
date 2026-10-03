# Locations: visual DNA, master plates and moving the camera

The look of the film is decided here - not in the character shots, and not in the grade afterwards. Film stock, hour of day and sun direction are set once, in the location work, and then carried unchanged into every shot prompt for the rest of the production.

The hardest idea in this document: **a location is a place, not a picture.** The moment the camera moves, the model rebuilds the world from scratch unless you tell it where the camera now stands relative to where it stood before.

## Contents
- [The visual DNA block](#the-visual-dna-block)
- [The location master plate](#the-location-master-plate)
- [Changing the viewpoint: rotate](#changing-the-viewpoint-rotate)
- [Changing the viewpoint: reposition](#changing-the-viewpoint-reposition)
- [The three slots to fill](#the-three-slots-to-fill)
- [The eight location locks](#the-eight-location-locks)

---

## The visual DNA block

Written once, pasted into every location prompt and every shot prompt, word for word, never edited. It contains the stock, the hour, the sun, the light behaviour, the grain, and the list of things that must not happen.

> **THE LOOK** - paste into every location prompt and every shot prompt, word for word, never edited.
>
> Shot on 35mm film, Kodak Vision3 500T, tungsten-balanced stock exposed in daylight through a warm 85 correction. Late golden hour, roughly forty minutes before sunset, the sun low at about ten degrees above the horizon. Warm golden-peach light on every surface facing the sun, cool pale blue-white sky, long soft shadows raking across the ground. Gentle halation blooming around the brightest highlights, fine organic grain, soft highlight roll-off, deep shadows that never crush to black. Natural colour, the way a real film stock renders a real street.
>
> No teal-and-orange grading. No HDR. No digital clarity or sharpening. No lens flare. No dramatic clouds. Nothing wet unless it rained in the story.

What makes this block work:

- **A named stock, not a vibe.** "Kodak Vision3 500T exposed in daylight through an 85 correction" gives the model a specific colour science to imitate. "Cinematic" gives it nothing.
- **A sun with a number.** "Low at about ten degrees above the horizon" is checkable; "golden hour" drifts.
- **Light behaviour, not just colour.** Halation around highlights, soft roll-off, shadows that do not crush - these are the physical tells of film.
- **A "no" list.** Teal-and-orange, HDR, sharpening, flare and dramatic clouds are exactly what models add unprompted. Naming them is how you keep them out.

Write your own on the same skeleton: stock or camera look, hour and sun height, what the warm and cool surfaces do, grain and halation, shadow behaviour, then the no-list. For phone-look films, swap the stock line for the phone-processing line and the no-list for "no cinematic grade, no bokeh, no colour grading, no stabilisation".

---

## The location master plate

The first view of a location: the look block, then the place.

```
=== LOOK - never changes, identical in every location ===
[paste the visual DNA block here, unedited]

=== PLACE - changes for every location ===
Photorealistic establishing plate of [WHAT THE PLACE IS]. [LENS]mm spherical lens, camera at
standing eye level, perfectly level horizon, no tilt, no wide-angle distortion. The sun rakes in
from [DIRECTION]. Documentary stillness, nobody in frame.

Foreground - [what is closest to the camera: the road surface, the kerb, the grass, the dust]
Midground - [the buildings, their material and colour, the vehicles, the fences]
Background - [what closes the frame at the far end]

Real-world imperfection: cracked asphalt, dry yellow grass, sun-faded paint, overhead power
lines on wooden poles.

This must read as a photograph of a real street, not as a render.

Avoid: people, tilted horizon, oversaturation, staged tidiness.
```

Notes that matter:

- **Nobody in frame.** Not one accidental person. People appear only where the story puts them, and an empty plate is reusable in every shot of that location.
- **Imperfection is the realism.** Cracks, fading, dry grass, wires. Staged tidiness is the giveaway of a render.
- **A level horizon, stated.** Models tilt by default when asked for anything "cinematic".
- **One lens per location.** A different focal length reads as a different place, so decide it here.

---

## Changing the viewpoint: rotate

For main locations, where the camera stays put and only turns. This is the safest way to get a second angle, because nothing about the camera's position has to be re-established.

```
Same location as the reference image. The camera has not moved from its position, it has rotated
[DEGREES] degrees to the [LEFT / RIGHT] and now faces [WHAT IS THERE].

KEEP IDENTICAL - the entire LOOK block, the sun in the same place in the sky, shadows falling in
the same direction and at the same length, the same ground surface continuing underfoot, the same
horizon height, the same lens, the same eye level.

WHAT STAYS VISIBLE - [the piece of the previous frame that must still be in view at the edge, so
the two frames physically connect]

WHAT IS NEW - [what the rotation reveals]

Nobody in frame. This is one continuous place photographed from one standing position, not two
different places.
```

The "what stays visible" line is what welds the two frames into one world. Without it you get two plausible streets that cannot be cut together.

---

## Changing the viewpoint: reposition

When the camera genuinely moves to a new position. The master plate goes in as the reference.

```
The same location as in the reference image, photographed from a different camera position.

CAMERA - [where the camera now stands and which way it faces. For example: the camera has turned
180 degrees and now looks back out of the cul-de-sac towards the main road.]

KEEP IDENTICAL - the entire LOOK block, time of day, height and direction of the sun, colour and
temperature of the light, length and direction of the shadows, architecture and its materials,
road surface, vegetation, sky, film stock and grain. Same lens, same standing eye level, same
level horizon.

NEW IN FRAME - [what becomes visible from this position that was behind the camera before]

Nobody in frame. Same documentary stillness. This is the same place at the same minute, only the
camera has moved.
```

---

## The three slots to fill

### Where the camera stands
Not "a view of the street" but a position: deep in the cul-de-sac, at the kerb, in the middle of the road, on the far side of the intersection. The model puts the camera exactly where your words put it, so vague words put it somewhere new each time.

### Which way it faces
Direction matters more than content. If the camera turned 180 degrees, write that - describing what is now visible is not the same instruction and produces a different place.

### What connects the frames
Name the object, edge or surface that appears in both frames. Continuity is a physical claim, and this is the evidence for it.

---

## The eight location locks

| Lock | Rule |
|---|---|
| The sun | Height and direction. Shadows that fall right in one frame fall right in all of them |
| Time of day | One hour for the whole location. Golden hour lasts forty minutes in life and the whole film in a film |
| Camera height | Eye level by default. Change it only when it is a decision, not an accident |
| Lens | One focal length per location |
| Materials | Stucco, asphalt, chain-link, dry grass. List them once and repeat them verbatim |
| Sky | Colour and condition. Clouds appearing break a location harder than a moved building |
| Emptiness | Not one accidental person. People only where the story puts them |
| The look block | Pasted unedited, every time, in location plates and shot prompts both |

## Building a location set

A main location usually needs three to five plates: the master view, the one or two views the action needs, and the exit or arrival view. An interior usually needs the exterior too, so an arrival can be cut.

Produce them in one sitting, from the same look block, in the same aspect ratio. A location built across two sessions almost always drifts, because the second session re-invents whatever was not written down.

Park the finished plates somewhere permanent and treat them as read-only. A shot prompt references the plate; it never references the previous shot's output, because small errors compound into a different street within five shots.

# The shot prompt, block by block

A film shot prompt is long - several hundred words is normal - and length is not the problem. Disorder is. Writing in named blocks, always in the same order, makes a long prompt editable, diffable between shots, and debuggable when a generation goes wrong.

Reference models that accept many images at once (current omni-reference models take up to around 50) are what make this possible: the passports carry identity, so the prompt carries only behaviour.

## The block order

```
01 STOCK AND LOOK
02 SCENE CONTEXT
03 REFS @1-@n
04 STRICT: HEADCOUNT
05 CAMERA  (or CAMERA BY PHASE)
06 STAGING
07 BACKGROUND LIFE
08 ACTION, TIMED
09 ACTING
10 WHO SPEAKS
11 SFX
12 STRICT NEGATIVES
```

Not every shot needs all twelve. A landscape insert needs 01, 02, 03, 05, 11, 12. A dialogue two-hander needs all of them. Keep the order even when blocks are skipped.

---

## 01 STOCK AND LOOK

The visual DNA block, unedited, plus the technical frame: frame rate, shutter, audio policy, language, and the shot's duration.

> 35mm Kodak 500T. Handheld dynamic cinematography. Low golden-hour sun, warm skin tones, cool skylight on the shadow side. Photorealistic live-action, raw documentary realism. No 3D render, no game engine, no plastic skin, no retouch, no oversharpening, no HDR grading. 24fps, 180-degree shutter blur. SFX only, no music. No subtitles. American accent. 14s.

"24fps, 180-degree shutter blur" earns its place: it gives motion the blur real cameras produce, and its absence is part of why AI footage looks too crisp.

---

## 02 SCENE CONTEXT

Two or three sentences of plain situation: where, when, who, what is happening, and what each person wants. This is the block that stops the model inventing a different scene from the staging alone.

> Scene context: A quiet LA cul-de-sac at golden hour, a crew of creators on their block. The man with the headband films himself on his own small camera, showing off to the lens. The blonde woman across the street undercuts him without raising her voice. Nobody travels anywhere.

"Nobody travels anywhere" is doing work - it pre-empts the model's instinct to move everyone somewhere.

---

## 03 REFS @1-@n

One line per reference, in the order they are attached, each in pure appearance terms:

> @image1 - Black man, black paisley headband, full black beard, olive bomber with orange BC monogram, white tee, silver chain, baggy dark jeans. Neck and chest tattoos read as dark texture only, never a legible drawing.
> @image2 - his BMX: matte dark-green scuffed frame, black parts, 4 pegs.
> @image8 - location only: LA cul-de-sac, cream and sand stucco houses, tall bare-trunk palms, cracked asphalt, poles and wires, dry lawns.

Then, always:

> All cards give appearance ONLY. Do NOT reproduce sheet layout, multiple views, panels, captions, grey backdrop or catalogue pose.

Two refinements worth knowing:
- A location reference can be told to carry the camera direction too: "@image7 - THE LOCATION AND THE EXACT DIRECTION THE CAMERA IS FACING. Use it for everything."
- Scenery inside the location reference can be neutralised in the same line: "ordinary cars are parked along the kerbs - scenery only, nobody is in them and none of them ever move."

---

## 04 STRICT: HEADCOUNT

Exact number, plus one unique identifying token per person, plus the prohibition.

> STRICT: EXACTLY THREE PEOPLE. @image1 = ONLY black headband and beard. @image3 = ONLY blonde ponytail and tinted glasses. @image5 = ONLY ponytail and tattooed neck. Never duplicate, never add a fourth person. No neighbours, no pedestrians, no extras.

For a solo shot: "STRICT: EXACTLY ONE PERSON IN THE WHOLE SHOT. The street behind him is completely empty of people: no crew, no neighbours, no pedestrians, no extras, no duplicates."

---

## 05 CAMERA, or CAMERA BY PHASE

State the rig, the lens, whether it is one continuous take, and what the camera does. Be explicit about whether we look *through* the camera or *at* it:

> CAMERA: ONE CONTINUOUS TAKE, no cuts, no change of framing. The camera is the small one in @image1's own outstretched right hand, selfie framing, 22mm, gentle barrel distortion at the edges. He is STANDING STILL and so is the camera position - the only motion is the live weight of his arm: vertical bobbing with his breathing, small lateral sway, occasional roll tilts, fine micro-jitter, and instinctive corrections keeping HIS FACE IN FRAME and readable. He sits in the RIGHT THIRD, the left two thirds open on the depth of the street. The background is fixed and does not travel.

When the camera changes state mid-shot, split it by phase with timestamps:

> 0.0-5.1s: in @image1's RIGHT hand at arm's length, selfie framing, 22mm, gentle barrel distortion. Live handheld weight: vertical bobbing with his breathing, lateral sway, roll tilts, micro-jitter.
> 5.1-7.3s: he lowers it and the framing falls with his hand - street, kerb, then asphalt swinging up through frame as the lens descends, still shaking.
> 7.3-16.0s: it rests ON THE GROUND, 25cm up, tilted slightly up, looking down the street. From this instant COMPLETELY DEAD STILL - no breathing, drift, float or jitter, because nobody holds it.

"Because nobody holds it" is the kind of causal reasoning that makes models comply - it explains *why* the stillness is absolute.

A walking camera needs its own geometry stated:

> 35mm, chest height, shoulder-mounted handheld walking BACKWARDS in front of him for all 20 seconds, retreating at exactly his pace so he stays the same size in frame. Real operator weight: a soft vertical step-bounce per stride, small roll, tiny reframing corrections, never smooth or mechanical. As the camera retreats his house falls away behind him and THE STREET opens up BEHIND HIS SHOULDERS. Parallax proves the move: the near palm sweeps past, poles cross slower, far houses barely drift.

---

## 06 STAGING

Where every person and object physically is, and what they are doing with their bodies. Precision here is what stops the model rearranging the scene.

> STAGING: @image1 stands planted on the asphalt, weight rocking foot to foot. RIGHT hand holds the camera at arm's length. LEFT hand is free, gesturing loosely as he talks, then dropping. @image2 lies FLAT ON ITS SIDE on the asphalt at his feet, front wheel turned, one pedal on the ground, shadow tight under it. Mid-ground left: @image4 PARKED at the kerb, engine off, completely stationary, wheels not turning. @image3 sits on its roof, one knee up, other leg hanging down the door; in her LEFT hand a light wooden baseball bat stands VERTICALLY, knob on the roof beside her hip, palm capping the end like a cane.

Note which hand holds what. Models swap hands freely otherwise, and across a sequence that reads as an error.

---

## 07 BACKGROUND LIFE

Anyone not driving the action will freeze into a statue unless told not to. This block is cheap and transforms how alive a shot feels.

> BACKGROUND LIFE - NEVER FROZEN, ESPECIALLY ONCE THE CAMERA IS DOWN. From 7.3s on, @image3 and @image4 sit at the LEFT EDGE of frame, soft and out of focus, both moving throughout. @image3 chews nonstop, her hanging leg swings and taps the door, she shifts her seat, regrips the bat, pushes hair off her face, turns to watch him. @image4 shifts weight hip to hip, unfolds and refolds his arms, pushes off the wing and settles back. Hair and clothes move in the breeze. Neither ever holds a pose or goes statue-still.

---

## 08 ACTION, TIMED

Timestamped beats covering the full duration, with dialogue in quotes inside the beat that contains it.

> ACTION, TIMED:
> 0.0-1.2s Frame is BLACK because his palm is pressed flat over the lens. The palm slides away and the street floods in. Not a fade.
> 1.2-2.2s Framing settles on his face. He is already mid-thought, into the lens.
> 2.2-4.0s @image1, grinning down the lens: "Some people make this look difficult."
> 4.0-4.8s In depth @image3 turns her head and finds the camera, looking past him into the lens, not at him.
> 4.8-7.6s @image3, flat and dry, chewing between words: "He rehearsed that line in the mirror. Changed shirts twice."
> 7.6-8.4s @image1 turns his HEAD sharply left toward her, then straight back to the lens.

Close the block with pacing instruction:

> Every beat lands on the tail of the one before. No dead air, no waiting. Speech is never sped up or compressed.

Or, for a slower scene: "Do not rush the dialogue. Leave silence between lines."

---

## 09 ACTING

Direct the performance physically, and name what it is *not*. Facial action units (AU numbers from FACS) are a precise shorthand many models respond to - AU4 brow lowerer, AU6 cheek raiser, AU12 lip corner puller, AU14 dimpler, AU17 chin raiser.

> ACTING: @image1's eyes are fully visible, uneven natural blinking, broad easy grin AU6+AU12. At 4.8s, on her words, the grin CRACKS for half a second - AU4 brows pull in, one lip corner tightens AU14 - then reasserts wider than before, a faint AU4 trace behind it. A man taking a hit and covering it, never a comic mug. @image3's eyes sit behind tinted lenses, so it all plays in her brows, nostrils, jaw, mouth and small tilts of the chin. Fully deadpan, never smiles, never seeks a reaction. Identity and skin texture stay constant.

Two reusable devices: when eyes are hidden, say where the performance moves instead; and always add "identity and skin texture stay constant" so the face does not soften over the take.

---

## 10 WHO SPEAKS

The block that fixes AI dialogue's worst failure - everyone silently mouthing every line.

> ONLY THE SCRIPTED LINES ARE SPOKEN. No ad-libs, no mumbling, no grunts, no unscripted sighs or breaths-as-voice, no chuckles, no overlapping speech, no offscreen voices. Mouths closed before and after their lines. @image5 never speaks.

When one character listens through another's line, say so explicitly:

> Throughout, @image1's MOUTH STAYS CLOSED - lips together, jaw still, not one word shaped. He only listens; he never mouths, echoes or lip-syncs her line.

For off-screen dialogue: "ONLY @image3 SPEAKS, AND ONLY FROM OFF-SCREEN - she is never seen delivering these lines and never enters focus."

And where body sound could be mistaken for voice: "His hard breathing after the effort is body sound only, never a vocalisation."

---

## 11 SFX

The physical sound layer, listed. State the music policy here or in block 01.

> SFX - wind past the mic, distant traffic, dry palm fronds, shoe scuff on grit, a small sharp bubblegum POP, the camera knocking onto grit, footsteps, chain and freewheel, tyres roaring, a hard landing behind camera, the boombox playing thin and small across the street.

"Thin and small across the street" is distance written as sound - that is what makes a soundscape read as a place rather than a layer.

---

## 12 STRICT NEGATIVES

Every failure this specific shot invites. Generic negatives do little; shot-specific ones do a lot.

> STRICT NEGATIVES: the camera body is never seen in frame. @image1 never lip-syncs or mouths @image3's line. @image3 and @image4 never freeze or go statue-still. No tripod, gimbal, dolly or crane. Once the camera is down it never moves again - no handheld breathing after 7.3s, no drift, reframing, pan, tilt or push. No slow motion or speed ramp; the hop plays full speed. No cuts. The BMX never spins in the air, no 180. NOTHING ELSE DRIVES OR ROLLS: every parked car stays parked, engines off, wheels never turning; the moto never moves. @image3 never leaves the roof of the coupe. No relighting or change of time of day.

The recurring categories worth checking on every shot:

| Category | Typical negative |
|---|---|
| Rig | No tripod, gimbal, dolly, crane or drone; no stabilised or smooth camera |
| Time | No slow motion, no speed ramp |
| Cuts | No cuts, no second angle, no close-up insert, no reverse angle |
| Vehicles | Nothing drives or rolls; engines off; wheels never turn |
| Freezing | Nobody goes statue-still |
| Camera visibility | The camera body is never seen |
| Mouths | Nobody lip-syncs another character's line |
| Light | No relighting, no change of time of day or weather |
| Invention | Characters named in dialogue but not present never appear; no flashback |

---

## Working practice

- **Write shot one in full, then diff.** Subsequent shots in the same scene change blocks 02, 05, 06, 08, 09 and 12. Blocks 01, 03, 04, 07 and 11 are mostly stable, which is why the fixed order pays off.
- **Count the references and keep their order stable** across a scene. Changing which number is which invites the model to swap people.
- **Prefer one long take to several short ones** where the performance can carry it. One generation, no continuity risk, and often a better shot.
- **Keep critical action out of the final second**, where models glitch.
- **When a generation fails, name the block that failed** rather than rewriting everything. A fourth person means block 04; a floating camera means 05 and 12; a frozen background means 07.

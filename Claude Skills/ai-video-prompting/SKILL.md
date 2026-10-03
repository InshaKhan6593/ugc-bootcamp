---
name: ai-video-prompting
description: >-
  Writes AI video prompts that move cleanly - image-to-video, text-to-video, start and end frames,
  multi-reference packs, timed sequences, multi-shot clips with built-in cuts, dialogue and lip-sync,
  consistent character voices, sound design and the post-generation realism pass - for models like
  Seedance, Kling, Veo, Gemini Omni and similar. Use when the user says "animate this image", "write a
  video prompt", "make this a 15 second clip", "shot list", "add dialogue", "the character should
  say", "my video looks warped / rubbery / drifts", "the lip-sync falls apart", "make AI footage look
  real", or "motion control". Do NOT use for still image prompts (use ai-image-prompting), pure
  camera/lighting craft questions (use ai-cinematography), ad scripts (use ugc-ad-creator) or a whole
  film (use ai-filmmaking).
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 4 (video models, camera movement, lip-sync, voices, removing the AI look)
---

# AI Video Prompting

Better input creates better output. Build a strong still first, give the model the right references, then write a prompt about what *moves*. Almost every warped, rubbery, drifting clip traces back to one of three things: a weak start frame, a prompt that re-describes the image instead of directing it, or too much happening at once.

## Critical rules

1. **Do not re-describe the start frame.** The model can see it. Describe the action, the camera, the environmental motion and the timing - nothing else.
2. **One main subject movement, one main camera movement, one clear scene.** Overcrowded prompts morph. If the shot needs two actions, it needs two clips.
3. **Fill all six movement slots** - movement and rig, start, speed, framing, end, time. An unspecified move becomes a slow aimless drift. The catalogue lives in `ai-cinematography/references/camera-moves-catalogue.md`.
4. **Static has to be stated:** "locked tripod, no camera movement, hold the same framing, zero drift". Silence gets you a float.
5. **Real time by default.** Ask for slow motion only on the one moment that needs it, and say exactly what slows - the whole world, or one object.
6. **The bigger the face, the simpler the move.** Wides forgive flights, spins and sweeps. Once a face fills the frame: a controlled push, a slow slide, or a focus shift.
7. **Think in shots, not videos.** Clips are short. Split the idea into shots, each with one purpose, then assemble in the edit.
8. **Keep the start frame's light.** The still already fixed the source, direction and mode. Adding "cinematic lighting" to a phone-lit UGC frame fights the image and the clip looks wrong.
9. **Dialogue length is a hard constraint.** Too many words in one clip makes the character speak unnaturally fast. Roughly 2.5 spoken words per second, and keep critical dialogue away from the final second where models glitch.
10. **Lock the voice once, then never reword it.** Even a one-word change in a voice description can hand you a different person.

## Workflow

### Step 1: Pick the input type
| Input | Use it for |
|---|---|
| Text-to-video | Fast concept tests where exact identity does not matter |
| Image-to-video / start frame | The default whenever character, product or look must be controlled |
| Start + end frame | Reveals, transitions, transformations. The two frames must feel like the same shot |
| Multi-reference (omni-reference) | Separate tagged images for character, product, location, style, plus audio. Say which reference appears in which beat |

Details in `references/video-inputs.md`. Get the image right first - a bad still gives a bad clip, and fixing it in the video model is the expensive route.

### Step 2: Choose the camera move
Pick the move that serves the story: push-in for emotion, pull-out for scale, orbit for a hero moment, handheld for UGC realism, static for performance. The decisive distinctions - dolly versus zoom, why sliders need a foreground object, what tracking from behind versus in front communicates, why a whip pan needs a target, and the documentary snap zoom that makes AI footage feel filmed by a human - are in `ai-cinematography` (step 6 and the two move references).

### Step 3: Write the prompt

**Single shot:**
[what moves in the subject] + [camera move in six slots] + [environmental motion] + [realism cues] + [sound direction, if the model makes audio]

> Steam rises gently from the coffee. Camera: slow dolly in from a locked start, easing in, keeping the cup centred, ending on a close-up of the rim and holding. Real time, no slow motion. Soft handheld realism, natural motion blur. Ambient cafe sound.

**Timed sequence (around 15 seconds):**
- 0-3s setup
- 3-7s action
- 7-12s escalation
- 12-15s payoff or hero moment

Write what the subject, the camera and the effects do in each beat. Every beat should land on the tail of the one before - no dead air. Worked examples in `references/seedance.md`.

**Multi-shot with built-in cuts:**
- Shot 1 setup and subject position
- Shot 2 camera cut or movement
- Shot 3 action or reaction
- Shot 4 payoff

Give each shot at least about three seconds. Examples in `references/kling.md`.

**Dialogue and talking avatars.** A plain prompt works well: `She is vlogging, she says, "..."`. Then:
- Keep lines short and natural. If it would not sound normal said out loud, it will not sync well.
- Punctuate for rhythm. Ellipses and commas tell the model to breathe; unpunctuated lines get read like a script.
- Paste the **voice blueprint** verbatim in every prompt for that character - for example "light Australian accent, relaxed and confident, medium pace, slight vocal rasp". Choosing an accent narrows the model's voice pool, which is exactly what makes the voice repeatable. Sixteen ready blueprints by delivery style are in `references/voice-and-sound.md`.
- Respect the model's sync window: Veo generates 8-second clips; Kling drifts past about ten seconds of speech. Model-by-model lip-sync ranking is in `references/model-choice.md`.
- State who speaks and who does not. "Only @image3 speaks this line; the others' lips never move to words, no ad-libs, no mumbling, mouths closed before and after" prevents the common failure where every character silently mouths the dialogue.

**Carry the image rules into motion.** A foreground layer creates parallax when the camera moves - a slow push or lateral slide past something near the lens is the cheapest way to make a shot read as three-dimensional. Match the move to the mode: UGC means handheld micro-jitter and small reframes; cinematic means dolly, orbit, crane.

### Step 4: Extend a scene
To continue, export the final frame of the clip and use it as the next start frame. Keep lighting direction, wardrobe and the look block identical across shots, or the cut will not hold.

### Step 5: Output
Return:

1. The **prompt(s)** in clean blocks, one per shot, with timings.
2. A **references line** - which image is the start frame, which references to attach, and in what order.
3. **Settings notes** - duration, aspect ratio, start/end frame or multi-reference.
4. A reminder of the **realism pass** for anything meant to look phone-shot.

### Step 6: Realism pass, after generation
Raw AI footage is too contrasty, too saturated and too stable - that combination is the giveaway. In the editor, on an adjustment layer:

1. Bring contrast down noticeably. This is the biggest tell; drop it until the image stops feeling like a render.
2. Lower saturation slightly. If it starts looking lifeless, you went too far.
3. Lift highlights a little if the image feels dense or heavy.
4. Add a handheld shake so subtle the viewer cannot notice it. If they notice the shake, reduce it.

Compare before and after rather than trusting the slider values. Details in `references/realism-pass.md`.

## Troubleshooting

| Problem | Fix |
|---|---|
| Warped faces, rubbery motion | Simplify to one action and one move; use a start frame plus a multi-angle character reference |
| Camera drifts or floats | Fill all six slots; for static shots state no movement, zero drift |
| Face changes when the subject turns | Attach a character sheet showing several angles as a tagged reference |
| Fake-looking slow motion | State real time, normal speed; or name exactly what slows |
| Character speaks too fast | Cut words; split the line across two shots |
| Lip-sync drifts late in the clip | Shorten the speech, or switch to a model that holds sync longer; keep the last second action-free |
| Everyone mouths the same line | Name the speaker explicitly and forbid the others' lips from moving |
| Voice changes between clips | Paste the identical voice blueprint; never paraphrase it |
| Glitch at the end of the clip | Move key action and dialogue earlier; end on a simple hold |
| Motion transfer broke | Use a cleaner reference clip: one visible person, unobstructed body, stable framing, no props the avatar lacks - see `references/motion-control.md` |
| AI edit changed too much | Smaller, iterative edits; check against the list in `references/video-editing.md` |
| Footage looks too clean to be real | Run the realism pass; it is a colour and movement problem, not a resolution problem |

## Reference files (open only the one you need)
- `references/video-inputs.md` - input types, reference packs, focus and duration
- `references/seedance.md` - start frames, timed sequences, continuation, acting direction, product ads
- `references/kling.md` - multi-shot, references, start/end frames, 30-technique camera toolkit, examples
- `references/voice-and-sound.md` - voice blueprints by delivery style, punctuation for rhythm, voiceover and SFX
- `references/motion-control.md` - transferring movement from a reference clip onto an avatar
- `references/video-editing.md` - AI video editing workflow and QA checklist
- `references/realism-pass.md` - removing the AI look in post
- `references/model-choice.md` - which model for which job, including the lip-sync ranking (dated; verify)

Related: `ai-cinematography` for camera moves and light; `ai-avatar-builder` for character sheets; `ai-filmmaking` for multi-shot films; `ai-clone-yourself` for talking-head clones of the user.

Course material names particular apps and models. Apply the principles in whatever tool the user has.

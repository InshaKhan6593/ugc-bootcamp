# Which model for which stage

> Model names and rankings date fast. The *reasoning* below stays useful; treat specific names as a snapshot from the course material (late 2026) and check current capability before committing a budget. Never tell the user a platform is required - these are jobs, and whatever they already pay for probably fills most of the slots.

## Stop asking which model is best

Ask what job the model has to do right now. Four families, four jobs:

| Family | Job | Where it sits in the workflow |
|---|---|---|
| Chat | Thinking, planning, scripts, prompts, troubleshooting | Step 2, and every time something is not working |
| Image | Characters, products, scenes, thumbnails, start frames | Steps 3 and 4 - the visual foundation |
| Video | Motion, camera, performance, dialogue | Step 5 |
| Voice and audio | Voiceover, dialogue, SFX, ambience, music | Step 6, and inside audio nodes |

A saw, a drill and a paint sprayer are all good tools; you would not use them for the same job. The skill is reaching for the right one.

## Chat: the planning layer
Any strong general chat model works. Use it for ideas when stuck, for writing image and video prompts, for scripts, hooks, captions and content plans, for diagnosing a bad result, and for planning the whole flow before a generator is opened. Most people use chat to write emails; the leverage is using it as the creative director for the entire pipeline.

## Image: the visual foundation
What differentiates image models in practice:

- **Realistic humans, skin and faces** - the deciding factor for avatars, UGC and influencers.
- **Reference fidelity and editing** - keeping a face, product or label identical while something else changes. This is what makes a model good for passports, product-in-hand and local fixes.
- **Text rendering** - whether a label or sign comes out legible.
- **Stylised and art-directed work** - concept frames, illustration, non-photoreal looks.

From the course material: GPT Image 2.0 and Nano Banana Pro are the current workhorses for realism, reference work and editing, and either can stand in where older material says Midjourney. Midjourney remains strong for stylised and cinematic concept frames.

Practical rule: generate on whichever model gives you the most believable skin, then do local fixes on whichever model follows a reference most faithfully.

## Video: the motion layer
Choose by what the shot has to do:

| The shot | What matters | Course guidance |
|---|---|---|
| Talking avatar, dialogue, hero ad cut | Lip-sync accuracy, expressive face, natural voice | Seedance is the clear top pick and the most expensive; Gemini Omni is the strong, cheaper second and notably natural on voice; Veo 3.1 (Fast or Quality) is solid and cheaper still, with 8-second clips; Kling drifts after about 10 seconds of speech and is not the first choice for talking heads; Grok Imagine syncs cleanly but sounds robotic |
| B-roll, slow cinematic movement, controlled camera | Camera obedience, clean motion, resolution | Kling 3.0 4K, and Kling Motion Control when the movement must follow a specific path |
| Multi-reference scenes (cast + props + location) | How many references it accepts | Seedance accepts up to 9 images, 3 videos and 3 audio at once - this is what makes film-scale shot prompts possible |
| Clone and talking-head volume | Identity stability over long takes | A dedicated clone platform, not a general video model - see `ai-clone-yourself` |
| Cheap iteration | Speed and cost | Any fast model. Find the hook on a cheap model, then regenerate the winner on the best one |

Two rules that outlast any model list:
1. **Cheap to find it, best for the hero.** Test three hooks on a cheap model; rebuild the winner on the strongest.
2. **Clip length is a real constraint.** Keep dialogue inside what the model holds in sync, and keep critical action away from the final second where models glitch.

## Voice and audio: the immersion layer
A clip can look right and still feel generated if the sound is empty. Use a voice model for narration, character dialogue and ad reads; a sound-effects tool for the physical layer (footsteps, fabric, traffic, room tone); and generated or library music for pacing and mood.

Audio is usually the cheapest large improvement available to a finished piece, and the one people skip.

## Cost discipline

- Generate images before video, always. Video is the expensive stage; the image stage is where mistakes should happen.
- Upscale before animating rather than regenerating a soft clip.
- Test one node before running a chain.
- Keep a cheap model configured for iteration and an expensive one for finals, rather than defaulting to the expensive one.
- Batch so that one locked decision serves many outputs.

# The six-step creator workflow, in full

Idea - Chat - Image - Refine - Video - Edit and post. The scale changes between a single still and a short film; the order does not.

## Contents
- [1. Idea: define the outcome](#1-idea-define-the-outcome)
- [2. Chat: plan and write](#2-chat-plan-and-write)
- [3. Image: generate the foundation](#3-image-generate-the-foundation)
- [4. Refine: edit and upscale](#4-refine-edit-and-upscale)
- [5. Video: add motion](#5-video-add-motion)
- [6. Edit and post](#6-edit-and-post)
- [Worked walkthroughs](#worked-walkthroughs)
- [The AVB six-part prompt framework](#the-avb-six-part-prompt-framework)

---

## 1. Idea: define the outcome

A vague desire is not an idea. "I want to make something cool" produces vague prompts, which produce average outputs, which produce content nobody cares about.

A proper idea is specific enough to imply its own settings:

- "A 15-second cinematic TikTok of a samurai standing in heavy rain, for my fantasy page."
- "A product photo of a perfume bottle in a luxury bathroom, for a client's Instagram."
- "A 30-second UGC-style skincare ad with hook, problem, solution, CTA."
- "A new recurring character for my AI influencer account."

Answer before generating:

| Question | Why it matters |
|---|---|
| What am I making? | Decides the whole pipeline |
| Where is it going? | Gives aspect ratio, duration and pacing |
| Who is it for? | Decides tone, references and language |
| What should it make them feel? | Becomes the mood word in every prompt |
| What is the final asset? | Still, clip, ad, thumbnail, film, client deliverable - stops you over-building |

Two minutes here saves an hour later. Knowing "9:16 TikTok of an AI influencer" already fixes the ratio, subject, environment, mood, platform and visual direction before a tool is open.

---

## 2. Chat: plan and write

Treat the chat as a creative director, prompt engineer and strategist - not a vending machine for prompts. This is where a general concept becomes something usable, and where a weak idea gets strengthened at zero credit cost.

The briefing formula: **context, goal, details, output format.** Full templates - idea generation, improving a weak idea, writing image prompts, fixing fake-looking results, scripts, critique, variations, JSON output, and the follow-up commands that upgrade any answer - are in `chat-prompts.md`.

Push back on the first answer every time. Ask: what is weak here, what will make this look fake, what did you leave vague, give me five stronger versions. The second answer is usually the usable one.

---

## 3. Image: generate the foundation

Start with images even when the final asset is video. Images are cheaper, faster and far easier to control, so they are where you lock composition, character, setting, light and feel. Jumping straight to video means fixing the wrong character, framing and light inside the most expensive model in the pipeline.

Practice:

- Set the aspect ratio for the destination before generating, not after.
- Generate several options, not one. The second or third is often the keeper.
- Keep the prompt intentional rather than long. A 35-word prompt where every word matters beats a 200-word pile of adjectives.
- Put the most important detail early; models weight the start of a prompt more heavily.

Then run the image gate (see the SKILL.md quality gates). A failed gate means regenerate or go back to chat - not forward.

---

## 4. Refine: edit and upscale

Beginners accept the first decent result. The habit that separates serious work is asking "what would make this better?" and then fixing exactly that.

Worth editing (local, specific problems):
- background needs changing
- light needs adjusting
- hands slightly wrong
- outfit not right
- product label not crisp
- face too smooth
- one detail ruining an otherwise strong frame

Worth regenerating instead (structural problems): wrong composition, wrong character, wrong concept, wrong camera angle, or a frame that just feels off. Do not polish a bad foundation.

Then upscale, before animation, not after: 2x takes 1K to 2K, 4x takes 1K to 4K. More pixels going into the video model means a visibly cleaner clip coming out. Always upscale hero images, client deliverables and anything headed for a website or static ad.

---

## 5. Video: add motion

Take the refined still as the start frame. Do not re-describe the image - the model can see it. Prompt what moves:

- **Camera movement** - dolly, push-in, pan, tilt, orbit, handheld follow (six-slot method in `ai-cinematography`)
- **Subject movement** - turns head, walks forward, picks up the object, exhales
- **Environmental motion** - wind in hair, rain, steam, traffic, fabric
- **Light changes** - sun shifting, shadows moving, a screen flickering

One main subject action and one main camera move per clip. If the final asset is a still, skip this step entirely - not everything needs to become video.

Depth and dialogue handling live in `ai-video-prompting`.

---

## 6. Edit and post

Editing is not an afterthought; pacing, sound and packaging are a large share of how the finished piece lands.

- Make the first second strong. The first clip should not run longer than about three seconds before something changes.
- Add captions when they help the viewer follow the idea - reading keeps people watching.
- Build ambient sound: footsteps, rain, crowd, fabric movement, room tone, traffic. Silence reads as unfinished.
- Cut pacing and music to the energy of the piece; shorten clips that sag.
- Run the realism pass on AI footage: drop contrast noticeably, reduce saturation slightly, lift highlights a little, add a shake subtle enough that the viewer never notices it. Details in `ai-video-prompting/references/realism-pass.md`.
- Export to the platform's preferred spec rather than the biggest numbers available. Posting mechanics and upload settings are in `viral-short-form`.

---

## Worked walkthroughs

### A single cinematic still for a fantasy page
Idea (9:16, melancholic knight) - chat (develop the scene, write the prompt with subject/environment/camera/lighting/mood/style) - image (generate 4, pick the one with the best light logic) - refine (fix armour texture, upscale 2x) - skip video - post as a carousel or still.

### A 15-second cinematic TikTok
Idea - chat (shot list of three or four beats, one look block) - images (one start frame per beat, same look block pasted verbatim) - refine (gate and upscale all of them) - video (animate each beat; one action, one move) - edit (cut to beat, sound design, realism pass, captions).

### A UGC ad
Idea and brief - `ugc-ad-creator` for strategy, hooks and script - character passport in `ai-avatar-builder` - shot stills in UGC/phone mode - refine with label-lock on the product - animate the talking beats and the product beats separately - edit with hard jump cuts and ambient sound only - produce two or three variations changing one variable each.

### A week of content for a persona
Lock persona, look block and voice blueprint once. Plan a grid of seven posts by angle. Generate all stills in one pass, gate, upscale the keepers, animate in a second pass, edit in a third. Details in `batching.md`.

---

## The AVB six-part prompt framework

The compass used at every stage. Whenever a prompt is not working, one of these six is missing, weak or unclear:

1. **Subject** - who or what is in frame. A person: age, hair, clothing, expression, posture, action. A product: shape, material, colour, texture, label, position.
2. **Environment** - a specific place, time of day, weather, background objects and textures. Environment is where story comes from: "a woman in a white studio" versus "outside a nightclub at 1am in the rain".
3. **Camera** - how we are seeing it. Angle, shot size, lens; for video, movement.
4. **Lighting** - the source, its direction and quality. Never just "cinematic lighting".
5. **Mood** - one or two words. The same setup turns inside out between "peaceful and nostalgic" and "tense and paranoid".
6. **Style** - optional, at the end. For realism, often best left off entirely.

Recipe: **[subject] in [environment], [camera angle and framing + lens], [light source and direction], [mood], [style or grade].**

Avoid words that push toward plastic renders: "cinematic masterpiece", "hyper-detailed", "ultra-glossy", "perfect lighting", "8K masterpiece", "flawless", "award-winning". Realism comes from specific cues, not hype.

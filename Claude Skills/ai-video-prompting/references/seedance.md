# Seedance: start frames, timed sequences, example prompts

Timed-sequence prompting, scene continuation, acting, product ads and omni-reference.

# Seedance 2.0 Video Generation Power

## Contents

- [1. Use start frames for stronger control](#1-use-start-frames-for-stronger-control)
- [2. Prompt with timed sequences](#2-prompt-with-timed-sequences)
- [3. Turn text prompts into movie-style scenes](#3-turn-text-prompts-into-movie-style-scenes)
- [4. Continue scenes with exported still frames](#4-continue-scenes-with-exported-still-frames)
- [5. Use slow motion and acting prompts](#5-use-slow-motion-and-acting-prompts)
- [6. Build product ads with the same method](#6-build-product-ads-with-the-same-method)
- [8. Use Omni Reference for more control](#8-use-omni-reference-for-more-control)
- [The big idea](#the-big-idea)
- [Timed-sequence examples from the course notes](#timed-sequence-examples-from-the-course-notes)
- [🎬 AI Video Prompt – “Neon Duel” (15s Time Sequence)](#ai-video-prompt-neon-duel-15s-time-sequence)
- [🎬 AI Video Prompt – “Neon Duel” (15s Time Sequence)](#ai-video-prompt-neon-duel-15s-time-sequence)
- [🎬 AI Video Prompt – “Awakening Power” (15 Seconds, 3–5s Beats)](#ai-video-prompt-awakening-power-15-seconds-35s-beats)

---

## 1. Use start frames for stronger control

Seedance can work from text, but start frames give the model a visual foundation. For cinematic action scenes, product ads, or character-based shots, create the first frame first, then animate it.

* Use NanoBanana Pro, GPT Image 2.0, or another image model to make the starting frame.

* Bring the image back into ChatGPT and ask for a video prompt based on that image.

* Upload the image as the start frame in Seedance.

* Use the prompt to describe motion, effects, camera movement, and timing.

give me a detailed image prompt for Nanobanana pro, I want a scene of a young woman outside in natural lighting, at a park

Here's a high-end **NanoBanana Pro prompt** designed for maximum realism, strong composition, and clean lighting 👇

📷 **NanoBanana Pro Image Prompt (Ultra-Realistic Park Portrait)**

**Prompt:**

A hyper-realistic close-up portrait of a young woman standing in a peaceful park during late afternoon golden hour. She is positioned slightly off-center, framed by soft greenery and blurred trees in the background. Natural sunlight filters through the leaves above, creating soft dappled lighting across her face and shoulders.

She has natural skin texture with visible pores, faint freckles across her cheeks and nose, and subtle imperfections that enhance realism. Her expression is calm and introspective, with a soft, relaxed gaze looking slightly past the camera. A gentle breeze moves a few loose strands of her hair across her face.

Her hair is medium-length, slightly wavy, and naturally flowing, catching highlights from the sunlight. The lighting creates a warm glow on her skin, with soft shadows shaping her cheekbones and jawline.

She is wearing a simple, neutral-toned outfit (light beige or white), with soft fabric that reacts naturally to the breeze. No logos or text.

Shot on a high-end mirrorless camera with an **85mm lens**, shallow depth of field, cinematic bokeh, ultra-sharp focus on the eyes. Background is softly blurred with creamy bokeh, featuring hints of green foliage and warm sunlight.

Color grading is natural and true-to-life, slightly warm tones, no over-processing. The overall look should feel like a real photograph, not AI-generated.

Start frames lock in the visual direction before Seedance adds motion, acting, effects, and camera movement.

## 2. Prompt with timed sequences

For 15-second generations, a normal paragraph prompt can work, but timed sequence prompts give more control. Break the shot into sections so Seedance knows what should happen across the clip.

* Ask ChatGPT for a 15-second time sequence layout.

* Describe what should happen in each beat or camera cut.

* Use timestamps to control action, effects, character movement, and reveals.

* This is especially useful for battle scenes, product ads, and cinematic sequences.

I want a video prompt, action scene where this woman powers up and saves some people from a giant monster. <mark>Give it to me broken up into a time sequence over 15 seconds</mark>

Here's a high-intensity, cinematic 15-second video prompt tailored to that exact character and realism style
👇

🎬 AI Video Prompt - "Awakening Power" (15 Seconds. 3-5s Beats)

Timed prompts help control what happens in each moment instead of letting the model guess the full sequence.

```text
Prompt structure

Start frame + 15-second time sequence prompt: 0-3s setup, 3-7s action, 7-12s
escalation, 12-15s final hero moment.
```

## 3. Turn text prompts into movie-style scenes

Text to video can still work well when the prompt is detailed. Use it when you do not need exact character or product consistency, or when you want fast concept exploration.

* Give ChatGPT a rough idea and ask for a strong video prompt.

* Paste the prompt directly into Seedance without a reference image.

* Use this for action concepts, cinematic scenes, and quick visual exploration.

* For tighter control, move back to image-to-video with a start frame.

Text-to-video is useful for testing cinematic ideas quickly when exact identity or product accuracy is less important.

## 4. Continue scenes with exported still frames

To extend a scene, export the last frame of the video and use it as the start frame for the next generation. This lets you build longer sequences shot by shot.

* Upload the video to CapCut.

* Use the menu to export a still frame from the final moment.

* Use that still frame as the next Seedance start frame.

* Generate the next clip as a continuation.

Exporting the final frame lets you continue the same scene instead of trying to create one long video in a single generation.

## 5. Use slow motion and acting prompts

Seedance is strong at action, fighting, emotional acting, and realistic character performance. Slow motion can add contrast and make visual effects feel more cinematic.

* Prompt for specific acting beats, facial reactions, and emotional changes.

* Add slow motion where the moment needs impact.

* Do not overload the motion with too many unrelated actions.

* Use dialogue or emotional conflict when testing acting realism.

Seedance handles acting and character emotion well when the prompt gives it a clear dramatic moment.

## 6. Build product ads with the same method

Product ads can use the same start-frame and timed-sequence workflow. Create the product hero frame first, then prompt Seedance to turn it into a high-production ad.

* Generate a clean product start frame.

* Ask ChatGPT for a 15-second product ad sequence.

* Use timed beats for product reveal, ingredient shots, splash shots, camera motion, and final hero moment.

* Refine prompts when the first result is not strong enough.

A product start frame plus a timed sequence prompt can turn one image into a full ad-style clip.

**Prompt structure**

Start frame + 15-second time sequence prompt: 0-3s setup, 3-7s action, 7-12s escalation, 12-15s final hero moment.

## 8. Use Omni Reference for more control

Omni Reference gives the model multiple visual references at once. Use it when the ad needs a product, person, ingredient, prop, or scene element to appear in a specific order.

* Upload separate reference images for each important element.

* Tell ChatGPT which image should appear in which beat.

* Tag or identify each reference clearly so the model knows what belongs where.

* Use this when a single start frame is not enough context.

Multiple references help Seedance understand products, people, ingredients, and scene elements instead of inventing them.

## The big idea

Seedance 2.0 is strongest when you treat it like a shot-based production tool. Build the visual foundation first, describe the motion clearly, use timed sequences for control, and use references when the model needs to preserve specific people, products, or scene elements.

* Start with a strong image when control matters.

* Use timed prompts for 15-second scenes.

* Use final-frame exports to extend scenes.

* Use Omni Reference when the scene needs multiple controlled elements.

---

## Timed-sequence examples from the course notes

- Phase4_04_Seedance-20_seedance_2_video_generation_power_(1).pdf (Lesson Guide)
  - Phase4_04_Seedance-20_transcript33.pdf (Transcript)

1080p and 4k now available!

PROMPT EXAMPLES FOR TIME SEQUENCES -

## 🎬 AI Video Prompt – “Neon Duel” (15s Time Sequence)
Style: ultra-realistic cyberpunk, Tron-inspired, cinematic combat
Environment: dark digital temple, reflective black floor, neon glow (blue vs red)
Characters: two Japanese cyber warriors with glowing armor lines + energy katanas

### ⏱️ 0:00 – 0:03 (Standoff)
Shot: Wide cinematic, slow push-in
Both warriors stand facing each other in a dark neon arena.
Blue and red light reflects across the glossy floor.
Their armor pulses faintly, energy katanas humming in their hands.
Particles float in the air, subtle fog drifting.
SFX: low ambient hum, energy blade buzz, faint digital atmosphere

### ⏱️ 0:03 – 0:06 (Engage)
Shot: Fast tracking shot circling them
They explode into motion — rapid strikes and parries.
Blades collide, sending bursts of glowing sparks.
Camera orbits them as reflections streak across the floor.
SFX: sharp metallic energy clashes, fast movement swishes

### ⏱️ 0:06 – 0:09 (Momentum Shift)
Shot: Medium → close-up sequence
The red warrior gains the upper hand, pushing forward aggressively.
Blue warrior steps back, narrowly blocking incoming strikes.
Camera cuts tighter — intensity builds.
SFX: heavier blade impacts, rising tension hum

### ⏱️ 0:09 – 0:12 (SLOW MOTION NEAR-DEATH MOMENT)
Shot: Extreme slow-motion, cinematic close-up
The red warrior swings a powerful horizontal strike toward the blue warrior’s neck—
Time slows dramatically.
The blue warrior leans backward just in time…
The glowing blade passes inches from their face.
Neon light reflects in their eyes.
Tiny particles and sparks float in the air.
Hair, fabric, and armor subtly react to the motion.
The blade leaves a glowing trail as it slices past.
SFX: deep slowed-down energy hum, distorted blade whoosh

### ⏱️ 0:12 – 0:15 (Counterattack & Reset)
Shot: Snap back to full speed → dynamic tracking
Time snaps back.
The blue warrior pivots instantly and counters with a fast upward slash.
The red warrior barely blocks — both slide apart across the reflective floor.
Final shot: Wide symmetrical frame
Both warriors reset, glowing blades raised, tension still high.
SFX: sharp clash, energy crackle, ambient hum returns

## 🎬 AI Video Prompt – “Neon Duel” (15s Time Sequence)
Style: ultra-realistic cyberpunk, Tron-inspired, cinematic combat
Environment: dark digital temple, reflective black floor, neon glow (blue vs red)
Characters: two Japanese cyber warriors with glowing armor lines + energy katanas

### ⏱️ 0:00 – 0:03 (Standoff)
Shot: Wide cinematic, slow push-in
Both warriors stand facing each other in a dark neon arena.
Blue and red light reflects across the glossy floor.
Their armor pulses faintly, energy katanas humming in their hands.
Particles float in the air, subtle fog drifting.
SFX: low ambient hum, energy blade buzz, faint digital atmosphere

### ⏱️ 0:03 – 0:06 (Engage)
Shot: Fast tracking shot circling them
They explode into motion — rapid strikes and parries.
Blades collide, sending bursts of glowing sparks.
Camera orbits them as reflections streak across the floor.
SFX: sharp metallic energy clashes, fast movement swishes

### ⏱️ 0:06 – 0:09 (Momentum Shift)
Shot: Medium → close-up sequence
The red warrior gains the upper hand, pushing forward aggressively.
Blue warrior steps back, narrowly blocking incoming strikes.
Camera cuts tighter — intensity builds.
SFX: heavier blade impacts, rising tension hum

### ⏱️ 0:09 – 0:12 (SLOW MOTION NEAR-DEATH MOMENT)
Shot: Extreme slow-motion, cinematic close-up
The red warrior swings a powerful horizontal strike toward the blue warrior’s neck—
Time slows dramatically.
The blue warrior leans backward just in time…
The glowing blade passes inches from their face.
Neon light reflects in their eyes.
Tiny particles and sparks float in the air.
Hair, fabric, and armor subtly react to the motion.
The blade leaves a glowing trail as it slices past.
SFX: deep slowed-down energy hum, distorted blade whoosh

### ⏱️ 0:12 – 0:15 (Counterattack & Reset)
Shot: Snap back to full speed → dynamic tracking
Time snaps back.
The blue warrior pivots instantly and counters with a fast upward slash.
The red warrior barely blocks — both slide apart across the reflective floor.
Final shot: Wide symmetrical frame
Both warriors reset, glowing blades raised, tension still high.
SFX: sharp clash, energy crackle, ambient hum returns

## 🎬 AI Video Prompt – “Awakening Power” (15 Seconds, 3–5s Beats)
Style: hyper-realistic, cinematic, handheld + slow motion mix, natural lighting turning dramatic
Character consistency: same woman as image (freckles, natural skin, wavy brown hair, beige top)
Environment: park, golden hour shifting into chaotic atmosphere
Tone: grounded → explosive → heroic

### ⏱️ 0:00 – 0:03 (Calm Before Chaos)
Shot: Medium close-up, slow push-in
The woman stands in the park, soft golden sunlight hitting her face, trees gently swaying. Her hair moves slightly in the breeze.
In the distance, faint rumbling begins. Birds suddenly scatter overhead.
Her expression shifts from calm to alert as she turns her head slightly.
SFX: light wind, distant low rumble, leaves rustling

### ⏱️ 0:03 – 0:06 (Threat Revealed)
Shot: Wide cinematic reveal, slight handheld shake
A massive, terrifying creature bursts through the trees in the background — towering, muscular, unnatural, destroying branches as it moves forward.
People in the park begin running, screaming, chaos erupting.
Dust and debris fill the air, sunlight now partially blocked.
SFX: heavy footsteps, cracking wood, distant screams, deep monster growl

### ⏱️ 0:06 – 0:09 (Power Awakens)
Shot: Close-up → slight slow motion
The woman closes her eyes briefly, breathing in. Subtle glowing light begins forming under her skin, starting from her chest and spreading outward.
Her hair lifts slightly as energy builds. The air around her distorts with heat-like shimmer.
Her eyes open — now glowing faintly.
SFX: rising energy hum, low-frequency pulse, wind intensifying

### ⏱️ 0:09 – 0:12 (Transformation & Takeoff)
Shot: Dynamic tracking shot, slight slow motion
A burst of energy explodes outward from her body, pushing leaves and dust away in a shockwave.
Her stance becomes grounded and powerful. Light radiates around her, subtle aura forming.
She launches forward at high speed toward the monster, camera follows with motion blur.
SFX: energy burst, shockwave blast, wind tearing past camera

### ⏱️ 0:12 – 0:15 (Hero Moment / Impact)
Shot: Slow-motion impact + cinematic wide
She slams into the monster mid-attack just as it’s about to reach fleeing civilians.
A massive energy impact erupts on contact, sending the creature recoiling backward.
People in the foreground shield themselves as light floods the scene.
Final frame: she stands between the monster and the people, glowing, calm, powerful.
SFX: heavy impact boom, energy crackle, debris falling, fading wind

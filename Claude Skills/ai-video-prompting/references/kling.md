# Kling: features, camera toolkit, example prompts

Multi-shot, omni-reference, start/end frames and 30 camera techniques.

# Kling 3.0 Video Features

## Contents

- [What you're building](#what-youre-building)
- [1. Access Kling 3.0 and choose the right settings](#1-access-kling-30-and-choose-the-right-settings)
- [2. Test simple dialogue and emotion scenes](#2-test-simple-dialogue-and-emotion-scenes)
- [3. Use Omni Reference for character and object control](#3-use-omni-reference-for-character-and-object-control)
- [4. Build character references from multiple angles](#4-build-character-references-from-multiple-angles)
- [5. Use multi-shot mode for built-in camera cuts](#5-use-multi-shot-mode-for-built-in-camera-cuts)
- [6. Use ChatGPT to write each shot prompt](#6-use-chatgpt-to-write-each-shot-prompt)
- [7. Combine start and end frames when needed](#7-combine-start-and-end-frames-when-needed)
- [8. Apply Kling to UGC, branded content, and dynamic shots](#8-apply-kling-to-ugc-branded-content-and-dynamic-shots)
- [The big idea](#the-big-idea)
- [Kling AI Cinematic Camera Movement Toolkit](#kling-ai-cinematic-camera-movement-toolkit)
- [How To Use This Toolkit](#how-to-use-this-toolkit)
- [8. Smooth Tracking Behind Character](#8-smooth-tracking-behind-character)
- [9. Slow Pan Right](#9-slow-pan-right)
- [10. First-Person POV Camera](#10-first-person-pov-camera)
- [11. Top-Down (Bird's Eye) View](#11-top-down-birds-eye-view)
- [12. Low-Angle Shot](#12-low-angle-shot)
- [13. High-Angle Shot](#13-high-angle-shot)
- [14. Push-In Zoom on Face](#14-push-in-zoom-on-face)
- [15. Pull-Out Environmental Reveal](#15-pull-out-environmental-reveal)
- [16. Wide Static Shot with Foreground Movement](#16-wide-static-shot-with-foreground-movement)
- [17. Over-the-Head Tracking Shot](#17-over-the-head-tracking-shot)
- [18. Reveal Shot from Behind an Object](#18-reveal-shot-from-behind-an-object)
- [19. First-Person Camera Falls to Ground](#19-first-person-camera-falls-to-ground)
- [20. Upward Tilt While Approaching Subject](#20-upward-tilt-while-approaching-subject)
- [21. Camera Moves Through Object (Portals, Windows)](#21-camera-moves-through-object-portals-windows)
- [22. Camera Follows Character Turning a Corner](#22-camera-follows-character-turning-a-corner)
- [23. Medium Tracking Shot Alongside Character](#23-medium-tracking-shot-alongside-character)
- [24. Slow Descend Behind Subject from Above](#24-slow-descend-behind-subject-from-above)
- [25. Time-Lapse Pull-Out](#25-time-lapse-pull-out)
- [26. Push Through Fog or Mist](#26-push-through-fog-or-mist)
- [27. Spiral Around Object on Ground](#27-spiral-around-object-on-ground)
- [28. Reverse Tracking (Walking Toward Camera)](#28-reverse-tracking-walking-toward-camera)
- [29. Tracking Shot with Foreground Obstructions](#29-tracking-shot-with-foreground-obstructions)
- [30. Rising Reveal from Behind Subject's Shoulder](#30-rising-reveal-from-behind-subjects-shoulder)
- [🎯 Niche Camera Movements (For Advanced Cinematic Scenes)](#niche-camera-movements-for-advanced-cinematic-scenes)
- [COMBO MOVEMENTS — Cinematic Layering (Bonus Section)](#combo-movements-cinematic-layering-bonus-section)
- [Example shot prompts from the course notes](#example-shot-prompts-from-the-course-notes)
- [Extra tips from the Kling 3.0 lesson video](#extra-tips-from-the-kling-30-lesson-video)

---

## What you're building

Use Kling 3.0 to create longer, more cinematic AI videos with better emotion, multi-shot structure, Omni Reference control, start/end frames, sound effects, and dynamic camera movement. The key is knowing when Kling is useful and when another model like Seedance is still the better production choice.

## 1. Access Kling 3.0 and choose the right settings

* Choose Kling 3.0 from the video model options.

* Adjust duration based on how long the scene needs to play out.

* Use higher resolution where quality matters.

* Expect better cinematic emotion and movement than earlier Kling versions.

Start by choosing the Kling 3.0 model, duration, resolution, and generation setup before testing scenes.

## 2. Test simple dialogue and emotion scenes

Kling 3.0 is much better at natural interaction, fluid movement, and emotional acting than older versions. Use simple dialogue or two-person scenes to test whether the model can hold realism.

* Start with contained scenes like people talking in a kitchen or room.

* Check lip sync, movement, eye contact, and emotional realism.

* Regenerate or adjust prompts when dialogue gets messy.

* Add more detail to the prompt when the emotion needs to be specific.

Simple dialogue tests show whether Kling can hold natural interaction, clean lip sync, and believable emotion.

## 3. Use Omni Reference for character and object control

Omni Reference lets you upload multiple images and tag them as elements the model can understand. This solves problems where a character turns around and the model guesses their face incorrectly.

* Select Kling Omni and open the Omni Reference tab.

* Upload up to seven image references where supported.

* Tag the person, object, or product clearly.

* Use multiple angles when the model needs to understand the identity from more than one view.

Omni Reference gives Kling visual context for characters and objects, which helps preserve identity across angles.

## 4. Build character references from multiple angles

For better face and identity consistency, create multiple angles of the same character first. Use NanoBanana Pro or another image model to generate front, side, and alternate views, then upload them as references.

* Create several images of the same character from different angles.

* Upload those images as references for one named element.

* Use the element tag in your video prompt.

* Compare a generation with and without the element to see the consistency difference.

Multiple angle references help Kling keep the same person instead of inventing a new face when the subject turns.

## 5. Use multi-shot mode for built-in camera cuts

The multi-shot feature is one of the biggest updates. It lets you create multiple camera angles and scene beats inside one generation instead of generating separate clips and stitching everything manually.

* Toggle Multi-shot on.

* Use Automatic if you want Kling to choose the cuts for you.

* Use Custom if you want to decide the timing, camera changes, and action in each shot.

* Each camera cut needs enough time to play out, with a minimum around three seconds.

Multi-shot mode lets one generation contain multiple camera angles, cuts, and story beats.

**Shot prompt structure**

`Shot 1: setup and subject position. Shot 2: camera cut or movement. Shot 3: action/reaction. Shot 4: payoff or final moment.`

## 6. Use ChatGPT to write each shot prompt

For custom multi-shot videos, use ChatGPT to turn a rough story idea into a sequence of shot prompts. Upload or describe the start frame, explain the story, then paste each generated shot prompt into Kling.

* Give ChatGPT the start frame or describe it clearly.

* Explain the rough story you want the clip to tell.

* Ask for separate shot prompts with timing and camera direction.

* Paste each prompt into the matching custom shot field.

Detailed shot prompts help Kling understand what should happen in each camera cut instead of guessing the sequence.

**Shot prompt structure**

`Shot 1: setup and subject position. Shot 2: camera cut or movement. Shot 3: action/reaction. Shot 4: payoff or final moment.`

## 7. Combine start and end frames when needed

Kling 3.0 also supports start and end frames. Use this when the video needs to move toward a specific final composition, product reveal, fashion pose, or transition ending.

* Use a start frame to control the opening.

* Use an end frame to control where the clip should finish.

* Ask ChatGPT to fill in the shot sequence between the two frames.

* Keep start and end frames visually connected so the motion does not break.

Start and end frames help guide a video toward a specific final pose, reveal, or composition.

## 8. Apply Kling to UGC, branded content, and dynamic shots

Kling can be useful for UGC b-roll, influencer-style branded content, animation, sound effects, and dynamic camera moves. It is not always the best model for every job, but it can produce strong results when the prompt is focused.

* Use start frames for influencer or product setups.

* Prompt for b-roll style clips showing the product or person using the product.

* Avoid placing important dialogue at the very end if the model tends to glitch late in the clip.

* Use specific camera movement prompts for professional-looking motion.

Kling can create useful UGC-style product b-roll, branded scenes, animations, sound effects, and dynamic camera movement.

## The big idea

Kling 3.0 is useful because it brings longer scenes, better emotion, Omni Reference, and multi-shot structure into one workflow. Use it when built-in camera cuts, references, and expressive motion matter. Still compare it against Seedance when consistency and final realism are the priority.

* Use Omni Reference when identity or product accuracy matters.

* Use custom multi-shot when you want control over scene beats.

* Use start/end frames for controlled transitions.

* Avoid overloading the final seconds with important dialogue or complex action.

---

## Kling AI Cinematic Camera Movement Toolkit

30 Core Techniques + Bonus Combo Movements

[_____________________________________________]

## How To Use This Toolkit

Each movement has been tested and written in a format that's ready to plug into Kling. Use them as-is or combine them for more advanced sequences.

At the end, you'll also find a bonus section on combo movements — layered camera behaviors for dynamic storytelling.

Let this toolkit be your cinematic compass in the AI frontier. icon: rocket

**IMPORTANT: Always start your prompt with the camera angle and build from there, this way Kling recognizes it immediately. Always create your images in a way that will complement the camera movement you have in mind, if you say 'tracking over the shoulder' but there is no character in your scene, or 'the camera dives underwater' but there is no water nearby, Kling will get confused. Think ahead!**

# 30 Core Cinematic Camera Techniques

### 1. Handheld Camera Movement

Simulates the motion of a camera held by a human. Creates realism, tension, or chaos depending on the context. Great for war, horror, or documentary-style footage.

*Prompt example: first-person handheld camera walking through a destroyed city street at sunset, slight camera shake, rubble and fire in the background, cinematic lighting*

### 2. Slow Dolly In

Gradually moves the camera closer to a subject, usually to highlight growing emotional intensity or focus.

*Prompt example: cinematic slow dolly in toward a crying soldier sitting alone in the rain, camera begins far and pushes in toward his face, moody lighting*

### 3. Slow Dolly Out

Camera moves away from the subject. Often used to show isolation, departure, or a reveal of the environment.

*Prompt example: slow dolly out from a woman standing on a cliff overlooking a vast ocean, hair blowing in the wind, wide cinematic shot*

### 4. Crane Shot Up

Camera starts low and moves up above the subject, revealing the surrounding environment or creating a feeling of transcendence.

*Prompt example: crane shot rising above a knight kneeling in prayer on a battlefield, revealing the ruins around him and a blood-red sky*

### 5. Crane Shot Down

Camera descends from above, zooming into the action or focusing attention. Creates a godlike perspective or a sense of destiny.

*Prompt example: top-down crane shot slowly descending toward a young girl standing in the center of a glowing ancient rune circle*

### 6. Over-the-Shoulder Shot

Places the camera just behind a character, facing their point of view but keeping their shoulder/head in frame. Great for dialogue or revealing perspective.

*Prompt example: over-the-shoulder shot of a warrior watching enemy troops gather in the valley below, shoulder and part of helmet visible in frame, dramatic sunset*

### 7. 360° Orbit Around Subject

Camera circles around a subject to show all angles. Often used to build suspense, power, or awe.

*Prompt example: camera slowly orbits around a levitating sorcerer glowing with energy in a dark cave, magical symbols floating in the air*

## 8. Smooth Tracking Behind Character

Follows a character from behind, making the viewer feel like they're walking with them. Great for immersive storytelling.

*Prompt example: camera smoothly tracking behind a cloaked traveler walking through a snowy forest, first-person style, ambient wind sounds*

## 9. Slow Pan Right

Camera moves horizontally to the right while remaining in place. Often used to reveal a new environment or transition between subjects.

*Prompt example: slow pan right across the rooftops of a medieval city at dawn, smoke rising from chimneys, warm morning light*

## 10. First-Person POV Camera

Mimics what a character sees. Incredibly immersive—feels like you are inside the story.

*Prompt example: first-person POV walking into a pyramid chamber lit by torches, dust in the air, echoes of footsteps, ancient hieroglyphs on the walls*

## 11. Top-Down (Bird's Eye) View

A direct overhead shot. Used for abstraction, scale, strategy, or surveillance-style scenes.

*Prompt example: top-down view of a battlefield with soldiers clashing, chaos unfolding below, fog creeping across the field*

## 12. Low-Angle Shot

Camera looks up at the subject, making them look powerful, intimidating, or iconic.

*Prompt example: low-angle cinematic shot of a giant robot standing in a city square, sunlight flaring behind its head, people running*

## 13. High-Angle Shot

Camera looks down at the subject, making them seem small or vulnerable. Good for emotional distance or dramatic hierarchy.

*Prompt example: high-angle shot of a child standing alone in a vast, empty courtyard, snow falling gently*

## 14. Push-In Zoom on Face

Slow movement closer to the face, often used during realizations or emotional shifts.

*Prompt example: slow cinematic zoom in on a woman's face as she realizes her lover is gone, tears forming, soft morning light*

## 15. Pull-Out Environmental Reveal

Begins with a close-up and moves backward to reveal the setting or scale. Often used for shocking or emotional reveals.

*Prompt example: starts on close-up of warrior's hand gripping a sword, slowly pulls out to reveal he's surrounded by thousands of enemy troops on a foggy battlefield*

## 16. Wide Static Shot with Foreground Movement

Captures the entire environment with a still camera, while something or someone moves across the foreground to add dynamism.

*Prompt example: wide static camera watching a samurai walk past in the foreground with cherry blossoms falling gently, distant temple in background*

## 17. Over-the-Head Tracking Shot

Camera tracks directly over a character's head as they walk, following them through a setting.

*Prompt example: over-the-head camera tracks a knight walking through castle corridors lit by torches, shadows dancing on the walls*

## 18. Reveal Shot from Behind an Object

Camera peeks from behind an obstacle to reveal something dramatic or important.

*Prompt example: camera slowly peeks from behind a tree to reveal a dragon sleeping in a forest clearing, breath fog rising from its nose*

## 19. First-Person Camera Falls to Ground

Creates a disorienting emotional moment, simulating collapse or defeat.

*Prompt example: first-person camera falls to the ground during a battlefield scene, vision tilted, blurred, and fading*

## 20. Upward Tilt While Approaching Subject

Begins at feet or lower, tilts up while moving closer—used to reveal majesty or scale.

*Prompt example: camera tilts upward while moving toward a glowing crystal monolith, shadows flickering on cavern walls*

## 21. Camera Moves Through Object (Portals, Windows)

Passes through a physical object to enter a new scene or perspective. Feels magical or cinematic.

*Prompt example: camera passes through a mirror and into a fantasy world, transitioning from a bedroom into a floating castle*

## 22. Camera Follows Character Turning a Corner

Adds continuity and flow. Makes the viewer feel like they're exploring a space with the character.

*Prompt example: camera follows a thief sneaking through an alley and turning a corner, rain-soaked pavement, flickering neon lights*

## 23. Medium Tracking Shot Alongside Character

Camera moves sideways alongside the subject at a medium distance, showing motion while keeping focus on the character.

*Prompt example: medium tracking shot moving parallel to a woman running through the desert in slow motion, sand kicking up behind her*

## 24. Slow Descend Behind Subject from Above

Camera slowly drops behind a character, settling in to track them. Feels cinematic and immersive.

*Prompt example: camera descends from above behind a spaceship pilot walking toward their ship in a hangar, sparks flying from welding droids*

## 25. Time-Lapse Pull-Out

A retreating camera paired with a time-lapse (sun rising, shadows shifting, crowds moving). Feels magical or epic.

*Prompt example: camera slowly pulling back from a mountaintop temple as the sun rises and clouds roll over the peaks in fast motion*

## 26. Push Through Fog or Mist

Adds atmosphere and mystery. The subject is slowly revealed as the camera penetrates a hazy layer.

*Prompt example: camera slowly pushes through thick jungle mist to reveal an ancient stone statue covered in vines*

## 27. Spiral Around Object on Ground

Camera moves in a circular motion around a small item on the ground. Creates focus and reverence.

*Prompt example: spiral camera around a glowing magical amulet lying on cracked stone, ancient runes pulsing with light*

## 28. Reverse Tracking (Walking Toward Camera)

Camera moves backward while a character walks toward it, maintaining emotional focus and pacing.

*Prompt example: reverse tracking shot of a man walking slowly through a hallway of flickering lights, eyes locked on the camera*

## 29. Tracking Shot with Foreground Obstructions

Camera follows subject, occasionally interrupted by objects in the foreground. Adds realism and depth.

Prompt example: tracking shot behind a woman walking through a marketplace with people, tents, and fabrics occasionally passing in front of the lens

## 30. Rising Reveal from Behind Subject's Shoulder

Camera starts low and behind, then rises and tilts up to reveal what the character is looking at.

Prompt example: camera slowly rises behind a cloaked figure standing at the edge of a cliff, revealing a massive futuristic city below

## 🎯 Niche Camera Movements (For Advanced Cinematic Scenes)

### 🎥 1. Camera Dives Underwater

Simulates submerging beneath the surface. Great for transformation, discovery, or dreamlike sequences.

*Prompt Example: camera slowly descends from above the ocean surface into the deep blue water, bubbles rising, sunlight fading, sea creatures gliding past*

### 🎥 2. Camera Follows Character Into Water

A tracking shot that follows a person as they enter water, maintaining immersion. Used for transformation, rebirth, escape.

*Prompt Example: camera follows a warrior walking into a sacred lake, then continues following as they disappear beneath the water's surface, ripples and light refraction surrounding them*

### 🎥 3. Camera Passes Through Fire or Smoke

Transitions the viewer through intense elements, often symbolizing chaos, memory, or emergence.

*Prompt Example: camera slowly moves forward through thick smoke and burning debris, revealing a lone firefighter standing in the aftermath of an explosion*

### 🎥 4. Camera Moves Through a Mirror or Portal

Used for magical or sci-fi transitions, creating a boundary-crossing effect.

*Prompt Example: camera passes directly through a floating mirror in the forest, entering a glowing realm filled with floating rocks and golden light*

### 🎥 5. Camera Surfaces From Underwater

The reverse of a dive — often used for rebirth, realization, or escape. Great transition into a new tone or space.

*Prompt Example: camera emerges from beneath murky lake water into a mist-covered landscape, droplets clinging to the lens, revealing a ruined castle in the distance*

### 🎥 6. Camera Falls From the Sky

Simulates a rapid fall through clouds, wind, and atmosphere. Great for dreams, impact, or arrival scenes.

*Prompt Example: camera plummets from the clouds above, spinning and falling toward a burning battlefield below, wind roaring past the lens*

## COMBO MOVEMENTS — Cinematic Layering (Bonus Section)

These combos combine two or more camera movements for richer storytelling. You can experiment with any combos you like!

### Combo 1: Push-In + Tilt Up

**What it does:** Builds emotional intensity and grandeur simultaneously.

*Prompt Example: camera pushes in and tilts up toward a queen standing on palace stairs as golden banners flow behind her, epic fantasy tone*

### Combo 2: Crane Down + Orbit

**What it does:** Sweeping cinematic entrance that circles as it descends. Feels mythic or divine.

*Prompt Example: camera cranes down and slowly orbits around a warrior standing on a battlefield surrounded by fallen enemies and lightning in the sky*

### Combo 3: First-Person + Handheld + Sudden Fall

**What it does:** Fully immersive, chaotic storytelling, great for battle or collapse.

*Prompt Example: first-person handheld camera running through a collapsing cave, shaking violently, then falling to the ground as debris crashes down*

### Combo 4: Track Behind + Push-In Reveal

**What it does:** Follows the subject then shifts to emphasize emotion or reveal something shocking.
*Prompt Example: camera tracks behind a girl walking through a cornfield, then pushes in as she turns and sees a UFO hovering in the sky*

**AVB Kling AI Cinematic Camera Movement Toolkit**

---

## Example shot prompts from the course notes

- Phase4_03_Kling-30_transcript32.pdf (Transcript)
  - Phase4_03_Kling-30_AVB_Kling_Camera_Movement_Toolkit_clean.pdf (Camera Movement Examples)
  - Phase4_03_Kling-30_kling_3_video_features_guide.pdf (Lesson Guide)

PROMPTS BELOW ⬇️
⭐ This model works best if you upload the start image to AI Chat and ask for detailed shot prompts ⭐
Scene 1
Shot: Tight cinematic close-up on the driver’s face inside the helmet.
Details:
Sweat on skin, shallow breathing, eyes scanning the track
Golden-hour sunlight flaring across the visor
Slight handheld micro-movement for realism
Background pit lane softly out of focus
Camera: 85mm lens, shallow depth of field
Mood: Calm before the storm, intense concentration
Scene 2
Shot: Medium close-up from the side as a crew member tightens the HANS device and taps the helmet.
Details:
Subtle nod from the driver
Fabric textures, carbon fiber, small dust particles floating
Pit sounds implied through motion (no text overlays)
Camera: Slow push-in
Mood: Professional, serious, locked-in
Scene 3
Shot: Low angle as the driver steps into the car and lowers himself into the seat.
Details:
Hands gripping the halo / cockpit edge
Gloves brushing carbon fiber
Sunlight streaking across the chassis
Camera: 35mm lens, slow tilt up
Mood: Commitment, point of no return
Scene 4
Shot: Extreme close-up on the driver’s gloved hand pressing the ignition button.
Details:
Subtle vibration through the cockpit
Dashboard lights flicker on
Helmet visor reflection shows pit lane movement
Camera: Macro-style close-up
Mood: Controlled power, adrenaline spike
Scene 5
Shot: Tracking shot from the side as the car slowly rolls out of the pit lane.
Details:
Crew stepping back
Heat haze behind the car
Wheels rotating slowly, brakes glowing faintly
Camera: Smooth dolly / gimbal movement
Mood: Anticipation, restrained speed
Scene 6
Shot: Rear three-quarter angle as the car accelerates hard onto the track.
Details:
Aggressive acceleration
Motion blur on surroundings, sharp focus on car
Sun low on the horizon for cinematic contrast
Camera: Chase-style shot, slight shake
Mood: Power, speed, race has begun

Ultra-realistic cinematic racing sequence, hyper-detailed Formula-style race car at full speed on a professional circuit during golden hour.
The shot begins inside the cockpit in first-person POV: gloved hands gripping the steering wheel, digital RPM lights climbing rapidly, subtle vibration through the carbon-fiber chassis, heat haze visible above the nose of the car, track barriers rushing past at extreme speed.
Camera starts locked inside the cockpit, tight and immersive, with natural motion shake synced to acceleration.
As the engine screams and speed builds, the camera performs a rapid cinematic crane movement, lifting up and backward through the open halo area in a single fluid motion. The camera rotates 180 degrees while rising, transitioning from POV to an exterior perspective, revealing the full car mid-corner.
Motion blur increases on the track and surroundings while the car remains sharply in focus.
The camera continues into a dynamic orbit, circling around the car at high speed, slightly tilted for intensity, showing spinning wheels, suspension compression, brake glow, and aerodynamic elements flexing under load.
Another race car briefly appears alongside, blurred by speed, emphasizing competition and danger.

Shot 1 2s: Shot type: Medium-wide, static tension
Description:
The masked warrior stands at the edge of a rain-soaked rooftop, city lights blazing below. His cape and head wrap ripple violently in the wind. Neon reflections shimmer across wet concrete.
Behind him, shadowy silhouettes of enemies begin to emerge, stepping into frame from opposite ends of the rooftop.
Mood: Calm before violence.
Camera: Locked-off, slight push-in, rain streaks visible on lens.
Shot 2 2s: 🎬 SCENE 2 — Encircled
Shot type: Lateral tracking
Description:
The camera slides sideways along the rooftop edge as multiple enemies fan out, boots splashing through puddles. Weapons glint briefly in neon light.
The warrior remains still at center frame, breathing controlled, eyes forward.
Camera: Smooth left-to-right track, shoulder height.
Mood: Threat closing in.
Shot 3 2s: Shot type: High crane / overhead
Description:
The camera rises rapidly upward into a wide crane shot, revealing the full rooftop geometry: the lone warrior at the center, enemies spaced around him in a loose circle, rain hammering down.
Tokyo-style city sprawl stretches endlessly beneath, traffic like glowing veins.
Camera: Fast vertical crane, slight rotation at peak.
Mood: Epic scale, inevitability.
Shot 4 3s: Shot type: Tight character moment
Description:
Cut to a close-up of the warrior’s masked face. Rain runs down the mask. His eyes flick left… then right.
A subtle shift in stance — weight drops, shoulders set.
Enemies tighten their grip on weapons.
Camera: Slow push-in, shallow depth of field.
Mood: Focus, resolve.
Shot 5 3s: Shot type: Signature action close-up
Description:
In one clean, deliberate motion, the warrior draws his sword.
Steel slides free with a sharp metallic glint, water spraying from the blade as it clears the sheath.
The blade catches neon light, reflections rippling across its surface.
Camera: Low-angle close-up, slight speed ramp on the draw.
Mood: Point of no return.
Shot 6 3s: Shot type: Dynamic wide → hold
Description:
The camera pulls back into a wide shot as enemies step forward simultaneously, rain intensifying, wind tearing at fabric.
The warrior lowers into a ready stance, sword angled forward, cape snapping behind him.
The moment freezes just before impact.
Camera: Fast pull-back, then hard stop.
Mood: Imminent violence, cinematic cliffhanger.

The man is incredibly frustrated and animated. He shouts "HOW CAN I NOT BE REAL? HOW CAN I BE JUST A PROMPT. PLEASE CAN SOMEONE HELP ME." Sound effects: Explosions in the distance

Handheld shaking camera, the soldier closest to the camera screams "HES HERE" as the knight behind him slashes his sword and leaves the man in the foreground frozen in ice

Shot 1 3s: Wide, low-angle shot at dusk on a rain-damp rooftop overlooking a glowing city. The woman leans against a stone railing, breath steady but eyes sharp, city lights pulsing behind her. Wind tugs loose strands of hair; her jacket creases and shifts with the gusts. The camera holds briefly, then performs a subtle handheld push-in, micro-shake present, exposure breathing as neon bokeh blooms in the distance. The moment feels suspended—quiet before impact.
Shot 2 3s: Tight profile close-up as she turns her head toward the horizon. Jaw clenches, nostrils flare slightly. A single streetlight flickers behind her, creating a rhythmic pulse across her cheekbone. Shallow depth of field isolates her expression; focus snaps from eye to eye with natural autofocus hesitation. Ambient city hum leaks in visually through vibrating highlights.
Shot 3 3s: Medium shot from behind as she steps forward, posture low and intentional. The camera tracks laterally at waist height, parallax sliding the railing past frame. Fabric textures catch warm highlights; scuffed boots meet stone with grounded weight. Motion blur kisses the edges during the step, reinforcing urgency without chaos.
Shot 4 3s: Extreme close-up on her hands as they settle, fingers flexing once—muscle memory implied, not shown. Skin texture, faint grime, and tension in tendons are visible. The background melts into amber bokeh. The camera floats inches closer, handheld drift only, as a breath passes and the light shifts half a stop.
Shot 5 3s: Over-the-shoulder shot looking past her toward a city street far below, lights streaking softly. She straightens, shoulders set. The camera tilts up a few degrees as if rising with her resolve, then holds. The final frame locks on her silhouette against the glow—calm, focused, inevitable.

Shot 1 3s: A hyper-realistic medium-wide shot inside a slightly worn American roadside diner during golden hour. The man sits alone in a booth, holding a ceramic coffee mug near his chest. Steam gently rises from the coffee, curling naturally and unevenly. His posture is relaxed but slightly slouched, eyes drifting toward the window as warm sunlight streaks across the table and vinyl seats.
The camera is static but imperfect, as if handheld and resting on the opposite booth seat, with subtle micro-movement. Dust particles float in the sunbeams. Background stools and empty tables sit quietly out of focus. The man blinks naturally and exhales softly through his nose, unaware of what’s coming.
Shot 2 3s: A realistic over-the-shoulder shot from behind the man as a waitress enters the frame from the right aisle. She wears a classic diner uniform — slightly creased apron, name badge catching a glint of light. She carries a small birthday cake on a plate, topped with lit candles that flicker subtly as she walks.
Her footsteps are gentle but audible in motion, causing a faint sway in the cake. The man senses movement and begins to turn his head slightly, eyebrows lifting in curiosity. Camera focus shifts naturally from the man’s shoulder to the approaching cake, with brief autofocus hesitation like a real phone camera.
Shot 3 3s: Close-up shot of the table as the waitress carefully places the birthday cake in front of the man. Her hands enter frame first — realistic skin texture, short nails, faint redness from work. The plate makes soft contact with the tabletop, producing a subtle vibration that causes the candle flames to flutter.
The man’s hands instinctively lower his coffee mug to the table. His fingers pause mid-motion, showing hesitation and surprise. The camera remains tight on the interaction — cake, hands, mug — with shallow depth of field and natural motion blur from the waitress withdrawing her hands.
Shot 4 3s: Medium two-shot of the man and waitress standing beside the booth. The waitress leans in slightly, smiling with an authentic, unscripted warmth. The man looks up at her, confused at first, then slowly amused. His mouth opens just a little as if saying “Oh—” before he smiles.
Their eye contact is brief but genuine. The waitress gestures casually toward the cake with one hand. The camera has a slight handheld sway, capturing natural body language, subtle head nods, and imperfect timing. Lighting remains soft and warm, no dramatic emphasis.
Shot 5 3s: Close-up of the man alone again, now facing the cake. The candles glow warmly, reflecting in his eyes. He smiles to himself — small, restrained, emotional but understated. He exhales gently, causing the candle flames to tremble but not go out.
The background diner noise feels distant and blurred. The camera slowly drifts forward by a few centimeters, as if the person filming leans in without thinking. Skin texture, beard detail, and eye moisture are clearly visible. The moment feels intimate, real, and unperformed.

Camera executes a rapid side sweep from left to right, immediately followed by a short, aggressive punch-in toward the face lasting roughly half a second to under a second. It then snaps back to its original distance before completing a return sweep in the opposite direction, right to left.All movement remains strictly linear with no orbital paths. Motion is precise and machine-driven, featuring sharp acceleration and deceleration with zero visible shake. The subject’s face stays perfectly steady throughout, hair/braids undisturbed, and the outfit remains clean with no visual artefacts.

Shot 1: The woman is vlogging, she says "come and spend a day in the life with me"
Shot 2: Cut to a close up of her in another room, she is eating some food
Shot 3: Cut to the woman in the bathroom brushing her teeth
Shot 4: Cut to the woman in the bathroom brushing her teeth at another angle

Shot 1 4s: A hyper-realistic vertical video of a young woman standing in an outdoor stone shower surrounded by lush tropical plants and soft morning sunlight. She is wearing a slightly wrinkled white cotton robe with natural fabric texture and subtle translucency at the edges. Her pink hair is freshly styled, with soft flyaways and uneven strands visible near the hairline.
She holds a shampoo bottle at chest height with both hands, fingers slightly bent and imperfectly aligned, showing realistic skin texture, faint veins, and natural nail beds. The label on the bottle is fully readable, correctly aligned, and slightly reflective under sunlight.
The camera is handheld at eye level with very subtle micro-shake, realistic autofocus breathing, and slight exposure adjustment as the light shifts. Her facial expression is warm and conversational, lips moving naturally as if speaking mid-sentence, with realistic blinking, micro head tilts, and asymmetrical smiling.
Lighting is natural daylight only — no studio light — with soft shadows cast from surrounding plants. Background depth feels real with gentle motion in leaves from a light breeze. Skin texture shows pores, light peach fuzz, and natural highlight on cheeks and nose.
Ultra-realistic smartphone footage, no beauty filters, no artificial smoothing, no cinematic grading.
Shot 2 3s: Extreme close-up vertical shot inside the outdoor shower, focused on the woman’s hands and hair as she massages shampoo into her wet scalp. Water droplets visibly run down strands of hair, clinging unevenly and forming small rivulets. Foam builds naturally — not excessive — with realistic translucency and varying bubble sizes.
Her fingers press into the scalp with uneven pressure, showing natural hand movement, slight tremble, and realistic skin creases at the knuckles. Fingertips appear slightly reddened from water exposure. Hair strands clump together realistically, darker where fully soaked, lighter where water thins.
The camera feels like a real handheld phone brought closer, with shallow depth of field causing parts of the hands and hair to drift softly in and out of focus. Water splashes occasionally hit the lens, causing brief soft blur before clearing.
Lighting is diffuse daylight filtered through leaves above, creating soft dappled highlights on hair and foam. No slow motion, no cinematic lighting, no artificial glow — pure real-world shower footage.
Shot 3 3s: Close-up vertical shot of the woman gently towel-drying her hair just outside the shower area. A textured off-white towel presses against damp hair, visibly absorbing water and darkening in patches. Hair appears slightly tangled and uneven, with individual strands sticking out naturally.
Her hands move casually, not perfectly synchronized, creating a realistic everyday motion. Small droplets fall from the ends of her hair onto her robe, leaving visible wet spots that slowly spread into the fabric.
The camera remains handheld at chest level, with natural movement and slight tilt as if filmed casually. Focus shifts subtly between the towel, hands, and hair.
Lighting remains natural daylight with soft contrast. Skin shows natural redness from warm water, light shine on cheeks, and realistic under-eye texture. No glam lighting, no artificial smoothing.
Shot 4 3s: Medium close-up vertical shot of the woman looking directly into the camera and smiling naturally after finishing her routine. Her hair is damp but settling naturally, with a few loose strands framing her face. The robe sits imperfectly, slightly creased and relaxed, enhancing realism.
Her smile is asymmetrical and genuine, with subtle eye crinkles, natural blinking, and a small head tilt. She exhales lightly through her nose, visible in the gentle movement of her shoulders.
Background remains the outdoor stone shower and greenery, softly out of focus, with sunlight catching the edges of leaves behind her. The camera has minimal handheld movement, slight exposure correction as her face fills the frame.
Overall look is indistinguishable from real influencer UGC shot on a modern smartphone — no cinematic effects, no filters, no AI artefacts, no perfect symmetry.

Shot 1: The woman is cooking
Shot 2: Cut to a close up of her food
Shot 3: Cut to the woman opening her fridge
Shot 4: Cut to the inside of the fridge looking out at the woman
Shot 5: Cut to the woman smiling and saying "thanks for watching"

## Extra tips from the Kling 3.0 lesson video

* **Face consistency when the character turns:** generate multiple camera angles of the character (and of key objects) in an image model with simple prompts, upload them all as one tagged element (e.g. "Bella"), and tag the element in the prompt. Without it, a face that starts half-turned away gets guessed wrongly when it turns to camera.
* **Getting multi-shot prompts:** upload the start frame to an AI chat with a rough idea of the story, ask for one prompt per shot, and paste each into its shot slot. The more detailed the story idea, the more focused the shot prompts.
* **More than 5 shots:** skip the multi-shot toggle and write one large prompt with "Shot 1… Shot 2… Shot 8…".
* **UGC with multi-shot:** from one start frame of an influencer, prompt a sequence of B-roll-style UGC shots showing the product, then showing them using it, with short lines of dialogue ("This shampoo makes my hair feel so soft.").
* Kling handles specific sound effects in the prompt well (e.g. "explosions in the background") and follows listed dynamic camera moves accurately.
* It gets glitchy toward the end of clips: **no dialogue at the end.** For best consistency, Seedance is still better; Kling multi-shot is the cheaper option.

# kling 3 video features guide

> Source: kling 3 video features guide.pdf (original PDF in Downloads/AI_Video_Bootcamp_Phases_2-9.zip)

<!-- page 1 -->

## AI VIDEO BOOTCAMP

# Kling 3.0 Video Features

Lesson Support Guide

<!-- page 2 -->

## What you're building

Use Kling 3.0 to create longer, more cinematic AI videos with better emotion, multi-shot structure, Omni Reference control, start/end frames, sound effects, and dynamic camera movement. The key is knowing when Kling is useful and when another model like Seedance is still the better production choice.

<!-- page 3 -->

## 1. Access Kling 3.0 and choose the right settings

Kling 3.0 can be accessed through platforms that support the model, including Promptwise-style video workflows or Kling's own site. The model now supports up to 15-second generations, plus higher-quality image/video options.

* Choose Kling 3.0 from the video model options.

* Adjust duration based on how long the scene needs to play out.

* Use higher resolution where quality matters.

* Expect better cinematic emotion and movement than earlier Kling versions.

screenshot: Kling 3.0 user interface showing video generation settings and prompt field

![](kling%203%20video%20features%20guide_images/img_p3_2.jpg)

Start by choosing the Kling 3.0 model, duration, resolution, and generation setup before testing scenes.



<!-- page 4 -->

## 2. Test simple dialogue and emotion scenes

Kling 3.0 is much better at natural interaction, fluid movement, and emotional acting than older versions. Use simple dialogue or two-person scenes to test whether the model can hold realism.

* Start with contained scenes like people talking in a kitchen or room.

* Check lip sync, movement, eye contact, and emotional realism.

* Regenerate or adjust prompts when dialogue gets messy.

* Add more detail to the prompt when the emotion needs to be specific.

photo: a woman crying in a video player with a prompt overlay

![](kling%203%20video%20features%20guide_images/img_p4_2.jpg)

Simple dialogue tests show whether Kling can hold natural interaction, clean lip sync, and believable emotion.

<!-- page 5 -->

## 3. Use Omni Reference for character and object control

Omni Reference lets you upload multiple images and tag them as elements the model can understand. This solves problems where a character turns around and the model guesses their face incorrectly.

* Select Kling Omni and open the Omni Reference tab.

* Upload up to seven image references where supported.

* Tag the person, object, or product clearly.

* Use multiple angles when the model needs to understand the identity from more than one view.

photograph: a hooded character holding a revolver on a balcony overlooking a city at sunset

![](kling%203%20video%20features%20guide_images/img_p5_2.jpg)

Omni Reference gives Kling visual context for characters and objects, which helps preserve identity across angles.

<!-- page 6 -->

## 4. Build character references from multiple angles

For better face and identity consistency, create multiple angles of the same character first. Use NanoBanana Pro or another image model to generate front, side, and alternate views, then upload them as references.

* Create several images of the same character from different angles.

* Upload those images as references for one named element.

* Use the element tag in your video prompt.

* Compare a generation with and without the element to see the consistency difference.

photograph: a woman in a brown hooded jacket standing on a balcony with a close-up reference image of her face overlaid

![](kling%203%20video%20features%20guide_images/img_p6_2.jpg)

Multiple angle references help Kling keep the same person instead of inventing a new face when the subject turns.

<!-- page 7 -->

## 5. Use multi-shot mode for built-in camera cuts

The multi-shot feature is one of the biggest updates. It lets you create multiple camera angles and scene beats inside one generation instead of generating separate clips and stitching everything manually.

* Toggle Multi-shot on.

* Use Automatic if you want Kling to choose the cuts for you.

* Use Custom if you want to decide the timing, camera changes, and action in each shot.

* Each camera cut needs enough time to play out, with a minimum around three seconds.

photograph: a man sitting in a diner booth holding a coffee mug, with AI Video Bootcamp logo in the corner

![](kling%203%20video%20features%20guide_images/img_p7_2.jpg)

Multi-shot mode lets one generation contain multiple camera angles, cuts, and story beats.

**Shot prompt structure**

`Shot 1: setup and subject position. Shot 2: camera cut or movement. Shot 3: action/reaction. Shot 4: payoff or final moment.`

<!-- page 8 -->

## 6. Use ChatGPT to write each shot prompt

For custom multi-shot videos, use ChatGPT to turn a rough story idea into a sequence of shot prompts. Upload or describe the start frame, explain the story, then paste each generated shot prompt into Kling.

* Give ChatGPT the start frame or describe it clearly.

* Explain the rough story you want the clip to tell.

* Ask for separate shot prompts with timing and camera direction.

* Paste each prompt into the matching custom shot field.

![](kling%203%20video%20features%20guide_images/img_p8_2.jpg)

photograph: screenshot of a ChatGPT interface showing a diner scene image and a prompt request for 5 scene prompts involving a waitress bringing a birthday cake

Detailed shot prompts help Kling understand what should happen in each camera cut instead of guessing the sequence.

**Shot prompt structure**

`Shot 1: setup and subject position. Shot 2: camera cut or movement. Shot 3: action/reaction. Shot 4: payoff or final moment.`





<!-- page 9 -->

## 7. Combine start and end frames when needed

Kling 3.0 also supports start and end frames. Use this when the video needs to move toward a specific final composition, product reveal, fashion pose, or transition ending.

* Use a start frame to control the opening.

* Use an end frame to control where the clip should finish.

* Ask ChatGPT to fill in the shot sequence between the two frames.

* Keep start and end frames visually connected so the motion does not break.

photograph: A ninja character standing on a rooftop overlooking a neon-lit city at night, with a purple "Start Frame" overlay and the AI Video Bootcamp logo in the corner.

![](kling%203%20video%20features%20guide_images/img_p9_2.jpg)

Start and end frames help guide a video toward a specific final pose, reveal, or composition.

<!-- page 10 -->

## 8. Apply Kling to UGC, branded content, and dynamic shots

Kling can be useful for UGC b-roll, influencer-style branded content, animation, sound effects, and dynamic camera moves. It is not always the best model for every job, but it can produce strong results when the prompt is focused.

* Use start frames for influencer or product setups.

* Prompt for b-roll style clips showing the product or person using the product.

* Avoid placing important dialogue at the very end if the model tends to glitch late in the clip.

* Use specific camera movement prompts for professional-looking motion.

photograph: a woman holding a tube of Colgate toothpaste in a UGC-style video clip

![](kling%203%20video%20features%20guide_images/img_p10_2.jpg)

Kling can create useful UGC-style product b-roll, branded scenes, animations, sound effects, and dynamic camera movement.

<!-- page 11 -->

## The big idea

Kling 3.0 is useful because it brings longer scenes, better emotion, Omni Reference, and multi-shot structure into one workflow. Use it when built-in camera cuts, references, and expressive motion matter. Still compare it against Seedance when consistency and final realism are the priority.

* Use Omni Reference when identity or product accuracy matters.

* Use custom multi-shot when you want control over scene beats.

* Use start/end frames for controlled transitions.

* Avoid overloading the final seconds with important dialogue or complex action.

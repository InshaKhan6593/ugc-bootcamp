---
name: ai-creator-workflow
description: >-
  The six-step production process behind every piece of AI content - idea, chat, image, refine, video,
  edit and post - plus node/flow pipelines, batching, model choice per stage and the quality gates
  that stop wasted credits. Use when the user asks "where do I start", "what is the workflow", "how do
  I make this video", "plan my content", "batch a week of posts", "build a flow", "which model should
  I use for this step", "I am generating loads of stuff and none of it looks good", or hands over a
  vague idea with no clear output. Also use to route a bigger job to the right specialist skill (ai-
  image-prompting, ai-cinematography, ai-video-prompting, ai-avatar-builder, ai-filmmaking, ugc-ad-
  creator, ai-clone-yourself, viral-short-form).
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 2 (foundations, workflow, prompting) and Phase 6 (flows)
---

# AI Creator Workflow

Most people treat AI creation as: type a prompt, get a result, post it. That is step three of six. The people who consistently produce strong work are not better at the tools - they know what they are making before they open a generator, they develop the idea in chat before spending credits, they lock the image before paying for video, and they refine before they animate.

**Idea - Chat - Image - Refine - Video - Edit and post.**

The scale changes between one still and a short film. The order does not.

## Critical rules

1. **Define the outcome before generating.** "Something cool" is not an idea. "A 15-second 9:16 cinematic TikTok of a samurai in heavy rain for my fantasy page" is. Knowing the platform gives you the aspect ratio, the mood and half the prompt for free.
2. **Start with images, even when the output is video.** Images are cheap, fast and controllable. Lock composition, character, light and feel as a still, then animate. Trying to fix a wrong character or wrong framing inside a video model is the expensive way to work.
3. **Refine only what is nearly right.** If the composition, character, concept or angle is wrong, go back and rewrite the prompt - do not polish a bad foundation. Editing is for a shot that is 90% there.
4. **Upscale before you animate.** More pixels going in means a clearly better clip coming out.
5. **Cheap model to find the idea, best model for the hero.** Test hooks and directions on fast or cheap models, then regenerate the winner on the strongest model you can afford.
6. **Do not re-describe the image in the video prompt.** The model can see the start frame. Describe what moves.
7. **One decision, reused forever.** A persona, a look block, a voice blueprint, a working flow - define it once, then every future piece starts from it instead of from zero. This is the whole difference between making content and running a content system.
8. **Not everything needs to become video.** If the final asset is a still, stop at step four.

## The six steps

### 1. Idea - define the outcome
Answer five questions. If you cannot, you are not ready to generate:

- What am I making?
- Where is it going (platform, aspect ratio, duration)?
- Who is it for?
- What should it make them feel?
- What does the final asset need to be - still, clip, ad, thumbnail, film, client deliverable?

### 2. Chat - plan, write, strengthen
Use an AI chat as a creative director, not a writer. Develop the concept, write the script or shot list, build the prompts, then push back on the first answer: ask what is weak, what will make this look fake, what is missing. Strengthen a weak idea here, where it costs nothing.

This is also where the specialist skills come in. Route by job:

| The job | Skill |
|---|---|
| Write or fix a still-image prompt | `ai-image-prompting` |
| Light, frame, lens, grade or move a shot | `ai-cinematography` |
| Animate an image, write motion or dialogue prompts | `ai-video-prompting` |
| A recurring person - influencer, UGC creator, brand face | `ai-avatar-builder` |
| A short film: cast, locations, props, shot-by-shot | `ai-filmmaking` |
| An ad: strategy, hooks, script, production blueprint | `ugc-ad-creator` |
| A digital twin of the user, talking-head at scale | `ai-clone-yourself` |
| Hooks, retention, posting, growth, viral niches | `viral-short-form` |

### 3. Image - generate the foundation
Pick the model for the job, set the aspect ratio for the platform, and generate several options rather than one. Then run the quality gate (below) before going further.

### 4. Refine - edit and upscale
Fix specific, local problems with an editing model: background, light, hands, outfit, a label that is not crisp, skin that is too smooth. Then upscale - 2x takes 1K to 2K, 4x takes 1K to 4K - especially for hero images, client work and anything about to be animated.

### 5. Video - add motion
Take the refined still as the start frame and prompt only what moves: subject action, camera movement, environmental motion, light changes. One main subject action and one main camera move per clip; crowded prompts morph.

### 6. Edit and post - finish and ship
Assemble in an editor. The first second decides whether anyone sees the rest. Add captions if they help the viewer follow, build ambient sound (footsteps, rain, room tone, fabric, traffic), cut pacing to the energy, and run the realism pass on AI footage - lower contrast noticeably, drop saturation slightly, lift highlights a touch, add a shake so subtle the viewer cannot notice it. Export to the platform's preferred spec rather than the highest number available; `viral-short-form` covers upload settings and posting.

## Quality gates
Check these before spending the next stage's credits. They are cheap; regeneration is not.

**After the image:**
- Is it consistent with the other shots in this piece - same person, same world, same light direction?
- Does the light match the mood, and could it exist in that place?
- Does the person, product or character look believable - skin texture, real imperfection, no plastic gloss?
- Is the aspect ratio right for where this is going?
- Is the product label correct, legible and undistorted?

**After the video:**
- Did the identity hold for the whole clip, including the last second?
- Did the camera do what was asked, or drift?
- Is anything warped, duplicated or rubbery?
- Does the speech sound like a person talking, not a script being read?

**Before posting:** does the first second earn the second one?

A failed gate sends you back one step, not forward.

## Flows: building the pipeline instead of the piece
A flow is a canvas of nodes - each node does one job - wired together so one node's output feeds the next automatically. An image node connected to a video node means the generated image becomes the start frame with nothing downloaded, re-uploaded or lost. Once a flow works, it stops being a project and becomes a template: you start future work from a machine instead of from an empty box.

The nodes worth understanding, and what they are actually for:

| Node | Use it to |
|---|---|
| Image / video / audio generation | The three engines; audio covers SFX, ambience, music and character voices |
| Prompt | One text box feeding several generators - the single source of truth when testing one concept across models |
| Storyboard | Feed it a finished image and it returns continuation shots that keep the subject and style - the fix for "I have one good image and no idea what the next five shots are". Attach two references (avatar + product) and it builds shots using both |
| Angles | More framings of the same subject, as opposed to storyboard's new story beats |
| Upscale | Raise resolution before a hero use or before animating |
| Remove background | Cutouts for thumbnails, product shots, stickers, compositing |
| Gallery | Collect and compare outputs, keep the canvas readable, and act as a reference bank - connect a gallery to a video node to pick start and end frames, or animate the whole gallery at once |

Two ways to run: single node while testing a step, or run-the-flow, which resolves dependencies in order and will not generate a video before the image it needs exists. Test one node before committing a chain - that is what keeps credit spend sane.

A worked pipeline, concept to finished ad: references in (avatar + product) with a brief - generate a batch of images - run angles on the best product frame and storyboard on the best character frame - send both into galleries - animate all - generate music on an audio node - download and assemble with transitions, pacing and sound. The creative work is the brief and the edit; the middle is machinery.

## Batching: one decision, many posts
Batch by locking everything that repeats and varying one thing at a time:

1. Lock the persona or cast (passports), the look block and the voice blueprint.
2. Plan the week as a grid - post type by angle - rather than inventing each post on the day.
3. Generate all stills for the batch in one sitting, at one aspect ratio, from the same locked blocks.
4. Gate the batch, keep the winners, upscale them.
5. Animate the keepers in a second pass.
6. Edit in a third pass, reusing the same template, captions style and sound bed.

Working in passes beats working piece by piece, because you stay in one mode and the outputs stay consistent with each other.

## Choosing the model for each stage
Ask "what am I trying to make", not "which is best". Current guidance, which dates fast:

- **Images:** a strong general image model for scenes and characters; an editing-capable model for local fixes and reference-faithful product work.
- **Avatars and talking shots:** the strongest lip-sync model you can afford for the hero cut; a cheaper one to test hooks.
- **B-roll and slower cinematic shots:** a model known for camera control and clean motion; use its motion-control feature when the movement must follow a specific path.
- **Clones and talking-head at volume:** a dedicated clone platform - see `ai-clone-yourself`.
- **Sound:** a voice and SFX tool for ambience and effects; generate music on an audio node or library track.

Per-model notes, with the caveat that they go stale, are in `ai-video-prompting/references/model-choice.md` and `ai-image-prompting/references/models-and-settings.md`.

## Output format
When the user brings a project, return:

1. **Outcome** - one line: what is being made, for where, at what ratio and length.
2. **Plan** - the six steps as they apply to this specific job, with what to lock once (persona, look block, voice).
3. **The next action** - the one prompt or asset to make right now, written out in full, not described.
4. **Gates** - what to check before moving to the following step.
5. **Which skill handles the next stage**, if it is not this one.

Keep the user generating, not reading. One concrete artefact beats a complete plan.

## Troubleshooting

| Problem | Likely cause | Fix |
|---|---|---|
| Generating a lot, keeping nothing | No outcome defined | Go back to step one and answer the five questions |
| Burning credits on video | Skipped the image stage | Lock the still first; animate only gated images |
| Clips do not cut together | No shared look block or anchored light | Define one look block, repeat it verbatim across shots |
| Character drifts across a batch | No passport | Build a character sheet in `ai-avatar-builder`, reference it every time |
| Final video looks cheap | Edit treated as an afterthought | Pacing, sound design, captions and the realism pass are half the result |
| Flow produces junk at scale | Never tested one node | Test a single node, fix the prompt, then run the chain |
| Overwhelmed by tools | Chasing tools instead of process | The process is the skill; any competent model in each slot will do |

## Reference files (open only when needed)
- `references/six-step-workflow.md` - the full workflow with worked examples per content type
- `references/chat-prompts.md` - how to brief an AI chat: roles, idea development, rewrite and critique prompts
- `references/flows-and-nodes.md` - node-by-node guide, canvas practice, worked pipelines
- `references/batching.md` - batch planning grids, passes, and what to lock
- `references/model-map.md` - which model for which stage, with ageing caveats

Course material names particular apps and models. Apply the principles in whatever tool the user has; do not push them toward a platform.

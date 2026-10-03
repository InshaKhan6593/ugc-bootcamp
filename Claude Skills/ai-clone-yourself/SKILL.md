---
name: ai-clone-yourself
description: >-
  Builds and runs an AI clone of a real person - face clone, voice clone, talking-head video at scale
  - so content ships without filming. Covers the capture recording that trains a good clone, voice
  cloning and script delivery, writing clone-optimised scripts that lip-sync naturally, the B-roll
  editing method that makes clone footage believable, turning one clone into many content jobs, and
  packaging clone work as an offer. Use when the user says "clone myself", "AI clone", "digital twin",
  "HeyGen", "clone my voice", "talking head without filming", "my clone looks robotic", "scripts for
  my clone", "one recording into many videos", "clone content for a client", or "sell cloning to
  founders". Do NOT use for fictional AI personas (use ai-avatar-builder) or ad strategy and scripts
  (use ugc-ad-creator).
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 9 (cloning yourself) and Phase 4 (voices, lip-sync, realism pass)
---

# AI Clone Yourself

Up to this point the bottleneck is you. Ideas depend on your time, your energy, your presence on camera. A clone changes the economics: one good recording becomes an asset that delivers scripts indefinitely, so output stops scaling with hours and starts scaling with decisions.

What this is not: a shortcut past having something to say. A clone delivers; it does not think. The quality of clone content is set entirely by the scripts you feed it, which is why half of this skill is about writing.

## Ground rules

Clone a real person only with that person's clear permission - yourself, a client who has signed off, a founder who commissioned it. No cloning public figures, no cloning someone from footage they did not supply for this purpose, and no putting words in a real person's mouth that they have not approved. When a platform asks whether content is AI-generated, say yes; the labelling cost is trivial next to the account risk, and the course's own guidance is to tick the box.

## Critical rules

1. **Capture quality caps everything.** A clone trained on soft, badly lit, oddly framed footage cannot be fixed later with prompts. Spend the effort here once.
2. **Go light on gestures during capture.** Some movement is good. A strong or repeated gesture gets learned and then repeated far too often in every output, which is the fastest way to look fake.
3. **Write for the ear, not the page.** If a line would not sound normal said out loud, it will not lip-sync well. Read every script aloud before it goes near the clone.
4. **Never leave a clone talking uncut for a minute.** Clone footage works mixed with B-roll - cut away over the weak moments, keep the audio running. This is also just better editing for retention.
5. **Fix locally, not globally.** If one part of a generation looks wrong, do not regenerate the whole video. Cover that beat with B-roll and move on.
6. **One idea, many variations.** The point of a clone is that a script change costs nothing: new hook, new pacing, new CTA, same everything else.
7. **Position the offer as time, not technology.** Nobody buys "AI videos". They buy speed, consistency, authority and presence without time cost.

## Workflow

### Step 1: Decide what the clone is for
The use case sets the capture. A talking-head short-form clone needs a different framing and energy from a corporate explainer presenter or an ad spokesperson. Decide: platform, typical length, tone, framing (close talking-head, mid-shot, seated), and whether it will be cut with B-roll (almost always yes).

### Step 2: Record the capture
The recording that trains the clone is the whole foundation. Full checklist in `references/clone-capture.md`; the essentials:

- Even, soft, front-biased light. No hard shadow crossing the face, no backlight, no colour cast.
- Camera at eye level, stable, framed as the finished content will be framed.
- Plain, non-distracting background that suits every future video.
- Natural speaking energy at the pace you actually want in output - the clone inherits your rhythm.
- Small, varied movement. Avoid any gesture you repeat.
- Follow the platform's own capture instructions and watch its explainer video before recording; each one has quirks worth knowing.

### Step 3: Clone the voice
Record clean voice samples in a quiet room, at consistent distance, in the register you will actually use. Then lock a **delivery description** and reuse it unchanged, the same way a video voice blueprint works - accent, pace, warmth, texture. Punctuation is your pacing tool: ellipses and commas tell the engine to breathe, and unpunctuated text gets read like a label. Detail in `references/voice-clone.md`.

### Step 4: Write clone-optimised scripts
This is where clone content is won or lost. Treat the chat model as a creative director, give it your persona and audience, and have it write for speech.

- Lock a master system prompt describing who the clone is, how they speak, who the audience is, and what is being sold. Reuse it for every script.
- Ask for **angles**, not ideas: controversial, insightful, pattern-interrupting in the first three seconds.
- Multiply one working idea into five tones - curious and subtle, confident and bold, slightly controversial, educational but casual, direct and blunt.
- Keep scripts under about 30 seconds of speech for short form, written in short sentences with real contractions and deliberate pauses.
- Hooks carry everything: ten options per script, two seconds each, natural and slightly unexpected.

Templates and the batching prompts are in `references/clone-scripts.md`.

### Step 5: Generate and edit
Generate the talking footage, then edit it into something a person would watch:

- Cut to B-roll over any weak beat, and regularly regardless - a clone talking straight to camera for a minute looks unnatural however good the sync is.
- If the delivery feels slow or stilted, speed the clip to about 1.1-1.2x. This single adjustment fixes most of the "robotic" complaints.
- Hooks can be re-generated alone: rewrite the first two seconds and replace them without touching the rest.
- Run the realism pass on the footage - lower contrast, slightly lower saturation, lift highlights, add a shake too subtle to notice.
- Build the sound: room tone, B-roll audio, music under. Dead-silent clone audio over silent B-roll sounds synthetic.

Full method in `references/editing-and-broll.md`.

### Step 6: Deploy one clone across many jobs
A clone is a reusable asset, not a video. The jobs it covers, and the time-savers that most people miss, are in `references/deployment-and-offers.md`:

talking-head short-form, ad variations without reshooting, course lessons that can be corrected without re-recording, podcast clips from text, brand intros and outros, A/B tests of tone and pacing, FAQ and objection libraries, funnel videos, localisation into other languages, internal and training video.

### Step 7: Package it as an offer, if selling
Clone work sells on outcome. Paths, positioning and the pitch that lands with founders are in `references/deployment-and-offers.md`. The core line: you are not selling avatars or AI videos, you are selling speed, consistency, authority, scale and presence without time cost - which is why the price is not tied to the production effort.

## Output format
Depending on what the user needs:

- **Setting up:** a capture checklist tailored to their use case, then the voice-sample plan.
- **Scripts:** the master system prompt, then the requested scripts with hook options, written for speech, with pause marks.
- **A content batch:** a grid of day, topic, hook, 20-30 second script, tone - plus which B-roll each needs.
- **An offer:** the positioning line, what is included, and the pitch opening.

Always flag what needs their real input - claims, proof, product details - rather than inventing it.

## Troubleshooting

| Problem | Cause | Fix |
|---|---|---|
| Clone looks robotic | Script written for the page | Rewrite for the ear: short sentences, contractions, punctuation for pauses |
| Speech too slow or flat | Capture pace, or engine default | Speed the clip 1.1-1.2x in the edit |
| The same gesture over and over | A strong gesture was learned from capture | Re-record capture with smaller, varied movement |
| One bad second ruins a take | Trying to fix it with regeneration | Cut to B-roll over that beat, keep the audio |
| Looks fake over a long take | No cutaways | Never run more than a few seconds of uncut clone; mix B-roll throughout |
| Lip-sync mushy on some lines | Words that are awkward to say | Read aloud; replace anything that trips the tongue |
| Voice differs between videos | Delivery description reworded | Paste the identical description every time |
| Footage looks too clean | No realism pass | Lower contrast, slight desaturation, highlight lift, imperceptible shake |
| Content stopped performing | Script quality, not the clone | The clone is fine; test new angles and hooks |
| Scripts take hours | Writing each one from scratch | Lock the master system prompt and batch a week in one pass |

## Reference files (open only the one you need)
- `references/clone-capture.md` - the capture recording: light, framing, audio, movement, what to avoid, re-record triggers
- `references/voice-clone.md` - voice sample capture, delivery descriptions, punctuation for pacing, multilingual notes
- `references/clone-scripts.md` - master system prompt, angle prompts, the five-tone multiplier, hook prompts, weekly batch prompt, humanising passes
- `references/editing-and-broll.md` - the B-roll method, speed fix, hook swapping, sound, realism pass, retention editing
- `references/deployment-and-offers.md` - one clone many jobs, advanced time-savers, monetisation paths, positioning and pitching

Related: `ai-video-prompting` for voice blueprints and the realism pass; `ugc-ad-creator` for ad strategy behind clone ads; `viral-short-form` for hooks, retention and posting; `ai-creator-workflow/references/batching.md` for running it as a system.

Course material names particular platforms. Apply the principles in whatever tool the user has.

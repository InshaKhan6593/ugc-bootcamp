---
name: ugc-ad-creator
description: >-
  Plans and writes short-form video ads - UGC creator ads, talking-avatar ads, podcast-style, 2D
  animation, claymation and demo ads - from a product brief. Places the audience on an awareness
  level, picks one of 16 proven script frameworks, writes 5 hooks, a timestamped script, and a shot-
  by-shot production blueprint with character, location and shot prompts. Use when the user says
  "write an ad", "UGC script", "TikTok ad", "Meta ad", "hooks for my product", "ad concept", "ad
  variations to test", "my ads are not converting", or "turn this product into a video". Do NOT use
  for organic growth and posting strategy (use viral-short-form), standalone image prompts (use ai-
  image-prompting), avatar creation alone (use ai-avatar-builder) or narrative films (use ai-
  filmmaking).
metadata:
  author: insha
  version: 2.0.0
  source: AI Video Bootcamp - Phase 5 (advertising, UGC, ad formats) and Phase 7 (hooks)
---

# UGC Ad Creator

Most ads fail before a word is written, because the wrong message goes to the wrong person at the wrong moment. Decide who this is for and what it has to do first; the script is downstream of that decision.

The second thing that kills ads is polish. On TikTok and Reels, native beats produced - phone-shot, imperfect framing, a real room, casual delivery. An ad that announces itself as an ad gets scrolled.

## Critical rules

1. **Never invent proof.** No fabricated numbers, reviews, results, medical or financial claims. Use only what the user supplies; otherwise write placeholders like [REVIEW COUNT] and tell them what needs filling. A made-up statistic is a liability for their brand, not a creative flourish.
2. **Match the ad to the awareness level.** A hard-sell conversion script aimed at a cold audience wastes the spend.
3. **Choose the framework that gives the strongest reason to keep watching and to act** - not the one that sounds most interesting to write.
4. **Sound human.** Contractions, natural rhythm, specific details. Avoid "game changer", "you need this", "trust me", corporate register, and walls of choppy three-word lines.
5. **Show the product accurately** - real shape, colour, packaging and label - being used the way it is actually used.
6. **Change one variable per variation.** Three changes at once teaches you nothing about which one worked.
7. **The first three seconds carry the whole spend.** If the hook does not earn second four, nothing after it matters.

## Workflow

### Step 1: Brief intake
Collect, or assume sensibly and state the assumption:

product and what it does, target audience and their actual pains, desired outcome, proof available, mechanism (why it works), offer and CTA, platform, length (15/30/45/60s), tone, and format (UGC selfie, talking avatar, podcast, 2D animation, claymation, demo).

### Step 2: Strategy
Place the audience on the five awareness levels and pick the objective. Full detail in `references/ad-strategy.md`.

| Audience | Objective | Frameworks that fit |
|---|---|---|
| Unaware / problem-aware (cold) | Awareness | Spark, Myth Killer, Raw Take, Educator, Pressure Cooker, Cliffhanger |
| Problem / solution / product-aware | Conversion | Countdown, Shortcut, Witness, Demo Drop, Time Machine, Face-Off, Bridge |
| Product-aware / most aware (warm) | Retargeting | Conviction, Origin Story, Witness, Grit Ad |

Grit Ad also works as a lo-fi filter over any other framework. Add one psychology angle from `references/psychology.md` - mass desire, market sophistication, beliefs, gradualization, intensification, identification, redefinition, mechanization, concentration, camouflage.

### Step 3: Framework
State the selling angle in one sentence. Pick a **primary framework** and say why, plus a **backup** for the second variation. Open the matching file in `references/frameworks/` (`01-spark-method.md` through `16-educator.md`, plus `extras.md` for static-ad frameworks and combinations) for its steps, template, example script and hook bank.

### Step 4: Hooks
Write **five hooks** - specific, scroll-stopping, native to the platform. Mix types: curiosity, contrarian, shock, value, story, reaction. Mark the strongest and say why it wins. The library is in `references/hooks.md`.

### Step 5: Script with timestamps
Default 30-45s structure, compressed for 15s:

- **0-3s** hook
- **3-10s** problem, tension or curiosity
- **10-25s** product, method, story or mechanism
- **25-40s** proof, demo or transformation
- **final seconds** one clear CTA that feels like the obvious next step

Budget around 2.5 spoken words per second. For UGC formats, adapt one of the ten templates in `references/ugc-script-templates.md`.

### Step 6: Production blueprint
A shot-by-shot table:

| Shot | Time | What we see | Dialogue / VO | On-screen text | Camera | Notes (props, B-roll, product moment) |
|---|---|---|---|---|---|---|

Then, for AI generation:

- **Characters.** A character-passport prompt per person, identity and wardrobe locked - see `ai-avatar-builder`.
- **Look block.** One visual-DNA paragraph (film stock or phone look, time of day, light direction, grade) pasted word for word into every location and shot prompt.
- **Shot prompts.** Tagged references (@image1 = character, @image2 = product, @image3 = location), timed beats, one action and one camera move per shot.

**Per-shot check** - every shot prompt should answer these before it is final:

1. **Mode** - UGC/phone or cinematic B-roll. One mode per shot, vocabularies never mixed.
2. **Six parts** - subject, environment, camera, lighting, mood, style all present.
3. **Camera** - where it stands (including where the phone physically is), shot size chosen for what the viewer must read, lens.
4. **Depth** - foreground / midground / background named. UGC layers: hand or product near the lens, face, lived-in room.
5. **Light logic** - a named real source, its side, hard or soft, warm or cool, matching catchlight - and the same logic across every shot in that location.
6. **Product** - label text written out, product closer to the lens and flat to camera when it is the hero, scale given.
7. **9:16 safe area** - face and product in the middle band, clear of captions and side buttons.
8. **Shot-size contrast** - alternate talking-head medium close-up, product detail, and a wider context shot. Seven identical mediums is why an ad feels flat.

Blocks 1-8 are `ai-cinematography`'s job; ask it for the lines rather than writing them loosely here. Full production method in `references/production-plan.md`.

**Format specifics:**
- `references/formats/ugc-selfie-ad.md` - phone-held selfie, hard jump cuts, handheld micro-jitter, ambient sound only
- `references/formats/podcast-ad.md` - host and guest, the guest carries the insight, reaction shots, studio mics
- `references/formats/2d-animation-ad.md` - master prompt and worked production
- `references/formats/claymation-ad.md` - master prompt and worked production

### Step 7: Native check and variations
Read it back and ask: does this open like a real post or like an ad? Does the product appear naturally, and early enough? Is there anything a commenter would call fake?

Then offer **two or three test variations**, each changing exactly one variable - hook, framework, or format. Testing is the strategy; the first script is a hypothesis.

## Output format
1. **Strategy** - awareness level, objective, angle, framework and backup, with reasons
2. **5 hooks**, winner marked
3. **Script**, timestamped
4. **Production blueprint** - shot table, and prompts if the user is generating
5. **Variations to test**, one variable each

## Troubleshooting

| Problem | Fix |
|---|---|
| Sounds like an ad | Switch to Raw Take or apply the Grit Ad filter; open on a relatable moment and bring the product in later |
| Hook is generic | Make it concrete: a number, a named group, a surprising claim, a visible moment |
| Script too long for the length | About 2.5 words per second; one idea per beat; cut adjectives before cutting beats |
| No proof available | Use Demo Drop, Educator or Shortcut, where the demonstration *is* the proof |
| Shots inconsistent across the ad | Character passports, one look block repeated verbatim, tagged references in every shot |
| Looks too polished to be UGC | Strip cinema-camera and bokeh words, name the room's real light, add phone realism cues, then run the video realism pass |
| Product label warped | Label-lock template plus a clean product reference with size comparison |
| Shots feel flat | Add a foreground layer (hand, product, counter edge) and make the background darker than the subject |
| Ads fatigued after a week | Same script, new hooks and pacing - the hook fatigues first, not the offer |

## Reference files (open only the one you need)
- `references/ad-strategy.md` - awareness levels, objectives, funnel position, testing discipline
- `references/psychology.md` - ten persuasion principles with examples
- `references/frameworks/01-…16-*.md` - one file per framework: template, example, hook bank; `extras.md` for static ads and combinations
- `references/hooks.md` - hook library plus platform-native do's and don'ts
- `references/ugc-script-templates.md` - ten UGC script templates
- `references/formats/*.md` - UGC selfie, podcast, 2D animation, claymation
- `references/production-plan.md` - character passports, visual DNA, location plates, tagged-reference shot prompts

Related: `ai-avatar-builder` for the creator or spokesperson; `ai-cinematography` for every camera and light line; `ai-video-prompting` for motion and dialogue; `viral-short-form` for organic posting; `ai-clone-yourself` for ads fronted by the user's own clone.

Course material names particular apps and models. Apply the principles in whatever tool the user has.

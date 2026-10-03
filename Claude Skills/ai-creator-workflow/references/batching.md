# Batching: deciding once, publishing many times

Volume does not come from working faster on each piece. It comes from locking everything that repeats, then varying one thing at a time. The creator who posts daily without burning out is not more productive per video - they made their decisions once.

## What to lock before a batch

| Asset | What it is | Where it comes from |
|---|---|---|
| Persona / cast | Who appears, and their locked identity and wardrobe | `ai-avatar-builder` character passport |
| Look block | Stock or phone look, hour, sun direction, grade, grain, the "no" list - pasted verbatim into every prompt | `ai-cinematography` step 7 |
| Lighting block | Per location: source, direction, quality, colour | `ai-cinematography/references/lighting.md` |
| Voice blueprint | Accent, tone, pace, texture, in one unchanged sentence | `ai-video-prompting/references/voice-and-sound.md` |
| Product plate | Clean product reference plus the label text written out | `ai-avatar-builder/references/product-in-hand.md` |
| Edit template | Caption style, transitions, sound bed, intro/outro | Your editor's project template |
| Aspect ratio | One per batch | The destination platform |

Changing any of these mid-batch is what makes a set of posts look like a set of unrelated posts.

## Plan the batch as a grid, not a list

Pick the axis that varies and hold everything else still. Useful axes:

- **Post type** - lifestyle, product, educational, reaction, behind-the-scenes, mirror selfie, night out
- **Angle on one idea** - curious, confident, slightly controversial, educational, blunt
- **Hook style** - question, claim, number, visual gag, cold open
- **Shot size** - so the feed does not become seven identical medium shots

A week for a persona might be seven rows: day, topic, hook, 20-30 second script, tone, shot type. One prompt in a chat produces that grid; your judgement picks which rows survive.

## Work in passes, not pieces

Piece-by-piece work means switching modes constantly - writing, then generating, then editing, then back. Batch by stage instead:

1. **Write pass.** All scripts, hooks and prompts for the batch, from the locked blocks.
2. **Image pass.** Every still for every post, one sitting, one ratio, same blocks.
3. **Gate pass.** Run the image gate on all of them. Keep the winners, bin the rest without sentiment.
4. **Upscale pass.** Only on the keepers.
5. **Animate pass.** Every clip, with the same movement vocabulary.
6. **Edit pass.** Same template, same captions, same sound bed, varying only the content.
7. **Schedule pass.** Fill the posting slots; keep one or two spare pieces for a low-energy day.

Staying in one mode is faster and the outputs stay consistent with each other, because they were made under the same decisions in the same hour.

## Variations: twelve posts from one idea

Once an idea works, multiply it along independent axes rather than inventing new ideas:

- 3 hook styles
- 2 pacing styles
- 2 emotional tones
- 2 CTAs

That is twelve pieces from one concept with no new creative decisions. For ads, this is also the testing discipline: change one variable per variation so the result tells you something. Changing three at once tells you nothing.

## Double down on what works

Batching is only half the system; the other half is reading the results. When one piece outperforms, do not move on to the next idea - make more of that one, immediately, while the momentum is live. Posting frequently while something is working carries viewers from the hit to the newer piece. Details in `viral-short-form`.

## Keeping the library

- Keep locked references together in one place (a gallery node, a folder, a passport set). Regenerating a passport by accident restarts your consistency from zero.
- Keep a bank of winning prompts, not just winning outputs. The prompt is the reusable asset.
- Keep the rejects for a while. A frame that failed one gate sometimes passes for a different post.
- Note the settings that produced a keeper - model, ratio, seed if available, reference order. "I cannot remember how I made that" is the most expensive sentence in AI content.

## Scaling without degrading

Three failure modes to watch for as volume rises:

1. **Drift.** The persona slowly changes. Fix: re-reference the original passport, not the most recent output.
2. **Sameness.** Every post is the same shot size, same light, same energy. Fix: vary one deliberate axis per batch; the locked blocks are for identity and look, not for framing.
3. **Slop.** Volume without gates. Fix: the gate pass is not optional - a smaller batch that all passes beats a large batch where half is unusable and the feed shows it.

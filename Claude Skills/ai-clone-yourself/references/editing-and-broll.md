# Editing clone footage: the B-roll method

A clone talking straight to camera for a solid minute looks unnatural no matter how good the sync is. Clone footage works when it is *cut* - which is also how you should be editing talking-head video anyway, for retention. The editing is not damage control; it is the format.

## The core method

1. **Generate the full take.** Let the clone deliver the whole script in one pass.
2. **Watch it once and mark the weak beats** - a mushy word, an odd blink, a gesture that repeated, a frame where the mouth looks wrong.
3. **Cut away over each weak beat**, keeping the clone's audio running underneath. The viewer hears continuous speech and sees something relevant.
4. **Cut away anyway, every five to eight seconds**, whether or not there is a problem. This is what makes the video feel edited rather than generated.
5. **Return to the clone** for the points that need a face - the hook, the turn, the CTA.

The consequence worth internalising: if one part of a generation looks bad, you usually do not have to regenerate the whole thing. Cover it. A regeneration costs credits and may break something else; a B-roll insert costs nothing and improves the video.

## What to cut away to

| B-roll type | Where to get it | Best for |
|---|---|---|
| Screen recordings | Your own screen | Anything about a tool, a result, a process |
| Product footage | Phone, or generated | Demos, unboxing, "this is the thing" |
| Stock or library clips | Stock libraries | Abstract concepts, locations, mood |
| Generated B-roll | An AI video model | Scenes you cannot film - see `ai-video-prompting` |
| Text cards and graphics | Your editor | Numbers, lists, quotes, the punchline of a point |
| Your own old footage | Camera roll | Authenticity, personal story beats |

Match the cut to the word being spoken. B-roll that illustrates what is being said right now holds attention; B-roll that is merely pretty loses it.

## The speed fix

If the clone speaks too slowly or the delivery feels slightly unnatural, speed the clip up. Around **1.1 to 1.2x** solves it in most cases - fast enough to add energy, not fast enough to sound chipmunked. Use your editor's pitch-preserving speed change.

This one adjustment resolves most "my clone sounds robotic" complaints, because what reads as robotic is often just pacing.

## Swapping hooks without regenerating

Because the hook is the first two seconds, you can rewrite only the hook, generate that fragment alone, and splice it onto the existing body. One video becomes three hook tests for a fraction of the cost - and the hook is what fatigues first in both organic and paid content.

The same trick works for CTAs at the other end.

## Retention editing

- **First second does the work.** Open on the hook, mid-sentence if needed. No logo, no intro, no "hey guys".
- **First clip under three seconds.** If nothing changes on screen within three seconds, people leave.
- **Captions on.** If people are reading, they are still watching. Keep them clean, two or three words a line, in the safe area.
- **Vary shot size** across inserts - a wide screen recording, a tight product detail, a text card - so the rhythm changes even when the speaker does not.
- **Cut the dead air.** Clone speech has small gaps. Tighten every one.
- **Sound design under everything.** Room tone, a quiet music bed, and the B-roll's own audio ducked under the voice. Silence behind a synthetic voice makes it sound more synthetic.
- **End on the payoff, then stop.** Trailing frames are where viewers drop before the loop.

## The realism pass

Apply to the finished timeline, on an adjustment layer:

1. **Lower contrast noticeably.** The single biggest tell of AI-generated video, and clone footage has it too.
2. **Reduce saturation slightly.** Stop before it looks lifeless.
3. **Lift highlights a little** if the image feels dense or heavy.
4. **Add handheld shake, barely.** The viewer should feel the footage is handheld but never notice an effect. If they notice it, reduce it.

Compare before and after rather than trusting slider positions. Full detail in `ai-video-prompting/references/realism-pass.md`.

## Quality checks before posting

- Does the first second hold?
- Is there any shot of the clone longer than about eight seconds uncut?
- Does every B-roll cut relate to the words under it?
- Any moment where the mouth looks wrong and is not covered?
- Captions accurate, in the safe area, not covering the face?
- Audio level consistent with your other posts?
- Would you know it was a clone if you had not made it?

The last question is the real test, and the honest answer is usually "not if the editing is good" - which is the whole reason the editing matters more than the generation.

## Long-form and courses

For lessons and long-form, the same method scales with two additions:

- **Section the script** and generate per section, so a correction re-renders one section rather than forty minutes.
- **Keep a slide or screen layer running** for most of the duration, with the clone in a corner or cut in at transitions. This is both more watchable and far more forgiving.

The advantage over filming is not speed alone: a mistake in lesson nine is a text edit and one re-render, with no studio, no lighting setup, and no need to match how you looked eight months ago.

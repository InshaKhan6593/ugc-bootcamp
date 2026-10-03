# UGC / phone realism mode

Use when the image or video must look like a real person filmed it on a phone: UGC ads, TikTok/Reels/Shorts, influencer selfies, testimonials, "caught on camera" hooks.

The course's depth, lighting and camera lessons are taught with cinema cameras (ARRI, Sony Venice, f/1.8, 85mm, film grades). Those rules still decide *what* is in the frame. But a phone records the frame differently, and mixing the two is one of the main reasons AI UGC looks fake. Pick a mode first.

## Step 0: choose the mode

| Lever | Cinematic mode | UGC / phone mode |
|---|---|---|
| Camera words | ARRI Alexa, Sony Venice 2, RED, Hasselblad | "iPhone front camera", "phone back camera", "raw phone photo/footage" |
| Lens | 24-200mm, chosen for the emotion | ~24-26mm main, ~22-26mm selfie, telephoto only if "zoomed in" |
| Camera distance | anywhere | arm's length (40-60cm), propped on a surface, or a friend 1-2m away |
| Focus | shallow depth of field, bokeh, f/1.4-f/2 | **deep focus**: background mostly sharp, softened a little by phone processing. Blur only if you say "portrait mode" |
| Light | motivated, shaped, often dramatic | the light that is actually in that room (see `ai-cinematography/references/lighting.md`, UGC table). Mixed temperatures are fine |
| Composition | thirds, leading lines, lead room | still thirds, but slightly imperfect: a little tilted, subject a bit off, hand or arm in frame; keep face and product inside the 9:16 safe area (`ai-cinematography/references/composition.md`) |
| Colour | film grade (teal-orange, Kodak, desaturated) | phone processing: slightly bright, slightly sharpened, natural colour, no grade name |
| Texture | film grain | fine digital noise in shadows, mild compression, slight HDR from the phone |
| Movement (video) | dolly, crane, orbit | handheld micro-jitter, small reframes, phone propped still |
| Negative | no CGI, no plastic skin | + "no cinematic colour grade, no studio lighting, no professional camera look" |

A **hybrid** is fine and common in ads: a cinematic B-roll product shot cut against phone-mode talking-head shots. Just decide per shot and do not mix the two sets of words inside one prompt.

## Depth of field: the key logic

* Phone sensors are tiny, so at normal selfie distance **most of the scene stays in focus**. Real selfies show a readable room behind the person.
* Heavy creamy bokeh + "iPhone selfie" = an image that no phone would produce. Many prompts (including course examples) write "shallow depth of field" on phone selfies. It can work, but it pushes the look toward a DSLR portrait. Prefer: "background slightly soft but recognisable" or explicitly "iPhone portrait mode, slightly artificial background blur with soft edges around the hair".
* Close objects *do* blur on a phone: a hand or product pushed very close to the lens can go soft. Use this for a natural foreground layer.

## Phone realism cues (pick 3-5, do not stack them all)

* "raw unedited phone photo", "posted straight to Instagram Stories", "no filter"
* "slight wide-angle distortion from holding the phone close", "arm and hand near the lens look slightly larger"
* "slightly off-centre, a little tilted, casual framing", "top of the head slightly cropped"
* "phone camera sharpening, fine digital noise in the shadows, mild compression"
* "slightly blown-out window behind her" (phones clip bright windows; a perfect exposure everywhere looks fake)
* "mixed window daylight and warm lamp light"
* "visible pores, faint blemishes, slight redness, natural oiliness, flyaway hairs"
* "real lived-in room: unmade bed, charger cable, water glass on the side table"
* for video: "handheld, tiny natural hand shake, small reframes", then apply the realism pass (lower contrast, slightly lower saturation, subtle shake) from `ai-video-prompting/references/realism-pass.md`

## Wording that fights realism (both modes)

Avoid or use sparingly: "8K", "8K masterpiece", "hyper-detailed", "ultra-glossy", "perfect lighting", "flawless skin", "cinematic masterpiece", "HDR" (heavy). Some course example prompts use "8K photorealism", "ultra-realistic" or "hyper-realistic" and still get good results; these words are acceptable as a single realism trigger, but never pile them up, and never pair them with beauty words. "Ultra realistic" at the end of a prompt, as the course does, is fine. The realism comes from the specific cues (light source, texture, imperfection), not the resolution words.

## UGC prompt skeleton

**[Shot type + phone camera position]** → **[Subject: who, age, look, expression, what they are doing]** → **[Product, if any: held where, label facing camera, exact label text]** → **[Foreground / midground / background as everyday objects]** → **[The real light in that room + catchlight]** → **[Phone realism cues]** → **[Negatives]**

Example:
"Raw iPhone front-camera selfie at arm's length, camera slightly above eye level, a 27-year-old woman sitting cross-legged on her unmade bed in the morning, messy bun, oversized grey t-shirt, mid-sentence, eyebrows raised like she's telling a friend something. She holds a small amber serum bottle toward the lens, slightly closer to the camera than her face, label facing the camera reading "GLOW DROPS". Foreground: her hand and the bottle, slightly soft from being close to the lens. Midground: her face, sharp. Background: rumpled white duvet, a nightstand with a phone charger and a water glass, still readable. Soft daylight from a window on her left, the right side of her face in soft shadow, rectangular window catchlight in her eyes, the window behind slightly blown out. Visible pores, faint freckles, a little shine on the nose. Slight wide-angle distortion, casual slightly tilted framing, phone sharpening and fine noise. No studio lighting, no cinematic colour grade, no plastic skin, no text overlays."

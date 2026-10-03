# Depth and cinematic framing

Use when an image looks flat or badly composed: layers, atmosphere, rule of thirds, leading lines, lead room.

## Depth & Cinematic Framing

## What you're building

Use depth, composition, and framing to stop AI shots from looking flat. The goal is to think like a cinematographer before writing the prompt, so the model has enough direction to build a frame with space, atmosphere, and visual intention.

Flat AI shots usually describe only one layer: subject plus background. That often makes the person feel pasted onto the scene.

## 1. Build the frame in layers

Real scenes have depth because your eye reads the world in layers. A cinematic prompt should describe what sits close to the camera, where the subject lives, and what falls away in the distance.

* Foreground: the closest layer to the camera - leaves, grass, smoke, a window edge, a shoulder, railing, wall, car hood, or any object partially framing the shot.

* Midground: the subject or main object the viewer should look at.

* Background: the world behind the subject - street, room, skyline, landscape, bridge, sky, or distant environment.

Write foreground, midground, and background into the prompt so the AI understands the frame as a real space, not a flat backdrop.

**Prompt structure**

Weak: man standing beside an orange sports car in a city street, cinematic lighting.

Better: orange sports car close to the camera in the foreground, man standing beside it in the midground, city street and tall buildings falling away into the background, cinematic lighting.

## 2. Add a foreground object

The foreground is the fastest fix when an AI image feels too flat. Add something close to the lens, slightly out of focus, so the viewer's eye travels from front to subject to background.

Foreground objects like leaves, grass, windows, smoke, shoulders, railings, or walls make the shot feel physically layered.

**Prompt structure**

**Add**: out-of-focus leaves in the foreground close to the lens.

**Other options**: blurred window frame, grass near the camera, smoke drifting across the lens, shoulder in the foreground, railing cutting through the frame.

## 3. Use atmosphere to separate the layers

Atmosphere is anything in the air between the camera and the distance: haze, fog, mist, dust, smoke, exhaust, or light rays. It pushes the background back and makes depth easier to read.

* Light haze makes a city or street feel larger and more cinematic.

* Dust in a shaft of light makes the air visible and creates god rays.

* Low fog separates the foreground, subject, and background clearly.

* Smoke or exhaust adds mood and movement while also creating depth.

**PROMPT:**

Medium-wide shot, eye-level, slight three-quarter angle. The man from @Image1 leaning on an orange Ferrari electric sports car from @Image2, recolored from blue to bright orange, in an empty underground parking structure - keep his face, beard, hair and outfit exactly as in @Image1 (white technical tracksuit with orange piping, orange wraparound shield-visor sunglasses, orange chrome-soled sneakers). Concrete columns recede behind him.

[ATMOSPHERE] Drifting smoke and exhaust hanging in the air around the subject and the car, slowly moving, adding movement and mood on top of the depth.

Cold light, wet reflective floor. Shot on Sony Venice 2 cinema camera, ARRI Master Prime lens, 35mm, f2. Desaturated cool grade, concrete greys with orange accents only. Layered foreground-midground-background depth. Ultra realistic.

Atmosphere gives the frame physical space: haze, fog, smoke, and reflections separate the subject from the background.

### Prompt structure

`industrial street at night, wet reflective ground, low fog rolling across the street, soft haze in the background, cinematic overhead lights, subject in the midground`

## 4. Stop defaulting to dead center

Dead center can work for a hero shot, symmetry, or a direct stare into the lens. But if the AI centers every subject by default, the frame starts to feel static. Use the rule of thirds to create balance and direction.

* Imagine the frame split into nine boxes with two vertical and two horizontal lines.

* Place the subject along one of the lines or on an intersection point.

* Use the empty space to show where the subject is looking, moving, or reacting.

**PROMPT:**

Wide shot, eye-level, subject small on the left third. The man from @Image1 walking across a wide viewpoint near the Golden Gate Bridge, a small figure on the left third, dwarfed by the open space on the right - keep his face, beard, hair and outfit exactly as in @Image1 (white technical tracksuit with orange piping, orange wraparound shield-visor sunglasses, orange chrome-soled sneakers).
[FOREGROUND] Out-of-focus grass and railing of the viewpoint close to the lens, framing the lower edge.
The Golden Gate Bridge and the vast bay sprawl across the right two thirds of the frame, muted warm desaturated tones fading into deep haze, a helicopter hovering in the distant sky. Cold cinematic daylight. Shot on ARRI Alexa LF, 24mm, f4. Desaturated cool grade, bridge muted, orange the only saturated color. Deep layered depth, strong rule-of-thirds, vast and directional. Ultra realistic.

Placing the subject off-center gives the frame space to breathe and creates a more intentional composition.

### Prompt structure

`Prompt direction: place the subject on the right third of the frame, looking across the open space to the left, cinematic composition, background receding into fog.`

## 5. Lead the viewer's eye

The viewer's eye doesn't move randomly. Lines inside the frame pull attention. Roads, railings, walls, fences, light beams, bridges, parked cars, and building edges can all point the viewer toward the subject.

* Look for natural lines already in the location.

* Angle those lines toward the subject or main point of interest.

* Use roads, curbs, railings, architecture, light beams, or rows of objects to guide attention.

**PROMPT:**
Wide shot, eye-level, subject small on the left third. The man from @Image1 walking across a wide viewpoint near the Golden Gate Bridge, a small figure on the left third, dwarfed by the open space on the right - keep his face, beard, hair and outfit exactly as in @Image1 (white technical tracksuit with orange piping, orange wraparound shield-visor sunglasses, orange chrome-soled sneakers).
[FOREGROUND] Out-of-focus grass and railing of the viewpoint close to the lens, framing the lower edge.
The Golden Gate Bridge and the vast bay sprawl across the right two thirds of the frame, muted warm desaturated tones fading into deep haze, a helicopter hovering in the distant sky. Cold cinematic daylight. Shot on ARRI Alexa LF, 24mm, f4. Desaturated cool grade, bridge muted, orange the only saturated color. Deep layered depth, strong rule-of-thirds, vast and directional. Ultra realistic.

The railing, path, and bridge structure create visual direction, pulling attention through the frame instead of leaving it static.

## 6. Use lead room

Lead room is the space in front of where a subject is looking or moving. If someone is looking right, leave space on the right. If they're walking left, leave space on the left. Without lead room, the frame feels trapped.

Leave room in the direction the subject is facing or moving. Empty space becomes visual direction.

**Prompt structure**

`Prompt direction: subject positioned on the right side of the frame, looking left into open city space, strong lead room, cinematic composition.`

## The 5 rules to remember

| 5 RULESOF CINEMATIC FRAMING   | 5 RULESOF CINEMATIC FRAMING | 5 RULESOF CINEMATIC FRAMING                                                                                                          |
| ----------------------------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| \[icon: three stacked layers] | **1. DEPTH**                | AI builds flat by default, a strong frame is built through foreground / midground / background.                          |
| \[icon: cloud/smoke]          | **2. ATMOSPHERE**           | Haze, dust, fog, smoke/exhaust help separate layers and enhance the sense of space.                                          |
| \[icon: grid with dots]       | **3. RULE OF THIRDS**       | The subject should not stand in the center by default. You need to consciously place it on a third to let the frame breathe. |
| \[icon: perspective lines]    | **4. LEADING LINES**        | Lines in the frame guide the viewer's eye to the subject.                                                                        |
| \[icon: person with arrow]    | **5. LEAD ROOM**            | You need to leave space in the direction the subject is looking or moving, otherwise the frame will feel cramped.            |

Use these five rules as the quick mental checklist before writing any cinematic AI prompt.

* · **Depth:** build the shot in foreground, midground, and background.

* · **Atmosphere:** add haze, fog, dust, mist, smoke, or visible air between layers.

* · **Rule of thirds:** stop letting the AI center everything by default.

* · **Leading lines:** use roads, rails, walls, bridges, or light to guide the eye.

* · **Lead room:** leave space in the direction the subject is looking or moving.

## Extra teaching from the lesson video (not in the PDF)

* **Why atmosphere creates depth:** in the real world air is not empty. The further away something is, the more air sits between you and it, so distant things get **lighter, softer and lower in contrast**. The brain reads that instantly as distance (it is why far buildings fade into city haze). You can add it on purpose. To push a background back, write "background slightly hazy, lighter and lower in contrast".
* **The one question when a shot feels flat:** *What's in my foreground, and what's in the air?* Nine times out of ten, that is what's missing.
* **Background alone is not depth.** Most people only describe the background, which is why their shots stay flat. The foreground is the layer everyone forgets.
* **The midground is where the subject lives:** the person, character or product the viewer should look at.
* **Dead centre is a tool, not a mistake.** A powerful hero shot, raw symmetry, or a character staring straight down the lens hits hardest centred. The point is you choose it on purpose, not land there by default.
* **Leading lines example:** the street, the curb and the line of parked cars all run toward the subject, and the eye has no choice.
* **Lead room mistake:** crowding the space in front of the subject and leaving the empty room behind them makes the shot feel trapped, as if they are about to walk into the frame edge.
* Everything comes down to one idea: direct the frame instead of accepting whatever the AI gives you by default.

## Depth layers for UGC / phone content

Foreground/midground/background still applies to UGC, but the layers are everyday things, not leaves and fog:

| Shot type | Foreground | Midground | Background |
|---|---|---|---|
| Arm's-length selfie | edge of the extended arm/hand, or the product held toward the lens | face and shoulders | lived-in room: unmade bed, shelf, plants, door |
| Product-in-hand | the product, slightly closer to the camera than the face, label facing the lens | face, eyes on camera | kitchen / bathroom / bedroom slightly soft |
| Propped-phone talking head | edge of the counter/desk, a mug, the product standing on the table | the creator | room with real clutter |
| Car | steering wheel or seatbelt edge | driver's face | side window, street outside |
| Mirror selfie | phone and hand | body in the mirror | reflected room |
| Bathroom routine | sink edge, bottles on the counter | face at the mirror | tiles, towel, shower curtain |

UGC "atmosphere" is steam from a shower or coffee, dust in window light, or a slightly dirty mirror, not fog and smoke. Keep the background believable and lived-in (not staged): a few specific real objects beat a generic "modern apartment".

## Vertical 9:16 framing for social ads

The rule of thirds still applies, but TikTok, Reels and Shorts cover part of the frame with the interface:

* Keep the face and product in the **centre band, roughly the middle 60% of the height**.
* Keep the bottom ~20% free of anything important (captions, username, CTA button) and the right edge free (like/comment/share icons).
* Keep the top ~10% clear of key detail (status bar, search).
* The eye line usually sits on the **upper third line**. The product is best in the middle of the frame, not at the bottom edge where the caption sits.
* Leave clean space for on-screen text (usually upper-middle) if the ad uses text hooks.

**The big idea:** don't just describe what is in the image. Direct how the frame is built. The difference between a flat AI shot and a cinematic shot usually comes from spatial thinking before the prompt is written.

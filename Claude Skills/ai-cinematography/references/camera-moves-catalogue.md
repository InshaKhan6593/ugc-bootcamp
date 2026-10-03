# Camera movement catalogue: 37 moves, six-slot template

Copy-ready prompts using Movement / Start / Speed / Framing / End / Time, with AI failure notes.

# Camera Movement The Full Catalogue

## Contents

- [What you're building](#what-youre-building)
- [Static Shot](#static-shot)
- [Pan](#pan)
- [Whip Pan](#whip-pan)
- [Dolly In](#dolly-in)
- [Dolly Out · and the Reveal](#dolly-out-and-the-reveal)
- [Zoom In / Zoom Out](#zoom-in-zoom-out)
- [Slow Zoom](#slow-zoom)
- [Fast Zoom](#fast-zoom)
- [Crash Zoom In](#crash-zoom-in)
- [Crash Zoom Out](#crash-zoom-out)
- [Truck](#truck)
- [Slider](#slider)
- [Pedestal](#pedestal)
- [Push Past](#push-past)
- [Arc](#arc)
- [Orbit](#orbit)
- [Spiral](#spiral)
- [Follow From Behind](#follow-from-behind)
- [Reverse Tracking](#reverse-tracking)
- [Side Tracking](#side-tracking)
- [Low Tracking Shot](#low-tracking-shot)
- [Vehicle Tracking](#vehicle-tracking)
- [Chase Shot](#chase-shot)
- [Handheld Shot](#handheld-shot)
- [Reactive Snap Zoom](#reactive-snap-zoom)
- [Snorricam](#snorricam)
- [Crane Up / Crane Down](#crane-up-crane-down)
- [Drone Shot](#drone-shot)
- [Fly-Through](#fly-through)
- [FPV Dive](#fpv-dive)
- [Dolly Zoom](#dolly-zoom)
- [Macro Exit](#macro-exit)
- [Probe Lens Shot](#probe-lens-shot)
- [Bullet Time](#bullet-time)
- [Gravity Roll](#gravity-roll)
- [Infinite Zoom](#infinite-zoom)

---

## What you're building

A complete camera movement reference for AI video. This catalogue turns 37 camera moves into copy-ready prompts using one repeatable six-slot structure: movement, start, speed, framing, end, and time.

### 37 camera moves · 8 groups · 1 prompt template

The goal is not to add movement for decoration.

* Make the model understand what physically moves.

* Define the start, speed curve, and final frame.

* Keep the subject/framing stable where needed.

* Avoid default AI drift, floating cameras, and fake slow motion.

* Use the AI note to prevent common model failures.

Use this as a practical directing catalogue: pick the move, copy the prompt, then replace the scene details with your own subject, setting, and action.

# The six-slot prompt template

A camera prompt fails when it leaves decisions to the model. These six slots are the decisions.

### Movement

The move by name and what it rides on: rails, shoulder, crane, drone.

### Speed

The curve: ease in, build, decelerate, constant, violent, or creeping.

### End

The final frame and the hold, or an exit still in motion.

### Start

How it begins: locked frame or already moving on frame one.

### Framing

What stays stable while everything else changes.

### Time

Real time, no slow motion - or exactly what slows down and nothing else.

# Quick index

Camera move groups

* **GROUP 1**: The Camera Stays Put (4 moves)

* **GROUP 2**: Closer and Further (7 moves)

* **GROUP 3**: Traveling Past (4 moves)

* **GROUP 4**: Around (3 moves)

* **GROUP 5**: Tracking (6 moves)

* **GROUP 6**: The Human Camera (3 moves)

* **GROUP 7**: The Air (4 moves)

* **GROUP 8**: The Impossible (6 moves)

# Move index

Moves 01-19

**01. Static Shot**

The Camera Stays Put

**02. Pan**

The Camera Stays Put

**03. Tilt**

The Camera Stays Put

**04. Whip Pan**

The Camera Stays Put

**05. Dolly In**

Closer and Further

**06. Dolly Out · and the Reveal**

Closer and Further

**07. Zoom In / Zoom Out**

Closer and Further

**08. Slow Zoom**

Closer and Further

**09. Fast Zoom**

Closer and Further

**10. Crash Zoom In**

Closer and Further

**11. Crash Zoom Out**

Closer and Further

**12. Truck**

Traveling Past

**13. Slider**

Traveling Past

**14. Pedestal**

Traveling Past

**15. Push Past**

Traveling Past

**16. Arc**

Around

**17. Orbit**

Around

**18. Spiral**

Around

**19. Follow From Behind**

Tracking

# Move index continued

Moves 20-37

| 20. Reverse Tracking Tracking           | 21. Side Tracking Tracking         |
| ------------------------------------------- | -------------------------------------- |
| 22. Low Tracking Shot Tracking          | 23. Vehicle Tracking Tracking      |
| 24. Chase Shot Tracking                 | 25. Handheld Shot The Human Camera |
| 26. Reactive Snap Zoom The Human Camera | 27. Snorricam The Human Camera     |
| 28. Crane Up / Crane Down The Air       | 29. Drone Shot The Air             |
| 30. Fly-Through The Air                 | 31. FPV Dive The Air               |
| 32. Dolly Zoom The Impossible           | 33. Macro Exit The Impossible      |
| 34. Probe Lens Shot The Impossible      | 35. Bullet Time The Impossible     |
| 36. Gravity Roll The Impossible         | 37. Infinite Zoom The Impossible   |

01

## Static Shot

The camera is locked. Nothing moves but the scene itself, so the audience reads every detail inside the frame.

GROUP 1 · The Camera Stays Put · Rotation on a fixed point · the foundation

### Use it

when the scene is strong on its own - a face about to break, two people at a table - and when you need a clean cut into the next shot.

**AI note**

without "no camera movement, hold the same framing", the model almost always adds a slow drift.

Copy-ready prompt

**Movement:** locked static shot, camera on a tripod, no camera movement of any kind. **Start:** the framing is already set on frame one. **Speed:** none, zero drift. **Framing:** hold the exact same composition for the entire clip. **End:** same frame as the start. **Time:** real time, normal speed, no slow motion.

02

## Pan

The camera stays on its spot and rotates left or right - a standing person following the action with their head.

GROUP 1 · The Camera Stays Put · Rotation on a fixed point · the foundation

### Use it

to follow someone crossing a room, or to carry attention from one thing to another inside the same space.

**AI note**

give the pan a destination; a pan with no target turns into drift.

**Copy-ready prompt**

Movement: pan right from a fixed camera position. Start: hold the opening composition for a beat, then begin the rotation. Speed: smooth constant rotation. Framing: keep the horizon level throughout. End: settle on the final composition and hold. Time: real time, normal speed, no slow motion.

03

The same rotation, vertical: the camera tips up or down from a fixed point.

GROUP 1 · The Camera Stays Put · Rotation on a fixed point · the foundation

Use it

tilt up a character from boots to face to introduce them in pieces; tilt down to land on what's on the floor.

AI note

keep the tilt on one axis; mixed pan-tilt paths on faces often warp geometry.

Copy-ready prompt

Movement: tilt up from a fixed camera position. Start: hold on her shoes for a beat, then begin the tilt. Speed: slow, even rotation upward. Framing: camera position fixed, only the angle changes. End: land on her eyes and hold. Time: real time, normal speed, no slow motion.

04

## Whip Pan

A pan so fast the frame smears into blur. Punctuation: something just happened over there. Also hides cuts - two shots stitched inside one blur read as a single take.

GROUP 1 · The Camera Stays Put · Rotation on a fixed point · the foundation

**Use it**

reactions, reveals, comedic beats, invisible transitions between two clips.

**AI note**

always whip toward something. No target - the model whips toward nothing.

**Copy-ready prompt**

Movement: fast whip pan to the right from a fixed position. Start: locked frame, then the whip fires suddenly. Speed: violent, near instant rotation with heavy motion blur through the turn. Framing: start sharp, blur through the middle. End: land sharp on the new subject and hold. Time: real time, normal speed, no slow motion.

05

## Dolly In

The camera physically travels toward the subject. It shrinks the world: context falls away until only the face - or the object - is left.

GROUP 2 · Closer and Further · Closing the distance and breaking it · the most used group

### Use it

the moment something changes inside a person: a realization, a decision. On objects, it assigns importance: this matters, remember it.

**AI note**

"slow push-in" alone names only the pace - the model invents the start and the ending. Fill both slots.

**Copy-ready prompt**

Movement: dolly in toward her face, camera on rails. Start: begin from a locked static frame, then ease into the move. Speed: smooth push, building momentum, then decelerating. Framing: keep camera height and lens direction constant as the distance closes. End: settle into a close-up and hold the final frame. Time: real time, normal speed, no slow motion.

06

## Dolly Out · and the Reveal

The reverse: the frame keeps opening and the world comes back. Retreat far enough onto something the audience didn't know was there, and it becomes the reveal.

GROUP 2 · Closer and Further · Closing the distance and breaking it · the most used group

**Use it**

isolation (he's small inside the empty room), endings, and the reveal: she's not alone in that room.

**AI note**

for a reveal, describe what the frame opens onto - the new information is the shot.

**Copy-ready prompt**

Movement: dolly out from her face, camera on rails, straight backward. Start: begin locked on a close-up, then ease into the retreat. Speed: steady, even pull backward. Framing: she stays centered as the space grows around her. End: settle on a wide shot, she is a small figure in the empty hall; hold. Time: real time, normal speed, no slow motion.

## Zoom In / Zoom Out

The camera stays planted; the lens crops in and magnifies. No parallax, no perspective shift - the framing tightens, the viewpoint doesn't move.

GROUP 2 · Closer and Further · Closing the distance and breaking it · the most used group

**Use it**

when you want the frame to tighten without moving the audience through the space. A different sentence from the dolly, not a cheaper one.

**AI note**

say "camera stays in a fixed position" - otherwise the model blends zoom and dolly into a mongrel move.

**Copy-ready prompt**

Movement: zoom in on her face, camera fixed in place, optical zoom only. Start: hold the wide framing, then begin the zoom. Speed: smooth and even. Framing: camera position never changes, only the field of view narrows. End: settle on the close-up and hold. Time: real time, normal speed, no slow motion.

08

## Slow Zoom

Creeping, almost invisible tightening. Tension building - something is quietly becoming important.

GROUP 2 · Closer and Further · Closing the distance and breaking it · the most used group

### Use it

monologues, dread, the slow realization the audience gets before the character does.

**AI note**

the safest zoom for faces - no parallax means nothing warps.

**Copy-ready prompt**

Movement: slow zoom in on his face, camera fixed, optical zoom only. Start: the zoom is already creeping on frame one, almost imperceptible. Speed: very slow, constant, never accelerating. Framing: he stays centered as the frame tightens. End: the clip ends with the zoom still creeping. Time: real time, normal speed, no slow motion.

09

## Fast Zoom

Quick and clean tightening - noticeable, but controlled.

GROUP 2 · Closer and Further · Closing the distance and breaking it · the most used group

**Use it**

a sudden discovery, a reality check, something just went wrong.

**AI note**

the faster the zoom, the harder the model pushes everything else into slow motion - the Time slot is doing real work here.

**Copy-ready prompt**

Movement: fast zoom in onto the object in her hands, camera fixed, optical zoom only. Start: locked frame; the zoom fires on the trigger - she gasps. Speed: quick, decisive, one clean motion. Framing: the object stays centered. End: land tight on the object and hold. Time: real time, normal speed, no slow motion.

10

## Crash Zoom In

A violent snap onto the subject, blur and all. Shock, a punchline, a hard emphasis.

GROUP 2 · Closer and Further · Closing the distance and breaking it · the most used group

### Use it

comedic beats, sudden overwhelming realizations, hard emphasis on a face or a detail.

**AI note**

land the crash on a strong feature - eyes, hands, an object - or the snap reads as a glitch.

**Copy-ready prompt**

Movement: crash zoom in onto his face, camera fixed, optical zoom only. Start: locked frame, then the zoom snaps with no ramp. Speed: violent, near-instant, motion blur through the snap. Framing: from wide to extreme close-up in one hit. End: land sharp on his eyes and hold. Time: real time, normal speed, no slow motion.

## Crash Zoom Out

The same violence in reverse: the frame punches open and the context lands all at once.

GROUP 2 · Closer and Further · Closing the distance and breaking it · the most used group

### Use it

comedy - the suit with no pants - and shock: crash out from a calm face to the chaos all around them.

### AI note

describe what the wide reveals - the joke or the shock is in the new context, not in the move.

### Copy-ready prompt

Movement: crash zoom out from her calm face, camera fixed, optical zoom only. Start: locked close-up, then the zoom punches out with no ramp. Speed: violent, near-instant, motion blur through the snap. Framing: from close-up to a wide shot in one hit, revealing the full scene around her. End: land sharp on the wide and hold. Time: real time, normal speed, no slow motion.

12

## Truck

The camera moves left or right on a straight path, lens facing forward. The scene slides across the frame like a panorama you're driving past.

GROUP 3 · Traveling Past · Straight lines that don't aim at the subject

### Use it

to unfold a space piece by piece: a market street, a wall of photographs, a line of suspects. The environment is the subject.

**AI note**

long trucks need consistent environments - describe the space, or the model improvises new geometry mid-slide.

**Copy-ready prompt**

Movement: truck right along the scene on a straight path, lens facing forward the whole way. Start: begin from a locked frame, ease into the slide. Speed: smooth constant lateral speed. Framing: camera height and lens direction never change. End: ease off and settle at the end of the space. Time: real time, normal speed, no slow motion.

## Slider

The truck at small scale: a short, controlled slide. Foreground and background shift against each other, and a flat shot gains depth.

GROUP 3 · Traveling Past · Straight lines that don't aim at the subject

### Use it

tabletops, interiors, product shots - anywhere a big move would be too loud.

**AI note**

put something real in the foreground - the parallax is the whole point of the move.

**Copy-ready prompt**

Movement: slow slider move to the left, a short controlled slide past the objects in the foreground. Start: locked frame, then ease into the slide. Speed: slow and even, subtle. Framing: subject readable behind the foreground, parallax between the layers. End: settle softly and hold. Time: real time, normal speed, no slow motion.

14

## Pedestal

Straight up or straight down without tilting, like an elevator. The framing stays level; the height changes.

GROUP 3 · Traveling Past · Straight lines that don't aim at the subject

### Use it

rise from the evidence on the desk to the face reading it; drop from a calm face to what the hands are doing.

**AI note**

say "no tilt" - without it the model blends pedestal and tilt into a curve.

**Copy-ready prompt**

**Movement:** pedestal up from the desk to his face, straight vertical rise, no tilt. **Start:** locked frame on the desk, then ease into the rise. **Speed:** steady, even vertical speed. **Framing:** camera stays level the whole way. **End:** settle at eye level and hold. **Time:** real time, normal speed, no slow motion.

15

## Push Past

Forward travel past a foreground object - a doorframe, a shoulder, hanging cables - into what's behind. For one moment the shot has skin.

GROUP 3 · Traveling Past · Straight lines that don't aim at the subject

### Use it

to enter a scene instead of cutting into it - the audience slips into the room past the doorway.

**AI note**

the foreground must pass fully out of frame - half-crossed foregrounds read as a glitch.

**Copy-ready prompt**

Movement: the camera pushes forward past the doorframe into the room. Start: begin just outside, already easing forward. Speed: smooth, unhurried push. Framing: the doorframe passes close to the lens, almost touching it. End: settle on the subject inside and hold. Time: real time, normal speed, no slow motion.

16

## Arc

A curved path around the character - a quarter turn, maybe half. They stay put; the background swaps behind them.

GROUP 4 · Around · Curved paths · one rule: the circle must earn its ending

### Use it

when the situation needs to be seen from another side, literally. The person she's talking to enters the frame.

AI note

quarter and half turns hold identity far better than full circles - especially on close shots.

Copy-ready prompt

Movement: arc right around her, a quarter turn on a curved path. Start: locked frame, then ease into the curve. Speed: smooth, leaning into the curve, then easing off. Framing: keep the distance and height constant, she stays centered. End: settle on the new angle and hold. Time: real time, normal speed, no slow motion.

17

## Orbit

The arc taken all the way: a full circle. Spectacular - and empty, unless the frame ends holding something it didn't hold at the start.

GROUP 4 · Around · Curved paths · one rule: the circle must earn its ending

### Use it

when the whole world around the subject is worth showing, and something changes during the circle: a figure appears, the light shifts, the room empties.

**AI note**

full orbits are where faces melt. The wider the shot, the safer the circle.

**Copy-ready prompt**

Movement: orbit clockwise around her at a consistent radius, on a stabilized rig. Start: locked frame held for a beat, then ease into the orbit. Speed: accelerate into the curve, carry momentum, then decelerate. Framing: she stays centered while the background rotates around her. End: come to a full stop on the figure standing behind her; hold. Time: real time, normal speed, no slow motion.

18

## Spiral

An orbit that leaves its circle: around and inward reads as obsession; around and upward reads as release.

GROUP 4 · Around · Curved paths · one rule: the circle must earn its ending

**Use it**

when the circling and the closing serve one destination. If you can't name where it ends in one sentence, it's two moves pulling apart.

**AI note**

one full revolution maximum - spirals past 360° lose the geometry.

**Copy-ready prompt**

Movement: spiral around her, circling clockwise while slowly closing in. Start: locked frame, then ease into the spiral. Speed: even through the curve, decelerating as the radius closes. Framing: she stays centered, the frame tightening with each degree. End: end on a close-up of her face and hold. Time: real time, normal speed, no slow motion.

19

## Follow From Behind

Shoulder height, one step behind. We see what they see - everything except their face - and discover the place the same moment they do.

GROUP 5 · Tracking · The camera takes the character's pace

### Use it

walking into the unknown: the dark corridor, the crowd, the door at the end.

**AI note**

tracking legally starts in motion - that's its nature. The ending still needs a decision.

**Copy-ready prompt**

Movement: follow her from behind at shoulder height. Start: already moving with her on frame one. Speed: match her walking pace exactly. Framing: keep the route ahead readable over her shoulder. End: when she stops, the camera stops with her. Time: real time, normal speed, no slow motion.

20

## Reverse Tracking

The camera retreats in front of them as they advance. The distance never grows - they keep closing it - and the face carries the shot.

GROUP 5 · Tracking · The camera takes the character's pace

Use it

determination: someone who has decided and is already on the way.

AI note

the most stable tracking for faces - the relative stillness protects identity.

Copy-ready prompt

Movement: reverse tracking in front of him, the camera moving backward. Start: already moving as he walks on frame one. Speed: match his pace, the distance constant. Framing: hold his face centered, background streaming past behind him. End: he stops; the camera settles with him. Time: real time, normal speed, no slow motion.

21

## Side Tracking

Parallel travel at their pace. The subject becomes the walk itself: the body, the stride, the world flowing past.

GROUP 5 · Tracking · The camera takes the character's pace

**Use it**

journeys, athletes, montage beats where the distance covered is the story.

**AI note**

side tracking is the profile shot - describe the background layers, they carry the sense of speed.

**Copy-ready prompt**

Movement: side tracking shot, camera moving parallel to her. Start: already moving with her on frame one. Speed: constant, locked to her stride. Framing: side profile at a constant distance, background passing behind her. End: the clip can end mid-stride - the walk continues. Time: real time, normal speed, no slow motion.

22

## Low Tracking Shot

The same following move below the waist: boots, hands, wheels. The audience reads the walk before they're allowed to read the person.

GROUP 5 · Tracking · The camera takes the character's pace

### Use it

introductions that keep the mystery; tension before a face is earned.

**AI note**

"face never shown" is a framing instruction the model respects - use it, don't hope.

**Copy-ready prompt**

Movement: low tracking shot at knee height, following her heels. Start: already moving with her steps on frame one. Speed: locked to her stride. Framing: below the waist the entire clip, face never shown. End: she stops at the door; hold on the heels. Time: real time, normal speed, no slow motion.

23

## Vehicle Tracking

Riding alongside a moving car, bike or train at matching speed. The vehicle sits almost still in frame while the world tears past - that contrast is what speed looks like.

GROUP 5 · Tracking · The camera takes the character's pace

### Use it

when the speed is the story: the escape, the race, the open road.

**AI note**

anchor the camera ("from a chase car alongside") - unanchored vehicle shots float.

**Copy-ready prompt**

**Movement:** vehicle tracking shot, camera traveling alongside the car. **Start:** already at matching speed on frame one. **Speed:** locked to the vehicle. **Framing:** car steady in frame, road and landscape streaking past behind it. **End:** the clip ends still in motion. **Time:** real time, normal speed, no slow motion.

24

## Chase Shot

Tracking at a run. The framing slips, corrects, loses the subject for half a beat and catches them again - that struggle is what panic looks like on screen.

GROUP 5 · Tracking · The camera takes the character's pace

**Use it**

panic, escape, pursuit.

**AI note**

constant chaotic shaking kills it - the corrections must have causes: a turn, an obstacle, a stumble.

**Copy-ready prompt**

Movement: handheld chase shot, the operator running behind the subject. Start: already sprinting on frame one. Speed: urgent, uneven human pace. Framing: framing slips and corrects, brief losses of the subject, brief motion blur on the fastest steps. End: the clip ends still running. Time: real time, normal speed, no slow motion.

25

## Handheld Shot

The operator's body gets into the image: the frame sways with breathing, shifts weight with each step, makes small corrections. A locked frame observes; a handheld frame attends.

GROUP 6 · The Human Camera · Making generated footage look shot

**Use it**

scenes that should be witnessed rather than staged: the argument, the interview going wrong, horror.

**AI note**

describe the person carrying it, not "shakiness" - models do humans better than abstract shake.

**Copy-ready prompt**

Movement: handheld shot at chest height, a human operator holding the camera. Start: the sway is present from frame one. Speed: organic, uneven, weight shifting with each step. Framing: natural sway and breathing, small human reframing, subject always readable. End: the operator steadies and settles on the subject. Time: real time, normal speed, no slow motion.

26

## Reactive Snap Zoom

A chain, in order: event · late turn · fast zoom · overshoot · correction · settle. The blur is the proof someone was standing there.

GROUP 6 · The Human Camera · Making generated footage look shot

### Use it

action, anything bursting into the scene - and comedy: the snap onto a face after the wrong thing was said.

**AI note**

the word documentary carries the whole package: weight, delay, blur, late focus.

**Copy-ready prompt**

**Movement:** documentary handheld shot with a reactive snap zoom. **Start:** calm handheld frame; the subject bursts into frame. **Speed:** the camera reacts a beat late, whips toward it, snaps a fast zoom with heavy motion blur. **Framing:** overshoots the framing, corrects, finds the subject. **End:** settles on the subject, focus arriving a moment late. **Time:** real time, normal speed, no slow motion.

27

## Snorricam

Rigidly mounted on the body, facing back at the face. The face sits pinned in center frame while the entire world swings around it: we're trapped with them.

GROUP 6 · The Human Camera · Making generated footage look shot

### Use it

panic, drunkenness, a mind coming apart - and in reverse: euphoria, the winning run.

**AI note**

the word rigidly matters - without it you get a handheld shot of a face, not a snorricam.

**Copy-ready prompt**

**Movement:** snorricam shot, camera rigidly mounted on her body, facing her. **Start:** already locked to her body as she moves on frame one. **Speed:** repeats every lurch and stumble she makes. **Framing:** her face locked centered, the background swinging and rotating around her. **End:** she stops; the world settles around her face. **Time:** real time, normal speed, no slow motion.

28

## Crane Up / Crane Down

A long arm lifts the camera over the scene, eyes still on the person below.
Up: the place swallows them - how films end. Down: the camera picks a story
out of the world - how films begin.

GROUP 7 · The Air · The camera leaves the ground

**Use it**

endings, openings, and any moment one life should meet the scale of the
world around it.

**AI note**

"keep her in frame as the camera climbs" is the line that makes
it a crane and not a fly-away.

**Copy-ready prompt**

Movement: crane up from her, rising and pulling away on a long arm.
Start: locked frame at eye level, then ease into the rise. Speed:
slow and steady, gathering height. Framing: keep her in frame as the
camera climbs; she stays in place while the environment grows around
her. End: settle on the wide high frame and hold. Time: real time,
normal speed, no slow motion.

29

## Drone Shot

Free flight, no anchor. Where the crane rises over a scene, the drone owns the whole map.

GROUP 7 · The Air · The camera leaves the ground

Use it

geography, scale, travel - the shot that tells the audience where this story lives.

AI note

give the flight a line to follow - a road, a river, a coastline - or the drone wanders.

Copy-ready prompt

**Movement:** aerial drone shot flying forward over the coastline. **Start:** already in flight on frame one. **Speed:** smooth, constant. **Framing:** constant altitude, horizon level, the road below leading toward the city in the distance. **End:** the flight continues past the end of the clip. **Time:** real time, normal speed, no slow motion.

30

## Fly-Through

Through an opening - a window, a doorway, a gap - and out into another space. Two worlds connected in one breath, no cut.

GROUP 7 · The Air · The camera leaves the ground

**Use it**

linking the establishing shot and the scene inside it; outside becomes inside.

**AI note**

the opening must be fully crossed - half-passed boundaries are the most common fly-through failure.

**Copy-ready prompt**

**Movement:** the camera flies through the open window into the apartment. **Start:** approaching the window from outside, already in motion. **Speed:** smooth continuous path, no pause at the boundary. **Framing:** the window frame passes fully around the lens. **End:** settle on the man at the desk inside and hold. **Time:** real time, normal speed, no slow motion.

31

## FPV Dive

The racing drone. It tips over the edge and falls, facade rushing past, pulls out at the last moment. The horizon tilts the whole way - the frame flies the way a body would feel it.

GROUP 7 · The Air · The camera leaves the ground

### Use it

adrenaline: the drop, the pursuit, routes no camera should survive.

**AI note**

the tilting horizon is the signature - a level FPV is just a fast drone.

**Copy-ready prompt**

Movement: FPV drone shot diving over the edge of the rooftop. Start: already in fast flight, tipping over the edge on frame one. Speed: accelerating through the dive. Framing: horizon tilting and swinging through the turns, facade rushing past. End: pulls up above the street at the last moment and keeps flying. Time: real time, normal speed, no slow motion.

32

## Dolly Zoom

Dolly and zoom at once, in opposite directions. On the subject they cancel out - same size in frame - while the background takes the full hit and stretches or collapses.

GROUP 8 · The Impossible · Five of these six, no physical camera can do at all

### Use it

the moment reality shifts: the diagnosis, the betrayal, the realization. Needs a background with depth - flat background, no effect.

### AI note

"keep her exact size constant" is the anchor line - it's what forces the model to run both motions.

### Copy-ready prompt

**Movement**: dolly zoom - the camera dollies in while the lens zooms out. **Start**: locked frame, then both motions begin together. **Speed**: slow, perfectly synchronized. **Framing**: keep her exact size constant in the frame; the corridor stretching and compressing behind her. **End**: the background reaches full distortion; hold on her unchanged face. **Time**: real time, normal speed, no slow motion.

33

## Macro Exit

The lens opens where no camera fits - inside the mechanism, the drop, the fabric - and travels outward until the tiny world turns out to be part of the big one.

GROUP 8 · The Impossible · Five of these six, no physical camera can do at all

Use it

scale shock; for a product, there is no stronger opening than starting inside the thing you're selling.

AI note

one clear micro starting point, one clear world payoff - vague transitions lose the audience between scales.

Copy-ready prompt

Movement: the camera starts inside the watch mechanism at macro scale and travels outward. Start: already gliding between the gears on frame one. Speed: steady, continuous, one unbroken move. Framing: passes through the gears, exits the case, keeps pulling back. End: the watch revealed on a wrist, the person wearing it entering the frame; settle and hold. Time: real time, normal speed, no slow motion.

34

## Probe Lens Shot

The camera stays tiny and flies through spaces nothing could ever film: the keyhole, the strings, the engine.

GROUP 8 · The Impossible · Five of these six, no physical camera can do at all

### Use it

technical wonder, tactile exploration, impossible access. One clear path beats three clever ones.

### AI note

textured environments help - a vague route turns into abstract noise.

### Copy-ready prompt

Movement: probe lens shot, the camera flies through the keyhole into the room. Start: approaching the keyhole from outside, already in motion. Speed: smooth continuous forward glide, macro scale. Framing: in at one point, through, out at the other - one readable route. End: settle on the scene inside and hold. Time: real time, normal speed, no slow motion.

35

## Bullet Time

The world freezes; the camera doesn't. It keeps traveling through the frozen moment, circling it from angles time never gives you.

GROUP 8 · The Impossible · Five of these six, no physical camera can do at all

### Use it

the one decisive instant: the impact, the leap, the collision.

**AI note**

the freeze must be total. One drifting element breaks the entire illusion.

**Copy-ready prompt**

**Movement:** bullet time - the camera orbits through the frozen scene. **Start:** the action freezes completely mid-moment, the splash suspended in the air; then the camera begins its path. **Speed:** smooth, deliberate travel through the stillness. **Framing:** the frozen subject centered, every droplet holding its place. **End:** the camera completes its path and holds; the world stays frozen. **Time:** the world is frozen - only the camera moves.

36

## Gravity Roll

Along the floor, up onto the wall, onto the ceiling - the room turns over while the camera keeps moving forward. Gravity becomes optional.

GROUP 8 · The Impossible · Five of these six, no physical camera can do at all

**Use it**

when the world stops being reliable: a dream, a memory coming apart, a mind losing its footing.

**AI note**

the environment needs clear geometry - corridors and rooms work; open landscapes lose the roll.

**Copy-ready prompt**

Movement: the camera travels forward along the floor, rolls up onto the wall and then onto the ceiling. Start: a level forward glide on frame one, then the roll begins. Speed: continuous forward motion through the entire rotation. Framing: the room rotating around the lens, geometry staying readable. End: level out on the ceiling, the room upside down; hold. Time: real time, normal speed, no slow motion.

37

## Infinite Zoom

The camera dives into the frame and never stops: world after world, no cuts, each one hiding inside the last.

GROUP 8 · The Impossible · Five of these six, no physical camera can do at all

### Use it

dreams, falling into a memory, any transition where one reality opens into another.

**AI note**

two worlds per clip maximum - chain clips for longer dives, stitching inside the darkest frame.

**Copy-ready prompt**

Movement: infinite zoom, the camera dives continuously into her eye. Start: a slow push toward her face that never decelerates. Speed: constant, seamless, accelerating slightly as each world opens. Framing: her eye opens into a night city, the city opens into the next scene. End: the dive continues past the end of the clip, no landing. Time: seamless continuous motion, no cuts.

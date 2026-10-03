# Story, script and planning motion

A film that looks extraordinary and means nothing is the most common AI film. Tools removed the production barrier, not the storytelling one - which means story is now the only thing separating work that holds attention from work that gets scrolled.

## Contents
- [What AI changes, and what it does not](#what-ai-changes-and-what-it-does-not)
- [Structure for short AI films](#structure-for-short-ai-films)
- [Writing the script with a chat model](#writing-the-script-with-a-chat-model)
- [Dialogue that survives AI generation](#dialogue-that-survives-ai-generation)
- [Planning motion](#planning-motion)
- [Breaking the script into shots](#breaking-the-script-into-shots)

---

## What AI changes, and what it does not

Removed: crew, locations, actors, equipment, insurance, schedules, and most of the budget. A sequence that needed a unit of thirty people can be built by one person in an afternoon.

Unchanged: the audience's patience. They still need a reason to care in the first few seconds, a situation they can read instantly, and a payoff. Think like a director, not a generator - a generator asks for a good-looking shot; a director decides what the audience must understand in this frame and where the camera has to stand to deliver it.

The practical consequence for AI specifically: **your shots are short and expensive to redo, so the writing has to be decided before generation.** Improvising a film inside a video model is the most expensive way to work that exists.

---

## Structure for short AI films

### The compressed three-act (60-180 seconds)
| Beat | Share | Job |
|---|---|---|
| Cold open | first 10-15% | Drop the audience mid-situation. No establishing preamble, no explanation |
| Want | next 20% | One character wants one thing, made visible |
| Obstacle | middle 40% | Escalation, with a turn - the plan fails, the stakes rise, someone lies |
| Payoff | final 20% | The thing resolves, reverses or lands a punchline |
| Hold | last 2 seconds | A frame worth holding. Short films almost always cut one beat too late |

### The scene-as-unit approach
A short AI film is usually three to six scenes. Each scene has a location (which means a master plate), a time (which means a sun position), and a reason to exist. If you cannot say what changes by the end of a scene, cut the scene - it is costing you twenty generations for nothing.

### Patterns that work well in AI short form
- **Two characters, one disagreement.** Cheap to build - two passports, one location - and dialogue carries it.
- **A journey with a destination stated early.** "Sunset. Under the bridge." Now every shot has tension because the audience knows where this is going.
- **An escalating set of small events.** Each shot tops the last; no complex staging needed.
- **A single unbroken take.** Comedy and tension both live in refusing to cut. A 20-second one-take is often stronger than five cuts, and it is one generation instead of five.
- **A world reveal.** The story is the place; the character is the excuse to tour it.

### What to avoid
- Crowd scenes and complex choreography - models invent extra people and duplicate limbs.
- Plot that depends on a face doing something subtle for four seconds in a wide shot.
- Anything requiring a prop to be in exactly the right hand across six shots unless you have an object passport for it.
- Voiceover explaining what we are watching.

---

## Writing the script with a chat model

Brief with context, goal, details and output format, then push back on the first draft. Useful asks:

> You are a screenwriter working in short form. Premise: [one line]. Two characters: [who they are and what each wants]. One location: [where]. Write it as 4 scenes, under 90 seconds total, dialogue-led, with no voiceover and no exposition. Every line has to sound like something a person would actually say out loud. End on a visual beat, not a line.

> Here is my script. Be blunt: where does it sag, which line is doing no work, where am I explaining instead of showing, and what would a director cut? Then give me a tightened version two beats shorter.

> Convert this script into a shot list: shot number, duration in seconds, scene, location, which characters and objects appear, what happens, and what moves. Keep each shot under 20 seconds and give every shot one purpose.

> For each shot in this list, tell me which reference images it needs and in what order.

The last two turn writing into production planning, which is the handover point to the shot prompts.

---

## Dialogue that survives AI generation

1. **Short lines.** A line that takes more than about three seconds to say will be rushed by the model. Two short lines beat one long one.
2. **If it would not sound normal said out loud, it will not sync.** Read everything aloud. Written-sounding dialogue produces mime.
3. **Punctuate for breath.** Commas and ellipses tell the model where to pause; unpunctuated text gets read like a label.
4. **Leave silence.** "Do not rush the dialogue. Leave silence between lines" in the prompt is what makes an exchange feel like people talking rather than lines being delivered.
5. **One speaker per beat**, named explicitly, with the others forbidden from mouthing. This single instruction fixes the most common AI dialogue failure.
6. **Off-screen lines are a gift.** A character speaking from off-screen needs no lip-sync at all, so the model spends its effort on the listener's face - which is usually where the drama is anyway.
7. **Write the subtext in the prompt, not in the line.** "Flat and dry, chewing between words" and "a man taking a hit and covering it" direct the performance; the line itself can stay plain.
8. **Accent locks the voice.** Choosing an accent narrows the model's voice pool, which is what makes the same character sound the same twice. Keep the voice blueprint identical in every prompt for that character - see `ai-video-prompting/references/voice-and-sound.md`.

---

## Planning motion

Decide, per shot, what moves. There are only four candidates, and the best shots usually pick one or two:

| What moves | Use it when |
|---|---|
| The subject | The story beat is physical - an entrance, a reach, a fall, a ride |
| The camera | The audience needs to be moved through the space or brought closer |
| The environment | Wind, rain, dust, steam, traffic, fabric - the layer that makes a frame feel alive even in a static shot |
| Nothing | A held frame. Needed more often than people think, and free |

Rhythm matters more than individual moves. A film where every shot pushes in reads as restless; a film of locked frames reads as dead. Plan the sequence as contrast:

- A long static cold open - the audience settles and reads the world.
- A drop or a sudden move - the first camera move in a film lands hardest.
- Escalation - faster cuts, bigger moves, a chase or a confrontation.
- A held final frame - let the ending breathe.

Two AI-specific rules:
- **Background life is part of motion planning.** Add the instruction that secondary characters never freeze: weight shifting, hair and clothes in the breeze, idle business. Without it, anyone not in the action becomes a statue and the shot dies.
- **State what does not move.** Parked cars roll, bikes drift, cameras float. The negatives block is where motion planning actually gets enforced.

Camera-move vocabulary, with six slots each, is in `ai-cinematography/references/camera-moves-catalogue.md`.

---

## Breaking the script into shots

For each shot, decide and write down:

| Field | Example |
|---|---|
| Number and duration | Shot 04, 20s |
| Scene | Scene 2, the whole street |
| What happens | He leaves the house mid-phone-call and walks out onto the street |
| Characters and objects | Papa Doc, brick phone, his house, the street |
| References needed, in order | @image1 character, @image2 phone, @image3 house, @image4 street |
| Camera | 35mm, chest height, shoulder-mounted, walking backwards at his pace |
| What moves | Subject walks; camera retreats; parallax on the near palm |
| Dialogue | Four lines, each under three seconds |
| One take or cuts | One unbroken take - the comedy lives in never cutting it |

Durations shape the build: a film of 72 generations is normal, and the shot list is what stops that becoming 150. Favour fewer, longer takes where the performance can carry; use short 4-6 second shots for inserts, reactions and transitions.

Once the list exists, the production bible follows directly from it: every character named needs a passport, every location needs a master plate, every recurring object needs an object sheet. Count them before starting - that count is the real cost of the film.

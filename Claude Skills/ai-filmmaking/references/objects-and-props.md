# Object passports: vehicles, props and anything that recurs

You need to protect the objects. A viewer will not consciously notice that the bat got longer between shots - but they will stop believing the shot. Any object appearing in more than one scene needs an object passport.

## Contents
- [The object passport prompt](#the-object-passport-prompt)
- [The three slots](#the-three-slots)
- [Object state sheets](#object-state-sheets)
- [What to lock across all objects](#what-to-lock-across-all-objects)
- [Which objects actually need one](#which-objects-actually-need-one)

---

## The object passport prompt

```
Photorealistic object reference sheet on one seamless pale grey studio background, arranged as a
clean two-row grid. Product photography, 85mm lens, soft even diffused studio light from above and
slightly front, gentle contact shadow under the object, no harsh reflections, neutral colour,
razor-sharp focus, high-end catalogue quality.

TOP ROW - six orthographic views of the same object, evenly spaced, identical scale, each with a
small uppercase sans-serif label beneath:
FRONT / FRONT 3-4 LEFT / LEFT SIDE / RIGHT SIDE / REAR 3-4 RIGHT / REAR

BOTTOM ROW - five macro detail panels, each labelled, showing the parts that make this object
recognisable: [name the five details that matter for your object - for example logo, seam,
hardware, texture, worn edge]

OBJECT - [what it is, its exact material and finish, colour, scale relative to a human, condition
and wear, any marking or logo and its exact placement]

Identical object, identical finish and identical lighting in every panel. Nothing else in frame.
No people, no props, no environment, no background scenery.

Avoid: dramatic rim light, coloured gels, reflections of a studio, floating shadowless object,
plastic CGI look.
```

4:3 suits this layout better than 16:9, because the two rows need vertical room.

---

## The three slots

### The object
What it is, what it is made of, its size relative to a person, its condition. **Wear and use matter more than shine** - a brand-new object always looks like a render. "Matte dark-green scuffed frame, black parts, four pegs" is a real bike; "sleek modern BMX" is a product render.

### Five details
Name the five macro panels this object needs. The model will not guess what matters to you:

| Object | Its five |
|---|---|
| Bike | Bars, weld, crank, wheel, saddle |
| Ring | Face, setting, shoulder, inner band, hallmark |
| Car | Badge, wheel, headlight, panel gap, interior stitch |
| Boombox | Speaker grille, tuner dial, handle, logo plate, worn corner |
| Jacket | Chest logo, cuff, zip pull, seam, hem |

### Markings
Logo, number, lettering, and exactly where they sit. This is what lets a viewer recognise the object in a shot faster than its shape does - and it is how a crew's identity carries onto their possessions (see `cast-and-wardrobe.md`).

---

## Object state sheets

When the same object appears in a second condition - repainted, reconfigured, damaged, fitted differently - do not write a new object. Reference the base passport and change only the state.

```
The same object as in the reference sheet, in a different state.

KEEP IDENTICAL - the sheet layout, the seamless pale grey background, the soft even light, the
contact shadow, the camera angles, the scale, the position and style of the labels.

WHAT CHANGES - [the new state: new paint, new material, new configuration, new fittings]

WHAT MUST NOT CHANGE - [the geometry, proportions and identifying details that prove it is still
the same object]

Both sheets must be able to sit side by side and read as one object photographed twice, not as two
objects.
```

The side-by-side test is the whole point: if the two sheets look like two objects, the audience will read them as two objects.

---

## What to lock across all objects

### Background and light
The same seamless pale grey and the same soft light on every object in the film. A different background turns a set of passports into a set of borrowed pictures, and the model starts treating them as different worlds.

### Scale
An object has to look its real size. A ring and a car are shot the same way, but they must never end up the same height in frame. State scale relative to a human in the OBJECT slot - "about the length of a phone", "roughly waist height", "fills two parking spaces".

### Wear
Decide a condition and keep it. An object that is scuffed in shot three and pristine in shot seven reads as a continuity error even when nobody can say why.

---

## Which objects actually need one

Build a passport when any of these is true:

- It appears in more than one shot.
- It is held, worn or ridden by a character.
- It carries a marking the audience is meant to recognise.
- It is the subject of an insert or close-up.
- It is a vehicle. Vehicles are the single most common continuity failure, because models redesign cars freely.

Skip the passport for set dressing that appears once and is never the subject - a parked neighbourhood car in depth, a bin, a bench. For those, describe them in the location plate instead and add the negative that keeps them inert:

> Ordinary neighbourhood cars are parked along the kerbs - they are scenery only, nobody is in them and none of them ever move.

That line, or something like it, belongs in nearly every exterior shot prompt. Models love to make vehicles drive.

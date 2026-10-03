# UGC Bootcamp — notes and Claude skills

Course notes from the AI Video Bootcamp, plus **nine Claude skills** built from them so the method
is usable while working rather than only readable.

The skills are the point of this repo. The phase folders are the source material they were derived
from, kept so anything in a skill can be traced back and checked.

---

## The skills

Nine skills in [`Claude Skills/`](Claude%20Skills/). Each is a `SKILL.md` plus reference files that
load only when needed, so they cost almost nothing until a task actually calls for one.

| Skill | What it does |
|---|---|
| [`ai-creator-workflow`](Claude%20Skills/ai-creator-workflow) | The six-step process behind every piece: idea → chat → image → refine → video → edit and post. Node/flow pipelines, batching, model choice per stage, and the quality gates that stop wasted credits. Also routes a job to the right skill below. |
| [`ai-image-prompting`](Claude%20Skills/ai-image-prompting) | Still-image prompts via the six-part method (subject, environment, camera, lighting, mood, style), realism cues, the cinematic-vs-phone mode split, and a diagnostic table for output that looks fake, flat or plastic. |
| [`ai-cinematography`](Claude%20Skills/ai-cinematography) | The shared craft layer: light logic, camera angle, shot size, lens, depth and composition, colour grade, and 67 camera moves in a six-slot format. The other skills borrow these blocks instead of redefining them. |
| [`ai-video-prompting`](Claude%20Skills/ai-video-prompting) | Motion prompts: input types, timed sequences, multi-shot cuts, dialogue and lip-sync, consistent character voices, sound design, and the post-generation realism pass. |
| [`ai-avatar-builder`](Claude%20Skills/ai-avatar-builder) | A recurring person who stays the same across outfits, locations and products: persona, base prompt, realism review, character passports, new scenes, product-in-hand with label lock. |
| [`ai-filmmaking`](Claude%20Skills/ai-filmmaking) | Multi-shot films: story and script, cast / location / object passports, one locked visual DNA, the twelve-block shot prompt, and the continuity checks that hold a world together across dozens of generations. |
| [`ugc-ad-creator`](Claude%20Skills/ugc-ad-creator) | Ads from a product brief: awareness levels, 16 script frameworks, a hook library, timestamped scripts, shot-by-shot production blueprints, and four ad formats (UGC selfie, podcast, 2D animation, claymation). |
| [`ai-clone-yourself`](Claude%20Skills/ai-clone-yourself) | Cloning a real person: the capture recording that trains a good clone, voice cloning, clone-optimised scripts, the B-roll editing method, deploying one clone across many jobs. |
| [`viral-short-form`](Claude%20Skills/viral-short-form) | Growth: platform choice and branding, hook and retention engineering, posting cadence and upload settings, engagement tactics, account health, and how to deconstruct and clone any viral format. |

### How they fit together

```
                          ai-creator-workflow          (process + routing)
                                   |
        +--------------------+-----+------+--------------------+
        |                    |            |                    |
 ai-image-prompting   ai-video-prompting  |             viral-short-form
        |                    |            |                    (distribution)
        +---------+----------+            |
                  |                       |
          ai-cinematography         deliverable skills:
          (light, camera, depth,    ai-avatar-builder
           grade, movement)         ai-filmmaking
                                    ugc-ad-creator
                                    ai-clone-yourself
```

Lighting and camera live in `ai-cinematography` once rather than being duplicated across four
skills — every other skill asks it for the camera, light and grade lines it needs.

---

## Installing

### Claude Code (any project on your machine)

```bash
git clone https://github.com/InshaKhan6593/ugc-bootcamp.git
cp -r ugc-bootcamp/"Claude Skills"/* ~/.claude/skills/
```

On Windows PowerShell:

```powershell
Copy-Item -Recurse "ugc-bootcamp\Claude Skills\*" "$env:USERPROFILE\.claude\skills\"
```

Installed at user scope they load in every project, not just one. **Keep all nine together** — they
cross-reference each other by sibling path (for example `ai-cinematography/references/lighting.md`),
so removing one breaks pointers in the others.

### claude.ai

Pre-built bundles are in [`Claude Skills/_packaged/`](Claude%20Skills/_packaged). Upload a `.skill`
file under Settings → Capabilities → Skills.

---

## Source material

| Folder | Contents |
|---|---|
| `Phase 2 - AI Creator Foundations` | Tools, models, AI chat technique, the creator workflow, the six-part prompt framework |
| `Phase 3 - AI Images` | Image basics, avatars, realism, editing, depth, lighting, camera, prompt banks, upscaling |
| `Phase 4 - AI Videos` | Video basics, model comparison, camera movement, lip-sync, motion control, voices, sound, removing the AI look |
| `Phase 5 - AI Advertising & UGC` | Ad strategy and psychology, avatar ads, a full shot-by-shot short film build, podcast / 2D / claymation formats, scriptwriting frameworks |
| `Phase 6 - Advanced Flows` | Node-based pipelines, the flows toolkit, storyboard and gallery nodes |
| `Phase 7 - Social Media & Going Viral` | Platform choice, virality, engagement, posting settings, viral niches and a prompt pack |
| `Phase 8 - AI Filmmaking` | Storytelling, planning motion, building short films |
| `Phase 9 - Clone Yourself` | Face and voice cloning, scripting for clones, deployment and monetisation |

Lesson markdown references images in sibling `*_images/` folders, so the guides read correctly
offline.

---

## Notes

- Model names, platform settings and rankings are a **late-2026 snapshot**. The reasoning holds;
  verify specifics before spending money on them.
- The skills apply the method tool-agnostically. Where course material names a particular app, the
  skills teach the principle instead of pushing a platform.
- Course material is the property of its author and is kept here as personal study notes.

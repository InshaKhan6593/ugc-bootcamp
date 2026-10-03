# UGC Bootcamp Skills

Nine Claude skills distilled from the AI Video Bootcamp course material in this folder's sibling
directories (Phases 2-9). This directory is the **source of truth**; the installed copies live in
`~/.claude/skills/`.

## The set

| Skill | Covers | Course source |
|---|---|---|
| `ai-creator-workflow` | The six-step process (idea, chat, image, refine, video, edit), node/flow pipelines, batching, model choice per stage, quality gates. Also the router to the other eight. | Phase 2, Phase 6 |
| `ai-image-prompting` | Still-image prompts: the six-part framework, realism, cinematic vs phone mode, reference instructions, diagnosing fake-looking output, 70+ tested prompts. | Phase 2, Phase 3 |
| `ai-cinematography` | The shared craft layer: light logic, camera angle / shot size / lens, depth and composition, colour grade, and 67 camera moves in the six-slot format. | Phase 3 (10, 11, 12), Phase 4 (06) |
| `ai-video-prompting` | Motion prompts, input types, timed sequences, multi-shot cuts, dialogue and lip-sync, voice blueprints, sound, motion control, the realism pass. | Phase 4 |
| `ai-avatar-builder` | A recurring person: persona, base prompt, realism review, character passports, new scenes, product-in-hand with label lock, content library. | Phase 3 (03-06), Phase 5 |
| `ai-filmmaking` | Multi-shot films: story and script, cast / location / object passports, visual DNA, the twelve-block shot prompt, continuity and assembly. | Phase 8, Phase 5 (05) |
| `ugc-ad-creator` | Ads: awareness levels, 16 script frameworks, hook library, timestamped scripts, production blueprints, four ad formats. | Phase 5, Phase 7 |
| `ai-clone-yourself` | Cloning a real person: capture recording, voice clone, clone-optimised scripts, B-roll editing, one clone many jobs, monetisation and positioning. | Phase 9 |
| `viral-short-form` | Growth: platform and branding, hooks and retention, posting and upload settings, engagement tactics, account health, cloning viral niches. | Phase 7 |

## How they fit together

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

`ai-cinematography` is the craft layer the others borrow from, which is why lighting and camera
material lives there once rather than being duplicated in four skills.

## Reinstalling after an edit

Edit the files here, then copy each skill directory into `~/.claude/skills/`. The skills
cross-reference each other by path (for example `ai-cinematography/references/lighting.md`), so keep
all nine installed side by side in the same directory.

## Notes

- Model names, platform settings and rankings in these skills are a late-2026 snapshot from the
  course. The reasoning holds; verify specifics before spending money on them.
- Precedence against overlapping platform skills (`higgsfield*`, `ugc-ad-studio`, `nim*`) is set in
  `~/.claude/CLAUDE.md`: bootcamp skills decide the creative content, tool skills execute it.
- Original course material - transcripts, guides, prompt banks, images - stays in the Phase folders
  and is the reference of record if anything here needs checking.

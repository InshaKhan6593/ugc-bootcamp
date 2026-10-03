# Flows and nodes: building the pipeline instead of the piece

A flow is a visual canvas where each block (a node) does one job and connections carry one node's output into the next. Instead of generating an image, downloading it, re-uploading it to a video tool and losing track of which version you used, the image node feeds the video node directly and the image becomes the start frame automatically.

The shift this creates: once a flow works, it is a template. You stop starting from an empty box and start from a machine you already built.

## Contents
- [Canvas basics](#canvas-basics)
- [Running a flow](#running-a-flow)
- [The nodes](#the-nodes)
- [Storyboard: the node that solves "what are my next five shots"](#storyboard-the-node-that-solves-what-are-my-next-five-shots)
- [Galleries as reference banks](#galleries-as-reference-banks)
- [Worked pipelines](#worked-pipelines)
- [Flow discipline](#flow-discipline)

---

## Canvas basics

- Place nodes from the sidebar; drag to position; resize from the corner.
- Connect by dragging a connector line from one node's output to another node's input. Remove a connection by clicking the line or its X.
- Drag images or videos in from the desktop (or right-click to upload). They sit as inspiration until you convert them to nodes, at which point they behave like any generated asset - so good work made elsewhere can enter the pipeline.
- Shift-select to move groups. Use centre to find yourself again. Clear wipes the canvas, so only use it to start fresh.
- Anything available in the main studio is available in a flow. These are the same tools, wired together, not cut-down versions.

## Running a flow

| Mode | When to use it |
|---|---|
| Single node | While testing. Generate the image first and check it before committing to the video that depends on it |
| Run flow | Once the chain is trusted. It resolves dependency order - a video node waits for its image node to finish, then takes the result |
| Rerun selection | Regenerate a subset without rebuilding |
| Stop | Cancel mid-run when you can already see it is going wrong |

Cost is calculated from the models and settings on the canvas, so a chain of expensive nodes run blind is the fastest way to waste a budget. Test one node, fix the prompt, then run the chain.

## The nodes

| Node | What it is for | Practical notes |
|---|---|---|
| Image generation | Create stills from a prompt | The foundation of nearly every flow - product shots, characters, scenes |
| Video generation | Animate an image or generate from text | Accepts a start frame from an image node; some models accept start and end frames |
| Audio generation | SFX, ambience, character voices, music | The layer most people skip; it is half of why a finished clip feels alive |
| Prompt | A text box that feeds other nodes | One prompt driving three image nodes is how you test a concept across models. Edits flow one way only: changing the prompt node updates the generators, but editing a generator does not flow back |
| Storyboard | Turns one image into a set of continuation shots | See below |
| Angles | More framings of the same subject | Use when you like a shot and want coverage of it, rather than new story beats |
| Upscale | 2x (1K to 2K) or 4x (1K to 4K) | Run before animating: more pixels in means a clearer clip out. Also for websites, static ads, client hero images |
| Remove background | Isolate a subject or product | Thumbnails, stickers, compositing, cutouts of a character you built |
| Image gallery | Collect, compare and store images | Also a reference bank and a batch animator - see below |
| Video gallery | Collect finished clips | Keeps a multi-shot piece together while you assemble it |

## Storyboard: the node that solves "what are my next five shots"

Most people get stuck at exactly one point: they make one good image and have no idea what the next five shots should be. The storyboard node reads a finished image and returns continuation prompts that keep the subject, style and lighting consistent while moving the idea forward.

How to use it well:

- Feed it your strongest image, not a draft. It extends whatever it is given.
- Choose how many prompts to turn into images, set aspect ratio and quality, and enhance the prompts if they read thin.
- Attach **two** references and it will build shots using both - an avatar plus a product is the obvious pairing for ads, and it will place the character with the product across several believable scenes.
- It continues a story rather than re-shooting one moment. For coverage of a single moment, use angles instead.

Examples of what it returns: a skier holding the board, sitting down, cutting through trees, fixing a binding; an influencer on a beach day reading, ordering a cocktail, taking photos, wandering off.

## Galleries as reference banks

A gallery holds many outputs in one node, which keeps a canvas readable once dozens of assets exist. Three uses beyond tidiness:

1. **Reference selection.** Connect a gallery to a video node and pick which images to use as references from a pop-up. On models that support start and end frames, the same pop-up lets you assign both.
2. **A stored bank.** Keep a gallery of locked references - passports, product plates, location plates - and pull from it instead of hunting for files.
3. **Animate all.** Generate videos from an entire gallery in one action. Storyboard into a gallery into animate-all is a complete sequence with almost no manual handling.

Convert anything back into a working node when you want to continue from it.

## Worked pipelines

### Concept to finished ad, hands-off middle
1. Upload the avatar reference and the product reference; write one brief.
2. Generate a batch of images (eight is a workable number).
3. Run **angles** on the best product frame; run **storyboard** on the best character frame.
4. Send both sets into galleries.
5. **Animate all** with your chosen video model.
6. Generate music on an audio node.
7. Download, assemble in an editor: transitions, tighter pacing, stronger shot order, music bed.

The creative work is the brief and the edit. The middle is machinery - which is the point.

### Testing one concept across three models
Prompt node - three image nodes on different models - one gallery. Change the prompt node once and all three regenerate, so you are comparing models rather than comparing prompts.

### Still to hero clip
Image node - upscale - video node - audio node for SFX. Four nodes, and the upscale is the one people skip and then wonder why the clip is soft.

## Flow discipline

- **Test a node before you trust a chain.** This is the entire cost-control strategy.
- **Keep one source of truth for prompts.** A prompt node beats pasting the same text into five places.
- **Name and park your locked references** in a gallery so they are never regenerated by accident.
- **Save working flows as templates.** A flow that produced a good ad will produce the next one.
- **The flow does not replace the gates.** Check the image before animating, even when the canvas makes it easy not to.

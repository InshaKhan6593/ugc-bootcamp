# 02 - Flows Overview - Transcript

> Source: Transcript.pdf (original PDF in Downloads/AI_Video_Bootcamp_Phases_2-9.zip)

<!-- page 1 -->

# AI VIDEO BOOTCAMP

## Flows Overview

### Lesson Transcript

0:00 Lesson one. Water flows and nodes. Okay, so first we need to make flows feel simple. Really. It's just a visual way of connecting steps together.

0:09 Think of it like a big creative whiteboard. On that whiteboard, you place blocks. These blocks are called nodes. Each node does one job.

0:17 One node might generate an image. Another node might generate a video. Another might collect your images into a gallery. Then, instead of doing every task separately, you connect the nodes together with connector lines.

0:34 Once they're connected, the output from one node can automatically move into the next node in a sequence. To connect two nodes together, you just need to click and drag the connector lines from the top corner of the node and attach to the other node like this.

0:47 So for example, you could have an image generator node connected to a video generator node. The image node creates the image, and that image automatically becomes the start frame for the video node.

0:58 You don't have to be downloading it, re-uploading it, dragging it around your computer, or losing track of what you used.

1:04 It just flows from one step to the next. Let's go over some of the basics of using the canvas. So when you first open flows, you'll see a completely empty canvas.

1:13 This is your workspace. You can zoom in or out by using your mouse scroll wheel or the zoom button in the top right corner.

1:20 Move around by clicking and dragging your screen and start placing nodes wherever you want by clicking on them in the sidebar or dragging them onto the canvas.

1:28 If you click them, they will just appear on the screen in the middle. You can also drag and drop images or videos into your canvas from your desktop.

1:37 Just grab them and then drop them in. Alternatively, you can right-click and select Upload Image or Video. These images or videos will then appear on the canvas.

1:46 You can either leave them as inspiration, like this, to give you some visual references, or you can convert them to nodes by pressing the convert button that will pop up.

1:56 If you convert to a node, they will turn into fully functional nodes that can then be used and connected

<!-- page 2 -->

to other nodes.

2:02 This is good because it means if you've made an awesome image or video somewhere else that you want to use on the canvas, you can just drag it in and use it.

2:10 Now if you want to resize nodes, you can drag the resize button in the bottom left. you can make them whatever size you want.

2:17 To view an image in full size you can click on it to expand. You can delete any nodes you don't want anymore by hitting the delete button up here.

2:29 If you lose track of where you are on the canvas, you can hit the center button and that will return you right back to the middle.

2:35 You can also clear and delete the entire canvas with the clear button, but obviously only do that if you want to start from scratch.

2:43 You can remove connector lines by either clicking on them anywhere or hovering over and finding the X button. You can also move nodes around the canvas by clicking on them and dragging.

3:00 You can also press Shift and select multiple nodes at once, then drag them around together. By the way, you can do literally everything you can in studio, inside flows.

3:17 It isn't watered down versions of the tools. They're the same core tools you already used inside studio But now they can be connected together For example, if you're using an image model inside studio that same kind of image generation can happen inside flows There are two main ways to run things inside

3:34 flows the first way is to run one node at a time This is useful when you're testing something Maybe you only want to generate the image first before you commit to making a video You can run that one node, check the result, and make sure it's strong before moving forward.

3:49 The second way is RunFlow. This runs any connected workflows on your canvas, in the correct order. Flows understands dependency order.

3:57 That basically means it knows which step has to happen first. If you hit RunFlow and your video node needs an image from the image node, it won't try to generate the video before the image exists.

4:07 It will generate the image first, wait for it to finish, then pass that image into the video node, and then run the video node.

4:14 Like in this example, you set it up once, then the system follows the chain. Our software will calculate the cost based on which models and settings you have set up.

4:33 There's also a rerun selection you can do too if you want, which will basically redo all of the nodes that are on the canvas at the time.

4:46 The stop button lets you stop a flow if something's running and you want to cancel it. Once you build a flow that works, it can become a template you reuse.

4:55 That's a massive shift because instead of starting from zero every time, you start building your own creative machines. Okay, so I'll go over each one in more detail in the upcoming lessons, but let's take a

<!-- page 3 -->

look at each of the options on the node selector.

5:10 First is image generation. This is where you'll create images from scratch using a prompt. So if you want to make a product shot, a character, or anything visual, this is the node you'll start with.

5:20 Next is video generation. This is where you'll turn your ideas and images into videos. So once you've created an image, or you've uploaded something you want to animate, this is the node you'll use to bring it to life.

5:31 Then we've got For audio generation, this is for creating sound, that could be sound effects, ambience, background, audio, character voices, or anything else you need to make the final video feel more alive.

5:44 We also have 11 labs hooked up to this node. After that is the prompt node. This is basically a text box inside the flow.

5:51 You can use it to write ideas, structure your prompts, store instructions, or pass information into multiple nodes at once. It's really useful when you want to keep everything organized instead of constantly copying and pasting prompts from somewhere else.

6:04 Then we've got Storyboard. This is for planning out and continuing the next steps of the story. So instead of just making a random image or one random video, you can create a whole world from one image.

6:15 This is really useful for anything where you need the scenes to flow together properly. Next is Remove Background. This does exactly what it sounds like.

6:23 You can take an image and remove the background from it. Then there's upscale. This is used to improve the quality and resolution of an image.

6:31 So if you've generated something you like but it looks a bit blurry or not sharp enough, you can run it through the upscale node to make it cleaner and more usable.

6:40 And finally, we've got galleries. These will help to keep your canvas super tidy and organized. So that's a quick overview of the node selector.

6:49 You don't need to fully understand every single one right now because we're going to go through them properly in the next lessons.

6:54 For now, just understand that nodes are the building blocks of your workflow. And creating on a canvas like this really starts to get your imagination going and makes it way easier to map out and plan your contents journey from start to finish.

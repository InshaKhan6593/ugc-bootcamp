# 03 - Image Generators - Transcript

> Source: Transcript.pdf (original PDF in Downloads/AI_Video_Bootcamp_Phases_2-9.zip)

<!-- page 1 -->

# AI VIDEO BOOTCAMP

## Image Nodes

Lesson Transcript

0:00 Okay, so the main node inside flows is obviously the image generator and that makes sense because in all AI workflows the image is the foundation we've already talked about this earlier in the course images are cheaper, faster and easier to control them video.

0:16 If the image is bad, the video will pretty much always be bad. If the character looks fake in the image, they'll probably look even worse in motion.

0:24 So the image stage matters massively. Let's go through how everything inside the image node works. When you add an image generator node to the canvas, you'll see the same things you're used to.

0:34 A prompt area, model options, aspect ratio and quality settings. You write your prompt, choose your model, choose the size or format you want, then run it.

0:43 Everything from the prompt framework still applies. You still need to think about the subject, environment, camera details, lighting and mood when prompting for the best results.

0:52 Flows doesn't change what makes a good image prompt, it just changes what you can do with the image after it generates.

0:57 You'll also see that we have the wise enhanced option to improve the prompts you add to if required. This works the same way as it does on the rest of the site.

1:06 Now let's talk about references. Inside the image generator node, you can add reference images in two ways. The first way is the obvious way.

1:14 You upload them manually. You can drag images from your computer into the reference area or click to upload them. This is useful if you already have a product photo, a character image, a brand mood board or something you want the model to follow.

1:27 The second way is the easier way. You connect another completed image node into the image generator node. So let's say you generate a character in one node and a product in another node.

1:37 You can connect both of those images into a third image node and ask it to create an image of that same character holding that product.

1:44 This is massive for consistency and speed. At the moment, you can connect up to eight image references into a single image generator node.

1:51 And when they're connected, you'll see thumbnails on the node, so you can visually understand what's

<!-- page 2 -->

feeding into what. This is especially useful for AI influencer content, product ads, brand visuals, and any workflow where you need the same subject to appear more than once, because it's so easy now

2:07 to just connect nodes and add references. Here's another example, with four image references connected. Now, another feature that's really important is the carousel.

2:19 When you run an image generator node once, it gives you an image. But if you run it again, it doesn't delete the first image.

2:25 It adds the new image into a carousel. That means you can generate multiple versions inside the same node and flick between them.

2:33 This is such a useful detail because AI creation is rarely perfect on the first attempt. Sometimes the first image is decent, the second has better lighting, and the third has a better pose.

2:44 In a normal workflow, it's very easy to lose track of those versions. But inside the node, they stay together. This carousel is dynamic as well, so whichever image you've selected in the carousel is the one that flows downstream to the next connected node.

2:57 The image generator node also gives you quick action buttons. Once an image has generated, animate is exactly what it sounds like.

3:05 It creates a connected video generator node and loads your image as the start frame, so if you generate an image and immediately want to bring it to life, you can do that quickly.

3:15 Remove background creates a remove background node connected to your image. Then you have variations and angles. You'll see the menu pop up where you can select how many images you want to generate.

3:31 Once you hit generate, an image gallery will spawn onto the canvas to hold all of the images for you. Variations helps you explore more versions of the same idea without starting from scratch.

3:41 So if you generate an image that is close to what you want, but not perfect, variations lets you create alternative versions while keeping the same general concept.

3:50 This is useful when you like the overall direction, but you want to test different outfits, lighting, colors, etc. For example, if you run variations on an image of an influencer like this, it will add, change and replace elements while maintaining the same image.

4:04 As you can see, it changed subtle details, like her pose, outfit, and bandana color. This matters because good content usually comes from exploration.

4:15 Angles helps you generate different camera angles of the same image, which is really helpful for campaigns, product shoots, AI, influencer content, and anything where consistency matters.

4:25 Instead of having one image from one angle, you can create a wider set of shots that feel like they belong together instantly.

4:32 For example, we get these cool, different angled shots super quickly. That gives you enough variety to build a full carousel, add sequence, or social media content set without the whole thing feeling repetitive.

4:45 Here's another example of how the angles feature can be used if you're creating a short film or

<!-- page 3 -->

something, and if you click edit, the image will automatically populate in the references box, so you can just type what edits you want to happen.

4:57 For example, if I do it on this node, I can ask for the ice cream to be changed to pink and I get a great result like this.

5:08 There is also now a rerun button. This is different to the edit button, because it will basically allow you to change and recreate the initial image that was produced, including any references you had attached rather than editing the current image like the edit button does, so this is like a redo button

5:25 . So yeah, that is how image generators work in flows. You can also line up and arrange your image nodes, which really helps you to storyboard and see how the videos you are creating could play out shot by shot.

5:37 The main thing to understand here is that image nodes are usually the starting point for everything else, and nailing how to use image nodes can really speed up your workflow.

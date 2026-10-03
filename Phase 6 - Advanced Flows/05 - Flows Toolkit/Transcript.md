# 05 - Flows Toolkit - Transcript

> Source: Transcript.pdf (original PDF in Downloads/AI_Video_Bootcamp_Phases_2-9.zip)

<!-- page 1 -->

# AI VIDEO BOOTCAMP

## Flows Toolkit

### Lesson Transcript

0:00 Image video and audio nodes are the main parts of most flows, but they're not the whole system. These other nodes might seem like smaller tools at first, but they can save you a lot of time when you start building bigger workflows.

0:12 Let's start with the prompt node. A prompt node is basically a text box that can feed text into other nodes.

0:18 At first, that might not sound very exciting, but it becomes useful when you want one prompt to control multiple generators.

0:25 For example, imagine you want to test the same concept across three different image models. Instead of copying and pasting the prompt into three different image nodes, you can write the prompt once inside a prompt node and connect it to the other nodes.

0:37 If you change the text in the prompt node, the connected generators update in real time. That means the prompt node becomes the source of truth, but you can still edit the text in each node manually if needed.

0:49 This is one directional, so the changes won't flow back to the main prompt node. This is useful for testing, variations, and keeping prompts organized.

0:57 You can also use the prompt node to hold or store prompts for you so you can just grab and reuse whenever you need them.

1:04 Next, we have the upscale node. Upscaling simply means increasing the resolution or quality of an image. We talked about this earlier in the course.

1:13 If you've got an image you love and you want it to look sharper, bigger, or more professional, you can upscale it before using it somewhere important.

1:20 For example, this might be useful if the image is going on a website, a presentation, a static ad, or if you want the video model to have more detail to work with.

1:28 Having a higher resolution in the image means that there is more pixels, so the video outcome will be way clearer after animating.

1:36 There's a few options. Two times turns a 1K resolution image into a 2K resolution image, and four times turns a 1K into a 4K resolution image.

1:44 This is one of those steps that's easy to skip, but it can make a real difference, especially when you're

<!-- page 2 -->

working with hero images or polished visuals for a client.

1:52 Then we have the Remove Background node. This does exactly what it sounds like. You connect an image, run the node, and it removes the background from the subject or object.

2:02 This is useful for product shots, thumbnails, stickers, and anything where you want to isolate a person, product or object. For example, if you created a character and want to use them in a thumbnail design, remove the background and you've got a cutout ready to work with.

2:16 It's a simple tool but very practical. Now let's talk about the storyboard node because this one is much more powerful than it might seem.

2:24 The storyboard node takes an image and creates a set of continuation prompts from it. So for example, let's say you've got one strong image of a character.

2:32 Maybe it's an AI influencer and you are trying to make an ad but you aren't sure where to take the story next or what other sort of shots you could include in the ad.

2:40 You connect that image into a storyboard node and the node automatically analyzes it. Then it generates a set of prompts that continue the idea across multiple scenes while keeping the subject and style consistent.

2:52 You can then add, remove and select how many prompts you want to actually turn into images, as well as selecting the aspect ratio and quality.

3:00 You can also enhance all of the prompts if needed. Then, all you need to do is hit generate, and as you can see, an image gallery will spawn and give you perfectly consistent story continuation shots.

3:15 You can see the results here, the consistency is perfect, the lighting, camera used, the woman and animal all great, and I literally had to do no work to get great results like this, the storyboard does it all for you in minutes.

3:38 You can also attach multiple image references to a storyboard, and it will analyze and create shots using both of them.

3:45 So let's say you've been commissioned to create some shots or an advert for this skincare product. You can attach the image of your influencer and the product then analyze both and generate Here's the awesome results.

3:58 That's why we made the storyboard node because it solves the issue of not knowing what to do next A lot of beginners usually get stuck at this point in their AI workflow.

4:06 They create one nice image Then they don't know what the next five shots should be. That's why it's different than angles It doesn't just give you angles of the same shot.

4:15 It continues the story and like I said before you can use this for literally anything Okay, so let's look at some other examples.

4:23 Let's say you're working on a cinematic short film of a guy skiing. Just connect to the storyboard and let it do the work for you.

4:31 You can see it created awesome shots of him holding the board, sat down, skiing through the trees, fixing

<!-- page 3 -->

his board, etc.

4:40 Or maybe your AI influencer is having a beach day and you wonder what else you can get up to. So now she's reading a book, getting a cocktail, taking some photos, exploring.

4:50 This is exactly the type of thing that makes flows valuable for ads and content in general. Next up we have galleries.

4:57 There are image galleries and video galleries. A gallery is basically a collection or storing node. It holds multiple outputs in one place to clean up your canvas.

5:07 This is useful because flows can get messy if every single image and video is floating around separately. Galleries help you collect options, compare results, and keep related assets sets together.

5:18 An image gallery can hold multiple images, you can open the images, view them larger, and convert them back into a node if you want to keep working with them by pressing the convert button.

5:29 You can send assets into galleries by connecting them, and then the send to gallery button will appear. Here's a cool trick, so let's say you are using on the reference on a video node, and you connect an image gallery to it, you'll see this pop-up where you can then select which images in the gallery

5:51 you want to use as references, and they will be immediately ported. This also works with models that support star and end frames, so when you connect the image gallery, on the pop-up, you'll see the start frame and end frame selection areas.

6:06 This also works with normal image nodes too, This essentially means you can use image galleries as reference banks to store references if you wanted Now following on from storyboarding image galleries also have an animate all option Which is exactly what it sounds like You can take a full gallery of

6:24 images and generate videos from all of them instantly So if you wanted to you could go from storyboard to image gallery to final video outputs all in one sequence Here's an example of an advert I was working on, and I did exactly that sequence.

6:38 You can see the storyboard I made, and then animated, and the results are awesome. A video gallery works in the same way as an image gallery, but for finished video clips.

6:48 It lets you collect the videos from different nodes into one place, which is really useful when you're building a multi-shot piece.

6:56 So yeah, that is all of the tools in the toolbar covered. As time goes on and we continue to improve and expand flows, we will add more tools so we can make this even better.

7:06 And as always, I'll update the videos if we add any new features. Plus I'm always open to hear your guys feedback on anything you want to see changed or added, just shoot me a message in the school group.

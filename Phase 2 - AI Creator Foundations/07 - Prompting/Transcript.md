# 07 - Prompting - Transcript

> Source: Transcript.pdf (original PDF in Downloads/AI_Video_Bootcamp_Phases_2-9.zip)

<!-- page 1 -->

# AI VIDEO BOOTCAMP

## Prompting

Lesson Transcript

00:00 This is one of the most important lessons in the entire course, and I really mean that. By the end of this lesson, you'll be a prompt engineer, because once you understand prompting properly, AI stops feeling random.

00:11 It stops feeling like you're just typing words into a box and hoping the machine gives you something good. You start to realize that the difference between average AI content and professional looking AI content is usually not the tool, luck, or that someone has some secret model you don't have access

00:26 to. Most of the time, the difference is the instruction. The same AI model can create something that looks flat, generic, plastic, fake, boring or forgettable.

00:35 And that exact same model can create something cinematic, emotional, realistic, and scroll-stopping. The only thing that changes is how clearly you communicate what you want.

00:44 That is what prompting is. We've gone over how to talk to the AI chats in the previous lessons, but this lesson is about prompting for image and video generation.

00:52 Prompting is not just writing a description. Prompting is direction. you are directing the subject, the scene, the camera, the light, the emotion, and the final look.

01:01 The better you get at giving direction, the better your results become and the more you will get the output you want.

01:06 By the end of this lesson, you are going to understand the exact prompting framework we use inside AI Video Bootcamp, how to improve bad prompts, how to diagnose what went wrong, and how to start building your own prompt library.

01:18 Now, it's worth noting that with all of the advancements in technology And especially with prompt wise being released, prompting is getting a lot easier.

01:26 In fact, if you don't want to, you barely even have to write a video or image prompt yourself anymore due to awesome features like wise enhance.

01:34 However, it's still important that you know what a good prompt looks like and how to make one. That way you aren't using advanced tools with zero knowledge on what output you should be getting.

01:42 So what actually is a prompt? A prompt is the instruction you give to an AI model. For an image model, your prompt tells the AI what the image should look like.

<!-- page 2 -->

01:51 For a video model, your prompt tells the AI what should move, what the camera should do, and what should happen in the shot.

01:57 The less direction you give, the more the AI has to fill in the blanks, and when AI fills in the blanks, it usually chooses the most average generic version of the idea.

02:06 That is why vague prompts create vague results. Bad prompt versus better prompt. Let me show you what I mean. Bad prompt.

02:13 A cool photo of a girl. Now, this might still generate something. The AI will probably give us a decent looking person, maybe a nice background, maybe be dramatic lighting, but the problem is that nothing in that prompt gives the AI a real direction.

02:27 Who is she? Where is she? What is she doing? What's the lighting? What's the camera angle? Is this supposed to feel candid, cinematic, luxurious, emotional?

02:35 The AI has to guess everything. Now look at this version. A candid photo of a woman in her late twenties with short dark hair wearing an oversized denim jacket, sitting at the counter of a tiny ramen shop in Tokyo late at night.

02:46 Steam rises from the bowl in front of her, warm overhead light hits the side of her face. The background is softly blurred with shelves of bowls and handwritten menus, shot from across the counter like an intimate documentary photo, quiet and cozy mood, realistic 35mm film look.

03:03 That is not just longer, it is clearer. The second prompt gives the AI a subject, a location, a time of day, a light source, a camera position, background details, emotional tone and visual style.

03:14 Now the model has something to work with and this is one of the biggest lessons in prompting. A good prompt is not just a longer prompt, a good prompt is a more intentional prompt.

03:23 You can write a 200 word prompt that is still bad if it is full of random details that don't matter.

03:27 And you can write a 35 word prompt that is brilliant if every detail is specific and useful. The AVB prompt framework.

03:36 From now on, I want you to use the AVB prompt framework. This is the framework you'll use for images, video, ads, cinematic scenes, product shots, AI influences, thumbnails, UGC, and almost everything else we create in this course.

03:50 The framework has six parts, subject, environment, camera, lighting, mood, style. That is your creative compass. Whenever a prompt is not working, it is usually because one or more of these six parts is missing, weak, or unclear.

04:04 Let's break each one down properly. One, subject, who or what is in the frame. The subject is the main thing we are looking at.

04:12 For a person, don't just write a man or a woman, that gives the AI too much freedom. Instead, describe the things that visually matter.

04:19 A weak subject description would be, a man standing in a street. A stronger subject description would be, a man in his early 40s with tired eyes, short messy brown hair, light stubble, wearing a worn black

<!-- page 3 -->

leather jacket, and holding a takeaway away coffee, standing still like he's waiting for someone

04:36 . That is much better because we can actually picture him. For people, think about age, hair, clothing, expression, posture and what they are doing.

04:44 For products, think about shape, material, color, surface texture, branding style, packaging and how the product is positioned. For AI content, the subject is where control begins.

04:55 If the subject is vague, the whole output becomes vague. 2. Environment. Where is this happening? The environment is the world around the subject.

05:04 This is one of the fastest ways to make AI content feel more expensive, more realistic, and more original. A weak environment is, in a city.

05:12 A better environment is, on a narrow side street in Hong Kong at night, neon signs stack above small food stalls.

05:18 Scooters parked along the pavement, steam rising from a noodle cart, wet ground reflecting the lights. That environment does more than create a background.

05:28 It creates context. It tells us what kind of story we are in. A woman standing in a white studio feels completely different from a woman standing outside the nightclub at 1am in the rain.

05:38 A man drinking coffee in a modern office feels completely different from a man drinking coffee alone in the petrol station at 3am.

05:44 When writing in the environment, include a specific place, time of day, weather, background objects, textures and atmosphere. Not every prompt needs loads of environmental But every strong prompt needs enough context for the AI to understand the world.

05:58 3. Camera. How are we seeing it? This is where most beginners massively improve once they understand it. The camera decides how the viewer experiences the image.

06:07 A subject can look powerful, vulnerable, intimate, distant, realistic, cinematic, or awkward depending on how the camera sees them. A few useful camera directions.

06:17 Wide shot means we see the full environment. This is great for big cinematic scenes, landscapes, interiors, streets, rooms, and world-building.

06:25 Medium shot usually shows the person from the waste or chest-up. This is great for social content, portraits, UGC, interviews, and natural-looking photos.

06:34 Close-up focuses on the face, emotion, texture, eyes, and expression. This is great for drama, beauty shots, emotional scenes, and realism.

06:42 Low angle makes the subject feel powerful, heroic, intimidating, or important. High angle can make the subject feel smaller, more vulnerable, or more observed.

06:51 Over the shoulder makes the viewer feel like they are inside the scene, watching from behind another person. POV means we see through someone's eyes, which is extremely useful for immersive content.

<!-- page 4 -->

07:01 You can get a ton of camera angles in the PDF that I've attached below the video. The mistake beginners make is they describe the scene, but forget to describe how the camera sees the scene.

07:11 So the AI chooses a default camera angle, and the result often feels generic. For example, weak, a businessman in a luxury hotel lobby.

07:19 better, a medium close-up shot of a businessman sitting alone in a luxury hotel lobby, camera positioned slightly below eye level across the table, background softly blurred.

07:29 Now we know how to see it. For video, camera becomes even more important because we add movement. Instead of just saying what the camera angle is, we say what the camera does.

07:38 Examples. The camera slowly pushes in towards her face. Hand-held camera follows behind him as he walks through the market. Slow orbit around a product as light reflects across the glass, static tripod shot with only the subject moving.

07:50 We will go deeper into video prompting later, but the key thing for now is this, the camera is not a technical extra, it is one of the main reasons an image looks professional.

07:59 4. Lighting. What is the light source? Lighting is where AI content either becomes believable or falls apart. Most people write lighting like this, cinematic lighting, beautiful lighting, golden lighting.

08:11 The problem is that these describe the effect but they don't tell the AI where the light is coming from. A much better way to prompt lighting is to describe the source Instead of warm lighting, say a small warm table lamp on the left side of the frame lighting her face, instead of dramatic lighting,

08:26 say a single overhead light casting harsh shadows under his eyes, instead of blue and red lighting, say red neon from a shop sign on the right and blue police lights.

08:37 When you describe the source, direction and quality of light, the AI understands the scene far better. This is especially important for realism.

08:43 Real photos have imperfect lighting. They have uneven shadows, soft window light, street lights, car headlights, phone screens, candles and cloudy skies.

08:53 So instead of always asking for perfect cinematic lighting, start asking yourself, where is the light actually coming from? That one question will instantly improve your prompts because a lot of the fake plastic looking AIC is due to bad lighting.

09:05 We're going to go over all of this in way more detail later in the course. But this is a great starting point Five mood how should it feel now next up is mood mood is the emotional direction of the image This is not always about what we see.

09:21 It is about what the image makes us feel Two prompts can have the same subject same environment same camera and same lighting But a completely different mood for example a man sitting alone in a diner at night Peaceful and the nostalgic that feels reflective now a man sitting alone in a diner at night

09:36 tense and paranoid Same setup, totally different image, mood words guide the model's interpretation, they influence expression, color, contrast, atmosphere, framing, and even body language.

09:48 Here's a few examples of mood words. You usually only need one or two mood words, don't overload it. The

<!-- page 5 -->

mood is like the invisible thread tying the whole prompt together.

10:00 6. Style. What should the final look be? ok so style is optional and this is important to remember a lot of beginners add style words because they think it makes the prompt better but sometimes it makes the result worse if you want a realistic photo you don't always need to add loads of style sometimes

10:16 saying realistic iPhone photo is enough style is useful when you want a specific treatment examples iPhone flash photo Polaroid photo luxury fashion campaign clean studio product photography anime style Oil painting, dark fantasy style, but if you want realism, be careful with over-stylizing.

10:35 Like I said before, words like cinematic masterpiece, hyper-detailed, ultra-glossy, award-winning, perfect lighting can sometimes push the image into that fake, overly polished AI look.

10:45 This matters massively for the kind of content we create, because we don't just want pretty perfect images, we want images that feel believable.

10:53 So yeah, that's the sixth step framework that you should include in pretty much all your prompts if you want to actually guide the image models to create what you want.

11:01 Obviously, there is more things you can add and we will go over that later on, but like I said earlier, this is a great starting point and can get you better results fast.

---
layout: post
title:  "Post-Mortem"
date:   2026-06-23 12:04:40 -0400
categories: naval-battle update
---
Despite the two months of silence (give or take a few days), the battle ship game I was building for my dad is now pretty much finished! Most items on the "nice to have" list that did not make it to the final product. I expect my dad will have a few requests in the future that will require updates. There is also a minor visual bug that I find annoying that I have been unable to fix, but I doubt my dad will even notice. For now though, I am considering this project as done. It is available to play to anyone from my GitHub pages site: https://bobbywatson100.github.io/bship . Give it a try if you have a few minutes to spare!

This means it's time for me to look back on the whole thing and evaluate how things went!

### What went well
- Building the whole game loop before I did anything else was actually a good thing. I had the idea when I watched a video from a young woman vlogging her way through making her own game with Godot on YouTube (her name is [Rooi](https://www.youtube.com/@rooiwhoo), and her videos are excellent). Once I had the loop implemented, I felt it was easier to go from state to state and making sure everything was working as expected.
- Coding the AI went much better than I expected. Starting by drawing an actual flowchart helped a lot. From the flowchart, it was fairly easily to convert that into GDScript. The flowchart wasn't as complete as it should have been (the AI has plenty of room for improvement), but this whole process ended up being easier than I expected, especially considering this is not something I had coded before.
- I tested and debugged the AI in a separate scene, and that helped the process a lot. All I had to do was to click a button and let it rip. 
- Choosing to use a web export for the executable was the right choice. From a performance perspective, the game works really well (let's be honest: this is not exactly Call of Duty Modern Warfare 69 or anything approaching that). This also avoids the issue of me having to call my dad to help him install a new version over and over again. All I had to do was to add a bookmark in his browser, and I was done. Now, whenever I make a change, I just re-export from Godot and commit the changes to my GitHub.
- I may not be John Carmack, but I still have a good idea of how code works, I've written a lot of it, and having gone through a Godot tutorial or two before jumping into this project was enough to ensure I didn't struggle with GDScript itself. I found the language to be easy to read, and the documentation is actually pretty good.
- The free tier of Claude may not always be right but, for Godot at least, it was actually good at answering my questions! (The day Anthropic financially collapses, you can blame/thank me for burning a lot of tokens for free.)

### What didn't go so well
Since this was my first real, serious game development project, I expected it to be bumpy, and I was right.
- The biggest fail, I think, was 100% unavoidable: I had no idea how to build a game. Obviously. I had never done it before. And I don't know that doing more tutorials ahead of time would have fixed that. The next game project, whatever it ends up being, will be different. Some of the things I learned here will be useful, no doubt, but there will be more to learn (and fail at). There always is.
- My lack of planning was obvious. I had no idea what I was getting myself into. I ran into stupid bugs that could have been avoided with a little bit of code organization.
- I didn't really know how to use the various UI elements in Godot. I had used some of them in tutorials, but this time I had to figure it out on my own, which was trickier.
- My files are very poorly organized. That's fine for a small project like this. Anything bigger will require serious consideration.
- Taking a year-long break between my first attempt and this second one was not great either. I was able to reuse a lot of code, but I had forgotten a lot of how the original worked, and figuring it out again took longer than it should have.

### What's next?
I have a couple of ideas percolating in my head. I know I want to do something a little more complex that incorporates some 3D elements. 

My next actual project won't be gaming related though: I plan to finally go back to that font I started designing a few years ago but never finished. Designing the characters should take a few weeks. Turning them into a usable font will take significantly longer.
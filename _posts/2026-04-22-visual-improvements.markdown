---
layout: post
title:  "Visual Improvements"
date:   2026-04-22 19:04:40 -0400
categories: naval-battle update
---
For the past week and a half, I have been focusing on the visual aspect of my BattleShip game project. As I said before, I'm not a graphic designer (although I did consider reorienting my career towards that area about a decade ago, before my brain switched to "Reach Financial Independence ASAP" mode). So far, my process has basically been:

1. Look at game screen. What is the worst part?
2. Ask myself what would make this part maybe 10% better
3. Make a new asset or find a free one online, import said asset in the project, and try it
4. Look at game screen again. If the part I was working on is no longer the worst part, go to step 1

Progress has been slow, but slow progress is better than no progress.

I work from home 100% of the time, so lately I've been feeling like it's time for me to start going out more. I started last Friday by taking a day off, hopping on a train and go to Montréal for a day trip, and that was great, but also costly. I logged back into my long-neglected MeetUp account on Sunday, and found a group called Minimum Viable Ottawa. This is a group that meets every other week in a co-working space, and everybody brings their laptop to work on their own project. I thought this sounded fun, so I signed up and attended my first event yesterday, bringing my trusty M2 MacBook Air (quite possibly the best laptop I've ever owned), my graphic tablet and my old-man glasses.

The whole event lasted two hours, and time really flew by. It has been a while since that had happened to me. I talked to a few folks about my project. I also spent most of the session developing the main theme of my game, updating the main font and the secondary font (I went with a type-writer/military-looking combo), creating textures for my buttons and score panels, fixing some text-replacement issues. Overall, it was a productive session! Plus, it forced me to go downtown, which I is something I should do more often (especially since it's easy to get there by public transit from my location, so I don't even have to deal with parking and traffic). I will definitely attend again in two weeks. Bonus: I got to go to the nearby Lego Store. I was very tempted by that $500 Enterprise set...

This is what the game looks like at the moment:

![Looks better](/assets/images/bship_20260422.png)

(It's small in the screenshot, but when played in a browser it takes up the whole window.)

I tried another web export of the project, and was able to play the game in my browser with zero issue. I will probably host it on GitHub pages. Hopefully by the next update I will be able to provide a link here.

Though there is still a lot of work ahead of me on this project, I think I got over the most significant tasks. Moving forward, this is what I still have on my kanban board:

- Allow the user to change the difficulty level (the dialog box is built, I just need to display and dismiss it as required)
- Update the look of the difficulty dialog box and make it more consistent with the rest of the game
- Announce the winner on the Game Over screen
- Redo the ship sprites
- Improve the contrast between the grid and the background for low-vision players
- Create a splash screen to replace the default Godot one

Once that is done, I will show the game to my dad to gather feedback.

I also have a few nice-to-have items on my to-do list:

- Save the wins/losses in the browser's local storage (which I think is supported by Godot), keep track of some fun stats like average hits needed to win, and add a statistics screen to display that
- Create multiple sprites for hits and misses and assign them at random to include more visual variety
- Add a few sound effects

With my sleep having improved significantly over the past two weeks and me being low on tasks as work (which happens every year around this time), I think I can wrap this project up in the coming weeks. I may write one more of these journals, before I start working on a post-mortem.

Fun fact: I have no idea how many times I heard the name "Claude" last night during the co-working session. That number has to be pretty high.
---
layout: post
title:  "Opponent AI Progress"
date:   2026-04-09 19:04:40 -0400
categories: naval-battle update
---
Things at work have slowed down significantly, which means I now have more brain power outside of business hours available to move forward on my project! I have now implemented the two difficulty levels of the opponent. The first one just picks cells randomly with no strategy whatsoever. The second one, once it has a hit, will try to poke around to find the rest of the ship.

I built a separate scene in my project that allows me to test and debug the AI without having to play a complete game. This allows me to compare how may turns it takes for the AI to sink all the ships. With the easy difficulty, the number if turns is typically somewhere between 85 and 97 (the maximum number of turns required to cover the board being 100). The normal difficulty level varies greatly, from the mid-40s to the 80s. I also put in some code to display the state of the grid after each turn in the log, with an optional wait time between turns, and it's been fun to see how the game progresses, turn after turn. 

The complete implementation of this took somewhere between 3 and 4 hours, so it was not too bad. I don't get to write a lot of code these days at work, and when I do it's usually a simple report, so I had a good time writing this code.

My initial flowchart for the normal difficulty was definitely on the right track, but there were a few things missing in it. Which, to be fair, I expected. Rather than update the flowchart, I just went ahead and made the changes in the code. This project is not done in a corporate environment, I don't have a responsibility to keep de design documents up to date, and in all likelihood I won't use them ever again. There are definitely a few sections of the code that I will refactor in the next few days, some lines repeat and I'm not a fan of. (My current job is to reverse engineer some old code that has been written by people who loved repeating themselves for no reason, and I want to do my best not to make the same mistake.)

The next step is to implement the Carreidas difficulty, which should be straightforward (I just need to add a method in my grid class that picks a random occupied cell and returns it, then call this method from the opponent class). I currently don't have plans for this weekend, and my boyfriend is working, so I should have time to complete this before EOD on Sunday.

Following this, the next few steps will be:
- Process the player turn and evaluate if they hit or miss
- Display the proper icons on the grid for hits and misses
- Show the number of HP remaining for each player on the side of the board
- Decrement the number of HP as required
- Evaluate if the game is over and announce the winner

I don't think any of these steps will be as difficult as implementing the AI. Once they're done, the game will be playable from start to finish. There are still a few things I want to improve on it after that (like adding sound effects, improving the transition animations between turns, etc.)
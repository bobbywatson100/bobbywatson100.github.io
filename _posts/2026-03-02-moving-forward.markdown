---
layout: post
title:  "Moving Forward"
date:   2026-03-02 19:04:40 -0400
categories: naval-battle update
---
Though I did not work on my dad's battleship game every day over the past two weeks, I have made some very good progress. 

The first significant progress has been the complete implementation of the game loop. The game now goes from initial setup to alternating between the player and the opponent's turn a few times, then goes to the game over screen, with a button to go back to the initial setup. The game is not actually a game yet, since the opponent's AI is non-existent, all the game does on a player's turn is to check whether the click occurred within the grid, and there is no actual winner yet. 

I've also completed the import of the objects from my first attempt at the game into this new project and, after some minor changes, I got the following items off of my Kanban board:
- Display an actual grid rather than my initial placeholder coloured rectangle
- Place the ships randomly on the grid for both player and opponent
- Allow the player to move the ships on the grid by dragging and dropping them during the initial setup phase
- Create a new scene so I can develop and test the opponent's AI efficiently

Speaking of the opponent's AI, this will be my main area of focus next, as I have identified it as the last major step in the development. One thing that has been on my mind in the past few days is: Is it allowed to place ships next to each other on the grid? I asked Claude this morning and, while apparently Hasbro's rule set allows it, it is a common house rule to not allow it. I am inclined to include this house rule for now (and maybe make it optional later). The main reason why it's on my mind is that it has serious implications in the implementation of the AI itself, allowing it to know which ships are left. Not knowing this means that it could waste several turns (e.g. if the AI knows that the carrier is already sunk and has just completed a row of 4, then it won't go for the 5th and instead choose to hit a random cell instead). This house rule also reduces the number of possible cells to hit. This also means that I need to change a few things in my drag and drop implementation, but that should not be a very hard thing to do, since my algorithm for random placement already has an exclusion zone around each ship.

I ran into a couple of issues in the process, of course. One I am stil, working on is to place the ships on the board randomly on the start of the game. Due to how my scenes are set up, I cannot use the ready function in my script. I have an idea (and Claude has suggested a few things as well), but I haven't focused on that yet, since I don't think it's a high priority (although I do need to get that fixed before I show the game to my dad).

As stated above, I next plan to focus on the AI, which I think should take the better part of a week (maybe more). Things at work are starting to slow down again (I've had this job for a few years, and each period of activity is usually followed by some down time with very little to do), so I should be able to squeeze in a few half-hour sessions of development here and there between meetings. I did write an algorithm for the AI, so I know what I have to do, I just need to sit down and do it. 
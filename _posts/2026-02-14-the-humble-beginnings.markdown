---
layout: post
title:  "The humble beginnings"
date:   2026-02-14 19:04:40 -0400
categories: naval-battle update
---

About a year ago, my father asked me to find him a Battle Ship game for his computer, since he was getting tired of playing Queen of Spades on his computer. I tried looking for one. I'm sure there's plenty of them but, for whatever reason, I could not really find one. My dad also has very low vision, so I needed one that was easy for him to use. So I thought, "Hey, this seems simple enough, I could probably make one myself". And so I downloaded the Godot game engine (since it's the one engine I've been meaning to learn) and got to work.

That was last year, around May. Nine months later, that game still does not exist. Now, back then, I put in a serious effort, and had several features already implemented:
- Display the player board
- Display the list of ships to place on the side of the screen
- Allow the player to drag the ships and drop them on the board
- Allow the player to rotate said ships by double-clicking on them
- Allow the player to place the ships randomly on the board with one click (and make sure none of them were contiguous)

And that's pretty much where I stopped. I ran into some problem I can't remember, and thought I would get back to it a few days later. Of course, I never did. 

Now, months later, I decided to take a second crack at it. This time, I am taking a different approach. Instead of starting with the placement of the ships, then implementing the turn order, I am going to do the whole game loop first. What that means is that, after that first step, I will have:
- A basic screen with a placeholder grid, and a button that allows for the game to start
- A transition from that starting screen to a screen that allows the player to click somewhere on the enemy's grid
- After the click, another transition goes from the player's turn to guess to the enemy's turn to guess
- A short timer to simulate the enemy thinking, then reverting back to the player's turn
- Loop from the player turn to the enemy's turn a few times
- Display a game over screen

Once I have this running, then I will start bringing in what I had in last's years attempt. I haven't taken a look at my old project recently, but I think a lot of what I did can be imported and reused (with some refactoring of the code). My algorithm for random ship placement is still good enough. My drag 'n drop code should still be usable.

At this point of the project, the only big issue I see is the enemy AI. I want to have three distinct levels:
- Easy - At this level, the enemy just picks random cells in the grid with no logic to it
- Normal - At this level, the enemy picks random cells and, once it has a hit, then focus around the hit until the ship is destroyed
- Hard - At this level, the enemy cheats. After 3 failed guesses, the 4th one will always hit, and then it will focus around the hit until the ship is destroyed

I put in a few hours this week, and I am actually very close to having the full game loop implemented. I think another hour or two of work will get me there. Once that is done, I will experiment with Godot's web exporter, since I think this will work well as a web game. It also means I can just add a shortcut to it in my dad's web browser and never have to worry about having to install updates.

I have not set a deadline for this project. If I spend 20 to 30 minutes a day on this (and maybe a bit more on weekends), I think I can get it done in about a month. My goal is not to make it pretty. My goal for now is to just make a functional version of the game. Once it's working, I plan to show it to my dad, and then start customizing the visuals according to his special needs. 

This time I made a Kanban board in my Obsidian vault to help me track my tasks. I'm the only developer on the project, so it doesn't matter that much, but I want to develop good habits that will be useful once I start working on a bigger game project. 
---
layout: post
title:  "Flowchart"
date:   2026-03-22 19:04:40 -0400
categories: naval-battle update
---
Lesson of the week: Know the types of your variables. The main issue I was having with the drag and drop code was due to the fact that I was certain that the ships already placed on the map was stored as an array. It turns out it was a dictionary. (If I can defend myself, I wrote this code more than a year ago.) Once I figured that out, I was able to fix all the remaining issues with the drag and drop code, I brought back the 'exclusion zone' around the ships, and everything was fine, and the changes were committed to my GitHub repository.

I spent a few extra days planning the rest of this project. I made a complete list of everything that needs to happen at each state of the game loop. I then made a flow chart of how the AI is going to work. It is way more elaborate than I expected. I did the whole thing on paper while sitting on the couch, so it's a bit messy:

![AI Flowchart](/assets/images/bship_ai_flowchart_20260322.jpg)

I think I am still missing a few steps, mostly with regards to declaring a ship as 'sunk' and removing them from the list of remaining ships, so I plan to spend an hour or so in Dia to make this diagram a bit cleaner and fixing what I missed on my first attempt.

The process of drawing the diagram gave me a very clear idea of a few things that I need to do before I jump in:
1. I need to modify my game grid class to add a method that returns all the cells that can possibly be picked for the next guess
2. I need to also add a method to my game grid class to check if a guess is a good one or not
3. Finally, I need to implement a 'Carreidas' method for cheating for the highest difficulty level (I could not resist adding a Tintin reference, since 'Flight 417 to Sydney' has been on my mind since I started this project)

I implemented (but not tested) the first change earlier today, and I started working on the second. The third one shouldn't take too long.
---
title: "Godot 4 porting progress update!"
date: 2022-09-18 18:59:44"
categories: gamedev
---

This took more time than I thought (mostly because I spent my summer biking, hiking, walking, and playing videogames), but I finished rewriting my dialog system for Godot 4 today! I still need to do some work to get localizations working, but for the most part, this is functional!

![Dialog In Progress](/assets/images/20220918_01.png)

On the left side, highlighted in yellow, is how the structure of the dialog is defined. At the top is a what I called a Dialog Block. By itself, it's nothing but a container. Inside the dialog block, I defined different kind of objects:
- Dialog commands (highlighted in red on the right hand side), which I can use to display dialog, along with a name tag and a character portrait
- Player choices & options for branching paths
- Single conditions (compare a value with different comparison operators)
- Multiple conditions (groupings of single conditions, and I have options for AND or OR)

A dialog block can have sub-blocks. I can put conditions anywhere in the block. Each item inside a block is processed in order. If the dialog system encounters a condition (single or multi), it evaluates it. If the condition fails, then it exits the block entirely and moves to the next block.

I added a feature this morning to replace placeholders in a text with variable values. I also spent some time this morning to rework the UI so that it doesn't get messed up when resized.

The game I'm working on (visual novel/dating sim with turn-based beach soccer/football) has four different types of scenes:
- Dialog section with 3D animated background (typically used when the team's minivan is on the road)
- Dialog section with 2D backgrounds (used for in car conversations, group meals, and dates)
- Explorable 3D environment with NPCs and NPC dialogs (for pre-match talks with teammates and possibly others)
- Turn-based beach soccer from an isometric perspective

I had the first three working last year. I started working on the fourth one a while ago (there is evidence of that further up in this blog), but I don't think I got very far into it. 

The next steps I want to focus on:
- Localizations
- Adding simple animations when showing/hiding the dialog box, name tag, and character portrait
- Import the dialog section with 2D backgrounds in Godot 4


This should keep me busy for the next two or three weeks.
---
title: "Storing Scenario Data"
date: 2022-11-09 12:00:00"
categories: gamedev
---
For the past few days, I've been wondering how I'm going to store my game's scenario data. By "scenario data", I mean:

- Character dialog
- The showing and hiding of backgrounds for visual novel sections
- Choices and options presented to the player

The requirements are few but not exactly simple:
- Ability to store hierarchichal data
- Simple to edit

Here a a few solutions I have considered.

### Database routes
My background as a developer so far in my career has mostly been on the SAP ERP platform. This is a platform that is entirely dependent on the system's database. So, naturally, when I started thinking about how I would store this information, I immediately thought "database". MySQL and other complex DBMS's are out of the question (too complex to include in the distribution of a relatively simple game), but SQLite could do nicely. There is a Godot plugin for that. Or there will be, as the version for Godot 4 is not released (which makes sense, considering the current status of Godot 4).

The issue with this approach is the complexity of editing the data. There is an open source program out there (DB Browser for SQLite) available I could theoretically use, but that is not exactly suitable for actual writing or text editing. 

### JSON files
A few years ago, when I started thinking about making a videogame, I considered using JSON files to store the scenario data. And, overall, I think it makes sense: 
- It's easy to create hierarchical data
- It is simple to edit with a text editor
- Godot can easily read and import the file

Since I'm probably going to do all the writing, this is certainly a viable solution. 

### Godot scenes
This is the method I am currently using. The main issue with it is that it's time consuming to write and edit. But I really like it's organized and how the hierarchy is visible in the scene tree, and how easy it is to traverse in code.

### Custom script format
I took some time yesterday to look at how the Ren'Py engine does it. It kinda [reads like a play](https://www.renpy.org/doc/html/thequestion.html#thequestion): very readable, easy to edit, with a simple syntax. In short: I quite like it! Due to localization and differences in "scene direction" instructions, I won't be able to use the same structure however.

***

So, what's the verdict? Databases are out, mostly because of how complex it would be to actually write the text. Theoretically, I could write a program that would do the inserts and updates for me, but I think this would take time, and that time would be better spent elsewhere. 

At the moment, my favorite solution is a mixture of custom script format and Godot scenes: write the script in a text file, and import that script into Godot scenes and nodes. Whether this import is done at ahead of time through a Godot plugin or at runtime is still up in the air. I know I will at least need a plugin to validate the content of the text file to avoid syntax issues. I do not know how hard it is to modify the content of a scene in a plugin.
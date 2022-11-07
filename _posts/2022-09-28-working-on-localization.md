---
title: "Working on Localization"
date: 2022-09-28 00:00:00"
categories: gamedev
---

Whatever I'm working on a project, the issue of translation is always high up on my priority list. Living in a bilingual environment most likely has something to do with it. The exception to this rule of mine is this blog. 

Godot has build-in localization capabilities. They are probably fine for most games. I will be using some of them, but because some of the text for my game will be stored in custom node types, I had to implement some extra functionalities. 

Here's an example of a dialog node:

![Dialog In Progress](/assets/images/20221001_01.png)

In the dialog system I've developed, dialog nodes have two properties that can be translated:
- Dialog ID
- Nametag ID

Godot can import CSV files into what's called the TranslationServer. Each string is identified by a specific ID. All a developer needs to do is call the `tr()` method and it will return the translation in the current language.

My biggest problem was the creation of the CSV files themselves. I needed a way to:
1. Go through the node tree of each scene (or level)
2. Identify nodes that have translatable content. Currently, this is limited to three different types of nodes: Dialogs, questions, and choices. 
3. Retrieve the various IDs and the text strings associated with those IDs
3. Add or update a CSV file with those IDs and text strings

I decided to write a plugin to accomplish this. With a small amount of googling, I was able to add an item to `Godot's Project > Tools` menu. 

![Dialog In Progress](/assets/images/20221001_02.png)

When triggered, the plugin will look at all the scene files (extension .tscn) in a specific folder of my project and generate a CSV file for each of those scenes. The IDs themselves are a concatenation of the scene name and the ID specified in the node (in case the ID is used in more than one scene, which is likely considering the amount of text this game will have). The plugin generates a small report to let me know what it did:

![Dialog In Progress](/assets/images/20221001_03.png)

Writing this plugin was pretty fun, even though I was fighting a cold and trying to stay awake after only sleeping for two hours the night before. I did break some code by adding the scene name as a prefix to translation IDs, I will have to spend some time in the coming days to fix that. Actually, I should stop here and do it now so I don't forget.


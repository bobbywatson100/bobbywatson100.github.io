---
title: "Dialog system is mostly complete"
date: "2021-10-19 10:00:53"
categories: gamedev godot SABSL
---
After weeks of little to no activity on the gamedev front, I finally sat down on Sunday and Monday to work on the dialog system. After several attempts at tree traversal algorithms, I googled 'tree traversal', and voilà! I found a simple C program that I was able to use as reference.

My dialog system now supports:
- Unlimited dialog lines (called DialogCommands). They can be accompanied by a character portrait or not
- Conditional dialog blocks
- Player choices

Here's a very simple example, with one line of dialog and then an question to the player:

<img src="https://confessionsbacklogger.files.wordpress.com/2022/01/c4241-image.png?w=547" alt="" class="wp-image-35" />

This is what it will look like in-game:

<img src="https://i.imgur.com/m2fbQfu.png" alt="" />

There are plenty of issues, of course:
- Inconsistent fonts
- Font is too small
- Inconsistencies between the dialog box and the buttons
- Question box is actually behind the dialog box

I will spend some time today to fix the font and window order issues. The UI inconsistencies will wait. I also need to test the conditional blocks feature to make sure it actually works. And with that, the dialog system will be mostly complete!
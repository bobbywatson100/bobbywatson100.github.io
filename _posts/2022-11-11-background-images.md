---
title: "Background Images and UID Issues"
date: 2022-11-11 15:24:00"
categories: gamedev
---

Adding background images for visual novel scenes to my game took more time than I thought it would, but it seems to be working:

![Dialog In Progress](/assets/images/20221111_01.png)

(The image itself was generated with Stable Diffusion.)

The code itself is incredibly simple, and almost identical to the code for the character portrait. Because of this, I duplicated the CharacterPortrait scene to instead of starting from scratch, and this caused issues. At first, I was blaming Godot but, upon further investigation, I discovered that each scene as a unique ID included in the .tscn file and, since I duplicated a scene, both the background image and the character portrait had the same ID. This caused issues during execution, because the character portrait now had the script for the background image associated with it. Some of the methods having different names, the debugger kept complaining about missing methods. I only realized this when I opened the dialog controller scene with a text editor, and noticed that both the background image and the character portrait instances had the same ID.

Lesson learned!
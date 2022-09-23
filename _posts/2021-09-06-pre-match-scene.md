---
title: "Pre-match scene"
date: "2021-09-06 20:46:22"
categories: gamedev godot SABSL
---

Before every match in the game, the player can walk around the changing room and talk to the other players. This is a simple one that I threw together with some sprites I generated from a generic tool and simple models I created in Blender:

<img src="https://i.imgur.com/g8hf1Kl.jpg" alt="" />

I am still  undecided regarding the dialog system: Do I create my own, or do I use a plugin called Dialogic? At the moment, I'm using my own. It can display dialog and character portraits. I have plans for user choices, and dialog trees.

Although I thought the dialog display elements were in a good state before I started working on this scene, I soon realized that there were major issues with how input was processed, and ran into all sorts of trouble: infinite loops, unable to get out of a dialog, the dialog box would close but the player couldn't move... Things are in better shape now.

The next step is to switch scene when the player moves close to the green rectangle in the background (which is a door, even though it doesn't really look like one).  Once that is complete, I will get started on the actual meat of the game: the beach!
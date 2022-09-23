---
title: "Cemu and Xemu on Moonlight"
date: "2021-08-08 16:49:22"
categories: in-home-streaming
---
I have been experimenting with both Cemu (Wii U emulator) and Xemu (original Xbox emulator) recently, streaming them to my TV using Moonlight. (At this point, the SteamLink app is but a distant memory, and will only use it for games for which Moonlight doesn't work, like *Valkyria Chronicles*).

For Cemu, my test games (so far) have been *Monster Hunter 3 Ultimate* and *The Legend of Zelda Wind Waker*. In both cases, I have had zero issue with Moonlight. Launching the games through Steam directly has been problematic. So, instead of doing that, I created a batch file to launch each game, and added those batch files to the NVidia GeForce Experience "Shield" settings. Here is the content of the batch file:

    echo off
    set Emu="C:\path\to\exe\file
    set Game="C:\path\to\iso\file"
    start /realtime /b "" "%Emu%" -g %Game% -f
    exit

For Xemu, the only game I've tested is *Jet Set Radio Future*. I was planning to play *Panzer Dragoon Orta* as well but, after giving the game a shot on original hardware, I quickly realized that the game was not for me and decided not to play it. Here, I have encountered the same issue I had when I first launched the emulator: my controller was not recognized. I had to use a mouse to navigate to the settings and select it, both on the computer and on the Raspberry Pi. After that, things have been running great. I think launching through Steam would have worked here, but instead I created a batch file to launch the game directly and also added in the "Shield" settings as well.
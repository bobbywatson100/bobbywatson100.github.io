---
title: "Getting Into Game Dev Again"
date: "2022-07-07 18:13:08"
categories: godot gamedev SABSL
---
After months of not working on my turn-based beach soccer game (except to give it some thought once in a while), I decided to go back to it today. (Work has been nothing but all-day meetings for weeks, and I got bored.)

The first thing I did was to download the latest Godot 4.0 alpha release. The decision to go with Godot 4 was tough. But, even though it is still in alpha, my main reason to go with it is that I'd rather bite the bullet and start updating my GDScript code right away while it is still pretty small, rather than having to do it later when I have tens of thousands of lines of code to review, fix, and test.

Instead of importing the whole project at once, I'm going to bring in things one component at a time. My file organization was… poor, let's say, so this gives me an opportunity to relocate all the elements in a more logical place, and to fix whatever import issue I run into, rather than having to sort through hundreds of errors.

Since I'm not doing anything too fancy with the graphics, I don't think I'm going to run into major issues. There are, of course, drawbacks with this approach:
- The engine is in alpha, and will change between now, the various beta releases, the RC releases, and the final release. It is very likely I will run into engine bugs. The problem then will be to determine whether the problems come from my code or the engine.
- Some useful plugins (like unit testing frameworks and to-do manager) will not work at all.
- Documentation is not up to date.

I started by importing the classes for my dialog system earlier today. I almost immediately ran into a few issues:
- Export variables for nodes are written differently in the new version of GDScript.
- The documentation says that the @export_enum annotation should support string arrays but, in fact, it does not. The sample code does not pass syntax check. I had to define my exported enums separately (which, to be fair, I think is a cleaner approach).

So far, that's about all I've done. My goal for the rest of the week and this weekend is to import the various UI elements for my dialog system so I can retest the whole thing and make sure everything works as it used to. I don't expect to run into major issues, but who knows!
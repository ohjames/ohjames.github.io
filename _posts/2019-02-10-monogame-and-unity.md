---
layout: post
title:  Moving from MonoGame to Unity
date:   2019-02-10 15:20:00
categories: MonoGame Unity SuperFightingTeam
---

I love MonoGame, but I'd love it even more if there was a good library (or few libraries) that provided these things:
- Ray-casting of polygon shapes into a scene of components, including spatial subdivision (e.g. quad trees) to reduce the number of collision tests.
- A Component/Object/Scene system for structuring code.
- A dependency injection system to allow data/code that can potentially live across many scenes to be injected into Objects/Components.
- A 2d tilemap system and editor with support for polygon colliders.

It would be fun (and also a little painful) to work on those things but I'm a little tired of reinventing wheels so, for now, I've switched from MonoGame to Unity.

Unity can be annoying. Certain areas of Unity are still not quite yet beta quality, on my first day experimenting with the tile editor and tile palette I suffered about fifty crashes in a single day. I've falls over itself without crashing leading to many restarts. I was importing a sprite-sheet into a tile-palette, at first it worked fine, but many subsequent attempts over several hours failed, with the tiles from the spritesheet getting imported into the tile-palette in the wrong order, even with gaps in between. Then it started working again. If the bug comes back it could waste a lot of time in the future, manually reordering a messed up tile-palette is no fun: a lot of mouse clicks. Tasks that require a series of repetitive mouse clicks are basically of the most annoying things about Unity. Maybe you'll have to do the same series of forty repetitive mouse clicks in a row to achieve a goal (say, setting the physics shapes on sprites within a spritesheet to a square). I'm more use to writing a vim macro to get tasks like this done in 10 seconds. The yaml files it generates absoultely everywhere are stupidly huge, specifying every single default everytime. This makes version control of said files very challenging. The merge conflicts can be impossible to deal with and often lead to work needing to be redone. Why can't each yaml file contain a single "version" flag which is associated with a set of default values, and then just leave all those defaults values out of the yaml? It would be more readable and less prone to version conflicts.

The user-interface and yaml files may suck but when it comes to the coding, I really like how everything is structured. I love that you write C#, it's a really great language. The API overall is really good, especially when it comes to collision detection and implementing custom physics. If the user-interface was even a third as good as the coding side then Unity could be so much better.

I foresee having hundreds of hours wasted by Unity being annoying but that will still be less time than it'll take to write the four items I described above. I'm still not sure which will be more fun, or less painful. If I eventually give up on Unity I will have just spent time learning a technology that becomes useless to me, and I'm only 60% sure going with Unity is the right option. This could be a very costly mistake.

We've also decided to call this game Super Fighting Team for now but that will almost definitely change. Our name [chilon.net](http://chilon.net) works okay for a web development studio but it's not great for a game development company, so our team name for this project is: Super Frolic Team.

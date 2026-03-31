---
title: Group Project.
publishDate: 2025-11-15 00:00:00
img: /assets/GroupProject.png
img_alt: A screeenshot from my OpenGL Graphics Demo
description: |
  Group Project for Intergrated Masters, including PS5 build
tags:
  - C++
  - OpenGL
  - CMake
  - PS5
---
## Masters Group Project
### Links:
PS5 Build: </n>
<iframe width="600" height="400" src="https://www.youtube.com/embed/QGP9eVH0AKo" 
title="CSC8508 Group Project PS5 Build" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</n>
PC Build: </n>
<iframe width="600" height="400" src="https://www.youtube.com/embed/iOAtWiHzFY4" title="CSC8508 - VideoSinglePlayer Game" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</n>

### Our Group Project:
For our masters group project, we were tasked with designing and creating a game from scratch. 
We were granted a considerable amount of creative freedom with both our themeing and our design,
with the only two requirements be the game was child freindly and that we had to build a PS5 version of our game.
We decided to make a quake smash-bros hybrid, where players would deal damage to each ranged weapons before running up to each other
and trying to bat each other out of the arena.

### What did I do?
For this project, I took the role of our lead engine programmer. This meant I had to implement our core engine systems such as rendering, physics and audio.
To do this effectively, I used multiple different libraries and middleware such as:
<ul>
	<li> OpenGL for rendering </li>
	<li> Jolt for physics </li>
	<li> FMOD for audio </li>
</ul>

I also took charge of our PS5 build, working to get our game running on the university's PS5 devkit. 
This was made easier due to our middleware libaries already having support for the PS5, but I still had to both
link all the libaries together using CMake and ensure our game compiled when other contributors made changes to the codebase.
### What did I learn?

This project has been my greatest insight into game development so far, espeically cross-platform development.
Learning how to use CMake to link together our libraries and ensure our code compiled consistently on both platforms was a major challenge.
There were also many quirks with the PS5, such as the renderer being very different in design to how opengl functions.

In the end, whilst our game was far from perfect, our engine worked well, compiling both PC and PS5 with minimal issues.

---
layout: post
title: "[Uni] Master of Science in Engineering: Game and Software Engineering"
date: 2025-06-04 12:00:00 +0100
description: A view of the largest and most impactful projects created by me during my time in university. # Add post description (optional)
img: bth_ute_vatten.jpg # Add image post (optional)
---
Note: Most of the code from these projects are available as private repositories on my github page. If you want to know more about the code, contact me and I can share the code.

Note(2): If you want to see my skillset at a glace I've marked `important` details in this page.
* auto-gen TOC:
{:toc}

# <ins>Master's Thesis (Meshlets in Ray-Tracing)</ins>

The project is currently a work in progress but will be updated here as soon as it is published on `DIVA`.

# <ins>Games</ins>
During the time of my education I partook in creating various different games with different scopes and goals. My responsabilities in each game differed depending on the competence of the group; however I mostly worked either with scripting or performance.

## [C++/LUA] TinkerTails (Large Game Project, 12 people)

<img align="left" width="300" src="/assets/img/tinkertails_logo.png" alt="logo" style= "margin-right: 5px;"/>
### The Project
TinkerTails is a multiplayer team fighting game where each team of 1-4 players has to sink the opponents skyships in a round based system to win the match. Each round has a building phase and a fighting phase. In the building phase every player is given blocks to expand their skyhip and add weapons, utility or mobility. During the fighting phase the teams fight in a ever shrinking arena until only one remains standing. The first team to a certain amount of rounds won, win the game.

The team consisted of 12 people with various skills. The project lasted roughly 6 months with 7 2-week sprints using the agile method of SCRUM. The game was built with the use of a custom created game engine and used LUA for all gameplay aspects combined with the engine's ECS.

### My contribution
During this project I primarily built the entire scripting backend for the game, I was also involved with the `profiling` and `logging` of the game engine. I however did not work on any of the shader code this time around. Other topics I worked on involved team colors, ghost blocks and general `QoL` and `QA`.

The `scripting` was made to mimic the interface given by other engines such as Unity or Unreal. We partially achieved this, however LUA provided some challanges which we had to work around to create the best interface we could.


There is currently no link available for the trailer of the game, however that will be added here as soon as we release it to youtube.


## [C++] Whisperwoods (Small Game Project, 6 people)
<img align="left" width="300" src="/assets/img/whisperwoods_logo.png" alt="logo" style= "margin-right: 5px;"/>
### The Project
Whisperwoods is a single player stealth roguelike game where the player has to sneak past the invading Carsinians (Yes they are crab people) to reach milestones before they can make an exit and save their planet. The group in whisperwoods was 6 students from BTH from the same class. The project took 6 weeks in total to create the entire game and engine from scratch. We used certain utility tools from one of the members of the group, as well as some common libraries such as ASSIMP.

### My Contributions
In Whisperwoods, we worked on an Intel NUC with an integrated graphic card, because of this we could not utilise modern graphics card tools such as compute shaders. My primary job in this game was the renderer and ensuring we reached the performance limit for the grade (30fps on 1080p or 60 fps on 720p). By utilising a `depth pre-pass`, `quadtree` culling and dynamic loading of scenes, we achieved a solid 45 fps in the end.

Due to the problems with compute shaders, moving post processing and other major pixel features into a pixel shader, helped with performance quite a lot. The `depth pre-pass` allowed for reduced overdraw, which further helped this effect.

The `Quadtree` helped with reducing the amount of data being sent to the GPU, due to the limited resources and vast amount of models in the scene, this provided a substantial boost.

Besides performance I also worked with various small things, such as `profiling`, `logging`, and some gameplay aspects.


The link to the trailer can be found on youtube with the link [here](https://youtu.be/jSfU6uw6qy8?si=XRqwhyuQbJasDkY8). It showcases gameplay at the start and all the technologies used at the end.

## [C++/LUA] Necrocade (Scripting, 2 people)
### The Project
A very small project using RayLib and LUA. The game is a turn based top-down mob survial game, where the player has to use generator buildings to generate towers or modules to empower their defenses. The enemies all move during their turn and attack the nearest structure. If the base is destroyed, you lose. 

The game was mostly made to test the capabilities of ESC and LUA, and thus provides a substantial editor in which the player can edit the starting map and place both terrain, enemy spawners, and all the buildings. 

The game was created by me and one of my class mates. The game features an arcade like gameplay style with fitting retro music and artstyle provided by my team mate.

### My Contributions
In this project my primary focus was on using `LUA` to create the interface and editor to be flexible. Much of the work was worked on together, however I lead the project in how `LUA` should be used, and implemented advanced features such as a unique `buffer based script loader` and `sandboxing` to isolate game from I/O and other unneeded features.

Currently no screenshots available, however this will be added in the future.

# <ins>Major Projects</ins>
## [C/Vulkan] 3D Meshlet Renderer
A renderer created in Vulkan to draw both `meshes` and `meshlets`. The purpose of this project was to analyse the use of modern rendering APIs. For my project I went with comparing meshlets to the more traditional approach. 

Graphs and more info will be added at a later date.

## [JS/WebGL] Web based Metaball Renderer
The project involves using `WebGL` and `glsl` to render meta balls on the web. The project uses `Ray Marching` to do this.
For now the project can be viewed [here](https://www.student.bth.se/~dahl20/dbwebb-kurser/webgl/me/kmom05/proj/).

## [C++/DX11] 3D Renderer
My first 3D renderer in DX11, this project included many features to create a relatively complex scene. Not much help was provided in terms of implementation, only theory of how the features should work. Each feature took a lot of research and trial to make work with the remainder of the application. The features implemented in the project were 
* `Deferred Rendering`
* `Blinn-Phong lighting`
* `Shadow mapping`
* `Level of Detail` (Using tessellation)
* `OBJ-Parser`
* `Dynamic cubic environment mapping`
* `Frustum culling` (Quadtree)
* `GPU-based billboarded particle system`

## [C] Mini Java Compiler (2 people)
For this project I worked with 1 other classmate, we created a compiler and interpreter for the language Mini Java. This is a subset of the Java programming language with much less features. The project was written entirely in `C11` and could compile the entire language into bytecode which our interpreter could then execute.

## [CUDA] LeNet-5 AI Model (2 people)
For this project me and a classmate transformed a already written LeNet-5 AI from C++ into `CUDA`, we achieved roughly 70% increased performance with the same results. We implemented both `forward and backward propagation` in `CUDA`.

## [C] UDP and TCP Realtime Chat server/client
For this project there were multple steps, I created both server and client to handle the chat functionallity; however the final project was a client that connects to a BTH hosted server. All of the code was written in Linux using `C11`. The clients used Linux `real time signals` to await and communicate information. The project was created with `C11` features and relied much on the `DRY` principles.

Another part of this project had a client connect to a `HTTP` server with `GET` to parse information and display it in the terminal.

## [C] FAT Shell
A small project which implements a `FAT32 shell` in the Linux terminal. The shell provided functionallity from file creation, writing, reading and moving. The shell also allowed for folders and an extensive error handling system.

# <ins>Minor Projects</ins>
## [ASM] Light Pin Simulator
A very minor project where I wrote a PIN simulator using only `ASM X86`. The project was made to emulate that of a rasberry pi with connected lights.

## And more...
Besides what is mentioned above I have created numerous more projects such as, a physics based glide plane simulator, snake, mutithreaded C applications that use SHA256, floodfill, and more.

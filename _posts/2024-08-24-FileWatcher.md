---
layout: post
title: "[C] Filewatcher"
date: 2024-08-24 00:00:00 +0100
description: # Add post description (optional)
img:  # Add image post (optional)
---

A proof of concept way to implement a file watching system for C. 

A file watcher is essential for a game engine where the code editor is integrated into the engine. Without it the user will have to relaunch the engine whenever they want to change any code, which is to be avoided at all costs. Therefore this concept was experimented on and will be expanded upon to become event based rather than poll based. The problem right now is that the implementation polls each frame instead of sleeping until a change has happend. This will be explored in future iterations.

Finally, this concept will be used in the future to create a feature complete game engine written entirely in C.

[Github link](https://github.com/Danhall01/FileWatcher)
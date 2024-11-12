---
layout: post
title: "[C] Mini-java compiler"
date: 2024-03-18 00:00:00 +0100
description: # Add post description (optional)
img: # Add image post (optional)
---

A project created by 2 students as part of a course in BTH. This compiler handles all features of Mini-Java and is written entirely in C. 

My primary part is this project was the Lexer, Semantic and Interpreter. We collaborated in all of the parts and ideas used where agreed on by both parties before implementation. We used a custom data structure to handle the symbol table which can be seen in the `CFG.c`, where header data was hidden inside of the first part of the node, and the rest was used as a normal blob of memory.

[Github link](https://github.com/Danhall01/DV1656_Compiler)
---
title: "Therasphere VR"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

{{< vimeo 1071248418>}}

#### Platform: Oculus Quest
#### Engine: Unity
#### Genre: Educational, Simulation
#### Team: 1 Developer (me) 1 3d artist, 1 project manager

I worked on this game with Razoredge LLC, who in turn was contracting with a local university. The game was created to improve the process of training nursing staff on how to correctly handle radioactive cancer treatment drugs. The existing training method was costly and slow, as it involved calling a van out to the worksite and taking an entire day to train nursing staff with the real equipment. Furthermore, they would only get one chance to go through the experience. I'm confident that due to our creation of this serious game, they were able to receive better, more accessible and more personalized training! 


# ENGINEERING TASKS:


## Gameplay Systems Programming

I programmed all the gameplay in the game including internal state of the lesson, tracking player objects, and hand interactions such as parts rubber banding to their correct positions within certain tolerances.

## Unity Timeline Sequencing

Using the same toolchain I was able to use from Future of Pet, I also authored all of the content in the game. There was less room for interpretation in this project, and I didn't have to consult so much with other members of the creative team. So, I just put all the content together myself, mostly by adapting existing didactic learning from an old training video covering the material.

## Editor Scripting

I made minor edits to the toolchain to support animation-related edge cases in the game.


# OTHER TASKS:


## Art Pipeline Coordination

![Alt text](/tubingbone.PNG)

The most involved part of this project was the animation of the small plastic tubing. While primarily a challenge for the artist to animate correctly, it was also troublesome to get it to align properly with the geometry over several stages of animation. It was also unusual to apply bone weights to an obviously rope-like structure. We initially considered a completely different architecture, making a fully articulated physics rope system rather than a baked animation on a single asset. We saw quickly that it would not just be less work, but also more true-to-life to simply portray the tubing assembly in a pre-animated way over the course of several gameplay interactions. I defined the animation steps with the artist based on our shared understanding of the learning requirements, and we worked together to make sure that it would look correct and convey correct information at each step of the animation. 

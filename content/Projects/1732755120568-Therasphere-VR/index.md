---
title: "Therasphere VR"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

{{< rawhtml >}} 

<video width=100% controls autoplay>
    <source src="/videos/mp4/thera-small.mp4" type="video/mp4">
    Your browser does not support the video tag.  
</video>

{{< /rawhtml >}}

#### Platform: Oculus Quest
#### Engine: Unity
#### Genre: Educational, Simulation
#### Team: 1 Developer (me) 1 3d artist, 1 project manager

I worked on this game with Razoredge LLC, who in turn was contracting with a local university. The game was created to improve the process of training nursing staff on how to correctly handle radioactive cancer treatment drugs. the existing training method was costly and slow, as it involved calling a van out to the worksite and taking an entire day to train nursing staff with the real equipment. Furthermore, they would only get one chance to go through the experience. I'm confident that due to our creation of this serious game, they were able to recieve better, more accessible and more personalized training. 

Engineering Tasks:

## GAMEPLAY SYSTEMS PROGRAMMING

I programmed all the gameplay in the game including internal state of the lesson, tracking player objects, and hand interactions such as parts rubber banding to their correct positions within certain tolerances.

## UNITY TIMELINE SEQUENCING

Using the same toolchain I was able to use from future of pet, I also authored all of the content in the game.

## EDITOR SCRIPTING

I made minor edits to the toolchain to support animation related edge cases in the game.

Other Tasks:

## ART PIPELINE COORDINATION

The most involved part of this project was the animation of the small plastic tubing. While primarily a challenge for the artist to animate correctly, it was also troublesome to get it to align properly with the geometry over several stages of animation, and to apply bone weights to an obviously rope-like structure. We initially considered making a fully articulated physics rope system for this asset, but saw quickly that it would be more accurate to real life to portray the tubing assembly as unfurling in a pre-animated way over the course of several steps. I defined these steps with the artist and we worked together to make sure that it would look correct and convey learning information at each step of the animation. 

---
title: "Squareforce"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

{{< rawhtml >}} 

<video width=100% controls autoplay>
    <source src="/videos/mp4/Short-Squareforce-Teaser.mp4" type="video/mp4">
    Your browser does not support the video tag.  
</video>

{{< /rawhtml >}}

#### Platform: PC
#### Engine: Unity
#### Genre: Fighting
#### Team: 1 solodev (me)

This was my first major effort in creating an indie game of my own. I was inspired by the super smash bros community to create SQUAREFORCE, a flying fighting game where you mix-and-match moves on your spaceship to create a custom moveset. I designed, programmed, and did all the artwork for the game, as well as took it to several conferences where I tabled and talked to journalists and industry contacts to promote the game. I had dozens of people play my game at the various conferences I went to and local game developer events I regularly attended. In the end, this served to get me my first paid jobs in the industry, and I did not release the game, though at some point I still might (there are a lot of things I wish to improve about it)


# DESIGN TASKS:


## Design Documentation

I created all the documentation by hand on physical paper- this was my first game and I didn't yet know about personal knowledge management systems, formal structures and procedures for design documents, or mockup software. Instead I worked out the design of gameplay systems I wanted and how to technically and artistically achieve my aims. I didn't stick to a specific small list of axioms for my goals, which is something I would do differently today. But in retrospect, I was basically trying to create a flying smash bros clone where you got to mix and match character normals. I also adopted spaceships as the characters early on, because I knew at the time that I wouldn't be able to animate an entire roster of humanoid characters myself. Also, it gave an in-universe excuse for the characters to be sending chunks of energy at each other- another design goal I had was to make the hurtboxes of moves visible in the actual final art of the game so that it would be easier for new players to understand the properties of moves at a glance than with other fighting games. Over time I was able to leverage these constraints into a unique visual theme

## Game Systems Design

I designed a number of game mechanics to compliment this vision. I really wanted to focus on accessibility because it was my view at the time that 2d fighting games were dwindling in popularity due to their steep learning curve and poor player communication. I made the movepool for each character very small (6) and made it so that you only needed to use 2 attack buttons and 4 face buttons total to play the game. I also was trying to design each type of input to also work with touch devices, but this was later scrapped. Many moves were only available through chording, which i thought would simplify the controls but actually it confused players. I also ran into some classic game engineering problems since it was my first project- one of which was the fact that my fast-moving attacks and ships would frequently clip through each other and terrain. I wrote a custom collision interpolation system to dynamically create meshes at runtime to interpolate between a hurtbox's last frame and current frame. In keeping with my commitment to show the hurtboxes AS the artwork, i even considered coloring the runtime-created meshes so they would look like 3d motion smears (this concept was also being used by another independent smashlike project, earth romancer). In the end I did not use the smears for artistic purposes, but I used them to manage collision for most of the project's lifetime until i eventually discovered established, simpler methods for continuous collision detection (i didn't even know there was a word for it at the time)

## UX Design

I designed a 3d menu for the game that was a rough skeudomorphism of putting the ship parts into a sort of builder. I overscoped greatly because I couldn't model all of the parts individually, but I was able to create a very tactile and satisfying menu system. I also responded to player confusion about input chording by making it so that in the menu, you have to input an attack in order to modify it on your loadout. This was a nice idea but in the end i think it made the menu controls too confusing. Other UI elements i was proud of the design of was the dash ring- I created a ring that expanded around the player while dash was held, and it would visually convey the dash 'charging up' while also indicating exactly how far you would go if you buffered a turnaround. using VFX for player communication is something I wanted to do more of, but I liked that I at least made this. Also, through the use of my 3d skeudomorphic GUI, i was able to work around the problem where the unity version I was using at the time (4.x) was not capable of natively supporting multiple players using the same GUI eventSystem.

## Content Design and Game Balancing

I designed all the playable stages in the game to wrap in both the X and Y so that it was impossible to camp opponents in a corner. I wanted the 'corner pressure' aspect of the fighting game to occur at the surfaces of the asteroids and other space objects floating in the stages. In the end this was a little confusing and a very big constraint on stage design, I'm not sure i would do it again if i made squareforce today. As for the moves themselves, it was very fun to create a lot of moves and think critically about how they could be used both in different kits, and in unconventional fighting game situations like continuously attacking below or above you. This was in addition to creating moves that obeyed the standards of fighting game content, such as fast pokes, combo starters, finishers, defensive attacks, and other well known tropes of fighting game move design.


## Focus Testing

I brought squareforce out to many different promotional events. I ran a booth at GDEX, an ohio convention where gamedevs from ohio and surrounding states could show their stuff. I also brought my game trailer out to GDC. I also got some professional smash players to try it at the cleveland esports summit! Most of all, I brought it out to local developer and enthusiast events in cleveland and Portland, Oregon many times (I was living in both places at the time). Each time I took notes on bugs players encountered, moments when they misunderstood what was happening in the game, common critiques, and negative possibility spaces/feature requests. 


# ENGINEERING TASKS:


GAME SYSTEMS PROGRAMMING

UI/UX PROGRAMMING

PROJECT ARCHITECTURE

CUSTOM COLLISION SYSTEM

## Dynamic Animation System

because of the fact that my characters all used dynamically chosen attacks, I had to create a lot of animation control systems at runtime, much more than any similar project would. I used unity's mecanim system and i made a generalized system of placeholders that could be overridden using an animatoroverridecontroller that I would create while the game was running. In retrospect, I wish I had known about unity playables or even some of the more basic code-only animation control systems available in the unity API. at the time though, I was very proud of the finite state machines I had built to drive character animation!

## Enemy AI

I also used mecanim to drive enemy ai behavior in the game. Rather than use it for animations, i leveraged mecanim in an unusual way as a general FSM system to drive behavioral state changes.  


# ART TASKS:


## 3D Object Art

I created all of the 3d objects in the game myself! I chose a low poly style, and tried to adapt the aesthetic to my capabilities and what i knew I would be able to make. I was a novice in blender at the time, but I was able to create a variety of player ships and objects for the stages and 3d GUI screens. I consulted with my artist friends on how to apply character design principles to the ships, such as by adding contrast to important parts of the model and suggesting movement and action through the silouette and shape of the ships.

## Animation

I also animated all of the attacks myself in addition to adding squash-and-stretch and 'facial animations' to the ships! If i had kept going, I was planning for the lore of the game to involve a toy story-like premise in which some bizarre space physics made the ships slightly alive, but only while not being observed (in a nod to quantum physics's wave-particle duality). I used blender shapekeys to animate all the facial expressions of the spaceships, and I used both blender and unity's built-in animation editor to edit all of the squareforce-based attacks. I carefully studied other fighting games frame-by-frame to better understand concepts like key poses, contrast against background elements, anticipation, and visual communication of the impact of the hits- in addition to referencing the frame times of common archetypes of attacks for balance purposes.

## Environment Art

Since my art was low-poly, I relied a lot on lighting and VFX to visually distinguish my stages from one another. I made use of unity's post-processing stack and experimented a lot with materials to visually define the objects in the stages. I wanted them to be atmospheric, but I also didn't want them to hurt the player's ability to see and understand what was going on. So I used very high contrast particle systems at the edges of certain objects to define them better, and I also would light the spaceships seperately with non-scene lighting in some of the stages. I also really enjoyed making all of the dust, plasma and explosion effects with unity shuriken! 

VFX ART

3D UI ART


# OTHER TASKS:


SOUND DESIGN

## Production Scheduling, Publisher Relations and Market Research

While I was running the live promotion circuit for my game, I also managed my own social media presence, production schedule, and market research efforts. I collected sales data and other metadata about various types of fighting games to try and analyze my niche and understand a budget and release strategy. I also was briefly in talks with 2 publishers who helped me refine my market research and brand identity.  

LIVE PROMOTION

## External Content Commissioning (Musicians)

The only piece of Squareforce that I did not directly create myself was the music- I reached out to several musicians including popular youtube musician Argofox and an independent musician from the UK. Music from both of them appears in the game!

SOCIAL MEDIA MARKETING

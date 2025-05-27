---
title: "Squareforce"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

{{< vimeo 1071247960>}}

#### Platform: PC
#### Engine: Unity
#### Genre: Fighting
#### Team: 1 solodev (me)

This was my first major effort in creating an indie game of my own. I was inspired by the Super Smash Bros. community to create SQUAREFORCE, a flying fighting game where you mix-and-match moves on your spaceship to create a custom moveset. I designed, programmed, and did all the artwork for the game, as well as took it to several conferences where I tabled and talked to journalists and industry contacts to promote the game. I had dozens of people play my game at the various conferences I went to, I attended local game developer events to get feedback. In the end, this served to get me my first paid jobs in the industry- while I did not ultimately release the game, at some point I still might (there are a lot of things I wish to improve about it!).


# DESIGN TASKS:


![Alt text](/ringsEdge.png)


## Design Documentation

I created all the documentation by hand on physical paper- this was my first game, so I didn't yet know about personal knowledge management systems, formal structures/procedures for design documents, or mockup software. Instead I worked out the design of gameplay systems I wanted, and how to technically and artistically achieve my aims. I didn't stick to a specific small list of axioms for my goals, which is also something I would do differently today. But in retrospect, I was basically trying to create a flying Smash Bros. clone where you get to mix and match character normals as you please. 

I also adopted spaceships as the character designs early on, because I knew at the time that I wouldn't be able to animate an entire roster of humanoid characters myself. Another design goal I had was to help new players understand the properties of moves better at a glance than in other fighting games. I did this by making the hurtboxes of moves visible in the actual final art of the game, visible as the red energy called squareforce. A fictional scenario where the players were spaceships gave an in-universe excuse for them to be sending these abstract chunks of energy at each other. Thus, the spaceship characters were an adaptation to my limitations while also serving a design goal.

## Game Systems Design

Other than the core concept of mixing-and-matching normals, I designed a number of other game mechanics to compliment my vision. I really wanted to focus on accessibility because it was my view at the time that 2d fighting games were dwindling in popularity due to their steep learning curve and poor player communication. So, I made the movepool for each character very small (6 normals) and made it so that you only needed to use 2 attack buttons and 4 face buttons in total to play the game. 

I was also trying to design each type of input to work with touch devices in addition to controllers, but this was later scrapped. Many moves were only available through input chording, which I thought would simplify the controls for mobile. Actually I think it confused players in the end, but by then, it was very tightly coupled to other systems in the game and hard to change. I specifically made it so you need to dash into most strong attacks to perform them, chording the input and incurring a possible positional disadvantage for a stronger move. In hindsight, I should have just tested these moves more before committing so hard to a design that would affect every strong attack.

The flying aspect of the game was inspired by 2 things - other fighting games which had longer average combo strings than those in Smash Bros., and the fact that I found it unsatisfying that many high-skill or 'hype' plays in the competition-level Smash metagame often involved SD'ing for the kill. In response to this, I conceived of a design where characters fly around, and thus never need to land and refresh their jump. This made it less costly for the player to press their advantage however. So to restore skillful and risky play, I also made it so that, rather than ring-outs as the primary means of defeating an opponent, you must cause them to crash into the terrain to take a stock. 

Crashing in SQUAREFORCE is like hard knockdown in traditional fighting games, but also a bit like being offstage in Smash. I tried to create ukemi/wakeup options to promote defensive complexity and thoughtful counterplay. In order to make it so that disadvantage always occured at the surface of the floating terrain, I got rid of the level boundaries and made the level wrap in the X and Y (as seen in the similar game Towerfall:Ascension). The disadvantage to all of this was the often-unworkable restrictions it placed on my level designs. It was hard to create a variety of levels while also ALWAYS wrapping in the XY, AND also being believable in-universe as chunks of space debris.

## UX Design
![Alt text](/screenshot1.png)

I designed a 3d menu for the game that was a rough skeuomorphism of putting the ship parts into a sort of builder or hangar. I over-scoped greatly because I couldn't model all of the parts individually, but I was able to create a very tactile and satisfying menu system that many people commented on. I also responded to player confusion about input chording by designing the menu so that you have to input an attack in order to modify it on your loadout. This was a nice idea but in the end I think it made the menu controls too confusing. 

Another interface design I was proud of was the dash ring- I created a ring that expanded around the player while the dash button was held, and it would visually convey the dash 'charging up' while also indicating exactly how far you would go. Using VFX for player communication is something I wanted to do more of, but I liked that I at least made this. Also, through the use of my 3d skeuomorphic GUI, I was able to work around the problem where the Unity version I was using at the time (4.x) was not capable of natively supporting multiple players using the same GUI.

## Content Design and Game Balancing

As stated previously, I designed all the playable stages in the game to wrap in both the X and Y so that it was impossible to camp opponents in a corner. I wanted the disadvantage aspect of the fighting game to occur at the surfaces of the asteroids and other space objects floating in the stages. In the end this was a little confusing and a very big constraint on stage design, I'm not sure I would do it again if I made SQUAREFORCE today. 

As for the moves themselves- it was very fun to create a lot of moves and think critically about how they could be used, both as part of different possible movesets, and in unconventional situations only found in SQUAREFORCE. I created moves that were iterations on the standard fighting game archetypes, such as fast pokes, combo starters, finishers, defensive attacks, and other well known tropes of fighting game move design.


## Focus Testing and Live Promotion

I brought SQUAREFORCE out to many different promotional events. I ran a booth at GDEX, an Ohio convention where gamedevs from Ohio and surrounding states could show their work. I also brought my game trailer out to GDC in California. I also got some professional Smash players to try it at the Cleveland Esports Summit! Most of all, I brought it out regularly to local developer and enthusiast events in both Cleveland and Portland, Oregon many times (I was living in both places). Each time I took notes on the bugs players encountered, moments when they misunderstood what was happening in the game, things they liked or understood right away, and negative possibility spaces for obvious future features. 

![Alt text](/IMG_2473.JPG)

# ENGINEERING TASKS:


![Alt text](/screenshot4.png)

## Game Systems Programming

I built the functionality in code for all the systems outlined above, myself! I ran into some classic game engineering problems at points, since it was my first project.

One of these was the fact that my fast-moving attacks and ships would frequently clip through each other and the terrain. I wrote a custom collision interpolation system to dynamically create meshes at runtime to interpolate between a hurtbox's last frame and current frame. In keeping with my commitment to showing the hurtboxes AS the game artwork, I even considered coloring the runtime-created meshes so that they would look like 3d motion smears (this concept was also being used by another independent smashlike project, Earth Romancer). 

In the end I did not use the 3D smears for artistic purposes, but I used them to manage collision for most of the project's lifetime. Later, I eventually discovered established methods for continuous collision detection (I didn't even know there was a word for it at the time).

## Dynamic Animation System

Because of the fact that my characters all used dynamically chosen attacks, I had to create a lot of animation control systems at runtime, much more than any similar project would. I used Unity's Mecanim system and I made a generalized system of placeholders that could be overridden using an AnimatorOverrideController created dynamically at runtime. This was a wildly complex system architecture that I built to force-fit my animation needs to the garden paths that Unity encourages developers to use for animation. In retrospect, I wish I had known about Unity Playables or even some of the more basic code-only animation control systems available in the Unity API, but these are more obscure and I didn't know about them until I was already a professional in the industry. At the time though, I was very proud of the elaborate and dynamic finite state machines I had built to drive character animation!

## Enemy AI

I also used Mecanim to drive enemy AI behavior in the game. Rather than using it for animations, I additionally leveraged it in an unusual way to also drive behavioral state changes as a pure FSM.  


# ART TASKS:


![Alt text](/screenshot3.png)

## 3D Object Art

I created all of the 3D objects in the game myself! I chose a low poly style, and tried to adapt the aesthetic to my capabilities and what I knew I would be able to make. I was a novice in Blender at the time, but I was able to create a variety of player ships and objects for the stages and 3D GUI screens. I consulted with my artist friends on how to apply character design principles to the ships, such as by adding contrast to important parts of the model and suggesting movement and direction through the silhouettes and shapes of the ships.

## Animation

I also animated all of the attacks myself in addition to adding squash-and-stretch and 'facial animations' to the ships! If I had kept going, I was planning for the lore of the game to include a toy story-like premise in which some bizarre space physics made the ships slightly alive, but only while not being observed (in a nod to quantum physics's wave-particle duality). 

I used Blender shapekeys to animate all of the 'facial expressions' of the spaceships, and I used both Blender and Unity's built-in animation editor to edit all of the squareforce-based attacks. I carefully studied other fighting games frame-by-frame to better understand concepts like key poses, color contrast against background elements, anticipation, and visual communication of the impact of the hits. I also referenced frame timings for attacks in other games to get a sense of how certain lengths of action states would feel to control.

## Environment Art and VFX Art

Since my art was low-poly, I relied a lot on lighting and VFX to visually distinguish my stages from one another. I made use of Unity's post-processing stack and experimented a lot with materials to visually define the objects in the stages. I wanted them to be atmospheric, but I also didn't want them to hurt the player's ability to see and understand what was going on. So I used very high contrast particle systems at the edges of certain objects to define them better, and I also would light the spaceships separately with non-scene lighting in some of the stages. I also really enjoyed making all of the dust, plasma and explosion effects with Unity Shuriken!


# OTHER TASKS:

![Alt text](/splash.png)


## Production Scheduling, Publisher Relations and Market Research

While I was running the live promotion circuit for my game, I also managed my own social media presence, production schedule, and market research efforts. I collected sales data and other metadata about various types of fighting games to try and analyze my niche and understand a budget and release strategy. I also was briefly in talks with 2 publishers who helped me refine my market research and brand identity.  

## External Content Commissioning (Musicians)

The only piece of SQUAREFORCE that I did not directly create myself was the music- I reached out to several musicians including popular YouTube musician Argofox and an independent musician from the UK. Music from both of them appears in the game!

---
title: "Sales Academy VR"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

{{< rawhtml >}} 

<video width=100% controls autoplay>
    <source src="/videos/mp4/store-vr-final-small.mp4" type="video/mp4">
    Your browser does not support the video tag.  
</video>

{{< /rawhtml >}}


Platform: Oculus
Engine: Unity
Genre: Sales Training, Dialogue Based
Team: 1 Engineer (me), 1 3d Artist and Project Manager, content writers from elsewhere in the company

Description: I was the sole engineer and developer on this VR sales training app that I completed for Pulse LLC, who in turn was working under contract with a top 5 tech company to create this serious game. I worked with the artist and project manager to create a dialogue based interactive sales training experience using Dialogue System for Unity as well as a bunch of different oculus-specific unity toolkits such as horizon worlds avatars. The goal of the game's creation was to produce an immersive retail sales training experience to get frontline staff used to sales techniques they would be expected to know. We also had ingame streaming video from the company website, and telemetry to track each user's progress and reflect it ingame from an online account system.

Design Tasks:

FOCUS TESTING

I didn't have much design input on this game, but the one designer task I did do was focus testing. I carefully paid attention and took notes on how playtesters interacted with content, and evaluated how closely it aligned with learning goals. I took note of confusion points and bugs. 

Engineering Tasks:

GAMEPLAY SYSTEMS PROGRAMMING

I programmed all the gameplay in the game, adapting content from oculus-recommended toolkits where needed and handrolling the rest. I made the navigation system and connected all world state logic to dialoguesystem for unity, and all avatar state and animation programming. Lastly I also did all telemetry and server integration.

3D UI/UX PROGRAMMING AND HARWARE ACCELLERATED RENDERING

In addition to programming all of the gameplay, I programmed the 3d GUI. the standards of fidelity for this UI system were quite high as there were many small details that were part of our client's brand identity. I ensured rigorous compliance with GUI mocks even when I had to completely recreate certain effects by hand (like gaussian blur for certain GUI elements). I also made use of oculus's hardware -accellerated gui rendering layer for crisper GUI elements.

LOADING DYNAMIC CONTENT AT RUNTIME / STREAMING VIDEO

I was able to dynamically load streaming video from the same server that powered the rest of the non-game learning material. This was an engineering constraint discovered mid-production cycle as we realized that shipping all video in the app would cause us to exceed oculus's app store size limit- it was scary and initially seemed like a showstopper. I figured out how to manage proper formatting and resolution so that online video would also appear in the same high fidelity as the brand guidelines required.

FACE AND MOTION CAPTURE MUXING

I also created a system to dynamically mix facial capture performance with humanoid body animation so that it would match our content pipeline.

LUA SCRIPTING

all of dialoguesystem for unity's content scripting database is in lua. I was able to rapidly learn enough lua to create content and pass important state info out to the rest of the game, as well as understanding some formatting quirks i would need to know to develop the tool pipeline

TOOLS DEVELOPMENT AND CONTENT PIPELINE COORDINATION

this time, the import process from non-developer friendly narrative content systems like twine was fairly easy to get working with the game. I didn't have to use regex again to parse and rewrite code which was a relief! I created some small editor scripts and directed the content team to use tools that would smoothly integrate with the pipeline- i also gave them special keywords to input that would parse their messages about the scenario into special lua commands so that they could control gamestate from their custom content without me having to write it for them. 


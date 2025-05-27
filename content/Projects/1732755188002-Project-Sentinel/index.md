---
title: "Project Sentinel"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

![Alt text](/compressed/ezgif-2-0a674e7f44dc.png)

#### Platform: PC
#### Engine: Unity
#### Genre: Various (adventure, platformer, management game)
#### Team: 1 Engineer and Designer(me), 1 Narrative Designer, 1 Artist, 1 Project Lead/Design Lead/Producer

I met with a team of creatives at GDC one year who were interested in adapting the work of an author friend of theirs into a climate fiction game. With my ambitions at the time to break into paid work in the industry, and my former life as an environmental science professional, it was a natural fit. I worked with their team on a contract basis consistently for several months, then more sporadically over the following year. I was able to produce and give design input on a number of diverse prototypes, as well as participate in the concept process with the 2d artist and narrative designer. I got the chance to meet and work with some impressive design consultants including former staff of Playdead (developers of LIMBO and INSIDE) and KeithBurgungames.


# DESIGN TASKS:

![Alt text](/ezgif-2-2412e913e268.gif)

## Design Documentation

I coordinated design meetings between the project's vision holder, artist, and narrative designer. I kept track of and updated design documentation as the project evolved. 

## Stakeholder Interviews

I also did multiple interviews of both the Vision holder and narrative designer to ascertain design goals and technical needs the project's gameplay prototypes and tools development needs. I helped to constrain over-scoping and I put schema and structure to the narrative content so it would fit a future narrative pipeline for the game. Over time, the narrative designer and I ended up working together a lot!

## Internal Pitching

In addition to the above, I also was able to pitch some of my own gameplay ideas during certain phases of the project. I was able to use my design knowledge to help the vision holder identify analogues to his gameplay ideas in published projects to help derive further insights for gameplay designs and features. 

![Alt text](/ezgif-3-c866e1c04980.gif)

## Mockups

I mocked some of the concepts on the design document using Figma. This was my first time using the tool, but I would go on to use it more frequently on other projects.

## Content Development and Narrative Content Pipeline Coordination

Over the course of the project, I ended up working more and more closely with the narrative designer, both so that she could understand the new medium she was entering into, and so that I could understand her needs for the content pipeline. Together, we created workflows and design axioms for how to structure and parameterize the content she was writing for the game. 


# ENGINEERING TASKS:

![Alt text](/ezgif-3-dff445d78cff.gif)


## Gameplay Systems Programming and Software Architecture

I programmed all the gameplay systems in all of the prototypes myself. Since the vision for the game was changing rapidly, I needed to make my code as modular and robust as possible to be able to reuse as much of it as I could. I was particularly proud of my internal architecture on the idle game -like prototype, because I created a lot of highly generalizable systems for rapid iteration on very diverse content. I was able to create a very robust and clean architecture that could ingest many types of narrative content with little to no additional scripting required. In hindsight, I may have overbuilt the architecture of this project a little bit. But I was quite proud of it's generalizability. 

## 3D UI/UX Programming

For the 3d globe / orrery prototype, I did a lot of complex math to ensure the dynamic camera and worldspace-based UI would line up properly regardless of edge cases. We also had proportionally accurate distances between planets in this scene, because it wasn't yet known if we would have a section where the player would directly control spacecraft. I was proud to have created such a setup that was robust to floating point precision limitations while performing gameplay operations.

## Tools Development

I did extensive tools development on this project. We kept changing the narrative tools we were using to create the content- we went from Articy:draft, to Inkle Writer, to Twine, to Dialoguesystem for Unity, ultimately ending with a custom system. I had to be pretty fast to adapt to the changing requirements on the tool integration side, and I created many of my own custom adapters and similar features. I also built an external tool to dynamically parse and restructure Inkle script using regex and Winforms while ingesting it into the Unity project assets- which was very difficult! I also made other developer tools such as Unity editor utilities and CSV ingestion/interop scripts.

## Plugin Integration

In addition to changing the external tool setup rapidly, I was also routinely asked to integrate large sections of store-bought asset code quickly. It was a challenge to learn the ins and outs of so many competing code structures and integrate them all without compatibility problems. I developed a very module-based coding style to accommodate the changes, and these lessons would serve me on later engineering projects.

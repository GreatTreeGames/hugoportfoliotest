---
title: "Project Sentinel"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

#### Platform: PC
#### Engine: Unity
#### Genre: Various (adventure, platformer, management game)
#### Team: 1 Engineer and Designer(me), 1 Narrative Designer, 1 Artist, 1 Project Lead/Design Lead/Producer

I met with a team of creatives at GDC one year who were interested in adapting the work of an author friend of theirs into a climate fiction game. With my ambitions at the time to break into paid work in the industry, and my former life as an environmental science professional, it was a natural fit. I worked contracts consistently for several months, then more sporadically over the following year with their team. Eventually, the team dissolved due to legal issues with the founder, but not before I was able to produce and give design input on a number of diverse prototypes, as well as participate in the concept process with the 2d artist and narrative designer. I also got the chance to meet and work with some design consultants from Playdead (developers of LIMBO and INSIDE) and KeithBurgungames.


# DESIGN TASKS:


## Design Documentation

I coordinated design meetings between the project's visionholder, artist and narrative designer, keeping track of and updating design documentation as the project evolved. 

## Stakeholder Interviews

I also did interviews of both the visionholder and narrative designer on design goals and technical needs for both tools and prototypes on the project. I helped to constrain over-scoping and also to help put schema and structure to the narrative content so it would fit a future narrative pipeline for the game. 

## Internal Pitching

In addition to listening and helping with design documentation, scope and tools requirements, I also was able to pitch some of my own gameplay ideas during certain phases of the project. I was also able to use my design knowledge to help the visionholder identify analogues to his gameplay ideas in published projects to help derive further insights for gameplay programming. 

## Mockups

I mocked some of my design ideas as well as some of the concepts on the design document using Figma. 

## Content Development and Narrative Content Pipeline Coordination

Over the course of the project, I ended up working more and more closely with the narrative designer, both so that she could understand the new medium she was entering into, and so that I could understand her needs for content pipeline and how to structure and parameterize the content she was writing for the game. 


# ENGINEERING TASKS:


## Gameplay Systems Programming and Software Architecture

I programmed all the gameplay systems in all of the prototypes myself. Since the vision for the game was changing rapidly, I needed to make my code as modular and robust as possible to be able to reuse as much of it as I could. I was particularly proud of my internal architecture on the idle game -like prototype, I created a lot of highly generalizable systems to create very diverse content ingame in a no-code fashion.

## 3D UI/UX Programming

For the 3d globe / orrery prototype, I did a lot of complex math to ensure the dynamic camera and worldspace-based UI would line up properly regardless of edge cases. We also had accurate distances between planets in this scene, because it wasn't yet known if we would have a section where the player would directly control spacecraft. So I was able to do that while accounting for floating point precision limitations.

## Tools Development

I did extensive tools development on this project. We kept changing the narrative tools we were using to create the content- we went from Articy:draft, to Inkle Writer, to Twine, to Dialoguesystem for Unity, to a custom system. I had to be pretty fast to adapt to changing requirements on the tool integration side, with my own custom adapters and similar features. I created a system to dynamically parse and restructure Inkle script using regex and Winforms while ingesting it into the unity project assets. I also made various editor utilities, and CSV ingestion functionality.

## Plugin Integration

In addition to changing the external tool setup rapidly, I was also routinely asked to integrate large sections of store-bought asset code quickly. It was a challenge to learn the ins and outs of so many competing code structures and integrate them all without compatibility problems, so I developed a very module-based coding style to accommodate the changes.

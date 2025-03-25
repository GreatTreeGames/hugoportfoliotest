---
title: "Virtual Clinic Scenarios"
date: 2024-11-28
draft: false
description: "a description"
tags: ["example", "tag"]
---

#### Platform: HTML5
#### Engine: Unity
#### Genre: Educational, dialogue based
#### Team: 2 game developers(me), 1 web developer, 1 project manager, 3 3d artists, 1 project lead, many subject matter experts and testers


This is an educational game done in under contract with Case Western Reserve at the Francis Payne Bolton School of Nursing. It was also in partnership with CVS and the Institute for Healthcare Improvement (IHI). I was a designer and developer on this project. I currently also do maintenance on the game. Our goal in creating the game was to produce an intuitive learning environment where nurses learn to deliver better geriatric care in Minute Clinics around the US, by using an approach to elder care called the 4 M's system.


# DESIGN TASKS:


## Whiteboarding Sessions

I shared design responsibilities with the other game developer and web developer, and we all participated in whiteboarding sessions to define a design for the game that would meet the learning goals defined by the SMEs and project oversight. I led a series of whiteboarding sessions with the development team, core stakeholders, and 2 SMEs. we whiteboarded possible screen layouts for each prototype as well as mind maps of the most important learning material and how it was structured according to the SMEs. this was early in my career, if I were to lead such a meeting again today, I would probably use Miro to outline the learning goals and Figma to mock screenshots.

## SME Consultation

I was working on the team with someone else from the Cleveland game developer scene and we pitched the idea that the learning platform could be a game. After stakeholder buy-in, we began meeting with Subject matter experts (SMEs) to hash out the design of the game. I initially believed we were replacing existing didactic learning material with a game, but actually a lot of the learning goals had not been defined yet for the learning intervention itself. We talked about what the difference in competencies would be between a hypothetical player who comes into the program, and one who has played the game and knows the skills. As stated, this was accomplished both in whiteboard meetings at the beginning of the project, but also through checking in with the SMEs when they were available. sometimes they disagreed on the material, and in this case it was left to the project stakeholder to give the final say.

## Paper Prototyping

For later prototypes we also advanced to paper prototyping to give stakeholders a better idea of what we were creating. this facilitated more rapid iteration on the way that players would best engage with the learning material in gameplay.

## Whiteboxing

I created all the level geometry in the early levels before it was time to do a more detailed pass with an artist. I also whiteboxed all the prototypes that preceded the final version of Scenarios, which included some very different types of gameplay including a character creator and isometric office view

## User Testing

I coordinated playtest sessions with nurse practitioners at the college to collect their thoughts on the gameplay and what should be improved. I told other observers what to watch for and take notes on while we physically observed people play the game. 

## UI Design

Once we got the go-ahead to adapt our third prototype into the full game, the other game dev on the staff and I both worked on many different versions of the GUI for the game. We created several versions of the radial menu seen here, and iterated on which ones would best show relationships between the content without explicitly telling the player. We used rules of graphic design and composition to best select what shapes and colors to use to help players form associations implicitly. we also created a 'mini map' on the scrollbar of the encounter text so the player has a visual sense of where and how much of the encounter has been modified by their actions.

## Prototyping Rounds

We did 3 prototypes of the game - one of which was a first - person game where you click visible signs of mobility issues on the patient, one where you create a patient as a puzzle for other players to solve, and one where you step through the encounter changing the language to be more age friendly. since the first one was needlessly timing-based, and coupled strongly to only focus on mobility issues (not medication ones for instance, that couldn't be easily seen in 3d), and since the second was explosively unbounded in terms of the content players would be able to create and we weren't sure if that would be accurate for educational purposes at that point, we chose our 3rd prototype to develop into the final game

## Art Pipeline Definition

We had many issues with the format, exposed design parameters, and detail level of the humanoid animations in the game. I took it upon myself to work with the artist on the team to more carefully define standards for how the 3d motion data should be formatted to help improve process flow during development.

## Art Style Development

The other gamedev, artist, and myself carefully chose a visual style for our game based on usability and cultural proximity to similar types of learning material. at first, we made abstract, color-field like characters and environments to cut down on visual complexity and evoke the look of a physical safety card. eventually though, we were asked by stakeholders to change to a look that focused on realism, presumably to better match video training material.


# ENGINEERING TASKS:


## UI Programming

The other gamedev and I did all the programming of the UI elements we designed. It was important to strike a balance between responsive animated UI and UI that would stay in the same place while being interacted with. also we custom-created a lot of radial layout functionality and nonstandard button colliders to match our initial UI design.

## Core Gameplay Systems

In addition to the UI programming, we also programmed all of the camera, character agent, scenario state management, and remote server infrastructure for the game. We initially thought that SMEs would be continuously wanting to add new content, so we created a CRUD system to help non-programmers edit ingame patient scenarios and load them ingame. ultimately this went unused, but I still learned a lot about server-based content loading in unity. 

## Mocap Custom Hardware Configuration

We set up a custom impromptu mocap studio at the college using a series of off-the-shelf parts such as XB1 kinect cameras. Using open source tools, we captured 3d motion data from several actors and medical experts who knew how to do the irregular walking gait that would be featured in the game. We used some of this animation, but it was also very messy and low-fidelity, so the artist manually created some other humanoid animations.

## Mocap Data Cleanup

I helped the artist do a bit of the cleanup of the captured animation. IK of the feet was a bit messy and there were a lot of excess keyframes. in the end it was mostly useful as a block-out for the handcrafted animations the artist made.

## 3D Animation Blending

I scripted all of the blending of the 3d animations in the game using unity's mecanim state machine. I also manually programmed some of the pathing for the characters

## FSM Management

there were a few other state machine driven systems in the game. due to having just worked on Squareforce before this game, I was used to unity's FSM/mecanim system and did every state machine in the project myself.

## Loading Dynamic Content From the Server at Runtime

As previously mentioned, scenario data including text and animation sequences were loaded dynamically at runtime. At this point in my career I hadn't done any server management yet, so my fellow gamedev programmed the API endpoint while I programmed the content ingestion on the unity side.

## CRUD Content Pipeline Setup

I created a visual CRUD application to constrain input to make sure that non-technical users could input valid scenario changes without breaking the game. ultimately the SMEs were not available to do this for most of the project's lifecycle, and we ended up just filling in most of the content ourselves anyway.

## Web Platform Deployment and Optimization

We deployed to a number of tightly constrained systems over the course of the game's life cycle. we initially deployed desktop builds, but switched to web builds due to internal legal restrictions at our client's worksite. This was a challenge as the web platform was much more memory constrained and difficult to optimize for, and also came with unseen gotchas like web rendering systems only respecting a lower number of bone weights, meaning some animation had to be redone. The three of us (2 gamedevs and artist) created a system to asynchronously load all of the character's textures, so by doing that and atlassing/downrezzing some others, we were able to improve the performance of the game on these machines. 

## Telemetry

We also programmed a lot of telemetry into the game to report certain ingame actions from the player to the server. My gamedev colleague did most of this, but I helped and was able to do similarly complex tasks on our next project together.


# OTHER TASKS:


## Scientific Writing Assistance

I made use of my former life as a science professional to help SME's and the data team to summarize/contextualize our efforts in the schema of study design and formal paper formatting. I also helped to add my perspective as a game developer to the discussion and analysis components of the paper.

## Public Speaking and Tabling at Conferences

When showing our prototypes at the QSEN medical conference, I was chosen by the team to deliver a short speech about our efforts. I like public speaking and summarizing scientific topics, so I happily volunteered. It was nice to meet so many people!

## Voice Acting

I also provided VO for supplemental materials on the project including video tutorials for the game and other aspects of the learning intervention. I tried to adopt a subdued and welcoming tone similar to an educational segment narrator. I also set up a small recording area in my home office with some audio foam, and I cleaned and cut all the audio myself using audacity on linux.

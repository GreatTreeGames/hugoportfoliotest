---
title: "Virtual Clinic Competency"
date: 2024-11-28
draft: false
description: "a description"
tags: ["Web", "Mobile"]
---

{{< vimeo 1071247942 >}}

#### Platform: Android, IOS, HTML5
#### Engine: Unity
#### Genre: Educational, Dialogue based
#### Team: 2 game developers(me), 1 web developer, 2 3d artists, 1 project lead, many subject matter experts and testers

This is an educational game done in under contract with Case Western Reserve at the Francis Payne Bolton School of Nursing. It was also in partnership with CVS and the Institute for Healthcare Improvement (IHI). I was the design lead and a developer on this project. I currently also do maintenance on the game. Our goal in creating this game was to improve upon virtual clinic scenarios by lowering cognitive load and making gameplay more intuitive, so nurses could complete the material quicker and easier, and focus more on the learning material itself while playing. We also wanted to create an interface that would be more suitable to mobile devices.


# DESIGN TASKS:


## Figma Mockups, Leading Design Session with Stakeholders

I was much more prepared this time to deliver design insights to the visionholders and project lead. I took the lead in designing this version of the experience, and I presented all of my designs as mockups in Figma or blender along with small prototypes of the gameplay systems that attracted the most stakeholder interest. I also led a design retreat where I guided all of the instructional design staff, SMEs, and project managers through brainstorming sessions about how things went with the first version of the virtual clinic and what we would want out of another such game, surfacing their most key concerns and insights and offering my best design responses backed up by evidence and rationale. 

## Internal Pitching and Revision Cycles

![Alt text](/hugoportfoliotest/wire1-3.png)

I pitched 3 different prototypes after the design retreat. Once decided on a direction, I checked in repeatedly with the core team to ensure we were still aligned with their vision and what they wanted to do. 

## Incorporation of Education Design Techniques

I quickly began to align with and request additional time with the instructional design staff: I began to realize that these professionals are very similar to game designers in terms of what they are trained to do. I was also able to learn some instructional design words for contemporaneous concepts in game design, and it helped me communicate with the rest of the team better.

## UI Design (Symbols)
![Alt text](/hugoportfoliotest/Icons.png)

One key idea I wanted to emphasize was to create a strong visual shorthand for the types of age-related abnormalities that the nurses playing the game would be learning. Just like in other games, developing a consistent visual shape-language is great for player knowledge retention.

## SME Consultation

As before, we checked in whenever we could with the SMEs to ensure we were still creating content that appropriately reflected the learning material and skills to be built by the playerbase. 


# ENGINEERING TASKS:

![Alt text](/hugoportfoliotest/connections.png)

## UI Programming

we designed the GUI systems in this version of the virtual clinic to be much more modular and easy to understand at a glance. We took extra care to ensure that a manageable amount of relevant information was onscreen at any one time. I worked with my fellow game developer colleague to define the internal structure of the encounter in a more robust way that was ultimately more extensible than what we did in virtual clinic scenarios. 

## Core Gameplay Systems

Each core gameplay system was more strongly representative of a single line of inquiry that real nurses are meant to follow while going through the process of diagnosing age-related abnormalities. Focusing very strongly on interactions that were easy to input and easy to understand at a glance, I created a modular camera and GUI 'docking' system where modular stages of gameplay could request sections of screenspace to use at a time. 

## Web Platform Deployment and Optimization

Having a better understanding of what platforms we intended to ship to this time, we were better able to optimize polycount and texture memory for both web and mobile. I was also able to handle more of the web deployment infrastructure myself this time. 

## Mobile Platform Deployment and Optimization

we also deployed cross-platform to iOS and android. Many of our interactions were clear and simple enough to translate easily with minor tweaking- however, we were not so lucky with accessibility. We were required by internal rules at case to equip any software we released with appropriate screenreader accessibility features for the visually impaired. While the specifics of these requirements did not seem designed for games, we followed them as best as we could. My fellow gamedev heroically did a lot of the work in moving both apple's core screen reader nodes as well as android's, but I helped. Unity's more advanced screenreader support did not roll out until unity 2023, so we had to retrofit and roll all of this functionality ourselves- it was a big lift!

## Custom Spline-Based Character Movement System

We created a simplified character movement system for the small characters in the 3d scene section of the game. I learned a lot about spline math from my developer friend, who helped me port a generalized spline system into unity from a separate software project and adapt it to work with our custom animation framework (whose state was driven by the dialogues we created the architecture for as well).

## Cinemachine False Perspective System

I incorporated unity's cinemachine into my screen element docking system, and utilized false perspective to make it so that certain 3d scene elements would appear in a similar manner to GUI objects.

## Loading Content Dynamically from Server

as was the case last time, we were loading dynamic content at runtime from our game's server, and I programmed the data ingestion into unity as before. this time we got a lot more activity from the SMEs who were able to dynamically submit changes to our server and experience live updates without having to redeploy the app!


# OTHER TASKS:

![Alt text](/hugoportfoliotest/assessmentsv4.png)


## Hiring and Managing Art Staff

Tragically, the artist on our team from the previous game passed away between development of the versions of the virtual clinic. After taking time to grieve, it was my responsibility to find a way to get new artwork done quickly as the college's formal hiring process would take too long before release of the game. I utilized my company and subcontracted 2 3d artists from my career network. In so doing, I got some experience managing employees, handling their taxes and paperwork, and delegating responsibilities to them. All of my previous struggles defining art pipelines paid off, as I feel I was able to communicate project requirements and scope to them very clearly and get great results.

## Art Cleanup

In the interim time, I was able to do a bit better than the standard 'programmer artwork.' Using Blender, I was able to create the 3d environment that was ultimately used in the final game. I used what I learned from the previous version of the game to do texture atlasing to save memory.

## Scientific Writing Assistance

As with the previous version of the virtual clinic, I once again helped the data science team to compile results for their formal scientific journal article. I helped to write some of the sections of the paper.

## Public Speaking and Tabling at Conferences

We showed this version of the virtual clinic at the 2022 serious play conference in Florida. Myself, the other game developer, and the web developer all went on the trip together and delivered our results along with gameplay and design rationale in a conference talk to the audience. It was great to meet other devs of serious games, and we were honored to have our game featured in the conference speaker lineup!


![Alt text](/hugoportfoliotest/gaits.gif)

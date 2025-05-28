---
title: "Virtual Clinic Competency"
date: 2025-05-28
draft: false
description: "a description"
tags: ["Web", "Mobile"]
---

{{< vimeo 1071247942 >}}

#### Platform: Android, IOS, HTML5
#### Engine: Unity
#### Genre: Educational, Dialogue based
#### Team: 2 game developers(me), 1 web developer, 2 3d artists, 1 project lead, many subject matter experts and testers

This was an educational game done under contract with Case Western Reserve University at the Francis Payne Bolton School of Nursing. It was also in partnership with CVS and the Institute for Healthcare Improvement (IHI). I was the design lead and a developer on this project. I currently also do maintenance on the game. Our goal in creating this game was to improve upon Virtual Clinic Scenarios by responding to a few key pain points and feedback from our target audience and SMEs. Our new design was an attempt to lower cognitive load and make gameplay more intuitive. This way, the nurses could complete the material quicker and easier, and also focus more on the learning material itself while playing. Additionally, we wanted to create an interface that would be more suitable to mobile devices.


# DESIGN TASKS:


## Figma Mockups, Leading Design Session with Stakeholders

I was much more prepared this time to deliver design insights to the vision holders and project lead. I took the lead in designing this version of the experience, and I presented all of my designs as mockups in Figma or Blender along with small prototypes of the gameplay systems that attracted the most stakeholder interest. I led a design retreat where I guided all of the instructional design staff, SMEs, and project managers through brainstorming sessions about how things went with the first version of the Virtual Clinic, and what we would want out of another such game. I surfaced their most key concerns and insights, and offered my best design responses backed up by evidence and rationale. 

## Internal Pitching and Revision Cycles

![Alt text](/wire1-3.png)

I pitched 3 different prototypes after the design retreat. Once the vision holders and management decided on a direction, I checked in repeatedly with the core team to ensure we were still aligned with their vision and what they wanted to do. 

## Incorporation of Education Design Techniques

I quickly began to align with and request additional time with the instructional design staff: I began to realize that these professionals are very similar to game designers in terms of what they are trained to do. I was also able to learn some instructional design words for contemporaneous concepts in game design, and it helped me communicate with the rest of the team better. I now often say that the disciplines of instructional design and game design are "like twins separated at birth!"

## UI Design (Symbols)
![Alt text](/Icons.png)

One design goal I had was to create a strong visual shorthand for the types of age-related abnormalities that the nurses needed to learn. Just like in other games, developing a consistent visual shape-language is great for player knowledge retention. We ended up creating the icons shown here for each of the age-related abnormalities and possible results of assessment- the goal is to aid nurses in memorizing the assessment types, and which procedures follow each type of assessment result.

## SME Consultation

As before, we checked in whenever we could with the SMEs to ensure we were still creating content that appropriately reflected the learning material and skills to be built by the playerbase. It was surprising just how often there was internal debate on which learning principles and perspectives were most important. I think that the mere act of trying to design better lesson material helped the SMEs to better formalize knowledge that they had gained over decades of medical practice!


# ENGINEERING TASKS:

![Alt text](/connections.png)

## UI Programming

We designed the GUI systems in this version of Virtual Clinic to be much more modular and easy to understand at a glance. We took extra care to ensure that a manageable amount of relevant information was onscreen at any given time, and that there was always only one intended point of focus. I worked with my fellow game developer colleague to define the internal structure of the encounter in a more robust way- one that was ultimately more extensible than what we built for Virtual Clinic Scenarios. 

## Core Gameplay Systems

We designed each core gameplay system to be more strongly representative of a single line of inquiry than in Virtual Clinic Scenarios. Real nurses are meant to follow these procedures while going through the process of diagnosing age-related abnormalities. Focusing very strongly on interactions that were easy to input and understand at a glance, I created a modular camera and GUI 'docking' system where modular stages of gameplay could request sections of screenspace to use at a time. 

## Web Platform Deployment and Optimization

Having a better understanding of what platforms we intended to ship to this time, we were better able to optimize graphics performance for both web and mobile. I was also able to handle more of the web deployment infrastructure myself this time, and I designed much of the current API backend myself. 

## Mobile Platform Deployment and Optimization

We also deployed cross-platform to iOS and Android. Many of our interactions were clear and simple enough to translate easily with minor tweaking- however, we were not so lucky with accessibility. We were required by internal rules at Case to equip any software we released with appropriate screen reader accessibility features for the visually impaired. While the specifics of these requirements did not seem designed for games, we followed them as best as we could. My fellow gamedev heroically did a lot of the work in integrating both apple's core screen reader nodes as well as android's, but I helped. Unity's more advanced screenreader support did not roll out until Unity 2023, so we had to retrofit and roll all of this functionality ourselves- it was a big lift!

## Custom Spline-Based Character Movement System

We created a simplified character movement system for the small characters in the 3D scene section of the game. I learned a lot about spline math from my developer friend, who helped me port a generalized spline system into Unity from a separate software project and adapt it to work with our custom animation framework. We changed the animation system's architecture so that it's state would be completely driven by the current dialogue line with no side effects.

## Cinemachine False Perspective System

I incorporated Unity's Cinemachine into my screen element docking system, and utilized false perspective to make it so that certain 3d scene elements would appear in a similar manner to GUI objects. Even though I still had to line up a lot of 3D geometry in false perspective with UI elements, Cinemachine is significantly easier to use than manually doing all the math to move the camera.

## Loading Content Dynamically from Server

As was the case last time, we were loading dynamic content at runtime from our game's server, and I programmed the data ingestion into Unity as before. This time we got a lot more activity from the SMEs, who dynamically submitted changes to our content so that our players could experience live content updates without us having to redeploy the app!


# OTHER TASKS:

![Alt text](/assessmentsv4.png)


## Hiring and Managing Art Staff

Tragically, the artist on our team from the previous game passed away between development of the two versions of the Virtual Clinic. This was sudden and unexpected, and none of us quite knew how to respond at the time. After taking the time to grieve, we were presented with the practical problem of getting new quality art staff onto the team quickly. The college's formal hiring process would take too long before release of the game, so as a contractor under my own company, I made this my responsibility.

I had never hired staff before or directly been anyone's boss. But in response to this issue, I quickly worked my contacts in the local gamedev scene and contracted 2 3D artists from my career network. In so doing, I got some experience managing employees, handling their taxes and paperwork, and delegating responsibilities to them. All of my previous struggles defining art pipelines paid off, as I feel I was able to communicate project requirements and scope to them very clearly and get great results.

## Art Cleanup

In the interim time, I was able to do a bit better than the standard 'programmer artwork.' Using Blender, I was able to create the 3D environment myself that was ultimately used in the final game. I used what I learned from the previous version of the game to do texture atlasing to save memory.

## Scientific Writing Assistance

As with the previous version of the Virtual Clinic, I once again helped the data science team to compile results for their formal scientific journal article. I helped to write some of the sections of the paper too!

## Public Speaking and Tabling at Conferences

We showed this version of the Virtual Clinic at the 2022 Serious Play Conference in Florida. Me, the other game developer, and the web developer all went on the trip together. We presented our results along with gameplay and design rationale in a conference talk to the audience. It was great to meet other devs of serious games, and we were honored to have our game featured in the conference speaker lineup!


![Alt text](/gaits.gif)

---
title: My first 3D Project
layout: post
post-image: 'https://user-images.githubusercontent.com/20461089/210930782-3cbd9ee2-71a1-4b4a-b2ee-234e32fe5b15.png'
description: One of my current projects that I am working on as a lead programmer on a team.
tags:
- Marbles
- Video Game
- Programming
---

This is a project I am working on with Artifex Interactive. It is my most recent project as of writing this blog, I lead the Project Management by keeping tabs on tasks and their deadlines while also leading the Programming team day-to-day. I also designed the game’s Player Controller for cross-platform compatibility, you can see some if it in action in the video below.

<video src="https://user-images.githubusercontent.com/20461089/210931056-89fcf57a-8410-4388-a89a-79c7f657d088.mp4" controls="controls" autoplay="autoplay" muted="muted" loop="loop"></video>

The player will be able to play the game with only two inputs, a joystick/WASD input for movement and a single button input for jumping. With simplified controls like this, we can easily have the game picked up by anyone and just start playing without much knowledge of games in general. This also makes it very compatible with Mobile and Console porting in the future. The thought process behind my design was to have it on mobile where your thumbs will naturally lay on the screen when holding a device in landscape. The other idea was co-op play on the switch platform where you can share joycons that only have two shoulder buttons, a single joystick, and 4 face buttons to use semi comfortably.

Due to the only input being for movement and jumping, the problem that needed solving was the Camera Behavior. I solved this problem by having the camera face the direction the marble's velocity movement Yaw wise. It uses Lerp functions on the rotators and smoothes out the spring-arm rotation while it trys to match the velcocity vector direction while also using the shortest route for it's smoothing. The marble also has custom gravity since it needed to stick to any surface. The camera also has lerps for Pitch and Roll movement to smooth out its camera movement when going up/down or the side of walls.

<video src="https://user-images.githubusercontent.com/20461089/210931067-72e83c67-1a8c-400d-b4b0-07c0382d5469.mp4" controls="controls" autoplay="autoplay" muted="muted" loop="loop"></video>

In the video above I showed a random snippet of some of my prototyping with Unreal Engine's Blueprint system. It makes it easy to iterate on designs by doing everything through visual based code before refactoring it into C++ for optimizations. It saves a lot of development time having to debug in blueprints rather than jumping back and forth between Unreal and an IDE constantly, so I instructed the team to follow this procedure and have had lots of success in the team keeping to their deadlines.

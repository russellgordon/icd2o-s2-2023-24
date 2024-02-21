---
{"dg-publish":true,"permalink":"/concepts/first-person-perspective-proximity-and-scoring/","tags":["C2.1","C2.3","C2.4","C2.5"],"dgHomeLink":true,"dgShowToc":true}
---


# First Person Perspective, Proximity, and Scoring

## Overview

To explore a 3D world interactively – as in a game – the "hero" character needs to be able to move through a scene.

The purpose of this tutorial will be to set up movement using the "WASD" keyboard pattern:

|key|action|
|-|-|
|W|Move forward|
|S|Move backwards|
|A|Slide to the left|
|D|Slide to the right|

Turning will be tied to the arrow keys:

|key|action|
|-|-|
|←|Turn left|
|→|Turn right|

To do this we will build a simple world where our hero is a bunny rabbit, whose job is to find and hug as many ogres as possible.

Ogres don't like to hug though, so when the rabbit gets close, they disappear.

Each time this happens, the score will increase.

It will look something like this:

![Screenshot 2024-02-20 at 9.02.27 PM.png](/img/user/Media/Screenshot%202024-02-20%20at%209.02.27%E2%80%AFPM.png)

This is clearly a non-sensical example, but after learning the techniques required to build this world you could surely build your own more interesting mini-games.

Let's get started!

## Lesson

In this case, the lesson will be provided [in video form](https://youtu.be/NkWOZrwL5aA) – please click the cover image below to watch the video on YouTube:

[![Screenshot 2024-02-20 at 9.04.25 PM.png](/img/user/Media/Screenshot%202024-02-20%20at%209.04.25%E2%80%AFPM.png)](https://youtu.be/NkWOZrwL5aA)

## Optional reading

For more details on events – specifically related to collision and proximity – you can [review these notes](https://docs.google.com/presentation/d/1gezpwu1o75FShUS69x48ZLM6C4D3xLISR5lfwt-OSuo/edit#slide=id.g3d02c045dc_0_152):

[![Screenshot 2024-02-20 at 9.13.23 PM.png](/img/user/Media/Screenshot%202024-02-20%20at%209.13.23%E2%80%AFPM.png)](https://docs.google.com/presentation/d/1gezpwu1o75FShUS69x48ZLM6C4D3xLISR5lfwt-OSuo/edit#slide=id.g3d02c045dc_0_152)

## Exercise

To practice applying the same concepts as shown in the lesson in another context, create a new world where the score changes based on the hero's proximity to items.

One possible example: a simple treasure hunt, where the user must collect certain items to finish the game.

When finished, share your results [on Notion](https://notion.so).






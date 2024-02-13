---
{"dg-publish":true,"permalink":"/concepts/movement-in-3-d-space/","tags":["C1.1","C1.2","C2.4"],"dgHomeLink":true,"dgShowToc":true}
---


# Movement in 3D Space

## Introduction

Before you keep reading, have a look at this [overview of camera movements](https://www.youtube.com/watch?v=GbnYBmqBbKA) from movies and television.

Here are the specific camera movements mentioned – all of these are possible to do in Alice:

- the [pan](https://youtu.be/GbnYBmqBbKA?t=47)
- the [tilt](https://youtu.be/GbnYBmqBbKA?t=69)
- the [zoom](https://youtu.be/GbnYBmqBbKA?t=85) 
- the [dolly](https://youtu.be/GbnYBmqBbKA?t=90)
- the [pedestal shot](https://youtu.be/GbnYBmqBbKA?t=113)
- the [crane or boom shot](https://youtu.be/GbnYBmqBbKA?t=123)

## Position and Orientation

The centre point of an object marks it's current *position*.

The centre point of an object is the intersection of its three axes:

![Screenshot 2023-02-21 at 1.33.01 PM.png|400](/img/user/Media/Screenshot%202023-02-21%20at%201.33.01%20PM.png)

- <span style="color:green;">Green</span> axis: up/down
- <span style="color:red;">Red</span> axis: right/left
- <span style="color:blue;">White/Blue</span> axis: forward/backward

The white axis indicates an object's *orientation*.

An object's orientation can be determined by which way it's white axis is pointing.

## Movement

Moving an object in Alice will change its *position*, but never it's orientation.

In each of the three movement examples below, notice that the direction of the white axis (orientation) never changes.

### Move Up/Down

Here a boulder moves up (along <span style="color:green;">green</span> axis), pauses, then moves down, and pauses.

This action is repeated three times:

![Move Up - Down copy.gif|450](/img/user/Media/Move%20Up%20-%20Down%20copy.gif)

Here is the code that produced the animation shown above:

![Pasted image 20230221134629.png|450](/img/user/Media/Pasted%20image%2020230221134629.png)

### Move Right/Left

Here a boulder moves right (along <span style="color:red;">red</span> axis), pauses, then moves left, and pauses.

This action is repeated three times:

![Move Right - Left copy.gif|450](/img/user/Media/Move%20Right%20-%20Left%20copy.gif)

Here is the code that produced the animation shown above:

![Pasted image 20230221135524.png|450](/img/user/Media/Pasted%20image%2020230221135524.png)

### Move Forward/Backward

Here a boulder moves forward (along white axis), pauses, then moves backward (along <span style="color:blue;">blue</span> axis), and pauses.

This action is repeated three times:

![Move Forward - Backward copy.gif|450](/img/user/Media/Move%20Forward%20-%20Backward%20copy.gif)

Here is the code that produced the animation shown above:

![Pasted image 20230221134408.png|500](/img/user/Media/Pasted%20image%2020230221134408.png)

## Orientation

*Turning* or *rolling* an object changes it's *orientation*, but never it's position.

In each of the three examples below, notice that the centre point of the object (position) never changes.

### Turn Right/Left

Here a boulder turns right, pauses, then turns left, and pauses.

This action is repeated three times:

![Turn Right - Left copy.gif|450](/img/user/Media/Turn%20Right%20-%20Left%20copy.gif)

Turning right/left can be thought of as a *rotation around the  <span style="color:green;">green</span> axis*.

Here is the code that produced the animation shown above:

![Pasted image 20230221140816.png|400](/img/user/Media/Pasted%20image%2020230221140816.png)

### Turn Forward/Backward

Here a boulder turns forward, pauses, then turns backward, and pauses.

This action is repeated three times:

![Turn Forward - Backward copy.gif|450](/img/user/Media/Turn%20Forward%20-%20Backward%20copy.gif)

Turning forward/backward can be thought of as a *rotation around the  <span style="color:red;">red</span> axis*.

Here is the code that produced the animation shown above:

![Pasted image 20230221140554.png|400](/img/user/Media/Pasted%20image%2020230221140554.png)

### Rolling Right/Left

Here a boulder rolls to the right, pauses, then rolls left, and pauses.

This action is repeated three times:

![Roll Right - Left copy.gif|450](/img/user/Media/Roll%20Right%20-%20Left%20copy.gif)

Rolling right/left can be thought of as a *rotation around the white/<span style="color:blue;">blue</span> axis*.

Here is the code that produced the animation shown above:

![Pasted image 20230221141533.png|400](/img/user/Media/Pasted%20image%2020230221141533.png)

## Movement and Orientation

An object can, of course, both move (change it's position) and turn or roll (change it's orientation) at the same time.

### Do Together

This is a *do-together* tile.

![Screenshot 2023-02-21 at 2.56.42 PM.png|600](/img/user/Media/Screenshot%202023-02-21%20at%202.56.42%20PM.png)

Any statements placed inside a do-together tile will run at the same time.

> [!NOTE]
> Usually, the *duration* for statements placed inside a do-together tile are made to be identical.
> 
> The duration for a tile in Alice can be set using the *add detail* drop-down:
> 
> ![Screenshot 2023-02-21 at 3.14.10 PM.png|300](/img/user/Media/Screenshot%202023-02-21%20at%203.14.10%20PM.png)

## Exercises

The [pan](https://youtu.be/GbnYBmqBbKA?t=47), [tilt](https://youtu.be/GbnYBmqBbKA?t=69), and [zoom](https://youtu.be/GbnYBmqBbKA?t=85) camera movements are all pretty straightforward to implement in Alice, if you have carefully studied the [[Concepts/Movement in 3D Space#Position and Orientation\|position and orientation examples]] given above.

The goal of these exercises is for you to be comfortable with understanding how to implement a semi-circular [dolly](https://youtu.be/GbnYBmqBbKA?t=90) shot, like this:

[![Screenshot 2023-02-21 at 3.18.47 PM.jpg|700](/img/user/Media/Screenshot%202023-02-21%20at%203.18.47%20PM.jpg)](https://www.youtube-nocookie.com/embed/8piXdy6_riI)

Camera movements of this nature are commonly used in movies or television shows to establish for the audience what a scene looks like.

### Exercise 1

First, [download the starter world](https://www.russellgordon.ca/lcs/2023-24/icd2o/Movement_and_Orientation.a3p.zip):

[![Pasted image 20230221163548.jpg](/img/user/Media/Pasted%20image%2020230221163548.jpg)](https://www.russellgordon.ca/lcs/2023-24/icd2o/Movement_and_Orientation.a3p.zip)

Notice that:

- there is a yellow sphere with its axes showing at the bottom of the frame
- there is a red sphere with its axes showing at the top of the frame
- there is a semi-transparent torus (essentially a circular path) connecting the two spheres

Your goal is to get the yellow sphere to follow the path of the torus, so that it ends up in the same position as the red sphere, like this:

[![Screenshot 2023-02-21 at 3.31.51 PM.jpg](/img/user/Media/Screenshot%202023-02-21%20at%203.31.51%20PM.jpg)](https://www.youtube-nocookie.com/embed/ejzzM82pxAA)

Carefully consider how the sphere will need to change it's [[Concepts/Movement in 3D Space#Movement\|position]] *and* [[Concepts/Movement in 3D Space#Orientation\|orientation]].

When you complete this execise, immediately make a post [on Notion](https://notion.so).
- Carefully explain *how* and *why* the code you wrote works.
- In particular, identify problems you encountered while completing the exercise, and how you resolved them.

### Exercise 2

Now apply the same concepts to create this camera pan movement within the same scene: 

[![Screenshot 2023-02-21 at 3.18.47 PM.jpg|700](/img/user/Media/Screenshot%202023-02-21%20at%203.18.47%20PM.jpg)](https://www.youtube-nocookie.com/embed/8piXdy6_riI)

You can use the camera marker named `startingCameraView` to get the camera in the correct position to begin.

Share your progress and results [on Notion](https://notion.so).

### Exercise 3

Finally, either:

- create a brand new Alice world
- modify one of your existing worlds

... and create a camera movement like you did in exercise 2.

To do so, you will need to carefully arrange objects in the scene, likely making good use of [one-shot procedures](https://www.alice.org/resources/how-tos/using-one-shots/).

And again, please share your progress and results [on Notion](https://notion.so).
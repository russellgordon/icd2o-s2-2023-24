---
{"dg-publish":true,"permalink":"/concepts/functions-and-expressions/","tags":["C1.2","C1.3","C1.4"],"dgHomeLink":true,"dgShowToc":true}
---


# Functions and Expressions

## Objects in 3D Space

Objects in Alice have a centre point.

![Pasted image 20230214135931.png|300](/img/user/Media/Pasted%20image%2020230214135931.png)

That centre point is the intersection of three axes:

- <span style="color:green;">Green</span> axis: up/down
- <span style="color:red;">Red</span> axis: right/left
- <span style="color:blue;">Blue</span> axis: forward/backward

For people, this centre point is often positioned at the bottom of the model:

![Pasted image 20230214140415.png|300](/img/user/Media/Pasted%20image%2020230214140415.png)

Distances between objects are measured between their centre points:

![Pasted image 20230214140546.png](/img/user/Media/Pasted%20image%2020230214140546.png)

### Exercise: Shrine Time

With that in mind, consider the following scene:

![Pasted image 20230214140638.png](/img/user/Media/Pasted%20image%2020230214140638.png)

What if we wanted the person to move *over* to the shrine, but not go inside?

Consider this carefully: remember our discussion earlier this year about algorithms.

Instructions must be precise – computers are not able to “guess” at what we want them to do.

> [!TODO]
> If you are present in class, pair up to your randomly assigned partner.
> 
> If you are reading this outside of class, pause and make a point form plan before continuing to read.
> 
> Thinking about the centre points of objects, what are the steps involved in getting the person over *to* the shrine, but not having them go inside?

#### Discussion: An initial plan

After some thought, you may written something like the following:

- Make the person walk over to the shrine.

If your plan looks like this – it is *not* detailed enough! 😅

Remember, objects in a 3D space like Alice have distances between them measured from their centre points:

![Pasted image 20230214140546.png](/img/user/Media/Pasted%20image%2020230214140546.png)

#### Discussion: A more detailed plan

A revised plan might look like this:

- point person in the direction of the shrine
- move person to "edge of shrine"

Find edge of shrine by:

- finding distance from person to shrine
	- subtracting half the width of the shrine

Let's program that together now. 

You can [download the starter world here](https://www.russellgordon.ca/lcs/2023-24/icd2o/Person%20and%20Shrine.a3p.zip).

> [!NOTE]
> 
> If you are reading this outside of class time, you can [watch this short video to see how this mini-task was completed](https://www.yout-ube.com/watch?v=O80VYKY1Kk8).

In completing this task, we made use of two new ideas: functions and expressions.

## Functions

In Alice, a **function** is used to get information we need about:

- the properties of objects
	- e.g.: *Is the snowwoman's face red?*
- the relationship between one object and another
	- e.g.: *What is the distance between the mummy and the pyramid?* 
- a current condition
	- e.g.: *What key (on the computer keyboard) was just pressed?*

When a function is used to ask a question or perform a computation, an answer is returned.

This answer is called a **value**.

The **type** of the value depends on what the function does for us.

In the example we completed earlier, we expected to get a numeric value because the function retrieved a distance. 

That distance could be a whole number, such as 3 meters.

It could also be a fractional value, such as 1.2 meters.

Other value types include:

- Boolean 
	- `true`, `false`
 - String 
	 - "Oh, Yeah!"
 - Object
	 - snowman, helicopter, et cetera
 - Position in the world
	 - `(0, 0, 0)` – the center of an Alice world 

## Expressions

An **expression** is a math or logical operation on numbers or other types of values.

Alice provides math operators for common mathematical expressions:
-   addition  `+`
-   subtraction `−`
-   multiplication `⨉` 
-   division   `÷`

We can combine functions and  expressions to do _calculations_ that are responsive to the location of objects in a scene.

Return to Alice now and move the shrine to a new position, something like what is shown in the animation below:

![Moving the Shrine.gif](/img/user/Media/Moving%20the%20Shrine.gif)

Run the program again. Did the person still go to the edge of the shrine?

This works because we used a procedure to turn toward the shrine – whereever it happens to be in the world:

![Screenshot 2023-02-14 at 3.06.17 PM.png|300](/img/user/Media/Screenshot%202023-02-14%20at%203.06.17%20PM.png)

Additionally, the person always moves the correct distance because we used a <span style="color:red">function</span> within an <span style="color:blue">expression</span> to find that distance:

![Screenshot 2023-02-14 at 3.09.45 PM.png](/img/user/Media/Screenshot%202023-02-14%20at%203.09.45%20PM.png)

Try moving the shrine a few more times. 

Every time you run the program, you should find the person moves to the edge of the shrine, but doesn't go inside.

### Exercise: Lost and Found

Oh dear! You have lost your AirPods case... again. 😭

![Pasted image 20230214151500.png](/img/user/Media/Pasted%20image%2020230214151500.png)

Download this [Lost and Found world](https://www.russellgordon.ca/lcs/2023-24/icd2o/Lost%20and%20Found.a3p.zip) and open it in Alice.

Run the world a few times. What do you notice about the position of the objects?

Now, add a person to the world.

Make your person:

- turn toward one of the objects
- move right up to the object, but not overlap with it
- turn back toward the middle of the room
- return to the middle of the room

Repeat this process for each object in the room.

> [!TIP]
> There is an `origin` object marker that you can use to find the middle of the room in this scene.

> [!NOTE]
> Using the clipboard in Alice *might* be helpful once you get your person doing the correct sequence of steps with a single object.
> 
> Here is a [20-second video on how to use the clipboard in Alice](https://www.yout-ube.com/watch?v=mbeQXeHqPvk).




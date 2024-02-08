---
{"dg-publish":true,"permalink":"/concepts/moving-object-sub-joints/","tags":["C1.1","C1.2","C1.4"],"dgHomeLink":true,"dgShowToc":true}
---


# Moving Object Sub-Joints

## Overview

With your partner, please watch the following video made by the team that created Alice, which is a good introduction to how sub-joints work within both the scene editor and code editor of Alice:

[![Screenshot 2023-02-21 at 6.54.14 PM.png](/img/user/Media/Screenshot%202023-02-21%20at%206.54.14%20PM.png)](https://www.youtube-nocookie.com/embed/EWUtVLWAcRk)

### Exercise 1

In an earlier tutorial, you learned how to use the [[Concepts/Movement in 3D Space#Do Together\|do-together control structure]].

You also saw several examples of how to [[Concepts/Movement in 3D Space#Move Up/Down\|repeat instructions using a loop]].

Based on that earlier learning, and the introduction given in the video above, see if you can re-create the following animation:

[![Screenshot 2023-02-21 at 7.27.17 PM.png](/img/user/Media/Screenshot%202023-02-21%20at%207.27.17%20PM.png)](https://www.youtube-nocookie.com/embed/RDuF099gEOM)

Consider:

- what sub-joints of the clownfish must move 
- how the clownfish itself must move
- what actions occur at the same time
- how long individual actions should take

## Tips for Moving Sub-Joints

When we manipulate sub-joints, we are changing their *orientation*.

As we learned in an earlier tutorial, there are three ways to change the orientation of an object or an object sub-joint:

1. [[Concepts/Movement in 3D Space#Turn Right/Left\|Turning right/left]] (rotation around <span style="color:green;">green</span> axis)
2. [[Concepts/Movement in 3D Space#Turn Forward/Backward\|Turning forward/backward]] (rotation around <span style="color:red;">red</span> axis)
3. [[Concepts/Movement in 3D Space#Rolling Right/Left\|Rolling right/left]] (rotation around <span style="color:blue;">blue</span> axis)

Say that we want to make a person use the lower portion of their leg, as if they were to kick a ball:

![Screenshot 2023-02-21 at 7.38.54 PM.png](/img/user/Media/Screenshot%202023-02-21%20at%207.38.54%20PM.png)

How do we know what sub-joint to use? How do we know whether to *turn* or *roll*? Which *direction*?

Here are some [steps to help you figure this out](https://www.youtube-nocookie.com/embed/Ptbc0xHK6Kg):

1. Drop a camera marker to be able to get back to where you started
2. Zoom in to the sub-joint
3. Make the character semi-transparent
4. Enable 'Show Joints'
   ![Screenshot 2023-02-21 at 7.42.34 PM.png|300](/img/user/Media/Screenshot%202023-02-21%20at%207.42.34%20PM.png)
5. Select the sub-joint
6. Select 'Rotation'
7. Use the rings to move the sub-joint
8. Take careful note of what axis the joint rotated around...
	- Rotation around <span style="color:green;">green</span> axis?
		- That's a [[Concepts/Movement in 3D Space#Turn Right/Left\|turn right/left]]
	- Rotation around <span style="color:red;">red</span> axis? 
		- That's a [[Concepts/Movement in 3D Space#Turn Forward/Backward\|turn forward/backward]]
	- Rotation around <span style="color:blue;">blue</span> axis?
		- That's a [[Concepts/Movement in 3D Space#Rolling Right/Left\|rolling right/left]]
9. Use the camera marker to get back to where you started
10. Optionally, make the character opaque again and hide joints
11. Edit the code
12. Select the sub-joint
13. Add the code based on what you figured out

Here's a short video illustrating the steps described above:

[![Screenshot 2023-02-21 at 8.25.37 PM.png|700](/img/user/Media/Screenshot%202023-02-21%20at%208.25.37%20PM.png)](https://www.youtube-nocookie.com/embed/Ptbc0xHK6Kg)

If that *seems* really time-consuming, know that you will get a feel for how sub-joints need to move pretty quickly, with a bit of practice.

### Exercise 2

You may have noticed that the "kick" action above is not completely realistic yet.

The foot does not quite reach the ball because a kick of that nature also involves a slight movement of the hip.

Try (carefully) observing your partner doing a kicking motion.

Then, see if you can use a combination of do-together and do-in-order control structures to make the animation complete:

- foot meets ball
- ball goes into the net

Something along these lines:

![Kicking a Soccer Ball - Complete copy.gif](/img/user/Media/Kicking%20a%20Soccer%20Ball%20-%20Complete%20copy.gif)

> [!NOTE]
> Here is a [starter world that you can use](https://www.russellgordon.ca/lcs/2023-24/icd2o/Kicking_a_Ball.a3p.zip) for this exercise.

> [!TIP]
> There is a tile named `straightenOutJoints` that can automatically "put sub-joints back" to their starting positions. This is useful near the end of the animation shown above:
> 
> ![Screenshot 2023-02-21 at 8.45.49 PM.png|400](/img/user/Media/Screenshot%202023-02-21%20at%208.45.49%20PM.png)

### Exercise 3

Say that we want to program an instance of the `Teen` class doing a jumping jack.

Like the kicking motion above, this will involve several object sub-parts moving at the same time.

Have your partner do a few jumping jacks!

Take careful note of what parts of their body are moving.

Then, program a character in Alice to do several jumping jacks in a row.

### Exercise 4

Mr. Gordon is *painfully* out of the loop when it comes to current dance moves.

However, he does gather that a "dab" and "flossing" are a *bit* out-of-date.

Nonetheless, given that there are many videos available demonstrating these dance moves, they are a good choice for practicing with moving object sub-joints.

Work with your partner to first make a plan for, and then program, a [dab or a floss](https://www.youtube.com/watch?v=6i3cjWn2nOQ).

> [!TIP]
> If you can find additional videos of these dance moves being demonstrated, they might be useful for figuring out the individual movements that occur. Consider pausing the video or watching it at a slower speed – something less than 1x.



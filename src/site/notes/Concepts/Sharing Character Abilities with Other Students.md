---
{"dg-publish":true,"permalink":"/concepts/sharing-character-abilities-with-other-students/","tags":["C3.1","C3.2","C3.3","C3.4","C3.5"],"dgHomeLink":true,"dgShowToc":true}
---


# Sharing Character Abilities with Other Students

## Classes 

In Alice, a **class** can be thought of like a blueprint.

For example, the `Person` class might have the following attributes:

- hair colour
- eye colour
- height
- weight

... and so on.

## Objects

An **object** is a particular instance of a class, where each attribute has a specific value:

![Screenshot 2023-02-22 at 2.42.53 PM.png|700](/img/user/Media/Screenshot%202023-02-22%20at%202.42.53%20PM.png)

One object may have different values for its attributes than another object based on the same class.

![Screenshot 2023-02-22 at 2.45.43 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%202.45.43%20PM.png)

For example:

- Mr. Gordon has red hair, green eyes, is 180 cm tall, and weighs 81.6 kilograms.
- Mr. Ross has blonde hair, blue eyes, et cetera.

In Alice, classes exist as 3D models in the gallery:

![Pasted image 20230222143953.png|500](/img/user/Media/Pasted%20image%2020230222143953.png)

When a class is dragged from the gallery into a scene, that is when an **object** is created – an object is an **instance** of a class.

## Generalizing and Sharing Procedures

In the [[Concepts/Methods with Parameters\|Methods with Parameters]] tutorial you learned, in detail, how to [[Concepts/Methods with Parameters#Generalize the procedure\|generalize a procedure]].

Mr. Gordon's solution to [[Concepts/Moving Object Sub-Joints#Exercise 2\|exercise 2 from the Moving Object Sub-joints]] tutorial looked like this:

![Screenshot 2023-02-22 at 2.56.54 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%202.56.54%20PM.png)

The kicking action shown here would be useful in other contexts – with other instances of classes such as `TeenPerson`, `Person`, `ElderPerson`, and so on.

So, we can generalize the procedure for kicking an object toward something.

Since classes inherit capabilities from their parent classes, if we create the new procedure on the `Biped` class then all its subclasses will be able to use the new procedure:

![Screenshot 2023-02-15 at 6.03.02 AM.png|175](/img/user/Media/Screenshot%202023-02-15%20at%206.03.02%20AM.png)

Finally, we can export the procedure from one world, and import it into another world.

In this way, procedures written by one person in an Alice world can be used by any other person within their Alice worlds.

Let's look at how to do all of this, step by step.

> [!TIP]
> 
> If you would like to follow along with the next part of this lesson, you can [download Mr. Gordon's "kicking code" here](https://www.russellgordon.ca/lcs/2023-24/icd2o/Kicking_a_Ball_-_Complete.a3p.zip).

### Generalizing the Kick Procedure

Here is what Mr. Gordon's code looked like immediately after he moved it into a procedure:

![Screenshot 2023-02-22 at 2.58.42 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%202.58.42%20PM.png)

After Mr. Gordon generalized by adding parameters, here is what the procedure looked like instead:

![Screenshot 2023-02-22 at 4.35.36 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%204.35.36%20PM.png)

- `this.adultPerson` was replaced with `this`
- `this.soccerBall` was replaced with `thisItem`
- `this.soccerGoal` was replaced with `towardItem`

Then, Mr. Gordon could replace the code he had in `myFirstMethod`:

![Screenshot 2023-02-22 at 2.56.54 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%202.56.54%20PM.png)

With this much shorter code instead:

![Screenshot 2023-02-22 at 3.04.36 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%203.04.36%20PM.png)

### Using the Kick Procedure in the Same World

Since the `Biped` class now has a new ability, or procedure, named `kick`:

![Screenshot 2023-02-22 at 3.06.38 PM.png|500](/img/user/Media/Screenshot%202023-02-22%20at%203.06.38%20PM.png)

... we can, for example, add a second instance of a subclass of `Biped` and have that object kick another ball into the net:

![Screenshot 2023-02-22 at 3.10.47 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%203.10.47%20PM.png)

.... which looks like this:

![Two People Kicking a Ball.gif](/img/user/Media/Two%20People%20Kicking%20a%20Ball.gif)

Note that we are *not* limited to just kicking a *ball* toward a *net*.

The `kick` procedure allows us to pass an argument (answer) of type `SProp` for the `thisItem` parameter (question).

The same is true for the `towardItem` parameter:

![Screenshot 2023-02-22 at 4.38.46 PM 1.png](/img/user/Media/Screenshot%202023-02-22%20at%204.38.46%20PM%201.png)

That means we could do the following:

![Screenshot 2023-02-22 at 3.24.42 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%203.24.42%20PM.png)

... which looks like this:

![Three People Kicking Things Around.gif](/img/user/Media/Three%20People%20Kicking%20Things%20Around.gif)

Perhaps the barista has just had enough of serving people coffee! 🤷🏽‍♂️

### Using the Kick Procedure in the Another World

#### Exporting a Procedure

Here is how to export a procedure for use in another Alice world:

1. Switch to the class that holds the procedure.
2. Choose **Save to Class File...**
3. Save the **.a3c** file somewhere that you can find it.

That looks like this:

![Exporting a Class File.gif](/img/user/Media/Exporting%20a%20Class%20File.gif)

#### Importing a Procedure

In a different Alice world, we can import procedures written by other people.

So, for example, we could use the `kick` procedure on an instance of `Biped` to make an animation like this:

![Kicking Example.gif|700](/img/user/Media/Kicking%20Example.gif)

Here is how to import procedure(s) from a class file:

1. Switch to the class that you want to import the procedure to.

> [!NOTE]
> This must match the class the procedure was exported from.
> 
> For example, the `kick` procedure was exported from the `Biped` class.
> 
> So, we must import the `kick` procedure to the same class, `Biped`, in the new Alice world.

2. Choose **Add from Class File...**
3. Find and select the file you want to import from, then choose **Open**.
   
   You will then see an interface that lets you select what procedure(s) you want to import. 
   
   For example:
   
   ![Screenshot 2023-02-22 at 3.48.44 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%203.48.44%20PM.png)
   
   Choose **Next**.
   
4. You will see a window that lets you preview what the procedure does:
   
   ![Screenshot 2023-02-22 at 4.44.57 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%204.44.57%20PM.png)
   
   Choose **Finish**.
   
   Now you will see the new procedure available for use with instances of the `Biped` class:
   
   ![Pasted image 20230222155123.png](/img/user/Media/Pasted%20image%2020230222155123.png)

Here is what the complete import process looks like:

![Importing from a Class File.gif](/img/user/Media/Importing%20from%20a%20Class%20File.gif)

> [!TIP]
> 
> If you would like to try following along with the animation above to practice importing a class-level procedure, you can [download this starter world](https://www.russellgordon.ca/lcs/2023-24/icd2o/Importing_Example_-_Starter.a3p.zip).

#### Using the New Procedure

To use the procedure, we drag out the tile, and select arguments (answers) for the parameters (questions).

![Screenshot 2023-02-22 at 4.52.56 PM.png](/img/user/Media/Screenshot%202023-02-22%20at%204.52.56%20PM.png)

In this case:

- parameter `thisItem` is given the argument `this.coconut`
- parameter `towardItem` is given the argument `this.fishingBoatCanopy`

## Exercise

You will now try importing and using a procedure written by Justin Hui, who took this course in 2021-22.

His procedure can be used on `Biped` subclasses, and looks like this:

![Backflip.gif](/img/user/Media/Backflip.gif)

Justin [documented how his procedure works](https://docs.google.com/document/d/11wYfHpA-N94SMnRyeX-_uvvGh6Rf3dtYGuwc4_1xIAc/edit#heading=h.8r2ricfo8v68), so that future users could determine if it would be suitable for their needs.

Download his class file, like this:

![Downloading a Class File.gif](/img/user/Media/Downloading%20a%20Class%20File.gif)

Then import his class file to an Alice world, as [[Concepts/Sharing Character Abilities with Other Students#Importing a Procedure\|explained earlier]].

Finally, use his procedure in your Alice world, and make a post [on Notion](https://notion.so) to show that you know how to do all of this.





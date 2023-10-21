---
{"dg-publish":true,"permalink":"/concepts/introduction-to-loops/","tags":["C2.4"],"dgHomeLink":true,"dgShowToc":true}
---

# Introduction to Loops

If we wanted someone to walk 5 steps toward us, it's easier to say just that – rather than say:

- walk 1 step
- walk 1 step
- walk 1 step
- walk 1 step
- walk 1 step

In the same way, we can use a loop to have a computer repeat an instruction – or a block of multiple instructions – more than once.
## Creating a loop

To make a function in Swift Playgrounds, just begin typing the keyword `for`, and then press the **Return** key to use autocomplete:

![Screenshot 2023-09-21 at 1.15.51 PM.png](/img/user/Media/Screenshot%202023-09-21%20at%201.15.51%20PM.png)

You will then have a template for a function that you can fill in:

![Screenshot 2023-09-21 at 1.16.18 PM.png](/img/user/Media/Screenshot%202023-09-21%20at%201.16.18%20PM.png)

First, fill in the *number*.

That describes how many times you want the block of code to run.

Let's choose 5:

![Screenshot 2023-09-21 at 1.17.19 PM.png](/img/user/Media/Screenshot%202023-09-21%20at%201.17.19%20PM.png)

Next, copy the code shown here below into the body of the loop:

```swift
turtle.penDown()
turtle.forward(distance: 50)
turtle.penUp()
turtle.forward(distance: 50)
```

... replacing the placeholder:

![Screenshot 2023-09-21 at 1.19.00 PM.png](/img/user/Media/Screenshot%202023-09-21%20at%201.19.00%20PM.png)

... with the code:

![Screenshot 2023-09-21 at 1.19.13 PM.png](/img/user/Media/Screenshot%202023-09-21%20at%201.19.13%20PM.png)

The opening `{` marks the start of the code block that will be repeated.

The closing `}` marks the end of the code block that will be repeated.

If you press **Command-Shift-R** to step through the code in the playground, you will see how the loop repeats the code:

![Loop Example.gif](/img/user/Media/Loop%20Example.gif)
---
{"dg-publish":true,"permalink":"/activities/introduction-to-generative-art/","tags":["C1.4","C1.5","C2.1","C2.2","C2.3","C2.4","C2.6","C2.7"],"dgHomeLink":true,"dgShowToc":true}
---

# Introduction to Generative Art

## Objectives

- See how following a simple algorithm, or recipe, can be used to create pleasing visual patterns.
- Make use of selection statements to run different blocks of code.

## What is generative art?

*Generative art* describes visual forms that are created wholly through the use of code.

The programmer makes decisions about how to write the code itself.

The programs authored by a generative artist use various types of input or random events to make decisions about how to structure the output each time the program is run.

In this way, running a generative art program several times will produce different output each time.

Here are some examples:

![Screenshot 2023-10-03 at 6.50.33 AM.png|400](/img/user/Media/Screenshot%202023-10-03%20at%206.50.33%20AM.png)

## Setup

Please create a new playground titled *Gen Art Intro*.

Then copy and paste this code into the playground:

```swift
// Black borders
turtle.penColor = .black

// "Flip a coin"
let coin = Int.random(in: 1...2)

// Set color based on coin
if coin == 1 {
    turtle.fillColor = .red
} else {
    turtle.fillColor = .blue    
}

// Draw a circle
turtle.arc(radius: 100, angle: 360)
```

Now run the program several times. What do you notice?

## Selection statements

*Selection statements* refer to structures in code that "select" a block of code to run based on a condition.

There are multiple types of programming language structures that allow for selection to occur.

In this discussion, we will look at `if` statements.

The general syntax is:

![Pasted image 20221216083514.png|225](/img/user/Media/Pasted%20image%2020221216083514.png)

In that example, only when the `condition` evaluates to `true` does the block of code inside the `{ }` brackets get selected to be run. Otherwise, the block of code is skipped.

Here is another example:

![Pasted image 20221216083829.png|175](/img/user/Media/Pasted%20image%2020221216083829.png)

In this example, when the `condition` is `true` the first block of code runs. Otherwise, `else`,  the second block of code runs.

When writing a `condition` we use comparison operators so that we can compare the left side of a condition to the right side. 

Here is the complete list of comparison operators that can be used in an expression:

![Pasted image 20221216090240.png|400](/img/user/Media/Pasted%20image%2020221216090240.png)

## Extend

[Stephen Boyd](https://www.sspboyd.ca/about) is an artist, based in Toronto, who has been making generative art for two decades.

He [shared this post](https://genart.social/@sspboyd/111141477055446415) on Mastodon on September 28, 2023:

![Screenshot 2023-10-03 at 7.02.52 AM.png|600](/img/user/Media/Screenshot%202023-10-03%20at%207.02.52%20AM.png)

After reviewing his algorithm (or recipe) use your understanding of how to create shapes using the `turtle` in Swift Playgrounds to write code that implements it.

Think about how you might use functions and loops while authoring your code.
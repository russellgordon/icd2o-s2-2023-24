---
{"dg-publish":true,"permalink":"/activities/going-home-again/","tags":["C3.3"],"dgHomeLink":true,"dgShowToc":true}
---

# Going Home Again

## Setup

Please create a new playground titled *Going Home Again*.

Then copy and paste this code into the playground:

```swift
// FUNCTIONS

// Teach the computer to put the turtle in a random position
func moveToRandomPosition() {
    // Select a horizontal position at random
    let x = Double.random(in: -400...400)
    
    // Select a vertical position at random
    let y = Double.random(in: -300...300)
    
    // Move to the random position, leaving a trail behind
    turtle.penDown()
    turtle.lineWidth = 10
    turtle.diagonal(dx: Double(x), dy: y)
    turtle.lineWidth = 3
    turtle.drawSelf()
    turtle.penColor = .red
    
}

// START OF ACTUAL PROGRAM

// Draw axes
turtle.drawAxes(withScale: true, by: 50, width: 800, height: 800, color: .black)

// Move to a random position
moveToRandomPosition()

// Print the current position
turtle.currentPosition().x
turtle.currentPosition().y
```

## Experiment

Run the program several times. What do you notice?

![Screenshot 2023-09-26 at 8.53.04 AM.png](/img/user/Media/Screenshot%202023-09-26%20at%208.53.04%20AM.png)

## Consider

1. Write a single line of code that moves the turtle home again. What problem do you notice when you run the program after adding your code?
2. In your notebook, use point-form English to describe the steps you might take to *always* move the turtle back to the correct location.
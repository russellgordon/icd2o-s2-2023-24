---
{"dg-publish":true,"permalink":"/activities/ramones-revisited/","tags":["C1.1","A1.1","A1.2","C1.1","C1.5","C2.4","C2.6","C2.7"],"dgHomeLink":true,"dgShowToc":true}
---

# Ramones

## A possible sequence of steps

To reproduce the [[Activities/Ramones\|Ramones]] gig poster, several approaches can be taken:

![ramones - with grid copy.png|800](/img/user/Media/ramones%20-%20with%20grid%20copy.png)

Here is a [45-second video that shows one way to build this poster out](https://www.russellgordon.ca/lcs/2023-24/icd2o/ramones_sequence.mp4).

## Making a plan

The key part of this poster is probably working out how to draw the diagonal lines.

This is where a paper-based plan – drawing part of the design with a ruler in your graph-paper notebook – would be very helpful.

This time, instead, you can analyze this in-between version of the poster to help get the idea:

![Screenshot 2023-12-07 at 7.03.53 AM.png|500](/img/user/Media/Screenshot%202023-12-07%20at%207.03.53%E2%80%AFAM.png)

After some thought, you might come up with something like this – looking at the start and end positions for the yellow lines:

![Pasted image 20231207070727.png|600](/img/user/Media/Pasted%20image%2020231207070727.png)

Here, what we notice is for two columns of numbers, the values change, and that two other columns of numbers remain constant.

We choose to use a loop with a `stride` function to express the pattern of values in the final column (pink highlight). That pattern of values will be stored in the variable `i`.

We notice that the first column of values (green highlight) only differs from the final column in that each value is 200 pixels less than the final column. So, we can use the expression `i - 200` to express the pattern of values in the first column.

Put together, this code will then draw the yellow lines for us:

```swift
// Draw the lines
turtle.lineWidth = 3
for i in stride(from: -250, through: 650, by: 50) {
    
    turtle.drawLine(from: Point(x: i - 200, y: -250),
                    to: Point(x: -450, y: i))
    
}
```

## Exercise

### Draw the grey lines

Use [this planning sheet](https://www.russellgordon.ca/lcs/2023-24/icd2o/ramones_lines_planning_sheet.pdf) and **take a few minutes to analyze the start and end points for the grey lines** in the same way as was done above for the yellow lines:

[![Screenshot 2023-12-07 at 7.15.22 AM.png](/img/user/Media/Screenshot%202023-12-07%20at%207.15.22%E2%80%AFAM.png)](https://www.russellgordon.ca/lcs/2023-24/icd2o/ramones_lines_planning_sheet.pdf)

Then, author the code you need to draw the grey lines as well.

### Finish the poster

From here, it is very likely that after [reviewing the suggested sequence video](https://www.russellgordon.ca/lcs/2023-24/icd2o/ramones_sequence.mp4) shared earlier, you can finish off this poster. Go for it – you've got this! 👊🏼
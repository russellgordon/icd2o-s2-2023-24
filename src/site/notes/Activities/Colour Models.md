---
{"dg-publish":true,"permalink":"/activities/colour-models/","dgHomeLink":true}
---

# Colour Models
## The RGB Colour Model

RGB stands for red, green, and blue.

It is a method for selecting a colour on a computer system.

Three *channels* – red, green, and blue – comprise a colour.

An RGB value of 0, 0, 0 is black.

An RGB value of 255, 255, 255 is white.

Values between 0 and 255 for each channel produce other colours.

While this is a relatively simple approach to understand, it has drawbacks.

Consider the following:

Colour|Red|Green|Blue|Result
-|-|-|-|-
Forest green|80|100|60|![Pasted image 20231011065655.png](/img/user/Media/Pasted%20image%2020231011065655.png)
Brighter, more saturated|?|?|?|![Pasted image 20231011065828.png](/img/user/Media/Pasted%20image%2020231011065828.png)
Complementary|?|?|?|![Pasted image 20231011065837.png](/img/user/Media/Pasted%20image%2020231011065837.png)

It is hard to think intuitively about how to change red, green, and blue values to obtain desired changes to a colour.

Fortunately, there is an alternative...

## The HSB Colour Model

HSB stands for hue, saturation, and brightness.

![Pasted image 20231011070754.png|300](/img/user/Media/Pasted%20image%2020231011070754.png)

The *hue* is a position on a colour wheel between 0 and 360 degrees.

*Saturation* describes the colour intensity, expressed as a percentage. 0% is white, 100% is a fully saturated colour.

Brightness describes how dark or bright a colour is, expressed as a percentage. 0% is black, 50% is considered the "true brightness" for a given hue, and 100% is very bright.

Let's revisit the previous example:

Colour|Hue|Saturation|Brightness|Result
-|-|-|-|-
Forest green|91°|41%|39%|![Pasted image 20231011065655.png](/img/user/Media/Pasted%20image%2020231011065655.png)
Brighter, more saturated|91°|41 + 40 = 81%|39 + 40 = 79%|![Pasted image 20231011065828.png](/img/user/Media/Pasted%20image%2020231011065828.png)
Complementary|91 + 180 = 271°|41%|39%|![Pasted image 20231011065837.png](/img/user/Media/Pasted%20image%2020231011065837.png)

You can increase or decrease saturation or brightness by simply adjusting the percentage value up or down.

And, it turns out, there is a mathematical relationship between colours. A *complementary* colour is always 180° more than (or less than) a given hue!

At first, it can be easiest to understand the HSB colour model by trying it out interactively.

Download and open the [Colour Selector 3D](https://russellgordon.ca/lcs/c3d.zip) app:

![Screenshot 2023-10-11 at 7.15.56 AM.png|600](/img/user/Media/Screenshot%202023-10-11%20at%207.15.56%E2%80%AFAM.png)

> [!NOTE]
> Mr. Gordon wrote this app many years ago in a Java-based programming environment. It looks a little dated at this point, but it still works!
### Advantages

Using the HSB colour model, we can easily find pleasing colour combinations by simple mathematical relationships.
#### Monochromatic colour

Same hue, vary the brightness – we reduce the brightness by 25% with each square:

![Screenshot 2023-10-11 at 7.22.48 AM.png|300](/img/user/Media/Screenshot%202023-10-11%20at%207.22.48%E2%80%AFAM.png)

The code that produces this example is included below – feel free to try it out:

```swift
// FUNCTIONS

func drawSquare() {
    for i in 1 ... 4 {
        turtle.forward(distance: 100)
        turtle.right(angleInDegrees: 90)
    }
}

func moveOver() {
    turtle.penUp()
    turtle.diagonal(dx: 100, dy: 0)
    turtle.penDown()
}

// CONSTANTS

// NOTE: Brightness is 75%
let originalRed = Color(hue: 0.0/360.0,
                        saturation: 100.0/100.0,
                        brightness: 75.0/100.0,
                        alpha: 100.0/100.0)

// NOTE: Brightness is 25% less than the original
let darkerRed = Color(hue: 0.0/360.0,
                      saturation: 100.0/100.0,
                      brightness: 50.0/100.0,
                      alpha: 100.0/100.0)

// NOTE: Brightness is 50% less than the original
let evenDarkerRed = Color(hue: 0.0/360.0,
                          saturation: 100.0/100.0,
                          brightness: 25.0/100.0,
                          alpha: 100.0/100.0)

// ACTUAL DRAWING

// Clear borders
turtle.penColor = .clear

// First square
turtle.fillColor = originalRed
drawSquare()

// Move over
moveOver()

// Second square
turtle.fillColor = darkerRed
drawSquare()

// Move over
moveOver()

// Third square
turtle.fillColor = evenDarkerRed
drawSquare()
```

#### Complementary colour

The complemenary colour for a given hue is directly across the colour wheel.

![Screenshot 2023-10-11 at 7.27.42 AM.png|200](/img/user/Media/Screenshot%202023-10-11%20at%207.27.42%E2%80%AFAM.png)

![Screenshot 2023-10-11 at 7.28.16 AM.png|300](/img/user/Media/Screenshot%202023-10-11%20at%207.28.16%E2%80%AFAM.png)

#### Triadic colour

Second and third colours form the base of the triangle across from the starting hue.

![Screenshot 2023-10-11 at 7.29.34 AM.png|300](/img/user/Media/Screenshot%202023-10-11%20at%207.29.34%E2%80%AFAM.png)

![Screenshot 2023-10-11 at 7.30.34 AM.png|300](/img/user/Media/Screenshot%202023-10-11%20at%207.30.34%E2%80%AFAM.png)

#### Analogous colour

Colours are near each other on the colour wheel.

![Screenshot 2023-10-11 at 7.31.18 AM.png|300](/img/user/Media/Screenshot%202023-10-11%20at%207.31.18%E2%80%AFAM.png)

![Screenshot 2023-10-11 at 7.31.30 AM.png|350](/img/user/Media/Screenshot%202023-10-11%20at%207.31.30%E2%80%AFAM.png)

## Exercises

1. Using the [[Activities/Colour Models#Monochromatic colour\|code provided above]] as a starting point, try creating a playground that generates complementary colours instead.
2. Using the [[Activities/Colour Models#Monochromatic colour\|code provided above]] as a starting point, try creating a playground that generates triadic colours instead.
3. Using the [[Activities/Colour Models#Monochromatic colour\|code provided above]] as a starting point, try creating a playground that generates analogous colours instead.
4. Try to reproduce the following drawing:
   
   ![Screenshot 2023-10-11 at 7.50.26 AM.png](/img/user/Media/Screenshot%202023-10-11%20at%207.50.26%E2%80%AFAM.png)
   
   Here is a code segment to get you started:
   
	```swift
	for i in 1 ... 36 {
	
	    let hue = Double(i) * 10.0
	
	    turtle.fillColor = Color(hue: hue/360.0,
	                             saturation: 80.0/100.0,
	                             brightness: 90.0/100.0,
	                             alpha: 100.0/100.0)
	}
	```

5. Experiment with changing the `alpha` value and making some overlapping shapes. What do you notice?
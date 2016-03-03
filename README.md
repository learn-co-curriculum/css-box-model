# CSS Box Model

## Overview

In this lesson we will look at the CSS Box Model. We will discover how to determine the height and width dimensions of elements taking into consideration the spacing inside and around elements, as well as the measure of their available content area. We will also discuss differences in size measurements from browser to browser and how to set widths and heights uniformly across browsers.

## Objectives

1. Applying Border, Padding and Margin
2. IE Box Model vs W3C Box Model
3. CSS3 Box-sizing property

## Every Element Is A Box

<iframe width="640" height="480" src="https://www.youtube.com/embed/tBSxuNfgRHc?rel=0" frameborder="0" allowfullscreen></iframe>

*Note: Slides for this lecture video are provided in the resources at the bottom of this lesson.*

### Characteristics Of A Box

All elements can be thought of as boxes on the screen in that they can have a height, a width, spacing within, and spacing outside of them. Furthermore, we can set these spacing properties independently on all four sides of our element. Let's start by familiarizing ourselves with the CSS properties neccesary to add borders, and spacing to our elements. The box model is made of the following CSS properties:

#### Margin

Margin is the spacing outside of an element. It pushes one element away from the other, creating an empty space between. Margin can be set in (px) pixels, (em) ems, or (%) percents. We can specify margin independently on all four sides of an element using the properties `margin-top`, `margin-right`, `margin-bottom`, `margin-left`, and also using the shorthand property `margin` while providing multiple values to determine which side each value will effect.

```css

```

#### Padding

Padding is the spacing inside of an element. It pushes content wihtin the element away from the elements outer walls. Padding can be set in (px) pixels, (em) ems, or (%) percents. We can specify padding independently on all four sides of an element using the properties `padding-top`, `padding-right`, `padding-bottom`, `padding-left`, and also using the shorthand property `padding` while providing multiple values to determine which side each value will effect.

```css

```

#### Border

Border creates a line against the edge of an element. It marks directly upon the elements outer walls. Border has three distinct properties that can be set upon it: `border-size`, `border-style`, and `border-color`. We can also use the shorthand property `border` to set all three values in this one property.  We can specify border independently on all four sides of an element using the properties `border-top`, `border-right`, `border-bottom`, `border-left`.

Border size can be set in (px) pixels, (em) ems, or (%) percents.

Border style can be set to: solid, dashed, dotted, ...

Border color can be set by color name, hexidecimal, rgb, rgba, hsl, or hsla.

```css

```

### IE Box Model vs W3C Box Model

...

## Summary

- ...

## Resources

- [Presentation Slides](https://docs.google.com/presentation/d/1UTUWDczUiDZ6byuhyHv0L3zJXQjdlnZheZXhRVLOL3Q/edit?usp=sharing)
- [MDN - Introduction CSS Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
- [Box Model - Code Example](http://jsfiddle.net/flatiron_school/jtFgz/)

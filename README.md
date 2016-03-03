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

Setting one value will apply a uniform amount of margin on all sides of the selected element.

```css
div {
  margin: 10px;  
}

/* is the same as */

div {
  margin-top: 10px;
  margin-right: 10px;
  margin-bottom: 10px;
  margin-left: 10px;
}
```

Setting two values will apply the first value on both the top and bottom, and the second value on the left and right of the selected element.

```css
div {
  margin: 10px 20px;  
}

/* is the same as */

div {
  margin-top: 10px;
  margin-right: 20px;
  margin-bottom: 10px;
  margin-left: 20px;
}
```

Setting three values will apply the first value on the top, the second on both the left and right, and the third value on the bottom of the selected element.

```css
div {
  margin: 10px 20px 30px;  
}

/* is the same as */

div {
  margin-top: 10px;
  margin-right: 20px;
  margin-bottom: 30px;
  margin-left: 20px;
}
```

Setting four values will apply the first value (clockwise) to the top, the second to the right, the third to the bottom, and the fourth to the left of the selected element.

```css
div {
  margin: 10px 20px 30px 40px;  
}

/* is the same as */

div {
  margin-top: 10px;
  margin-right: 20px;
  margin-bottom: 30px;
  margin-left: 40px;
}
```

#### Padding

Padding is the spacing inside of an element. It pushes content wihtin the element away from the elements outer walls. Padding can be set in (px) pixels, (em) ems, or (%) percents. We can specify padding independently on all four sides of an element using the properties `padding-top`, `padding-right`, `padding-bottom`, `padding-left`, and also using the shorthand property `padding` while providing multiple values to determine which side each value will effect. The order of the values for the `padding` shorthand property follow the same rules as for margin listed above.

Setting one value will apply a uniform amount of padding on all insides of the selected element.

```css
div {
  padding: 10px;  
}

/* is the same as */

div {
  padding-top: 10px;
  padding-right: 10px;
  padding-bottom: 10px;
  padding-left: 10px;
}
```

Setting two values will apply the first value on both the top and bottom, and the second value on the left and right of the selected element.

```css
div {
  padding: 10px 20px;  
}

/* is the same as */

div {
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 10px;
  padding-left: 20px;
}
```

Setting three values will apply the first value on the top, the second on both the left and right, and the third value on the bottom of the selected element.

```css
div {
  padding: 10px 20px 30px;  
}

/* is the same as */

div {
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 30px;
  padding-left: 20px;
}
```

Setting four values will apply the first value (clockwise) to the top, the second to the right, the third to the bottom, and the fourth to the left of the selected element.

```css
div {
  padding: 10px 20px 30px 40px;  
}

/* is the same as */

div {
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 30px;
  padding-left: 40px;
}
```

#### Border

Border creates a line against the edge of an element. It marks directly upon the elements outer walls. Border has three distinct properties that can be set upon it: `border-size`, `border-style`, and `border-color`. We can also use the shorthand property `border` to set all three values in this one property.  We can specify border independently on all four sides of an element using the properties `border-top`, `border-right`, `border-bottom`, `border-left`.

Border size can be set in (px) pixels, (em) ems, or (%) percents.

```css
border-size: 1px | 1em | 1%
```

Border style can be set to: solid, dashed, dotted, ...

```css
border-style: none | hidden | solid | dashed | dotted | double | groove | ridge | inset | outset
```

Border color can be set by color name, hexidecimal, rgb, rgba, hsl, or hsla.

```css
border-color: red | #f00 | rgb(255,0,0) | rgba(255,0,0,1) | hsl(0,100%,50%) | hsla(0,100%,50%,1)
```

Border shorthand applies border-size, border-style, and border-color in a single declaration.

```css
border: 1px solid red;
```

All of the properties above (border, border-size, border-style, border-color) can have up to 4 values set for each side of the selected element following the same rules we saw for both padding and margin listed above.

### IE Box Model vs W3C Box Model

...

### Solutions For Uniform Box Measurements

...

## Summary

- ...

## Resources

- [Presentation Slides](https://docs.google.com/presentation/d/1UTUWDczUiDZ6byuhyHv0L3zJXQjdlnZheZXhRVLOL3Q/edit?usp=sharing)
- [MDN - Introduction CSS Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
- [MDN - CSS - Margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
- [MDN - CSS - Padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
- [MDN - CSS - Border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
- [Box Model - Code Example](http://jsfiddle.net/flatiron_school/jtFgz/)

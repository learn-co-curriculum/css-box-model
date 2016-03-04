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

Microsoft the maker of Windows OS and the Internet Explorer Browser have always had their own opinion and their own way of doing things. One example of this is their own unique interpretation of the box model. As web developers it's important we understand the difference between the two available box models: the IE box model and the W3C box model.

#### W3C Box Model

The W3C, a standards commitee that oversees the spec for HTML and CSS specifies their own box model which has been adopted by Safari, Opera, Chrome, and FireFox browsers. It dictates that when we set a `width` or `height` property in CSS we are setting the size of the content area, and that any padding, border, or margin is an extra amount that we need to add on to the width or height. For example if we set the width of a div to 100px, and also give it 20px of padding, and 1px of border.

```css
div {
  width: 100px;
  padding: 20px;
  border: 1px solid black;
}
```

The real amount of space the element takes up is 100px width + 40px (20 on each side) + 2px border (1px each side) = 142px wide. This is the case for all browsers except for (IE) Internet Explorer. There is 100px of space for the content inside the element, but the element itself is 142px wide.

Total width in all browsers (except IE) = 142px

Total content area width in all browsers (except IE) = 100px

#### IE Box Model

Microsofts box model is built differently. When we set a width and padding and border on our element it is automatically included in the width. So using the same previous example if we set the width of a div to 100px, and also give it 20px of padding, and 1px of border.

```css
div {
  width: 100px;
  padding: 20px;
  border: 1px solid black;
}
```

IE, includes the padding and border in its measured width and thus the total measurement is still 100px. However to calculate the amount of space insid ethe element for content we must subtract the border and padding, so: 100px width - 40px padding (20px on each side) - 2px border (1px on each side) = 58px of space for the content area within the element.

Total width in all browsers (except IE) = 100px

Total content area width in all browsers (except IE) = 58px

### Margin Not Includded

Please note that neither box model includes margin in their width and height, so when calculating how much space an element takes up in relationship to other elements, it is important to factor in the margin as taking up its own space independent of the total width of the element.

### Solutions For Uniform Box Measurements

You can imagine seeing our elements as two different sizes in different browsers is enough to give anyone a headache. Fortunately, we can now use the CSS3 `box-sizing` property to force browsers to use either the IE box model or the W3C box model. To use the IE box model we simply set elements `box-sizing: border-box;` or to set elements to W3C box model we use `box-sizing: content-box`. We can conveniently use the universal selector to set this for all elements like so:

```css
* {
  box-sizing: border-box; /* IE */
}
```

or

```css
* {
  box-sizing: border-box; /* W3C */
}
```

## Summary

- Margin, border, padding, and content area combine to makeup the box model.
- Margin is the spacing outside of elements.
- Padding is the spacing inside of elements.
- Border is a stroke at the edge of elements.
- Margin, border, and padding have shorthand properties where we can define different values for each side of the element.
- There are two distinct and different box models: W3C and IE.
- The W3C Box Model does not include padding and border in its total width or height.
- The IE Box Model does include padding and border in its total width or height.
- Neither Box model includes margin in their total width or height.
- We can use the `box-sizing` property to set all browsers to use one or the other box model. To use IE set the `border-box` value and to use W3C set the `content-box` value. 

## Resources

- [Presentation Slides](https://docs.google.com/presentation/d/1UTUWDczUiDZ6byuhyHv0L3zJXQjdlnZheZXhRVLOL3Q/edit?usp=sharing)
- [MDN - CSS - Margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
- [MDN - CSS - Padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
- [MDN - CSS - Border](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
- [MDN - Introduction CSS Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
- [Box Model - Code Example](http://jsfiddle.net/flatiron_school/jtFgz/)

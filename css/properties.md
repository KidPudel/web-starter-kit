Here are some of the most important CSS properties to know:

- `display`: specifies how an element should be displayed (e.g. block, inline, inline-block).
  - `flexbox` and `grid`: layout systems for creating flexible, responsive designs.\
    - `flex-direction` set column-based or row-based
    - `flex-shring` in child, we can set it to 0, so it won't shrink at all
    - `flex-grow` in child, we can set it to 1(weight), so it will scale as our screen stretches
    - `align-self` in child, we can override cross-axis for each item
- `background-color`: sets the background color of an element.
- `color`: sets the text color of an element.
- `font-size`: sets the size of the text.
- `font-family`: sets the font family for the text.
- `font-weight`: sets the weight (boldness) of the text.
- `line-height`: sets the height of each line of text.
- `text-align`: sets the horizontal alignment of text within an element.
- `width` and `height`: sets the width and height of an element.
- `margin` and `padding`: controls the spacing around an element.
- `border`: sets the border around an element.
- `box-sizing`: specifies how the width and height of an element should be calculated.
- `position`: specifies the positioning method for an element (e.g. relative, absolute, fixed).
- `z-index`: sets the stacking order of elements.
- `float`: positions an element to the left or right of its container.


# Flexbox

```css
.App {
    display: flex;
}
```  
**_will create flexbox container_**

in flexbox there is a main and cross access represented by `justify-center` and `align-items` respectively

<img src="https://user-images.githubusercontent.com/63263301/229141149-51268235-fb6a-44bc-9309-ba8ae5f6477b.png" width=500px alt="image">
<img src="https://user-images.githubusercontent.com/63263301/229141218-9420920e-e0a7-4afb-acfa-d3f20e7c9220.png" width=500px alt="image">

class: middle, center

# CSS Box Model

---

## The CSS Box Model

In a document, each element is represented as a rectangular box. Determining the size, properties — like its color, background, borders aspect — and the position of these boxes is the goal of the rendering engine.

In CSS, each of these rectangular boxes is described using the standard box model. This model describes the content of the space taken by an element. 

Each box has four edges: 
- margin edge
- border edge
- padding edge
- content edge

---

## The CSS Box Model

.right[![boxmodel](boxmodel.gif)]

---

## Content

The content area is the area containing the real content of the element. It often has a background, a color or an image (in that order, an opaque image hiding the background color) and is located inside the content edge; its dimensions are the content width, or content-box width, and the content height, or content-box height.

If the CSS box-sizing property is set to default, the CSS properties width, min-width, max-width, height, min-height and max-height control the content size.

```css
div {
  width: 100px;
  height: 100px;
}
```

---

## Padding

The padding area extends to the border surrounding the padding. When the content area has a background, color, or image set on it, this will extend into the padding, which is why you can think of the padding as extending the content. The padding is located inside the padding edge, and its dimensions are the padding-box width and the padding-box height.

The space between the padding and the content edge can be controlled using the padding-top, padding-right, padding-bottom, padding-left and the shorthand padding CSS properties.

```css
div {
  padding: 100px;
}
```

---

## Border

The border area extends the padding area to the area containing the borders. It is the area inside the border edge, and its dimensions are the border-box width and the border-box height. This area depends on the size of the border that is defined by the border-width property or the shorthand border.

```css
div {
  border: 10px solid red;
}
```

---

## Margin

The margin area extends the border area with an empty area used to separate the element from its neighbors. It is the area inside the margin edge, and its dimensions are the margin-box width and the margin-box height.

The size of the margin area is controlled using the margin-top, margin-right, margin-bottom, margin-left and the shorthand margin CSS properties.

When margin collapsing happens, the margin area is not clearly defined since margins are shared between boxes.

```css
div {
  margin: 100px;
}
```

---

## The CSS Box Model

.right[![boxmodel](boxmodel-image.png)]

---

## The `display` property

#### The display CSS property specifies the type of rendering box used for an element. 

In HTML, default display property values are taken from behaviors described in the HTML specifications or from the browser/user default stylesheet.

In addition to the many different display box types, the value none lets you turn off the display of an element; **when you use none, all descendant elements also have their display turned off**. The document is rendered as though the element doesn't exist in the document tree.

```css
display: none;
display: inline;
display: block;
display: inline-block;
```

---

## The `display` property

#### Display is CSS's most important property for controlling layout. 

Every element has a default display value depending on what type of element it is. 

The default for most elements is usually block or inline. 
- A block element is often called a block-level element. 
- An inline element is always just called an inline element.

---

##The `display: block` property

**div** is the standard block-level element. A block-level element starts on a new line and stretches out to the left and right as far as it can. Other common block-level elements are p and form, and new in HTML5 are header, footer, section, and more. 

```css
div {
  display: block;
}
```

---

##The `display: inline` property

**span** is the standard inline element. An inline element can wrap some text inside a paragraph without disrupting the flow of that paragraph. The a element is the most common inline element, since you use them for links. 

```css
div {
  display: inline;
}
```

---

##The `display: inline-block` property

An element set to inline-block is very similar to inline in that it will set inline with the natural flow of text (on the "baseline"). 

The difference is that you are able to set a width and height which will be respected.

```css
div {
  display: inline-block;
}
```

---

##The `display: none` property

Another common display value is **none**. Some specialized elements such as script use this as their default. It is commonly used with JavaScript to hide and show elements without really deleting and recreating them.

This is different from visibility. Setting display to none will render the page as though the element does not exist. visibility: hidden; will hide the element, but the element will still take up the space it would if it was fully visible.

```css
div {
  display: none;
}
```

---

## Padding shorthand

```css
div {
  /* Apply to all four sides */
  padding: 1em;

  /* vertical | horizontal */
  padding: 5% 10%;

  /* top | horizontal | bottom */
  padding: 1em 2em 2em; 

  /* top | right | bottom | left */
  padding: 2px 1em 0 1em;

  /* Global values */
  padding: inherit;
  padding: initial;
  padding: unset;
}
```
```css
div {
  padding-bottom: 10px;
  padding-left: 10px;
  padding-right: 10px;
  padding-top: 10px;
}
```

---

## Border shorthand

The border CSS property is a shorthand property for setting the individual border property values in a single place in the style sheet. border can be used to set the values for one or more of: **border-width**, **border-style**, **border-color**.

```css
div {
  border: 1px;
  border: 2px dotted;
  border: 3px dashed green;
}
```
```css
div {
  border-bottom: 3px dashed yellow;
}
```

---

## Margin shorthand

```css
div {
  /* Apply to all four sides */
  margin: 1em;

  /* vertical | horizontal */
  margin: 5% auto;

  /* top | horizontal | bottom */
  margin: 1em auto 2em; 

  /* top | right | bottom | left */
  margin: 2px 1em 0 auto;

  /* Global values */
  margin: inherit;
  margin: initial;
  margin: unset;
}
```
```css
div {
  margin-bottom: 10px;
  margin-left: 10px;
  margin-right: 10px;
  margin-top: 10px;
}
```

---

## Properties controlling the size of a box

- height

- width

- max-height

- max-width

- min-height

- min-width

---

## Properties controlling 
## the flow of content in a box

- box-decoration-break

- box-sizing

- overflow

- overflow-x

- overflow-y

---

##The `box-sizing` property

The box-sizing property can be used to adjust the box model behavior:

- **content-box** gives you the default CSS box-sizing behavior. If you set an element's width to 100 pixels, then the element's content box will be 100 pixels wide, and the width of any border or padding will be added to the final rendered width.

- **border-box** tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to 100 pixels, that 100 pixels will include any border or padding you added, and the content box will shrink to absorb that extra width. This typically makes it much easier to size elements.

```css
div {
  box-sizing: border-box;
}
```

---

##The `overflow` property

The overflow CSS property sets what to do when an element's content is too big to fit in its block formatting context. 

It is a shorthand for overflow-x and overflow-y.

```css
/* Keyword values */
overflow: visible;
overflow: hidden;
overflow: scroll;
overflow: auto;
overflow: hidden visible;
```

---
class: center, middle

## Exercise: Exploring The Box Model

---

##Create a `div`

```html
<div id="main">
  Some content...
</div>
```
```css
#main {
  width: 600px;
  margin: 0 auto; 
}
```

Setting the width of a block-level element will prevent it from stretching out to the edges of its container to the left and right. Then, you can set the left and right margins to auto to horizontally center that element within its container. The element will take up the width you specify, then the remaining space will be split evenly between the two margins.

---

## `max-width`

```css
#main {
  max-width: 600px;
  margin: 0 auto; 
}
```

Using max-width instead of width in this situation will improve the browser's handling of small windows. This is important when making a site usable on mobile. Resize this page to check it out! 

---

##  `width`

```css
.fancy {
  width: 500px;
  margin: 20px auto;
  padding: 50px;
  border-width: 10px;
}
```

When you set the width of an element, the element can actually appear bigger than what you set: the element's border and padding will stretch out the element beyond the specified width. Look at the following example, where two elements with the same width value end up different sizes in the result. 

---

## `box-sizing`

```css
.fancy {
  box-sizing: border-box;
  
  width: 500px;
  margin: 20px auto;
  padding: 50px;
  border-width: 10px;
}
```

The original box model behavior was eventually considered unintuitive, so a new CSS property called box-sizing was created. When you set box-sizing: border-box; on an element, the padding and border of that element no longer increase its width.

---

## `box-sizing`


Since this is so much better, some authors want all elements on all their pages to always work this way. Such authors put the following CSS on their pages:


```css
** {
*  -webkit-box-sizing: border-box;
*  -moz-box-sizing: border-box;
*  box-sizing: border-box;
*}
```

This ensures that all elements are always sized in this more intuitive way.

Since box-sizing is pretty new, you should use the -webkit- and -moz- prefixes for now. This technique enables experimental features in specific browsers. Also, keep in mind that this one is IE8+. 

.footnote[http://learnlayout.com/]
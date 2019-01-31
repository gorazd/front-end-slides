class: middle, center

# CSS Typography

---
class: middle

### The **font** CSS property is either a shorthand property for setting font-style, font-variant, font-weight, font-size, line-height and font-family, or a way to set the element's font to a system font, using specific keywords.

[CSS Fonts on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Fonts)

---

## font-family

The font-family CSS property lets you specify a prioritized list of font family names and/or generic family names for the selected element. Values are separated by a comma to indicate that they are alternatives. The browser will select the first font on the list that is installed on the computer or that can be downloaded using a @font-face at-rule.

```css
body {
  font-family: "Lucida" Grande, sans-serif;
}
```

Web authors should always add at least one generic family in a font-family list, since there's no guarantee that a specific font is installed on the computer or can be downloaded using a @font-face at-rule. The generic family lets the browser select an acceptable fallback font when needed.

It is often convenient to use the shorthand property font to set font-size and other font related properties all at once.

---

## font-family

```css
.body {
  /* A font family name and a generic family name */
  font-family: Gill Sans Extrabold, sans-serif;
  font-family: "Goudy Bookletter 1911", sans-serif;

  /* A generic family name only */
  font-family: serif;
  font-family: sans-serif;
  font-family: monospace;
  font-family: cursive;
  font-family: fantasy;

  /* Global values */
  font-family: inherit;
  font-family: inherit;
  font-family: unset;
}
```

- [MDN: font-family](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)

- [CSS Reference](https://cssreference.io/typography/#font-family)

---

## font-style

The font-style CSS property lets you select italic or oblique faces within a font-family. Italic forms are generally cursive in nature, usually using less horizontal space than their unstyled counterparts, while oblique faces are usually just sloped versions of the regular face. Both italic and oblique faces are simulated by artificially sloping the glyphs of the regular face (see font-synthesis for control over this).

```css
.body {
  font-style: normal;
  font-style: italic;
  font-style: oblique;

  /* Global values */
  font-style: inherit;
  font-style: initial;
  font-style: unset;
}
```

---

## font-variant
      
The font-variant property acts as a shorthand for the longhand properties: font-variant-caps, font-variant-numeric, font-variant-alternates, font-variant-ligatures, and font-variant-east-asian. You can also set the CSS Level 2 (Revision 1) values of font-variant, (that is, normal or small-caps), by using the font shorthand.

```css
.body {
  font-variant: small-caps;
  font-variant: common-ligatures small-caps;

  /* Global values */
  font-variant: inherit;
  font-variant: initial;
  font-variant: unset;
}
```

---
## font-weight

The font-weight CSS property specifies the weight or boldness of the font. Some fonts are only available in normal and bold.

```css
.body {
  font-weight: normal;
  font-weight: bold;

  /* Relative to the parent */
  font-weight: lighter;
  font-weight: bolder;

  font-weight: 100;
  font-weight: 200;
  font-weight: 300;
  font-weight: 400;
  font-weight: 500;
  font-weight: 600;
  font-weight: 700;
  font-weight: 800;
  font-weight: 900;
}
```

---
## font-size

The font-size CSS property specifies the size of the font. Setting the font size may, in turn, change the size of other items, since it is used to compute the value of the em and ex `<length>` units.

```css
.body {
  /* <absolute-size> values */
  font-size: xx-small;
  font-size: x-small;
  font-size: small;
  font-size: medium;
  font-size: large;
  font-size: x-large;
  font-size: xx-large;

  /* <relative-size> values */
  font-size: larger;
  font-size: smaller;

  /* <length> values */
  font-size: 12px;
  font-size: 0.8em;

  /* <percentage> values */
  font-size: 80%;
}
```

---
## line-height

On block level elements, the line-height property specifies the minimum height of line boxes within the element.

On non-replaced inline elements, line-height specifies the height that is used to calculate line box height. On replaced inline elements such as buttons or other input elements, line-height has no effect.

```css
.body {
  /* Keyword values */
  line-height: normal;

  /* Unitless: use this number multiplied by the element's font size */ 
  line-height: 3.5;

  /* <length> values */
  line-height: 3em;

  /* <percentage> values */
  line-height: 34%;
}
```

---
## font shorthand

```css
.body {
  /* size | family */
  font: 2em "Open Sans", sans-serif;

  /* style | size | family */
  font: italic 2em "Open Sans", sans-serif;

  /* style | variant | weight | size/line-height | family */
  font: italic small-caps bolder 16px/3 cursive;

  /* style | variant | weight | stretch | size/line-height | family */
  font: italic small-caps bolder condensed 16px/3 cursive;

  /* The font used in system dialogs */
  font: message-box;
  font: icon;

  /* Global values */
  font: inherit;
  font: initial;
  font: unset;
}
```

---
## font shorthand

- Except when using a keyword, it is mandatory to define the value of both the font-size and the font-family properties.

- Not all values of font-variant are allowed. Only the values defined in CSS 2.1 are allowed, that is normal and small-caps.

- Though not directly settable by font, the values of font-stretch, font-size-adjust and font-kerning are also reset to their initial values.

- The order of the values is not completely free: 

  font-style, font-variant and font-weight must be defined, if any, before the font-size value. 
  
  The line-height value must be defined immediately after the font-size, preceded by a mandatory /.
  
  Finally the font-family is mandatory and must be the last value defined (inherit value does not work).

---
## @font-face
      
The @font-face CSS at-rule allows authors to specify online fonts to display text on their web pages. 

By allowing authors to provide their own fonts, @font-face eliminates the need to depend on the limited number of fonts users have installed on their computers. The @font-face at-rule may be used not only at the top level of a CSS, but also inside any CSS conditional-group at-rule.


```css
@font-face {
  font-family: "Bitstream Vera Serif Bold";
  src: url("../fonts/VeraSeBd.ttf");
}
``` 

---
class: middle

### **CSS Text** is a module of CSS that defines how to perform text manipulation, like line breaking, justification and alignment, white space handling, and text transformation.

[CSS Text on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Text)

---
## CSS Text

- letter-spacing
- text-align
- text-indent
- text-transform
- white-space
- word-break
- word-spacing
- word-wrap

---
## letter-spacing

The letter-spacing CSS property specifies spacing behavior between text characters.

```css
p {
  /* <length> values */
  letter-spacing: 0.3em;
  letter-spacing: 3px;
  letter-spacing: .3px;

  /* Keyword values */
  letter-spacing: normal;

  /* Global values */
  letter-spacing: inherit;
  letter-spacing: initial;
  letter-spacing: unset;
}
```

---
## text-align

The text-align CSS property describes how inline content like text is aligned in its parent block element. text-align does not control the alignment of block elements, only their inline content.

```css
p {
  /* Keyword values */
  text-align: left;
  text-align: right;
  text-align: center;
  text-align: justify;
  text-align: justify-all;
  text-align: start;
  text-align: end;
  text-align: match-parent;

  /* Global values */
  text-align: inherit;
  text-align: initial;
  text-align: unset;
}
```

---
## text-indent

The text-indent property specifies the amount of indentation (empty space) should be left before lines of text in a block. By default, this controls the indentation of only the first formatted line of the block, but the hanging and each-line keywords can be used to change this behavior.

Horizontal spacing is with respect to the left (or right, for right-to-left layout) edge of the containing block element's box.
      
```css
p {
  /* <length> values */
  text-indent: 3mm;
  text-indent: 40px;

  /* <percentage> value
  relative to the containing block width */
  text-indent: 15%;

  /* Keyword values */
  text-indent: 5em each-line;
  text-indent: 5em hanging;
  text-indent: 5em hanging each-line;

  /* Global values */
  text-indent: inherit;
  text-indent: initial;
  text-indent: unset;
}
```

---

## text-transform

The text-transform CSS property specifies how to capitalize an element's text. It can be used to make text appear in all-uppercase or all-lowercase, or with each word capitalized.

```css
p {
  /* Keyword values */
  text-transform: capitalize;
  text-transform: uppercase;
  text-transform: lowercase;
  text-transform: none;
  text-transform: full-width;

  /* Global values */
  text-transform: inherit;
  text-transform: initial;
  text-transform: unset;
}
```

---
## white-space

The white-space property is used to describe how whitespace inside the element is handled.

```css
p {
  /* Keyword values */
  white-space: normal;
  white-space: nowrap;
  white-space: pre;
  white-space: pre-wrap;
  white-space: pre-line;

  /* Global values */
  white-space: inherit;
  white-space: initial;
  white-space: unset;
}
```

---
## word-break

The word-break CSS property is used to specify whether to break lines within words.

```css
p {
  /* Keyword values */
  word-break: normal; 
  word-break: break-all; 
  word-break: keep-all;

  /* Global values */
  word-break: inherit;
  word-break: initial;
  word-break: unset;
}
```

---
## word-spacing

The word-spacing CSS property specifies the spacing behavior between tags and words.

```css
p {
  /* Keyword value */
  word-spacing: normal;

  /* <length> values */
  word-spacing: 3px;
  word-spacing: 0.3em;

  /* <percentage> values */
  word-spacing: 50%;
  word-spacing: 200%;

  /* Global values */
  word-spacing: inherit;
  word-spacing: initial;
  word-spacing: unset;  
}
```

---
## word-wrap

The word-wrap property is used to specify whether or not the browser may break lines within words in order to prevent overflow when an otherwise unbreakable string is too long to fit in its containing box.

```css
p {
  /* Keyword values */
  word-wrap: normal;
  word-wrap: break-word;

  /* Global values */
  word-wrap: inherit;
  word-wrap: initial;
  word-wrap: unset;
}
```
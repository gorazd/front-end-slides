class: middle, center

# CSS Units

---

## Font-relative lengths

**em**
      
This unit represents the calculated font-size of the element. If used on the font-size property itself, it represents the inherited font-size of the element.

* This unit is often used to create scalable layouts, which keep the vertical rhythm of the page, even when the user changes the size of the fonts. The CSS properties line-height, font-size, margin-bottom and margin-top often has a value expressed in em.


```css
p {
  font-size: 1em;
}
```

---

## Font-relative lengths

**rem**

This unit represents the font-size of the root element (e.g. the font-size of the `<html>` element). When used on the font-size on this root element, it represents its initial value. 

* This unit is practical in creating perfectly scalable layout. If not supported by the targeted browsers, such layout can be achieved using the em unit, though this is slightly more complex.


```css
p {
  font-size: 1rem;
}
```

---

##Viewport-percentage lengths

Viewport-percentage lengths defined a length relatively to the size of viewport, that is the visible portion of the document. 
      
Only Gecko-based browsers are updating the viewport values dynamically, when the size of the viewport is modified (by modifying the size of the window on a desktop computer or by turning the device on a phone or a tablet).

**vh**

1/100th of the height of the viewport.

**vw**

1/100th of the width of the viewport.

```css
article {
  max-width: 100vw;
}
```

---
## Viewport-percentage lengths

**vmin**

1/100th of the minimum value between the height and the width of the viewport.

**vmax**

1/100th of the maximum value between the height and the width of the viewport. 

```css
article {
  min-height: 100vmin;
}
```

- 100vmin = 100vw or 100vh, whichever is smaller
- 100vmax = 100vw or 100vh, whichever is larger

---
# Absolute length units

Absolute length units represents a physical measurement and when the physical properties of the output medium are known, such as for print layout. This is done by anchored one of the unit to a physical unit and to defined the other relatively to it. The anchor is done differently for low-resolution devices, like screens, and high-resolution devices, like printers.

### Users may increase font size for accessibility purpose. To allow for usable layouts whatever is the used font size, use only absolute length units when the physical characteristics of the output medium are known, such as bitmap images. When setting length related to font-size, prefer relative units like em or rem.

---
## Absolute length units

**px**

Relative to the viewing device.
For screen display, typically one device pixel (dot) of the display.
For printers and very high resolution screens one CSS pixel implies multiple device pixels, so that the number of pixel per inch stays around 96.

**mm**

One millimeter.

**cm**

One centimeter (10 millimeters).

**in**

One inch (2.54 centimeters).

**pt**

One point (which is 1/72 of an inch).

**pc**

One pica (which is 12 points).

---
## Percentage

Many CSS properties can take percentage values, often to define sizes in terms of parent objects.
      
Percentages are formed by a number immediately followed by the percentage sign %. Just as is the case with all other units in CSS, there isn't a space between the '%' and the number.

Many length properties use percentages, such as width, margin and padding. Percentages can also be seen in font-size, where the size of the text is directly related to the size of its parent.

```css
p {
  font-size: 100%;
}
```
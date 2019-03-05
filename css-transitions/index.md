class: middle, center

# CSS Transitions

---

## CSS Transitions

####CSS transitions, provide a way to control animation speed when changing CSS properties. 

Instead of having property changes take effect immediately, you can cause the changes in a property to take place over a period of time. 

For example, if you change the color of an element from white to black, usually the change is instantaneous. 

With CSS transitions enabled, changes occur at time intervals that follow an acceleration curve, all of which can be customized.


---

## CSS Transitions

####Animations that involve transitioning between two states are often called implicit transitions as the states in between the start and final states are implicitly defined by the browser.

CSS transitions let you decide: 

- which properties to animate (by **listing them explicitly**)

- when the animation will start (by **setting a delay**)

- how long the transition will last (by **setting a duration**)

- and how the transition will run (by **defining a timing function**, e.g. linearly or quick at the beginning, slow at the end).


---

## Animatable properties
  
These are some of the properties we can animate:

- background
- border
- color
- flex
- font (size, weight)
- margin and padding
- position (top, right, bottom, left)
- transform
- visibility
- z-index

.footnote[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties]


---

## Examples

![button](book.gif)

---

## Examples

![logo](logo_interaction.gif)

---

### CSS properties used to define transitions

CSS Transitions are controlled using the shorthand `transition` property. 

This is the best way to configure transitions, as it makes it easier to avoid that the lengths of the parameter list are out of sync, which can be very frustrating to have to spend lots of time debugging the CSS.

You can control the individual components of the transition with the following sub-properties:

**transition-property**

Specifies the name or names of the CSS properties to which transitions should be applied. 

```css
.element {
  transition-property: color;
}
```

.footnote[https://developer.mozilla.org/en-US/docs/Web/CSS/timing-function]

---

### CSS properties used to define transitions


**transition-duration**

Specifies the duration over which transitions should occur. You can specify a single duration that applies to all properties during the transition, or multiple values to allow each property to transition over a different period of time. 

```css
.element {
  /* using seconds */
  transition-duration: 1s;

  /* using milliseconds */
  transition-duration: 1000ms;
}
```

---

### CSS properties used to define transitions

**transition-timing-function**
      
Specifies a function to define how intermediate values for properties are computed. Timing functions determine how intermediate values of the transition are calculated. 

- linear
- ease
- ease-in
- ease-in-out
- ease-out

```css
.element {
  transition-timing-function: ease-in-out;
}
```

---

### CSS properties used to define transitions

**transition-timing-function**

- step-start
- step-end
- steps

```css
.element {
  /* There is 5 treads, the last one happens */
  /* right before the end of the animation. */
  transition-timing-function: steps(5, end);
  
  /* A two-step staircase, the first one happening */
  /* at the start of the animation. */
  transition-timing-function: steps(2, start);
  
  /* The second parameter is optional. */
  transition-timing-function: steps(2);
}
```

---

### CSS properties used to define transitions

**transition-timing-function**

- cubic-bezier(x1, y1, x2, y2)

```css
.element {
  transition-timing-function: cubic-bezier(0.1, 0.7, 1.0, 0.1);
}
```  

![cubic](cubic-bezier.png)

---

### CSS properties used to define transitions

**transition-delay**
      
Defines how long to wait between the time a property is changed and the transition actually begins.

```css
.element {
  transition-delay: 1s;
}
```

---

##CSS transition shorthand

The shorthand CSS syntax is written as follows:

```css
.element {
  transition: <property> <duration> <timing-function> <delay>;
}
```

```css
.element {
  transition: color 1s linear 1s;
}
```  

---

### A simple hover effect
      
```css
a {
  background-color: red;
  transition: background-color 0.5s ease;
}
a:hover {
  background-color: green;
}
```

---

### Multiple properties
      
You need to separate them by comma.

```css
a {
  transition: background-color 0.2s ease,
              padding 0.8s linear;
}
```

---

### All properties

You can use the **all** keyword to transition all animatable properties.

```css
a {
  transition: all 0.2s ease;
}
```

---

### Resources
      
- [CSS3 Transitions](http://www.w3schools.com/css/css3_transitions.asp)

- [Animatable properties](https://www.w3.org/TR/css3-transitions/#animatable-properties)

- [Transition property](https://css-tricks.com/almanac/properties/t/transition/)

- [Using CSS transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)

- [Cubic Bezier](http://cubic-bezier.com/)
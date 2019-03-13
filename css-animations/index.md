class: middle, center

# CSS Animations

---

## CSS Animations

####**CSS animations** make it possible to animate transitions from one CSS style configuration to another. 
      
Animations consist of two components:

- a style describing the CSS animation
- a set of keyframes that indicate the start and end states of the animation's style, as well as possible intermediate waypoints.

---

## CSS Animations

 There are three key advantages to CSS animations over traditional script-driven animation techniques:

- They're easy to use for simple animations; you can create them without even having to know JavaScript.

- The animations run well, even under moderate system load. Simple animations can often perform poorly in JavaScript (unless they're well made). The rendering engine can use frame-skipping and other techniques to keep the performance as smooth as possible.

- Letting the browser control the animation sequence lets the browser optimize performance and efficiency by, for example, reducing the update frequency of animations running in tabs that aren't currently visible.


---

## CSS Animations

To create a CSS animation sequence, you style the element you want to animate with the animation property or its sub-properties. 
      
This lets you configure the timing, duration, and other details of how the animation sequence should progress. 

This does not configure the actual appearance of the animation, which is done using the @keyframes at-rule.

---

### The sub-properties of the animation property

**animation-delay**

Configures the delay between the time the element is loaded and the beginning of the animation sequence.

**animation-direction**

Configures whether or not the animation should alternate direction on each run through the sequence or reset to the start point and repeat itself.

**animation-duration**

Configures the length of time that an animation should take to complete one cycle.

 **animation-iteration-count**

Configures the number of times the animation should repeat; you can specify infinite to repeat the animation indefinitely.

---

### The sub-properties of the animation property

**animation-name**

Specifies the name of the @keyframes at-rule describing the animation's keyframes.

**animation-play-state**

Lets you pause and resume the animation sequence.

**animation-timing-function**

Configures the timing of the animation; that is, how the animation transitions through keyframes, by establishing acceleration curves.

**animation-fill-mode**

Configures what values are applied by the animation before and after it is executing.

---

##Using keyframes

Once you've configured the animation's timing, you need to define the appearance of the animation. 

This is done by establishing two or more keyframes using the **@keyframes** at-rule. 

Each keyframe describes how the animated element should render at a given time during the animation sequence.

Since the timing of the animation is defined in the CSS style that configures the animation, keyframes use a percentage to indicate the time during the animation sequence at which they take place. 0% indicates the first moment of the animation sequence, while 100% indicates the final state of the animation. Because these two times are so important, they have special aliases: from and to. Both are optional. If from/0% or to/100% is not specified, the browser starts or finishes the animation using the computed values of all attributes.

You can optionally include additional keyframes that describe intermediate steps between the start and end of the animation.

---

##Using keyframes

Properties that aren't specified in every keyframe are interpolated (excepting those that can't be interpolated, which are dropped from the animation entirely).

```css
@keyframes animationName {
  0% { top: 0; left: 0; }
  30% { top: 50px; }
  68%, 72% { left: 50px; }
  100% { top: 100px; left: 100%; }
}
```

```css
div.test {
  animation-duration: 3s;
  animation-delay: 2s;
  animation-name: animationName;
}
```

---

###animation-delay, animation-duration

time (s, ms)

```css
animation-delay: 3s;
animation-duration: 2s, 4ms;
```

---

###animation-direction

**normal**

The animation should play forward each cycle. In other words, each time the animation cycles, the animation will reset to the beginning state and start over again. This is the default animation direction setting.

**reverse**

The animation plays backward each cycle. Each time the animation cycles, the animation resets to the end state and start over again.

**alternate**

The animation should reverse direction each cycle. When playing in reverse, the animation steps are performed backward. In addition, timing functions are also reversed; for example, an ease-in animation is replaced with an ease-out animation when played in reverse. The count to determine if it is an even or an odd iteration starts at one.

**alternate-reverse**
The animation plays backward on the first play-through, then forward on the next, then continues to alternate. The count to determinate if it is an even or an odd iteration starts at one. 
      
---

###animation-direction

```css
/* Single animation */
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;

/* Multiple animations */
animation-direction: normal, reverse;
animation-direction: alternate, reverse, normal;

/* Global values */
animation-direction: inherit;
animation-direction: initial;
animation-direction: unset;
```
---

###animation-iteration-count
      

**infinite**

The animation will repeat forever.

**number**

The number of times the animation should repeat; this is 1 by default. Negative values are invalid. You may specify non-integer values to play part of an animation cycle (for example 0.5 will play half of the animation cycle).

```css
animation-iteration-count: infinite;
animation-iteration-count: 3;
animation-iteration-count: 2.3;
```
      
---

###animation-name
      
**string**

This identifier is composed by a combination of case-insensitive letters a to z, numbers 0 to 9, underscores (_), and/or dashes (-). The first non-dash character must be a letter (that is, no number at the beginning of it, even if preceded by a dash.) Also, two dashes are forbidden at the beginning of the identifier. It can't be none, unset, initial, or inherit in any combination of cases.

```css
animation-name: myAnimationName;
```

**none**

Is a special keyword denoting no keyframes. It can be used to deactivate an animation without changing the ordering of the other identifiers, or to deactivate animations coming from the cascade.

```css
animation-name: none;
```

---

###animation-play-state

**running**

The animation is currently playing.

```css
animation-play-state: running;
```

**paused**

The animation is currently paused. 


```css
animation-play-state: paused;
```

---

###animation-timing-function
      
```css
/* Keyword values */
animation-timing-function: ease;
animation-timing-function: ease-in;
animation-timing-function: ease-out;
animation-timing-function: ease-in-out;
animation-timing-function: linear;
animation-timing-function: step-start;
animation-timing-function: step-end;

/* Function values */
animation-timing-function: cubic-bezier(0.1, 0.7, 1.0, 0.1);
animation-timing-function: steps(4, end);
```

---

###animation-fill-mode

**none**

The animation will not apply any styles to the target before or after it is executing.

**forwards**

The target will retain the computed values set by the last keyframe encountered during execution.

**backwards**

The animation will apply the values defined in the first relevant keyframe as soon as it is applied to the target, and retain this during the animation-delay period. 

**both**

The animation will follow the rules for both forwards and backwards, thus extending the animation properties in both directions.

---

###Resources

- [CSS3 Animations](http://www.w3schools.com/css/css3_animations.asp)
- [Animation property](https://css-tricks.com/almanac/properties/a/animation/)
- [CSS Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations)
- [CSS Animation for Beginners](https://robots.thoughtbot.com/css-animation-for-beginners)
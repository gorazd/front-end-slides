class: middle, center

# CSS Custom Properties

---

## CSS Custom Properties

####CSS Custom Properties for Cascading Variables is a CSS module that allows for the creation of custom properties that can be used over and over.

Property names that are prefixed with --, like --example-name, represent custom properties that contain a value that can be used in other declarations using the var() function.

Custom properties are scoped to the element(s) they are declared on, and participate in the cascade: the value of such a custom property is that from the declaration decided by the cascading algorithm.

---

## CSS Custom Properties

Declaring a custom property:

```css
element {
  --main-bg-color: brown;
}
```

Using the custom property:

```css
element {
  background-color: var(--main-bg-color);
}
```

By declaring a custom property on the :root pseudo-class and using it where needed throughout the document, a CSS author can reduce the need for repetition:

```css
:root {
  --main-bg-color: brown;
}
```

---

## Resources

- [Using CSS custom properties (variables)](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [CSS Custom Properties Draft](https://drafts.csswg.org/css-variables/)
- [It's Time To Start Using CSS Custom Properties](https://www.smashingmagazine.com/2017/04/start-using-css-custom-properties/)
- [A Strategy Guide To CSS Custom Properties](https://www.smashingmagazine.com/2018/05/css-custom-properties-strategy-guide/)
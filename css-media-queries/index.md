class: middle, center

# CSS Media Queries

---

## CSS Media Queries

####A media query consists of a media type and at least one expression that limits the style sheets' scope by using media features, such as width, height, and color. 
      
Media queries, added in CSS3, let the presentation of content be tailored to a specific range of output devices without having to change the content itself.

Media queries consist of a media type and can, as of the CSS3 specification, contain one or more expressions, expressed as media features, which resolve to either true or false.  
      
The result of the query is true if the media type specified in the media query matches the type of device the document is being displayed on and all expressions in the media query are true.

---

## CSS Media Queries
      
```html
<!-- CSS media query on a link element -->
<link rel="stylesheet" media="(max-width: 800px)" href="example.css" />
```

```html
<!-- CSS media query within a stylesheet -->
<style>
  @media (max-width: 600px) {
    .facet_sidebar {
      display: none;
    }
  }
</style>
```

---

## Media Types

####Media types describe the general category of a device.

**all**

Suitable for all devices.

**print**

Intended for paged material and for documents viewed on screen in print preview mode. Please consult the section on paged media, and the media section of the Getting Started tutorial for information about formatting issues that are specific to paged media.

**screen**

Intended primarily for color computer screens.

**speech**

Intended for speech synthesizers. Note: CSS2 had a similar media type called 'aural' for this purpose. See the appendix on aural style sheets for details. 


---

## Media Features

####Media features describe specific characteristics of the user agent, output device, or environment. (resolution, oreientation, pixel density,...)


**width** 	

Viewport width 	
  
**height**

Viewport height 	
  
**aspect-ratio**

Width-to-height aspect ratio of the viewport

.footnote[https://developer.mozilla.org/en-US/docs/Web/CSS/@media]

---

## Media Query Logical operators
      
####You can compose complex media queries using logical operators, including not, and, and only. 

**and**

The and keyword is used for combining multiple media features together, as well as combining media features with media types.

**not**

The not keyword applies to the whole media query and returns true if the media query would otherwise return false.

**only**

The only keyword prevents older browsers that do not support media queries with media features from applying the given styles.
      

---

## Media Query Examples


```css
@media print {
  body { 
    font-size: 10pt; 
  }
}
```
This CSS targets a printer device.



```css
@media (min-width: 700px) { ... }
```
This CSS will apply styles only if your browser's viewport width is equal to or larger than 700px.

```css
@media (min-width: 700px) and (max-width: 1200px) { ... }
```
This CSS will apply styles only if your browser's viewport width is equal to or larger than 700px and narrower than 1200px.
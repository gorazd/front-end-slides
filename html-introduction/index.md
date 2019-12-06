class: center, middle

##HTML Introduction

---

##HTML

**HyperText Markup Language**, commonly referred to as HTML, is the standard markup language used to create web pages. 

Web browsers can read HTML files and render them into visible or audible web pages.

---

##HTML

HTML is a markup language. The word markup was used by editors who marked up manuscripts (usually with a blue pencil) when giving instructions for revisions. 

"Markup" now means something slightly different: a language with specific syntax that instructs a Web browser how to display a page. 

---

##History

In 1980, physicist Tim Berners-Lee, then a contractor at CERN, proposed and prototyped ENQUIRE, a system for CERN researchers to use and share documents. 

In 1989, Berners-Lee wrote a memo proposing an Internet-based hypertext system.

Berners-Lee specified HTML and wrote the browser and server software in late 1990. 

He is best known as the inventor of the **World Wide Web**.

Berners-Lee is the director of the World Wide Web Consortium (**W3C**), which oversees the Web's continued development.

.footnote[https://en.wikipedia.org/wiki/Tim_Berners-Lee]
      
---

##W3C

The World Wide Web Consortium (W3C) is the main international standards organization for the World Wide Web (abbreviated WWW or W3).

The organization tries to foster compatibility and agreement among industry members in the adoption of new standards defined by the W3C. 

Incompatible versions of **HTML** are offered by different vendors, causing inconsistency in how web pages are displayed. The consortium tries to get all those vendors to implement a set of core principles and components which are chosen by the consortium.


.footnote[https://en.wikipedia.org/wiki/World_Wide_Web_Consortium]

---

##HTML versions

The first publicly available description of HTML was a document called "HTML Tags", first mentioned on the Internet by Berners-Lee in late 1991.

It describes 18 elements comprising the initial, relatively simple design of HTML. Eleven of these elements still exist in HTML 4.

- 1995 **HTML 2.0**

- 1997 **HTML 3.2**

It was the first version developed and standardized exclusively by the **W3C**, as the IETF had closed its HTML Working Group in September 12, 1996.

- 1997 **HTML 4**

- 1999 **HTML 4.01**

.footnote[https://en.wikipedia.org/wiki/HTML]
      
---

##XHTML

After HTML 4.01, the next revision to the language was called XHTML 1.0.

**Extensible Hypertext Markup Language** is part of the family of XML markup languages. It mirrors or extends versions of the widely used Hypertext Markup Language (HTML), the language in which Web pages are formulated.

The content of the XHTML 1.0 specification was identical to that of HTML 4.01. No new elements or attributes were added. The only difference was in the syntax of the language. Whereas HTML allowed authors plenty of freedom in how they wrote their elements and attributes, XHTML required authors to follow the rules of XML, a stricter markup language upon which the W3C was basing most of their technologies.

.footnote[https://en.wikipedia.org/wiki/XHTML]
      
---

##Birth of HTML5

HTML5 was being developed at the WHATWG (Web Hypertext Application Technology Working Group), the W3C continued working on XHTML 2.

In October 2006, Sir Tim Berners-Lee wrote a blog post in which he admitted that the attempt to move the web from HTML to XML just wasn’t working. A few months later, the W3C issued a new charter for an HTML Working Group. Rather than start from scratch, they wisely decided that the work of the WHATWG should be used as the basis for any future version of HTML.

The W3C was simultaneously working on two different, incompatible types of markup: XHTML 2 and HTML 5. Meanwhile a separate organization, the WHATWG, was working on a specification called HTML5 that would be used as a basis for one of the W3C specifications.

.footnote[https://en.wikipedia.org/wiki/WHATWG]
      
---

##Birth of HTML5

The W3C announced that the charter for XHTML 2 would not be renewed. The format had been as good as dead for several years; this announcement was little more than a death certificate.

There are two groups working on HTML5. The WHATWG is creating an HTML5 specification using its process of “commit then review.” The W3C HTML Working Group is taking that specification and putting it through its process of “review then commit.”
      

---

##HTML5

**HTML5**  is a markup language used for structuring and presenting content on the World Wide Web. It was finalized, and published, on 28 October 2014 by the World Wide Web Consortium (W3C). This is the fifth revision of the HTML standard since the inception of the World Wide Web.
```xml
<!DOCTYPE html> 
```

.footnote[https://en.wikipedia.org/wiki/HTML5]

---

class: center, middle

# HTML markup & elements

---

##HTML

Once again, HTML separates "content" (words, images, audio, video, and so on) from "presentation" (instructions for displaying each type of content). 

HTML uses a pre-defined set of elements to define content types. Elements contain one or more "tags" that contain or express content. Tags are enclosed by angle brackets, and the closing tag begins with a forward slash.

```html
<h1>Heading text</h1>
```
```html
<p>Paragraph text</p>
```
```html
<img src="imagefile.jpg" alt="Duomo of Milano" >
```
      
---

##HTML

HTML consists of a set of elements, which define the **semantic meaning** of their content. Elements include two matching tags and everything in between. For example, the `<p>` element indicates a paragraph; the `<img>` element indicates an image.

Most elements may contain other elements, forming a hierarchic structure.

```html
<html>
  <body>
    <p>Body text</p>
  </body>
</html>
```

---

##HTML

**Semantic HTML** is the use of HTML markup to reinforce the semantics, or meaning, of the information in webpages and web applications rather than merely to define its presentation or look. 

Semantic HTML is processed by traditional web browsers as well as by many other user agents.

As an example, recent HTML standards discourage use of the tag `<i>` (italic) in preference of more accurate tags such as `<em>` (emphasis). 

.footnote[https://en.wikipedia.org/wiki/Semantic_HTML]

---

class: center, middle

# HTML Elements

---

##`Tags`

HTML documents are written in plain text. You can write HTML in any text editor that lets you save content as plain text (e.g. Notepad, Notepad++, or Sublime Text),  but most HTML authors prefer to use a specialized editor that highlights syntax and shows the DOM. You may use uppercase for tag names, but the W3C (the global consortium that maintains the HTML standard) recommends using lower case (and XHTML requires lower case).

```xml
<p>This is text within a paragraph.</p>
```
Some elements do not contain any text content or any other elements. These are empty elements and need no closing tag. This is an example:

```xml
<img src="image.jpg" alt="" >
```


---

##`Attributes`

The start tag may contain additional information, as in the preceding example. Such information is called an attribute. Attributes usually consist of 2 parts:

- An attribute name
- An attribute value

```xml
<p class="introduction">This is text within...</p>
```

```xml
<img src="image.jpg" alt="" >
```


---

##`Comments`

HTML has a mechanism for embedding comments that are not displayed when the page is rendered in a browser. 

This is useful for explaining a section of markup, leaving notes for other people who might work on the page, or for leaving reminders for yourself.

```xml
<!-- This is comment -->
```


---

##`<doctype>`

A document type declaration, or DOCTYPE, is an instruction that associates a particular SGML or XML document (for example, a webpage) with a document type definition (DTD) (for example, the formal definition of a particular version of HTML).

The <!DOCTYPE> declaration is not an HTML tag; it is an instruction to the web browser about what version of HTML the page is written in.

```xml
<!DOCTYPE html> 
```

      
---

##`<html>`

Basic elements are the backbone of any HTML document.

The HTML `<html>` element (or HTML root element) represents the root of an HTML document. All other elements must be descendants of this element.
      
---

class: center, middle

# Document metadata

---

##`<base>`

The HTML `<base>` element specifies the base URL to use for all relative URLs contained within a document. There can be only one `<base>` element in a document.

```html
<head>
  <base href="http://www.my.com/" target="_blank">
</head>

<body>
  <img src="image.gif">
</body>
```
results in
```html
<img src="http://www.my.com/image.gif">
```

      
---

##`<head>`

The HTML `<head>` element provides general information (metadata) about the document, including its title and links to/definitions of scripts and style sheets.

```html
<head>
</head>
```
      
---

##`<meta>`

The HTML `<meta>` element provides metadata about the HTML document. 

Metadata will not be displayed on the page, but will be machine parsable.

```html
<head>
*  <meta charset="UTF-8">
*  <meta name="description" content="HTML">
*  <meta name="keywords" content="HTML,HTML5,XHTML">
*  <meta name="author" content="Author Name">
</head>
```
      
---

##`<title>`

The HTML `<title>` element defines the title of the document, shown in a browser's title bar or on the page's tab. It can only contain text and any contained tags are not interpreted.

```html
<head>
*  <title>Title of my website</title>
</head>
```
      
---

##`<style>`

  The HTML `<style>` element contains style information for a document, or part of a document. By default, the style instructions written inside that element are expected to be CSS.

```html
<head>
  <title>Title of my website</title>
*  <style>
*    body { color: black; background: white; }
*  </style>
</head>
```
      
---

##`<script>`

The HTML `<script></script>` element either contains scripting statements, or it points to an external script file through the src attribute.

Common uses for **JavaScript** are image manipulation, form validation, and dynamic changes of content.

```html
<head>
  <title>Title of my website</title>
* <script type="text/javascript" src="file.js"></script>
</head>
```
Simplify to:
```html
<script src="file.js"></script>
```
      
---

##`<link>`

The HTML `<link>` element defines a link between a document and an external resource.

It is used to link to external style sheets.

```html
<head>
*  <link rel="stylesheet" type="text/css" href="style.css">
</head>
```
Simplify to:

```html
<link rel="stylesheet" href="style.css">
```

      
---

##`<body>`

The HTML `<body>` element represents the content of an HTML document. There can be only one `<body>` element in a document.

```html
<head>
  <title>Title of my website</title>
  <style>
    body { color: black; background: white; }
  </style>
</head>

*<body>
*  
*</body>
```
      
---

class: center, middle

# Content sectioning

---

##`<article>`

The HTML `<article>` Element represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). This could be a forum post, a magazine or newspaper article, a blog entry, an object, or any other independent item of content. Each `<article>` should be identified, typically by including a heading (`<h1>-<h6>` element) as a child of the `<article>` element.

```html
<article>
</article>
```
      
---

##`<h1>`
```
<h2>
<h3>
<h4>
<h5>
<h6>
```

**Heading elements** implement six levels of document headings, `<h1>` is the most important and `<h6>` is the least. A heading element briefly describes the topic of the section it introduces. Heading information may be used by user agents, for example, to construct a table of contents for a document automatically.
```html
<article>
*<h1>Article title</h1>
</article>
```
      
---

##`<address>`

  The HTML `<address>` element supplies contact information for its nearest `<article>` or `<body>` ancestor; in the latter case, it applies to the whole document.
  
```html
<article>
<h1>Article title</h1>
*<address>
*    You can contact author at www.somedomain.com.
*</address>
</article>
```
      
---

##`<hgroup>`

  The HTML `<hgroup>` Element (HTML Headings Group Element) represents the heading of a section. It defines a single title that participates in the outline of the document as the heading of the implicit or explicit section that it belongs to.
```html
<article>
*<hgroup>
*  <h1>Article title</h1>
*  <h2>Subtitle</h2>
*</hgroup>
<address>
    You can contact author at www.somedomain.com.
</address>
</article>
```
  .footnote[This element has been removed from the HTML5 (W3C) specification, but it still is in the WHATWG version of HTML.]
      
---

##`<nav>`

  The HTML Navigation Element represents a section of a page that links to other pages or to parts within the page: a section with navigation links.

```html
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/events">Current Events</a></li>
      ...more...
    </ul>
  </nav>
```
      
---

##`<section>`

  The HTML Section Element represents a generic section of a document, i.e., a thematic grouping of content, typically with a heading. Each `<section>` should be identified, typically by including a heading (`<h1>-<h6>` element) as a child of the `<section>` element.
```html
  <section>
    <h1>Title</h1>
    <p>Body text</p>
  </section>
```
      
---

class: center, middle

# Text Content

---

##`<a>`

The HTML Anchor Element (`<a>`) defines a hyperlink to a location on the same page or any other page on the Web. It can also be used (in an obsolete way) to create an anchor point—a destination for hyperlinks within the content of a page, so that links aren't limited to connecting simply to the top of a page.
  
```html
<a href="http://www.website.com">Link to a website</a>
```  
```html
<a href="mailto:info@website.com">Email link</a>
```  

---

##`<div>`

The HTML `<div>` element (or HTML Document Division Element) is the generic container for flow content, which does not inherently represent anything. It can be used to group elements for styling purposes (using the class or id attributes), or because they share attribute values, such as lang. It should be used only when no other semantic element (such as `<article>` or `<nav>`) is appropriate.


---

##`<dl>`


  The HTML `<dl>` Element (or HTML Description List Element) encloses a list of pairs of terms and descriptions. Common uses for this element are to implement a glossary or to display metadata (a list of key-value pairs).

---

##`<dt>`


The HTML `<dt>` element (or HTML Definition Term Element) identifies a term in a definition list. This element can occur only as a child element of a `<dl>`. It is usually followed by a `<dd>` element; however, multiple `<dt>` elements in a row indicate several terms that are all defined by the immediate next `<dd>` element.


---

##`<dd>`

  
  The HTML Description Element (`<dd>`) indicates the description of a term in a description list (`<dl>`) element. This element can occur only as a child element of a definition list and it must follow a `<dt>` element.


  ```html
  <dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language...</dd>
  </dl>
  ```

---

##`<hr>`

  The HTML `<hr>` element represents a thematic break between paragraph-level elements (for example, a change of scene in a story, or a shift of topic with a section). In previous versions of HTML, it represented a horizontal rule. It may still be displayed as a horizontal rule in visual browsers, but is now defined in semantic terms, rather than presentational terms.

```html
<p>Body text</p>
<hr>
<p>Body text</p>
```

---

##`<li>`

  The HTML List Item Element (`<li>`) is used to represent an item in a list. It must be contained in a parent element: an ordered list (`<ol>`), an unordered list (`<ul>`), or a menu (`<menu>`). In menus and unordered lists, list items are usually displayed using bullet points. In ordered lists, they are usually displayed with an ascending counter on the left, such as a number or letter.


---

##`<ul>`

The HTML unordered list element (`<ul>`) represents an unordered list of items, namely a collection of items that do not have a numerical ordering, and their order in the list is meaningless. Typically, unordered-list items are displayed with a bullet, which can be of several forms, like a dot, a circle or a squared. The bullet style is not defined in the HTML description of the page, but in its associated CSS, using the list-style-type property.

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

- Item 1
- Item 2

---

##`<ol>`

  The HTML `<ol>` Element (or HTML Ordered List Element) represents an ordered list of items. Typically, ordered-list items are displayed with a preceding numbering, which can be of any form, like numerals, letters or Romans numerals or even simple bullets. This numbered style is not defined in the HTML description of the page, but in its associated CSS, using the list-style-type property.
```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
```

1. Item 1
2. Item 2

---

##`<p>`

  The HTML `<p>` element (or HTML Paragraph Element) represents a paragraph of text.

```html
<p>
  Body text.
</p>
```

---

##`<pre>`

The HTML Preformatted Text (`<pre>`) represents preformatted text. Text within this element is typically displayed in a non-proportional font exactly as it is laid out in the file. Whitespaces inside this element are displayed as typed.

```html
<pre>
body {
  color:red;
}
</pre>
```

---

class: center, middle

# Inline text

---

##`<br>`

The HTML `<br>` Element (or HTML Line Break Element) produces a line break in text (carriage-return). It is useful for writing a poem or an address, where the division of lines is significant.

```html
<p>Text<br>Text in a new line</p>
```
outputs to

Text<br>
Text in a new line

---

##`<em>`

The HTML Emphasis Element (`<em>`) marks text that has stress emphasis. The `<em>` element can be nested, with each level of nesting indicating a greater degree of emphasis.

```html
<p>Text<br><em>Text in italics</em></p>
```

outputs to

Text<br>
<em>Text in italics</em>

---

##`<span>`

The HTML `<span>` element is a generic inline container for phrasing content, which does not inherently represent anything. 

It can be used to group elements for styling purposes (using the class or id attributes), or because they share attribute values, such as lang. 

It should be used only when no other semantic element is appropriate. `<span>` is very much like a `<div>` element, but `<div>` is a block-level element whereas a `<span>` is an inline element.


---

class: center, middle

# Images and multimedia

---

##`<img>`

The HTML Image Element (`<img>`) represents an image in the document.

```html
<img src="image.jpg" alt="Image content">
```

---

##`<audio>`

The HTML `<audio>` element is used to embed sound content in documents. It may contain several audio sources, represented using the src attribute or the `<source>` element; the browser will choose the most suitable one.

```html
<audio controls="controls">
  Your browser does not support the 
  <code>audio</code> element.
  <source src="audio-file.wav" type="audio/wav">
</audio>
```

```html
<audio src="audio-file.wav" autoplay>
  Your browser does not support the 
  <code>audio</code> element.
</audio>
```

---

##`<video>`

The HTML `<video>` element is used to embed video content. It may contain several video sources, represented using the src attribute or the `<source>` element; the browser will choose the most suitable one.

```html
<video src="videofile.ogg" poster="posterimage.jpg">
  Sorry, your browser doesn't 
  support embedded videos, 
  but don't worry, you can 
  <a href="videofile.ogg">download it</a>
  and watch it with your 
  favorite video player!
</video>
```

---

##```Boilerplate```

Boilerplate is any text that is or can be reused in new contexts or applications without being greatly changed from the original.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Starting boilerplate</title>
</head>
<body>
  <h1>Main title</h1>
  <p>Body text</p>
</body>
</html>
```



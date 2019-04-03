class: middle, center

# JavaScript Statements

---

## Statements

In HTML, JavaScript statements are "instructions" to be "executed" by the web browser.

```js
document.getElementById("demo").innerHTML = "Hello.";
```

Statements are separated by semicolon.

---

## Programs

Most JavaScript programs contain many JavaScript statements. The statements are executed, one by one, in the same order as they are written.

```js
var x = 5;
var y = 6;
var z = x + y;
document.getElementById("demo").innerHTML = z;
```

---

## Code Blocks
JavaScript statements can be grouped together in code blocks, inside curly brackets {...}. The purpose of code blocks is to define statements to be executed together.

One place you will find statements grouped together in blocks, are in JavaScript functions:

```js
function myFunction() {
  document.getElementById("demo").innerHTML = "Hello Dolly.";
  document.getElementById("myDIV").innerHTML = "How are you?";
}
```
```html
<button type="button" onclick="myFunction()">Try it</button>
```

---

## Operators

**Arithmetic** operators are used to perform arithmetic on numbers (literals or variables).

`+`	Addition

`-`	Subtraction

`*`	Multiplication

`/`	Division

`%`	Modulus

`++`	Increment

`--`	Decrement

---

## Operators

**Assignment** operators assign values to JavaScript variables.

`=`  `x = y` `x = y`

`+=`	`x += y` `x = x + y`

`-=`	`x -= y` `x = x - y`

`*=`	`x *= y` `x = x * y`

`/=`	`x /= y` `x = x / y`

`%=`	`x %= y` `x = x % y`

---

## Operators

**String** operators are used to add (concatenate) strings.

```js
txt1 = "John";
txt2 = "Doe";
txt3 = txt1 + " " + txt2;
```
The result of txt3 will be:

```js
John Doe
```

---

## Operators

**Comparison and Logical** Operators

`==`	equal to

`===`	equal value and equal type

`!=`	not equal

`!==`	not equal value or not equal type

`<`	less than

`>`	greater than

`<=`	less than or equal to

`>=`	greater than or equal to

`?`	ternary operator

---

## Operators

**Type** Operators

`typeof`	

Returns the type of a variable

`instanceof`	

Returns true if an object is an instance of an object type

---

## Functions

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

```js
function myFunction(a, b) {
    return a * b;
}
document.getElementById("demo").innerHTML = myFunction(4, 3);
```

---

##Function Syntax

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

```js
function name(parameter1, parameter2, parameter3) {
    code to be executed
}
```
Function parameters are the names listed in the function definition.

Function arguments are the real values received by the function when it is invoked.

---

## Function Invocation

The code inside the function will execute when "something" invokes (calls) the function:

- When an event occurs (when a user clicks a button)
- When it is invoked (called) from JavaScript code
- Automatically (self invoked)

---

## Function Return

When JavaScript reaches a return statement, the function will stop executing.

If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.

Functions often compute a return value. The return value is "returned" back to the "caller":


```js
var x = myFunction(4, 3);        // Function is called, return value will end up in x

function myFunction(a, b) {
    return a * b;                // Function returns the product of a and b
}
```

---

## Why use Functions?

You can reuse code: Define the code once, and use it many times.

You can use the same code many times with different arguments, to produce different results.


```js
function toCelsius(fahrenheit) {
    return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);
```

---

## Output
      
JavaScript does NOT have any built-in print or display functions.

**JavaScript Display Possibilities**

JavaScript can "display" data in different ways:

- Writing into an alert box, using **window.alert()**
- Writing into the HTML output using **document.write()**
- Writing into an HTML element, using **innerHTML**
- Writing into the browser console, using **console.log()**

**window.alert()**

```js
window.alert("This will come out in the browser");
```

---

## Output

**document.write()**

```js
document.write("This will come out in the HTML");
```

**innerHTML**
 ```js
document.getElementById("demo").innerHTML = "This...";
```

**console.log()**

```js
console.log("This will be logged in the console");
```

---

##Selecting elements

**Select an element by ID**

Returns a reference to the element by its ID; the ID is a string which can be used to identify the element; it can be established using the id attribute in HTML, or from script.

```js
var el = document.getElementById('foo');
el.innerHTML = 'Hello World!';
```

---

##Selecting elements

**Select elements by tag name**

Returns an HTMLCollection of elements with the given tag name. The complete document is searched, including the root node. The returned HTMLCollection is live, meaning that it updates itself automatically to stay in sync with the DOM tree without having to call document.getElementsByTagName() again.

```js
var list = document.getElementsByTagName('a');

// get the number of selected elements
console.log(list.length);

// iterate over elements and output href attribute values
for (var i=0; i < list.length; i++)
    console.log(list[i].href);
```

---

##Selecting elements

**Select elements by class name**

Returns an array-like object of all child elements which have all of the given class names. When called on the document object, the complete document is searched, including the root node. 

```js
var list = document.getElementsByClassName('foo');

// get the number of selected elements
console.log(list.length);

// iterate over elements and output their HTML content
for (var i=0; i<list.length; i++)
    console.log(list[i].innerHTML);
```

You may also call getElementsByClassName() on any element; it will return only elements which are descendants of the specified root element with the given class names.

```js
var container = document.getElementById('header');
var list = container.getElementByClassName('foo');
```

---

##Selecting elements

**Select elements by selectors**

Returns the first element within the document (using depth-first pre-order traversal of the document's nodes|by first element in document markup and iterating through sequential nodes by order of amount of child nodes) that matches the specified group of selectors.

```js
var el = document.querySelector(".myclass");
```

Selectors can also be really powerful as demonstrated in the following example. Here, the first element `<input name="login"/>` within a `<div class="user-panel main">` in the document is returned:

```js
var el = document.querySelector("div.user-panel.main input[name=login]");
```

---

## Manipulating elements

**Create a DOM element**

This creates a new `<div>` and inserts it before the element with the ID "div1".

```js
document.body.onload = addElement;

function addElement () { 
  // create a new div element 
  // and give it some content 
  var newDiv = document.createElement("div"); 
  var newContent = document.createTextNode("Hi there and greetings!"); 
  newDiv.appendChild(newContent); //add the text node to the newly created div. 

  // add the newly created element and its content into the DOM 
  var currentDiv = document.getElementById("div1"); 
  document.body.insertBefore(newDiv, currentDiv); 
}
```

---

## Manipulating elements

**Get and set the HTML content of an element**


The Element.innerHTML property sets or gets the HTML syntax describing the element's descendants.

```js
var el = document.querySelector('div');

// get HTML content
console.log(el.innerHTML);

// set HTML content
el.innerHTML = '<p>Hello World!</p>'
```

---

## Manipulating elements

**Removing an element**


The Node.removeChild() method removes a child node from the DOM. Returns removed node.

```js
  var el = document.querySelector('div');
  el.parentNode.removeChild(el);
```

So, first select the element to remove. Then walk up the tree to its parent and remove the child element from there.

---

## Manipulating elements
**Replace a DOM element**

Replacing one element with another by use of the cross-browser safe DOM method replaceChild():

```js
// select the element that will be replaced
var el = document.querySelector('div');

// <a href="/javascript/manipulation/creating-a-dom-element-51/">create a new element</a> that will take the place of "el"
var newEl = document.createElement('p');
newEl.innerHTML = '<b>Hello World!</b>';

// replace el with newEL
el.parentNode.replaceChild(newEl, el);
```

---

## Manipulating elements

**Empty an element's content**


Use the innerHTML property of an element for removing all child elements, and thus clearing its content:

```js
var el = document.querySelector('div');
el.innerHTML = '';
```

---

## Events

Event handlers bound to any part of the element's content are destroyed in the process.

#### **addEventListener();**

The EventTarget.addEventListener() method registers the specified listener on the EventTarget it's called on. The event target may be an Element in a document, the Document itself, a Window, or any other object that supports events (such as XMLHttpRequest).

```js
var el = document.getElementById("outside");

el.addEventListener("click", doSomething, false);

function doSomething() {
  
};
```

---

## Events

#### Arguments

```js
target.addEventListener(type, listener[, useCapture]);
```

**type**

A string representing the event type to listen for.

For example: blur, click, keydown, load, mouseenter, mousemove, mouseover, resize, scroll...

Event types:
https://developer.mozilla.org/en-US/docs/Web/Events

**listener**

The object that receives a notification (an object that implements the Event interface) when an event of the specified type occurs. This must be an object implementing the EventListener interface, or simply a JavaScript function.**addEventListener();**

---

## Events

#### Arguments

**useCapture**

A Boolean that indicates that events of this type will be dispatched to the registered listener before being dispatched to any EventTarget beneath it in the DOM tree. 

Events that are bubbling upward through the tree will not trigger a listener designated to use capture. Event bubbling and capturing are two ways of propagating events that occur in an element that is nested within another element, when both elements have registered a handle for that event. The event propagation mode determines the order in which elements receive the event.

If not specified, useCapture defaults to false. 

---

## Events

#### **removeEventListener();**

The EventTarget.removeEventListener() method removes the event listener previously registered with EventTarget.addEventListener().

```js
var el = document.getElementById("outside");

el.addEventListener("click", doSomething, false);

function doSomething() {
  el.removeEventListener("click", doSomething, false);
};
```
---

## Events

#### Arguments

```js
target.removeEventListener(type, listener[, useCapture]);
```

**type**

A string representing the event type to remove.

**listener**

The EventListener function to remove from the event target.

**useCapture**

Specifies whether the EventListener to be removed is registered as a capturing listener or not. If this parameter is absent, a default value of false is assumed.

If a listener is registered twice, one with capture and one without, remove each one separately. Removal of a capturing listener does not affect a non-capturing version of the same listener, and vice versa.

---

## Sources

* [W3S JavaScript](http://www.w3schools.com/js/)
* [Mozilla Developer Network JS](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [Plain JavaScript](https://plainjs.com)
* [You Might Not Need jQuery](http://youmightnotneedjquery.com)

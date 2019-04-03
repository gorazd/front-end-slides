class: middle, center

# JavaScript Data types

---

## Data types

The latest ECMAScript standard defines seven data types:

- Six data types that are **primitives**:

  - **Boolean**. true and false.
  - **null**. A special keyword denoting a null value. Because JavaScript is case-sensitive, null is not the same as Null, NULL, or any other variant.
  - **undefined**. A top-level property whose value is undefined.
  - **Number**. 42 or 3.14159.
  - **String**. "Howdy"
  - **Symbol** (new in ECMAScript 2015). A data type whose instances are unique and immutable.

- and **Object**

Although these data types are a relatively small amount, they enable you to perform useful functions with your applications. 

Objects and functions are the other fundamental elements in the language. 

You can think of objects as named containers for values, and functions as procedures that your application can perform.

---

## Data type conversion
      
JavaScript is a dynamically typed language. That means you don't have to specify the data type of a variable when you declare it, and data types are converted automatically as needed during script execution. So, for example, you could define a variable as follows:

```js
var answer = 42;
```

And later, you could assign the same variable a string value, for example:

```js
answer = "Thanks for all the fish...";
```

Because JavaScript is dynamically typed, this assignment does not cause an error message.

---

## Data type conversion

In expressions involving numeric and string values with the + operator, JavaScript converts numeric values to strings. For example, consider the following statements:
      
```js
x = "The answer is " + 42 // "The answer is 42"
y = 42 + " is the answer" // "42 is the answer"
```

In statements involving other operators, JavaScript does not convert numeric values to strings. For example:

```js
"37" - 7 // 30
"37" + 7 // "377"
```

---

##Converting strings to numbers

In the case that a value representing a number is in memory as a string, there are methods for conversion.

- parseInt()
- parseFloat()

parseInt will only return whole numbers, so its use is diminished for decimals. Additionally, a best practice for parseInt is to always include the radix parameter. The radix parameter is used to specify which numerical system is to be used.

An alternative method of retrieving a number from a string is with the + (unary plus) operator:

```js
"1.1" + "1.1" = "1.11.1"
(+"1.1") + (+"1.1") = 2.2   
// Note: the parentheses are added for clarity, not required.
```

---

## Literals
     
You use literals to represent values in JavaScript. These are fixed values, not variables, that you literally provide in your script. 

- Array literals
- Boolean literals
- Floating-point literals
- Integers
- Object literals
- RegExp literals
- String literals

---

## Array literals
     
An array literal is a list of zero or more expressions, each of which represents an array element, enclosed in square brackets ([]). When you create an array using an array literal, it is initialized with the specified values as its elements, and its length is set to the number of arguments specified.

The following example creates the coffees array with three elements and a length of three:


```js
var coffees = ["French Roast", "Colombian", "Kona"];
```

---

## Boolean literals

The Boolean type has two literal values: true and false.

Do not confuse the primitive Boolean values true and false with the true and false values of the Boolean object. The Boolean object is a wrapper around the primitive Boolean data type. 

```js
var examPassed = true;
```

---

## Integers

Integers can be expressed in decimal (base 10), hexadecimal (base 16), octal (base 8) and binary (base 2).

- Decimal integer literal consists of a sequence of digits without a leading 0 (zero).
- Leading 0 (zero) on an integer literal, or leading 0o (or 0O) indicates it is in octal. Octal integers can include only the digits 0-7.
- Leading 0x (or 0X) indicates hexadecimal. Hexadecimal integers can include digits (0-9) and the letters a-f and A-F.
- Leading 0b (or 0B) indicates binary. Binary integers can include digits only 0 and 1.

Some examples of integer literals are:

```js
0, 117 and -345 (decimal, base 10)
015, 0001 and -0o77 (octal, base 8) 
0x1123, 0x00111 and -0xF1A7 (hexadecimal, "hex" or base 16)
0b11, 0b0011 and -0b11 (binary, base 2)
```

---

## Floating-point literals

A floating-point literal can have the following parts:

- A decimal integer which can be signed (preceded by "+" or "-"),
- A decimal point ("."),
- A fraction (another decimal number),
- An exponent.

The exponent part is an "e" or "E" followed by an integer, which can be signed (preceded by "+" or "-"). A floating-point literal must have at least one digit and either a decimal point or "e" (or "E").

For example:

```js
3.1415926
-.123456789
-3.1E+12
.1e-23
```

---

## Object literals
     
An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces ({}). 

You should not use an object literal at the beginning of a statement. This will lead to an error or not behave as you expect, because the { will be interpreted as the beginning of a block.

The following is an example of an object literal. 

```js
var car = {type:"Fiat", model:"500", color:"white"};
```

---

## Object literals

The first element of the car object defines a property, **myCar**, and assigns to it a new string, "Saturn"; the second element, the getCar property, is immediately assigned the result of invoking the function (carTypes("Honda")); the third element, the special property, uses an existing variable (sales).

```js
var sales = "Toyota";

function carTypes(name) {
  if (name === "Honda") {
    return name;
  } else {
    return "Sorry, we don't sell " + name + ".";
  }
}

var car = { myCar: "Saturn", getCar: carTypes("Honda"), special: sales };

console.log(car.myCar);   // Saturn
console.log(car.getCar);  // Honda
console.log(car.special); // Toyota
```

---

## Object literals

Additionally, you can use a numeric or string literal for the name of a property or nest an object inside another. The following example uses these options.
      
```js
var car = { manyCars: {a: "Saab", "b": "Jeep"}, 7: "Mazda" };

console.log(car.manyCars.b); // Jeep
console.log(car[7]); // Mazda
```

---

## Object literals

Object property names can be any string, including the empty string. If the property name would not be a valid JavaScript identifier or number, it must be enclosed in quotes. Property names that are not valid identifiers also cannot be accessed as a dot (.) property, but can be accessed and set with the array-like notation("[]").

```js
var unusualPropertyNames = {
  "": "An empty string",
  "!": "Bang!"
}
console.log(unusualPropertyNames."");   // SyntaxError: Unexpected string
console.log(unusualPropertyNames[""]);  // An empty string
console.log(unusualPropertyNames.!);    // SyntaxError: Unexpected token !
console.log(unusualPropertyNames["!"]); // Bang!
```

---

## RegExp literals

A regex literal is a pattern enclosed between slashes. 

The following is an example of an regex literal.

```js
var re = /ab+c/;
```

---

## String literals

A string literal is zero or more characters enclosed in double (") or single (') quotation marks. A string must be delimited by quotation marks of the same type; that is, either both single quotation marks or both double quotation marks. The following are examples of string literals:

```js
"foo"
'bar'
"1234"
"one line \n another line"
"John's cat"
```

You can call any of the methods of the String object on a string literal value—JavaScript automatically converts the string literal to a temporary String object, calls the method, then discards the temporary String object. You can also use the String.length property with a string literal:
      
```js
console.log("John's cat".length) 
// Will print the number of symbols in the string including whitespace. 
// In this case, 10.
```

---

## Expressions

An expression is a combination of values, variables, and operators, which computes to a value.

The computation is called an evaluation.

For example, 5 * 10 evaluates to 50:

```js
5 * 10
```

Expressions can also contain variable values:

```js
x * 10
```

The values can be of various types, such as numbers and strings.

For example, "John" + " " + "Doe", evaluates to "John Doe":

```js
"John" + " " + "Doe"
```

---

## Keywords

JavaScript keywords are used to identify actions to be performed.

The var keyword tells the browser to create a new variable:

```js
var x = 5 + 6;
var y = x * 10;
```

JavaScript statements often start with a keyword to identify the JavaScript action to be performed.

**function**	- Declares a function

**if ... else**	
Marks a block of statements to be executed, depending on a condition

**var** - Declares a variable

**return	**
Exits a function

**switch**	
Marks a block of statements to be executed, depending on different cases

---

## Keywords

**try ... catch**	
Implements error handling to a block of statements

**break**
Terminates a switch or a loop

**continue**
Jumps out of a loop and starts at the top

**debugger**	
Stops the execution of JavaScript, and calls (if available) the debugging function

**do ... while**	
Executes a block of statements, and repeats the block, while a condition is true

**for**
Marks a block of statements to be executed, as long as a condition is true

**JavaScript keywords are reserved words. Reserved words cannot be used as names for variables.**

---

## Sources

* [W3S JavaScript](http://www.w3schools.com/js/)
* [Mozilla Developer Network JS](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [Plain JavaScript](https://plainjs.com)
* [You Might Not Need jQuery](http://youmightnotneedjquery.com)

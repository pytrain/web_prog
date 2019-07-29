<center>
  <h1>Introduction to Javascript</h1>
</center>

## Useful Pointers

- [JavaScript Tutorial](https://www.tutorialspoint.com/javascript/)
- [Learn JavaScript - Free Interactive JavaScript Tutorial](https://www.learn-js.org)
- [The Modern JavaScript Tutorial](https://javascript.info)

**We will cover the following:**
- [What is JavaScripts?](#what-is-javascripts)
- [First Program](#my-first-program)
- [Code Structure](#code-structure)
- [Variables](#variables)
- [Data Types](#data-types)
- [Interaction](#interaction)
- [Conditional Statements](#conditional-statements)
- [Loops](#loops)
- [Functions](#function-expressions-and-arrows)
- [Arrays](#arrays)
- [Array Manipulations](#array-manipulations)
- [Objects](#objects)

## What is JavaScripts?
---

- Initially created to “make web pages alive”.
- JavaScript programs (scripts) can be written right in a web page’s HTML and run automatically as the page loads.
- Scripts are provided and executed as plain text. They don’t need special preparation or compilation to run.
- JavaScript can execute not only in the browser, but also on the server, or actually on any device that has a special program called the JavaScript engine.
- JavaScript has a unique position as the most widely-adopted browser language with full integration with HTML/CSS.

## My First Program
---

- JavaScript programs can be inserted into any part of an HTML document with the help of the **`<script>`** tag.
- The **`<script>`** tag contains JavaScript code which is automatically executed when the browser processes the tag.

```html
<!DOCTYPE HTML>
<html>

<body>

  <p>Before the script...</p>

  <script type="text/javascript">
    alert( 'Welcome to the JavaScript Tutorial!' );
  </script>

  <p>...After the script.</p>

</body>

</html>
```

- If we have a lot of JavaScript code, we can put it into a separate file.
- Script files are attached to HTML with the **src** attribute:

```html
<script src="/path/to/script.js"></script>

<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/3.2.0/lodash.js"></script>
```

## Code  Structure
---

### Statements
- Statements are syntax constructs and commands that perform actions.
- We can have as many statements in our code as we want.
- Statements can be separated with a semicolon.

```javascript
alert('Hello Class.'); alert('Welcome!');
```

### Semicolons
- A semicolon may be omitted in most cases when a line break exists.
- In most cases, a newline implies a semicolon. But “in most cases” does not mean “always”!
- There are cases when a newline does not mean a semicolon.

```javascript
alert('Hello Class.')
alert('Welcome!')

alert(3 +
1
+ 2);
```

### Comments
```javascript
// This comment occupies a line of its own
alert('Hello Class.');

alert('Welcome!'); // This comment follows the statement

/* An example with two messages.
This is a multiline comment.
*/
alert('Hello Class.');
alert('Welcome!');
```

### "use strict"
- When it is located at the top of a script, the whole script works the “modern” way.
- Strict mode is supported by all modern browsers.
- Always starting scripts with **"use strict"**.

```javascript
"use strict";

// this code works the modern way
...
```

## Variables
---

- To create a variable in JavaScript, use the **let** keyword.
- The name of a variable must contain only letters, digits, or the symbols `$` and `_`.
- The first character must not be a digit.
- A variable name is case sensitive

```javascript
let message;
message = 'Hello!';

alert(message); // shows the variable content
```

```javascript
let user = 'John', age = 25, message = 'Hello';

let user = 'John';
let age = 25;
let message = 'Hello';

let user = 'John',
  age = 25,
  message = 'Hello';
  
let user = 'John'
  , age = 25
  , message = 'Hello';
```

- To declare constants, use the **const** keyword instead of **let**.
- We generally use upper case for constants that are “hard-coded”, i.e., when the value is known prior to execution and directly written into the code.

```javascript
const firstAppoloLaunch = '16.07.1969';

const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";
const COLOR_BLUE = "#00F";
const COLOR_ORANGE = "#FF7F00";

// ...when we need to pick a color
let color = COLOR_ORANGE;
alert(color); // #FF7F00
```

### Exercise

1. Declare two variables: old_topic and new_topic.
2. Assign the value "JavaScript" to new_topic.
3. Copy the value from new_topic to old_topic.
4. Show the value of old_topic using alert.

## Data Types
---

- A variable in JavaScript can contain any data. 
- A variable can at one moment be a string and at another be a number:

### Numbers
- Represent both integer and floating point numbers.

```javascript
let n = 123;
n = 12.345;

alert( 1 / 0 ); // Infinity
alert( Infinity ); // Infinity

alert( "not a number" / 2 ); // NaN, such division is erroneous
alert( "not a number" / 2 + 5 ); // NaN
```

```javascript
// No effect on numbers
let x = 1;
alert( +x ); // 1

let y = -2;
alert( +y ); // -2

// Converts non-numbers
alert( +true ); // 1
alert( +"" );   // 0
```

```javascript
alert( 5 % 2 ); // 1 is a remainder of 5 divided by 2
alert( 8 % 3 ); // 2 is a remainder of 8 divided by 3
alert( 6 % 3 ); // 0 is a remainder of 6 divided by 3
```

```javascript
alert( 2 ** 2 ); // 4  (2 * 2)
alert( 2 ** 3 ); // 8  (2 * 2 * 2)
alert( 2 ** 4 ); // 16 (2 * 2 * 2 * 2)
```

```javascript
let counter = 2;
counter++;      // works the same as counter = counter + 1, but is shorter
alert( counter ); // 3

counter--;      // works the same as counter = counter - 1, but is shorter
alert( counter ); // 2
```

```javascript
let n = 2;
n += 5; // now n = 7 (same as n = n + 5)
n *= 2; // now n = 14 (same as n = n * 2)
alert( n ); // 14
```

```javascript
let a = (1 + 2, 3 + 4);
alert( a ); // 7 (the result of 3 + 4)
```

### Strings
- A string in JavaScript must be surrounded by quotes.

```javascript
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed ${str}`;
```

```javascript
let name = "Jules";

// embed a variable
alert( `Hello, ${name}!` ); // Hello, Jules!

// embed an expression
alert( `the result is ${1 + 2}` ); // the result is 3
```

```javascript
let s = "my" + "string";
alert(s); // mystring

alert( '1' + 2 ); // "12"
alert( 2 + '1' ); // "21"

alert(2 + 2 + '1' ); // "41" and not "221"
```

```javascript
alert( 'Z' > 'A' ); // true
alert( 'Glow' > 'Glee' ); // true
alert( 'Bee' > 'Be' ); // true
```

### Booleans
- The boolean type has only two values: **true** and **false**.

```javascript
let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked
```

```javascript
let isGreater = 4 > 1;
alert( isGreater ); // true (the comparison result is "yes")
```

```javascript
alert( 2 > 1 );  // true (correct)
alert( 2 == 1 ); // false (wrong)
alert( 2 != 1 ); // true (correct)
```

### The "null" Value
- Forms a separate type of its own which contains only the **null** value.
- It is a special value which represents “nothing”, “empty” or “value unknown”.

```javascript
let age = null;
```

### The “undefined” Value
- The meaning of **undefined** is “value is not assigned”.
- If a variable is declared, but not assigned, then its value is **undefined**.
- It is possible to assign undefined to any variable:

```javascript
let x;

alert(x); // shows "undefined"
```

```javascript
let x = 123;

x = undefined;

alert(x); // "undefined"
```

### The typeof operator
- Returns the type of the argument.
- Can use either **typeof x** or **typeof(x)**

```javascript
typeof undefined // "undefined"
typeof 0 // "number"
typeof true // "boolean"
typeof "foo" // "string"
typeof null // "object" 
typeof alert // "function"
```

### Exercise
What is the output of?

```javascript
let name = "Ilya";
alert( `hello ${1}` ); // ?
alert( `hello ${"name"}` ); // ?
alert( `hello ${name}` ); // ?
```

### Type Conversion

- **ToString**: Perform with **String(value)**. 
- **ToNumber**: Perform with **Number(value)**.
- **ToBoolean**: Perform with **Boolean(value)**.

```javascript
let value = true;
alert(typeof value); // boolean

value = String(value); // now value is a string "true"
alert(typeof value); // string
```

```javascript
alert( "6" / "2" ); // 3, strings are converted to numbers

alert( Number("   123   ") ); // 123
alert( Number("123z") );      // NaN (error reading a number at "z")
alert( Number(true) );        // 1
alert( Number(false) );       // 0
```

```javascript
alert( Boolean(1) ); // true
alert( Boolean(0) ); // false

alert( Boolean("hello") ); // true
alert( Boolean("") ); // false
```

## Interaction
---

### alert
- Shows a message (in a mini-window) and pauses script execution until the user presses “OK”.
- The mini-window with the message is called a modal window.

### prompt
- Accept two arguments:
  1. **title**: The text to show the visitor.
  2. **default**: An optional second parameter, the initial value for the input field.
- It shows a modal window with a text message, an input field for the visitor, and the buttons OK/Cancel.
- The call to **prompt** returns the text from the input field or **null** if the input was canceled.

```javascript
let age = prompt('How old are you?', 100);
alert(`You are ${age} years old!`); // You are 100 years old!
```

### confirm
- Shows a modal window with a **question** and two buttons: OK and Cancel.
- The result is **true** if OK is pressed and **false** otherwise.

```javascript
let isBoss = confirm("Are you the boss?");
alert( isBoss ); // true if OK is pressed
```

## Conditional Statements
---

- A number **0**, an empty string **""**, **null**, **undefined**, and **NaN** all become **false**. Because of that they are called “falsy” values.
- Other values become **true**, so they are called “truthy”.

```javascript
if (0) { // 0 is falsy
  ...
}

if (1) { // 1 is truthy
  ...
}
```

```javascript
let year = prompt('In which year was the ECMAScript-2015 specification published?', '');

if (year < 2015) {
  alert( 'Too early...' );
} else if (year > 2015) {
  alert( 'Too late' );
} else {
  alert( 'Exactly!' );
}
```

### Conditional operator ‘?’

```javascript
let result = condition ? value1 : value2;
```

The **condition** is evaluated: 
- if it’s truthy then value1 is returned, 
- otherwise – value2.

```javascript
let accessAllowed = (age > 18) ? true : false;
```

```javascript
let age = prompt('age?', 18);
let message = (age < 3) ? 'Hi, baby!' :
  (age < 18) ? 'Hello!' :
  (age < 100) ? 'Greetings!' :
  'What an unusual age!';

alert( message );
```

### The "switch" Statement
- A **switch** statement can replace multiple **if** checks.
- It gives a more descriptive way to compare a value with multiple variants.

```javascript
switch(x) {
  case 'value1':  // if (x === 'value1')
    ...
    [break]

  case 'value2':  // if (x === 'value2')
    ...
    [break]

  default:
    ...
    [break]
}
```

```javascript
let a = 2 + 2;

switch (a) {
  case 3:
    alert( 'Too small' );
    break;
  case 4:
    alert( 'Exactly!' );
    break;
  case 5:
    alert( 'Too large' );
    break;
  default:
    alert( "I don't know such values" );
}
```

**If there is no break then the execution continues with the next case without any checks.**

```javascript
let a = 2 + 2;

switch (a) {
  case 3:
    alert( 'Too small' );
  case 4:
    alert( 'Exactly!' );
  case 5:
    alert( 'Too big' );
  default:
    alert( "I don't know such values" );
}
```

```javascript
// In the example above we’ll see sequential execution of three alerts
alert( 'Exactly!' );
alert( 'Too big' );
alert( "I don't know such values" );
```

## Loops
---

- Loops are a way to repeat the same code multiple times.

### The “while” Loop

```javascript
// Syntax
while (condition) {
  // code
  // so-called "loop body"
}
```

```javascript
// An example
let i = 0;
while (i < 3) { // shows 0, then 1, then 2
  alert( i );
  i++;
}
```

```javascript
// Another example
let i = 3;
while (i) { // when i becomes 0, the condition becomes falsy, and the loop stops
  alert( i );
  i--;
}
```

### The “do…while” Loop

```javascript
// Syntax
do {
  // loop body
} while (condition);
```

The loop will first execute the body, then check the condition, and, while it’s truthy, execute it again and again.

```javascript
// An example
let i = 0;
do {
  alert( i );
  i++;
} while (i < 3);
```

### The "for" Loop

```javascript
// Syntax
for (begin; condition; step) {
  // ... loop body ...
}
```

```javascript
// An example
for (let i = 0; i < 3; i++) { // shows 0, then 1, then 2
  alert(i);
}
```

```javascript
// Another example
var myArray = ["A", "B", "C"];
for (var i = 0; i < myArray.length; i++)
{
    console.log("The member of myArray in index " + i + " is " + myArray[i]);
}
```

### Breaking the Loop
- We can force the exit at any time using the special **break** directive

```javascript
let sum = 0;

while (true) {
  let value = +prompt("Enter a number", '');
  if (!value) break; // (*)
  sum += value;
}
alert( 'Sum: ' + sum );
```

### Continue to the Next Iteration
- The **continue** directive  doesn’t stop the whole loop.
- It stops the current iteration and forces the loop to start a new one (if the condition allows).
- We can use it if we’re done with the current iteration and would like to move on to the next one

```javascript
// An example
for (let i = 0; i < 10; i++) {
  // if true, skip the remaining part of the body
  if (i % 2 == 0) continue;

  alert(i); // 1, then 3, 5, 7, 9
}
```

### Labels for break/continue

```javascript
// An example
outer: for (let i = 0; i < 3; i++) {

  for (let j = 0; j < 3; j++) {

    let input = prompt(`Value at coords (${i},${j})`, '');

    // if an empty string or canceled, then break out of both loops
    if (!input) break outer; // (*)

    // do something with the value...
  }
}
alert('Done!');
```

### Exercise
What is the last value alerted by this code? Why

```javascript
let i = 3;

while (i) {
  alert( i-- );
}
```

## Function Expressions and Arrows
---

- A function is a special kind of value.

```javascript
// Simple function

function sayHi() {
  alert( "Hello" );
} 
```

```javascript
// Function expression
// The function is created and assigned to the variable.
// No matter how the function is defined, it’s just a value 
// stored in the variable sayHi.

let sayHi = function() {
  alert( "Hello" );
};
```

- **Function Declaration**: a function, declared as a separate statement, in the main code flow.
- **Function Expression**: a function, created inside an expression or inside another syntax construct. Here, the function is created at the right side of the “assignment expression” =.
- **A Function Expression is created when the execution reaches it and is usable only from that moment.**
- **A Function Declaration can be called earlier than it is defined.**

```javascript
function sayHi() {
  alert( "Hello" );
}

alert( sayHi ); // shows the function code
```

We can copy a function to another variable:

```javascript
function sayHi() {   // (1) create
  alert( "Hello" );
}

let func = sayHi;    // (2) copy

func(); // Hello     // (3) run the copy (it works)!
sayHi(); // Hello    //     this still works too (why wouldn't it)
```

### Callback functions

Consider a function **ask(question, yes, no)** with three parameters:
- **question**: Text of the question
- **yes**: Function to run if the answer is “Yes”
- **no**: Function to run if the answer is “No”

```javascript
function ask(question, yes, no) {
  if (confirm(question)) yes()
  else no();
}

function showOk() {
  alert( "You agreed." );
}

function showCancel() {
  alert( "You canceled the execution." );
}

// usage: functions showOk, showCancel are passed 
// as arguments to ask
ask("Do you agree?", showOk, showCancel);
```

### Arrow Functions
---

```javascript
// Syntax
let func = (arg1, arg2, ...argN) => expression

// Is the same as:
let func = function(arg1, arg2, ...argN) {
  return expression;
};
```

```javascript
// An example
let sum = (a, b) => a + b;

/* The arrow function is a shorter form of:

let sum = function(a, b) {
  return a + b;
};
*/

alert( sum(1, 2) ); // 3
```

## Arrays
---

- JavaScript can hold an array of variables in an Array object.
- In JavaScript, an array also functions as a list, a stack or a queue.
- To define an array, either use the brackets notation or the **Array** object notation.

```javascript
var myArray = [1, 2, 3];
var theSameArray = new Array(1, 2, 3);
```

- We can use the brackets **`[ ]`** operator to address a specific cell in our array. 
- Addressing uses zero-based indices.

```javascript
console.log(myArray[1]);      // prints out 2
```

- Arrays in JavaScript are sparse, meaning that we can also assign variables to random locations even though previous cells were undefined.

```javascript
var myArray = []
myArray[3] = "hello"
console.log(myArray); 
// Will print out: [undefined, undefined, undefined, "hello"]
```

- Because JavaScript Arrays are just special kinds of objects, you can have elements of different types stored together in the same array.

```javascript
var myArray = ["string", 10, {}]
```

## Array Manipulations
---

### push and pop

```javascript
var myStack = [];
myStack.push(1);
myStack.push(2);
myStack.push(3);
console.log(myStack); // 1,2,3
```

```javascript
console.log(myStack.pop()); // 3
console.log(myStack); // 1, 2
```

### Queues using shift and unshift
- The **shift** and **unshift** methods are similar to **push** and **pop**, only they work from the beginning of the array. 
- We can use the **push** and **shift** methods consecutively to utilize an array as a queue.
- The **shift** keyword will remove the variables of the array in the exact order they were inserted in.
- The **unshift** method is used to insert a variable at the beginning of an array.

```javascript
var myQueue = [];
myQueue.push(1);
myQueue.push(2);
myQueue.push(3);

console.log(myQueue.shift()); // 1
console.log(myQueue.shift()); // 2
console.log(myQueue.shift()); // 3
```

```javascript
var myArray = [1,2,3];
myArray.unshift(0);
console.log(myArray);       // will print out 0,1,2,3
```

### splice
- Splicing an array removes a certain part from the array to create a new array, made up from the part we took out.
- After splicing the array, it will only contain the part before and after the splicing.

```javascript
var myArray = [0,1,2,3,4,5,6,7,8,9];
var splice = myArray.splice(3,7);

console.log(splice);        // will print out 3,4,5,6,7
console.log(myArray);       // will print out 0,1,2,8,9
```

## Objects
---

- JavaScript is a functional language, and for object oriented programming it uses both objects and functions.
- Objects are usually used as a data structure, similar to a dictionary in Python or a map in Java.

```javascript
// Initializing an object
var emptyObject = {};
var personObject = {
    firstName : "John",
    lastName : "Smith"
}
```

- Members of objects can be addressed using the brackets operator **`[ ]`**., 
- The period **`.`** operator can also be used.

```javascript
var personObject = {
    firstName : "John",
    lastName : "Smith"
}
personObject.age = 23;
personObject["salary"] = 14000;
```

- To iterate over members of an object, we use the **hasOwnProperty** method to check that the member in fact belongs to the object.

```javascript
for (var member in personObject)
{
    if (personObject.hasOwnProperty(member))
    {
        console.log("the member " + member + " of personObject is " + personObject[member])
    }
}
```

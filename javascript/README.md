# JavaScript Cheatsheet

## Table of Contents

- [JavaScript Cheatsheet](#javascript-cheatsheet)
  - [Table of Contents](#table-of-contents)
    - [Lesson 1 (What is JavaScript?)](#lesson-1-what-is-javascript)
    - [Lesson 2 (Data Types & Variables)](#lesson-2-data-types--variables)
    - [Conditionals](#conditionals)
    - [Loops](#loops)
      - [While Loops](#while-loops)
      - [Parts Of The `While Loops`](#parts-of-the-while-loops)
      - [Part of the For Loop](#part-of-the-for-loop)
      - [Increment and Decrement](#increment-and-decrement)
      - [Scope](#scope)

### Lesson 1 (What is JavaScript?)

`alert(str)`, `console.log(str)`, `document`, `getElementsByTag(str)`

```js
1. alert("Hello! I am an alert box!!"); // display an alert box
2. console.log("Hello, I am Nahid"); // display content on js console
3. document.getElementsByTag('h1')[0].style.color="#ff00fff"; // change first h1 tag color to red
```

### Lesson 2 (Data Types & Variables)

`numbers`, `arithmetic operator`, `comparison operators`, `booleans`, `comments`, `string`, `variable`, `==`, `===`, `!=`, `!==`, `booleans`, `null`, `NaN`, `undefined`, `if`, `else`, `Math.sqrt()`

[JS Style Guide](http://udacity.github.io/frontend-nanodegree-styleguide/javascript.html)

```js
// Numbers (3, 4.0, 4.5, -5.0, -10) etc
// Arithmetics Operator (+, -, *, /, %)
// Comparison Operators (>, <, ==, <=, >=, !=)
// Booleans (true, false)
// Single line comments
/*
multiline
comments
*/
1. "Hello," + " New York City"; // '+' string concatenation
2. "Hello" + 5*10; //Hello50

// Storing the value of a string in a variable is like packing it away for later use.
// var variable_name = value;
3. var greeting = "Hello";
console.log(greeting); // Hello
4. var quote = "Stay awhile and listen!";
console.log(quote[6]); // return `w`, call indexing
5. greeting.charAt(6); // return `w`, using charAt(index)
6. \"(double quote), \' (single quote), \\ (backslash), \n (newline), \t (tab) // escaping characters
7. 'yes' == 'Yes' // string comparison, return false, case-sensitive
8. 'y' != 'Y' // true
9. var my_string = 'a'
console.log(my_string.charCodeAt(0)) // return ASCII VALUE
```

**Booleans**:

```js
// ex-1
var studentName = "John";
var haveEnrolledInCourse = true;
var haveCompletedTheCourse = false;

if (haveEnrolledInCourse){
    console.log("Welcome "+studentName+" to Udacity!"); // Will run only if haveEnrolledInCourse is true
}

// ex-2
var a = 10;
var b = 20;
// a comparison - we will study this in detail in upcoming lesson
if (a>b) // The outcome of a>b will be a boolean
    console.log("Variable `a` has higher value"); // if a>b is true
else
    console.log("Variable `b` has higher value"); // if a>b is false

// ex-3
if(1){
    console.log("This statement will always execute because conditional is set to 1 i.e., true");
}

if(0){
        console.log("This statement will NEVER execute because conditional is set to 0 i.e., false");
}
```

**Null, undefined, and NaN**:

`null`: data type (value of notching)
`undefined`: absence of value
`NaN`: stands for "Not-A-Number"

```js
var x = null; // null
var y;
console.log(y); // undefined
Math.sqrt(-19); // return Nan
```

**Equality**:

`===`: check same type and same value
`==`: check same value??

> console.log(message + variable + message + variable + \escape_sequence);

### Conditionals

`If...else` statements allow you to execute certain pieces of code based on a `condition`, or set of conditions, being met.

```js
// if...else
if (/* this expression is true */) {
  // run this code
} else {
  // run this code
}

// if...else if... else
var weather = "sunny";

if (weather === "snow") {
  console.log("Bring a coat.");
} else if (weather === "rain") {
  console.log("Bring a rain jacket.");
} else {
  console.log("Wear what you have on.");
}
```

**Complex Logical Operators**:

`&&`(and), `||`(or), and `!`(not)

**Ternary Operator**:

```js
// conditional ? (if condition is true) : (if condition is false)

// ex#1
var isGoing = true;

var color = isGoing ? "green" : "red";
console.log(color);

// ex#2
var eatsPlants = false;
var eatsAnimals = true;

var category = eatsPlants ? (eatsAnimals ? "omnivore" : "herbivore") : (eatsAnimals ? "carnivore" : "undefined");
```

**Switch Statement**:

```js
switch (option) {
  case 1:
    console.log("You selected option 1.");
  case 2:
    console.log("You selected option 2.");
  case 3:
    console.log("You selected option 3.");
  case 4:
    console.log("You selected option 4.");
  case 5:
    console.log("You selected option 5.");
  case 6:
    console.log("You selected option 6.");
}

// ex#2
var month = 2;

switch(month) {
  case 1:
  case 3:
  case 5:
  case 7:
  case 8:
  case 10:
  case 12:
    days = 31;
    break;
  case 4:
  case 6:
  case 9:
  case 11:
    days = 30;
    break;
  case 2:
    days = 28;
}

console.log("There are " + days + " days in this month.");
```

### Loops

Loops will lets you `iterate` over the values and repeatedly run a block of code.

#### While Loops

```js
var x = 1;

while (x <= 10000) {
  console.log(x + "Bangladesh");
  x = x + 1;
}
```

#### Parts Of The `While Loops`

There are many different kinds of loops, but they all essentially do the same thing: they repeat an action some number of times.

Three main pieces of information that any loop should have are:

- `When to start`: The code that sets up the loop — defining the starting value of a variable for instance.
- `When to stop`: The logical condition to test whether the loop should continue.
- `How to get to the next item`: The incrementing or decrementing step — for example, x = x * 3 or x = x - 1
Here's a basic while loop example that includes all three parts.

```js
var start = 0; // when to start
while (start < 10) { // when to stop
  console.log(start);
  start = start + 2; // how to get to the next item
}
```

#### Part of the For Loop

The `for loop` explicitly forces you to define the **start** point, **stop** point, and each **step** of the loop. In fact, you'll get an Uncaught SyntaxError: Unexpected token ) if you leave out any of the three required pieces.

```js
for ( start; stop; step ) {
  // do this thing
}
```

Here's an example of a for loop that prints out the values from 0 to 5. Notice the semicolons separating the different statements of the for loop: `var i = 0; i < 6; i = i + 1`

```js
for (var i = 0; i < 6; i = i + 1) {
  console.log("Printing out i = " + i);
}
```

**Nested For Loop**:

```js
for (var x = 0; x < 5; x = x + 1) {
  for (var y = 0; y < 3; y = y + 1) {
    console.log(x + "," + y);
  }
}

/*
x = 0 and y = 0, 1, 2 // (0, 0) (0, 1) and (0, 2)
x = 1 and y = 0, 1, 2 // (1, 0) (1, 1) and (1, 2)
x = 2 and y = 0, 1, 2 // (2, 0) (2, 1) and (2, 2)
etc.
*/
```

#### Increment and Decrement

```js
x++ or ++x // same as x = x + 1
x-- or --x // same as x = x - 1
x += 3 // same as x = x + 3
x -= 6 // same as x = x - 6
x *= 2 // same as x = x * 2
x /= 5 // same as x = x / 5

// Note
x++; // first return value then increment it.
++x; // first increment it then return value.
```

#### Scope

**More to Read - Scope and Variable Declaration**:

At this point, you need to understand that there are ways to declare a variable, by using `let`, `const` or `var`. To understand the difference between the three, first you need to understand the term scope.

**What is a "Scope"?**:

The scope is defined as a specific portion of the code. There are three types of scope in Javascript

- `Global scope` - When a particular variable is visible (can be used) anywhere in the code. Such a variable is generally called as **Global** variable.
- `Function scope` - When a particular variable is visible (can be used) within a particular function only. Such a variable is generally called as **Local** variable.
- `Block scope` - When a particular variable is visible (can be used) within a pair of `{ . . . }` only.
Let us see an example of each type of scope:

```js
/*
 * Global scope.
 * This variable declared outside of any function is called Global variable.
 * Hence, you can use this anywhere in the code
 */
var opinion = "This nanodegree is amazing";

// Function scope
function showMessage() {
    // Local variable, visible within the function `showMessage`
    var message = "I am an Udacian!";

    // Block scope
    {
          let greet = "How are you doing?";
        /*
         * We have used the keyword `let` to declare a variable `greet` because variables declared with the `var` keyword can not have Block Scope.
         */
    } // block scope ends

    console.log( message ); // OK
    console.log( greet ); // ERROR.
    // Variable greet can NOT be used outside the block

    console.log( opinion ); // OK    to use the global variable anywhere in the code

} // function scope ends
```

**Variable Declaration**:

There are three ways to declare a variable:

1. `let` - It a new way to declare a variable in any scope - Global, Local, or Block. The value of this variable can be changed or reassigned anytime within its scope.
2. `const` - It is also a way to declare constants in any scope - Global, Local, or Block. Once you are assigned a value to a `const` variable, the value of this variable CANNOT be changed or reassigned throughout the code.
3. `var` - This is the old way of declaring variables in only two scope - Global, or Local. Variables declared with the `var` keyword can not have Block Scope. The value of this variable can be changed or reassigned anytime within its scope.

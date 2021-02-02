# JavaScript Cheatsheet

## Table of Contents

- [JavaScript Cheatsheet](#javascript-cheatsheet)
  - [Table of Contents](#table-of-contents)
    - [Lesson 1 (What is JavaScript?)](#lesson-1-what-is-javascript)
    - [Lesson 2 (Data Types & Variables)](#lesson-2-data-types--variables)
    - [Conditionals](#conditionals)
    - [Loops](#loops)
      - [While Loops](#while-loops)
      - [Parts Of The While Loops](#parts-of-the-while-loops)
      - [Part of the For Loop](#part-of-the-for-loop)
      - [Increment and Decrement](#increment-and-decrement)
      - [Scope](#scope)
    - [Function](#function)
      - [Function Recap](#function-recap)
      - [Scope Shadowing](#scope-shadowing)
      - [Remind about Scope](#remind-about-scope)
      - [Hoisting](#hoisting)
      - [Function Expressions](#function-expressions)
      - [Patterns with Function Expressions](#patterns-with-function-expressions)
      - [Function Expression Recap](#function-expression-recap)
    - [Arrays](#arrays)
    - [Array Indexing](#array-indexing)
      - [Array Methods and Properties](#array-methods-and-properties)
      - [forEach](#foreach)
      - [Map()](#map)
      - [2D Array](#2d-array)
    - [Objects](#objects)
      - [Objects in Code](#objects-in-code)
    - [Object-literal notation](#object-literal-notation)
      - [Summary of Objects(Naming Convention)](#summary-of-objectsnaming-convention)
      - [Donuts](#donuts)

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

#### Parts Of The While Loops

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
         * We have used the keyword `let` to declare a variable `greet` because
         variables declared with the `var` keyword can not have Block Scope.
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

### Function

**How to declare a function**:

Functions allow you to package up lines of code that you can use (and often reuse) in your programs.

```js
function findAverage(x, y) {
  var answer = (x + y) / 2;
  return answer;
}

var avg = findAverage(5, 9);
```

> **Parameters vs. Arguments**
At first, it can be a bit tricky to know when something is either a parameter or an argument. The key difference is in where they show up in the code. A parameter is always going to be a variable name and appears in the function declaration. On the other hand, an argument is always going to be a value (i.e. any of the JavaScript data types - a number, a string, a boolean, etc.) and will always appear in the code when the function is called or invoked.

In the above `findAverage(x, y)` `x`,`y` is called parameter.
and, `findAverage(5, 9)`, `5`, `9` is called arguments.

#### Function Recap

**What you've learned so far:**

**Functions** package up code so you can easily use (and reuse) a block of code. **Parameters** are variables that are used to store the data that's passed into a function for the function to use. **Arguments** are the actual data that's passed into a function when it is invoked:

```js
// x and y are parameters in this function declaration
function add(x, y) {
  // function body
  // Here, `sum` variable has a scope within the function.
  // Such variables defined within a function are called Local variables
  // You can try giving it another name
  var sum = x + y;
  return sum; // return statement
}

// 1 and 2 are passed into the function as arguments,
// and the result returned by the function is stored in a new variable `sum`
// Here, `sum` is another variable, different from the one used inside the function
var sum = add(1, 2);
```

The function body is enclosed inside curly brackets:

```js
function add(x, y) {
  // function body!
}
```

**Return statements** explicitly make your function return a value:

```js
return sum;
```

You **invoke** or **call** a function to have it do something:

```js
add(1, 2);
```

**Returns**: 3

#### Scope Shadowing

```js
var x = 1;

function addTwo() {
  x = x + 2; // x value is change
}

addTwo();
x = x + 1;
console.log(x);
// 4
```

```js
var x = 1;

function addTwo() {
  var x = x + 2; // declare new x
}

addTwo();
x = x + 1;
console.log(x);
// 2
```

#### Remind about Scope

- If an identifier is declared in global scope, it's available everywhere.
- If an identifier is declared in function scope, it's available in the function it was declared in (even in functions declared inside the function).
- When trying to access an identifier, the JavaScript Engine will first look in the current function. If it doesn't find anything, it will continue to the next outer function to see if it can find the identifier there. It will keep doing this until it reaches the global scope.
- Global identifiers are a bad idea. They can lead to bad variable names, conflicting variable names, and messy code.

#### Hoisting

Sometimes your JavaScript code will produce errors that may seem counterintuitive at first. Hoisting is another one of those topics that might be the cause of some of these tricky errors you're debugging.

Let's take a look at an example:

[![Image Alt Text Here](https://img.youtube.com/vi/8z-HSS34dsM/0.jpg)](https://www.youtube.com/watch?v=8z-HSS34dsM)

The function declaration is hoisted to the top of its current scope, and inside the function, the greeting variable declaration is also hoisted to the top of its function scope.

```js
sayHi("Julia");

function sayHi(name) {
  console.log(greeting + " " + name);
  var greeting;
}
```

- JavaScript hoists function declarations and variable declarations to the top of the current scope.
- Variable assignments are not hoisted.
- Declare functions and variables at the top of your scripts, so the syntax and behavior are consistent with each other.

#### Function Expressions

Once you know how to declare a function, a whole new set of possibilities will open up to you.

For instance, remember how you can store anything you want in a variable? Well, in JavaScript, you can also store functions in variables. When a function is stored inside a variable it's called a `function expression`.

```js
var catSays = function(max) {
  var catMessage = "";
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
};
```

Notice how the function keyword no longer has a name.

```js
var catSays = function(max) {
  // code here
};
```

It's an **anonymous** function, a function with no name, and you've stored it in a variable called **catSays**.

And, if you try accessing the value of the variable catSays, you'll even see the function returned back to you.

```js
catSays;
```

Returns:

```js
function(max) {
  var catMessage = ""
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
}
```

**Function expressions and hoisting**:

Deciding when to use a function expression and when to use a function declaration can depend on a few things, and you will see some ways to use them in the next section. But, one thing you'll want to be careful of is hoisting.

All function declarations are hoisted and loaded before the script is actually run. ***Function expressions are not hoisted***, since they involve variable assignment, and only variable declarations are hoisted. The function expression will not be loaded until the interpreter reaches it in the script.

#### Patterns with Function Expressions

**Functions as parameters**:

Being able to store a function in a variable makes it really simple to pass the function into another function. `A function that is passed into another function is called a callback`. Let's say you had a helloCat() function, and you wanted it to return "Hello" followed by a string of "meows" like you had with catSays. Well, rather than redoing all of your hard work, you can make helloCat() accept a callback function, and pass in catSays.

```js
// function expression catSays
var catSays = function(max) {
  var catMessage = "";
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
};

// function declaration helloCat accepting a callback
function helloCat(callbackFunc) {
  return "Hello " + callbackFunc(3);
}

// pass in catSays as a callback function
helloCat(catSays);
```

**Inline function expressions**:

```js
// Function declaration that takes in two arguments: a function for displaying
// a message, along with a name of a movie
function movies(messageFunction, name) {
  messageFunction(name);
}

// Call the movies function, pass in the function and name of movie
movies(function displayFavorite(movieName) {
  console.log("My favorite movie is " + movieName);
}, "Finding Nemo");
```

#### Function Expression Recap

**What you've learned so far:**

**Function Expression**: When a function is assigned to a variable. The function can be named, or anonymous. Use the variable name to call a function defined in a function expression.

```js
// anonymous function expression
var doSomething = function(y) {
  return y + 1;
};
```

```js
// named function expression
var doSomething = function addOne(y) {
  return y + 1;
};
```

```js
// for either of the definitions above, call the function like this:
doSomething(5);
```

> **Returns**: 6

You can even pass a function into another function inline. This pattern is commonly used in JavaScript, and can be helpful streamlining your code.

```js
// function declaration that takes in two arguments: a function for displaying
// a message, along with a name of a movie
function movies(messageFunction, name) {
  messageFunction(name);
}

// call the movies function, pass in the function and name of movie
movies(function displayFavorite(movieName) {
  console.log("My favorite movie is " + movieName);
}, "Finding Nemo");
```

### Arrays

An array is a data structure that you can use to store multiple values and arrays are also organized.

An array is useful because it stores multiple values into a single, organized data structure. You can define a new array by listing values separated with commas between square brackets [].

```js
// creates a `donuts` array with three strings
var donuts = ["glazed", "powdered", "jelly"];
```

But **strings** aren’t the only type of data you can store in an array. You can also store numbers, booleans… and really anything!

```js
// creates a `mixedData` array with mixed data types
var mixedData = ["abcd", 1, true, undefined, null, "all the things"];
```

You can even store an array in an array to create a nested array!

```js
// creates a `arraysInArrays` array with three arrays
var arraysInArrays = [[1, 2, 3], ["Julia", "James"], [true, false, true, false]];
```

Nested arrays can be particularly hard to read, so it's common to write them on one line, using a newline after each comma:

```js
var arraysInArrays = [
  [1, 2, 3],
  ["Julia", "James"],
  [true, false, true, false]
];
```

### Array Indexing

```js
var donuts = ["glazed", "chocolate frosted", "boston cream", "powdered", "sprinkled", "maple", "coconut", "jelly"];


donuts[2] = "cinnamon twist";
donuts[4] = "salted caramel";
donuts[5] = "shortcake eclair";
```

```js
console.log(donuts);
// ["glazed", "chocolate frosted", "cinnamon twist", "powdered", "salted caramel", "shortcake eclair", "coconut", "jelly"]
```

> One thing to be aware of is if you try to access an element at an index that does not exist, a value of undefined will be returned back.

#### Array Methods and Properties

[Array methods and properties - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

**Length**:

**Ex#1**:

```js
var donuts = ["glazed", "powdered", "sprinkled"];
console.log(donuts.length);
```

**Returns**: 3

**Ex#2**:

```js
var inventory = [
  ["gold pieces", 25],
  ["belt", 4],
  ["ring", 1],
  ["shoes", 2]
];
console.log(inventory.length);
```

**Returns**: 4

**Push()**: Add element in the end of the array.

```js
var nums = [1,2,3];
nums.push(4);
console.log(nums);
```

**Showed**: [1,2,3,4]

**Pop()**: Remove and return the last element of the array.

```js
var nums = [1,2,3];
console.log(nums);
nums.pop();
console.log(nums);
```

**Showed**: [1,2]

**Splice**:

`splice()` is another handy method that allows you to add and remove elements from anywhere within an array.

While push() and pop() limit you to adding and removing elements from the end of an array, `splice()` lets you specify the index location to add new elements, as well as the number of elements you'd like to delete (if any).

```js
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller"];
donuts.splice(1, 1, "chocolate cruller", "creme de leche"); // removes "chocolate frosted" at index 1 and adds "chocolate cruller" and "creme de leche" starting at index 1
```

Following is the syntax of `splice()` method:

```js
arrayName.splice(arg1, arg2, item1, ....., itemX); where,
```

- `arg1` = Mandatory argument. Specifies the starting index position to add/remove items. You can use a negative value to specify the position from the end of the array e.g., `-1` specifies the `last` element.

- `arg2` = Optional argument. Specifies the count of elements to be removed. If set to `0`, `no` items will be `removed`.

`item1, ....., itemX` are the items to be added at index position `arg1`

#### forEach

Arrays have a set of special methods to help you iterate over and perform operations on collections of data. You can view the MDN Documentation list of Array methods here, but a couple big ones to know are the `forEach()` and `map()` methods.

The `forEach()` method gives you an alternative way to iterate over an array, and manipulate each element in the array with an inline function expression.

```js
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

donuts.forEach(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  console.log(donut);
});
```

**Prints**:

```js
JELLY DONUT HOLE
CHOCOLATE DONUT HOLE
GLAZED DONUT HOLE
```

Notice that the `forEach()` method iterates over the array without the need of an explicitly defined index. In the example above, donut corresponds to the element in the array itself. This is different from a for or while loop where an index is used to access each element in the array:

```js
for (var i = 0; i < donuts.length; i++) {
  donuts[i] += " hole";
  donuts[i] = donuts[i].toUpperCase();
  console.log(donuts[i]);
}
```

**Parameters**:

The function that you pass to the `forEach()` method can take up to three parameters. In the video, these are called `element, index, and array`, but you can call them whatever you like.

The forEach() method will call this function once for each element in the array (hence the name forEach.) Each time, it will call the function with different arguments. The element parameter will get the value of the array element. The index parameter will get the index of the element (starting with zero). The array parameter will get a reference to the whole array, which is handy if you want to modify the elements.

Here's another example:

```js
words = ["cat", "in", "hat"];
words.forEach(function(word, num, all) {
  console.log("Word " + num + " in " + all.toString() + " is " + word);
});
```

**Prints**:

```js
Word 0 in cat,in,hat is cat
Word 1 in cat,in,hat is in
Word 2 in cat,in,hat is hat
```

On the next page, you'll do a quiz that uses the forEach() method to modify an array.

#### Map()

Using `forEach()` will not be useful if you want to permanently modify the original array. forEach() always returns undefined. However, creating a new array from an existing array is simple with the powerful map() method.

With the `map()` method, you can take an array, perform some operation on each element of the array, and return a new array.

```js
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

var improvedDonuts = donuts.map(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  return donut;
});
```

```js
donuts array: ["jelly donut", "chocolate donut", "glazed donut"]
improvedDonuts array: ["JELLY DONUT HOLE", "CHOCOLATE DONUT HOLE", "GLAZED DONUT HOLE"]
```

Oh man, did you just see that? The map() method accepts one argument, a function that will be used to manipulate each element in the array. In the above example, we used a function expression to pass that function into map(). This function is taking in one argument, donut which corresponds to each element in the donuts array. You no longer need to iterate over the indices anymore. map() does all that work for you.

#### 2D Array

```js
var donutBox = [
  ["glazed", "chocolate glazed", "cinnamon"],
  ["powdered", "sprinkled", "glazed cruller"],
  ["chocolate cruller", "Boston creme", "creme de leched"]
];

// here, donutBox.length refers to the number of rows of donuts
for (var row = 0; row < donutBox.length; row++) {
  console.log(donutBox[row]);
}
```

### Objects

Objects are a data structures in JavaScript that lets you data about a particular thing,
and helps you keep track of the data by using a **key**.

#### Objects in Code

```js
/*
 * Programming Quiz: Umbrella (7-1)
 */
/*
 * QUIZ REQUIREMENTS
 * - Your code should have a variable `umbrella`
 * - The variable `umbrella` should be an object
 * - Your `umbrella` object should have the `color` and `isOpen` property
 * - Your `umbrella` object should have an `open()` method that toggles the value of `isOpen` property
 * - Your `umbrella` object should have an `close()` method that toggles the value of `isOpen`
 */

var umbrella = {
    color: "pink",
    isOpen: true,
    open: function() {
        if (umbrella.isOpen === true) {
            return "The umbrella is already opened!";
        } else {
            umbrella.isOpen = true;
            return "Julia opens the umbrella!";
        }
    },
    // your code goes here
    close: function() {
        if (umbrella.isOpen === true) {
            umbrella.isOpen = false;
            return "Close the umbrella!";
        } else {
            return "Umbrella is already colsed!";
        }
    },

};
```

### Object-literal notation

```js
var sister = {
  name: "Sarah",
  age: 23,
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true
};
```

The syntax you see above is called **object-literal notation**. There are some important things you need to remember when you're structuring an object literal:

- The "key" (representing a property or method name) and its "value" are separated from each other by a colon
- The key: value pairs are separated from each other by commas
- The entire object is wrapped inside curly braces { }.

And, kind of like how you can look up a word in the dictionary to find its definition, the key in a key:value pair allows you to look up a piece of information about an object. Here's are a couple examples of how you can retrieve information about my sister's parents using the object you created.

```js
// two equivalent ways to use the key to return its value
sister["parents"] // returns [ "alice", "andy" ]
sister.parents // also returns ["alice", "andy"]
```

**What about methods?**:

The sister object above contains a bunch of properties about my sister, but doesn't really say what my sister does. For instance, let's say my sister likes to paint. You might have a paintPicture() method that returns "Sarah paints a picture!" whenever you call it. The syntax for this is pretty much exactly the same as how you defined the properties of the object. The only difference is, the value in the key:value pair will be a function.

```js
var sister = {
  name: "Sarah",
  age: 23,
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true,
  paintPicture: function() { return "Sarah paints!"; }
};
```

Call methods..........

```js
sister.paintPicture();
```

#### Summary of Objects(Naming Convention)

Objects are one of the most important data structures in JavaScript. Get ready to see them everywhere!

They have properties (information about the object) and methods (functions or capabilities the object has). Objects are an incredibly powerful data type and you will see them all over the place when working with JavaScript, or any other object-oriented programming language.

**Object literals, methods, and properties**:

You can define objects using **object-literal notation**:

```js
var myObj = {
  color: "orange",
  shape: "sphere",
  type: "food",
  eat: function() { return "yummy" }
};

myObj.eat(); // method
myObj.color; // property
```

**Naming conventions**:

Feel free to use upper and lowercase numbers and letters, but don't start your property name with a number. You don't need to wrap the string in quotes! If it's a multi-word property, use camel case. Don't use hyphens in your property names

```js
var richard = {
  "1stSon": true;
  "loves-snow": true;
};

richard.1stSon // error
richard.loves-snow // error
```

**Bank Accounts Object**:

```js
var savingsAccount = {
  balance: 1000,
  interestRatePercent: 1,
  deposit: function addMoney(amount) {
    if (amount > 0) {
      savingsAccount.balance += amount;
    }
  },
  withdraw: function removeMoney(amount) {
    var verifyBalance = savingsAccount.balance - amount;
    if (amount > 0 && verifyBalance >= 0) {
      savingsAccount.balance -= amount;
    }
  }
};
```

#### Donuts

```js
var donuts = [
  { type: "Jelly", cost: 1.22 },
  { type: "Chocolate", cost: 2.45 },
  { type: "Cider", cost: 1.59 },
  { type: "Boston Cream", cost: 5.99 }
];

donuts.forEach(function(donut){

    // donut represents a single element of donuts array
    // donut is an object, therefore you can access its properties using a dot notation
    console.log(donut.type+" donuts cost $"+donut.cost+" each");
});
```

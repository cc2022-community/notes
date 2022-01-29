# freeCodeCamp JavaScript Course Notes

## **Read me first**

[JavaScript course on freeCodeCamp](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/) | [JavaScript Bootcamp playlist](https://www.youtube.com/playlist?list=PLU3RKvMpgrSEswU7f9pg6EYaO1s944CDI) | [JavaScript on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

While it is not strictly necessary, it is a good practice to type the semicolon `;` at the end of each line.

## Comments

[Comments on MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#comments)

```js
// This is a single-line comment

let variableName; // This is also a single-line comment, next to some code

/* And this is a multi-line comment.
let variableName
See? You can even comment out code
so that it doesn't execute! */
```

## Variables, Constants

[Variables on MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables#content)

- `var` - **variable**; you can declare (create) it multiple times
- `let` - **variable**; you can declare it only once, but you can change its value later
- `const` - **constant**; you can declare it only once, its value will not change

It is recommended to use `let` for variables, since you won't be able to accidentally declare it multiple times.

```js
let myVariable; // Declare a variable
// Use what's called a "camelCase" to name your variables
myVariable = "Hello World"; // Assign a value to a variable
myVariable = 12; // You can assign numbers without quotation marks
```

```js
var myName = "Andrew"; // Declare a variable
var myName = "Barbara"; // You can declare a "var" multiple times
// Note that you can't do the same with a "let"
```

```js
const MY_CONSTANT;
/* It is a good practice to name constants using
what is called a "SCREAMING_SNAKE_CASE", so that
you can easily tell them apart from variables */
```

```js
myName = myVariable; // You can assign the value of one variable to another

let decimalValue = 3.59; // You can assign a decimal value to your variable as well
```

## Console Logging

[console.log on MDN](https://developer.mozilla.org/en-US/docs/Web/API/console/log#content)

You can print out anything you want to the JavaScript console - a string, a number, a variable, a constant, a mathematical equation, etc.

Very useful for checking the value of a variable

```js
console.log("Hello World"); // Prints "Hello World" to the console
console.log(myVariable); // Prints the (declared above) number 12 to the console
console.log(5 + 6); // Prints the number 11
```

## Mathematical Operations

[Arithmetic operators on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators#arithmetic_operators)

```js
let addVar = 5 + 10; // Value is 15
let subVar = 16 - 9; // Value is 7
let mulVar = 2 * 12; // Value is 24
let divVar = 21 / 7; // Value is 3

addVar++; // Increment the "addVar" variable - same as adding 1 to it
subVar--; // Same as above, but we are decrementing - subtracting 1

let myVar = subVar * 5; // Multiply the value of subVar by 5 - we get 35

let remainder = 11 % 3; // Gives the remainder of the division of two numbers
// Value is 2 (3 * 3 = 9; 11 - 9 = 2)
```

### Prefix and Postfix (increment/decrement)

[Increment and decrement on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators#increment_and_decrement)

```js
let a = 1;

// Postfix
console.log(a++); // First, 'a' is used to print to console, and THEN incremented
// Above statement prints 1

console.log(a); // This statement prints 2 (because we incremented it above)

// Prefix
console.log(++a); // 'a' is incremented first, then the new value of 'a' is printed
// Above statement prints 3
```

### Compound Assignment

[Assignment operators on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators#assignment_operators)

```js
let myVar = 1;

myVar += 5; /* Value is 6
This is the same as:
myVar = myVar + 5
*/

myVar -= 2; // Value is 4
// myVar = myVar - 2

myVar *= 2; // Value is 8
// myVar = myVar * 2

myVar /= 4; // Value is 2
// myVar = myVar / 2
```

## Strings

[Strings on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#contents)

### Quotation Marks

[Text formatting on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Text_formatting#content)

```js
// You can escape literal quotes inside your string using a backslash
let myVar = 'This is a "JavaScript" course.';
console.log(myVar); // This is a "JavaScript" course.

// You can also use single quotes
let doubleQuoteStr = "This is a string";
let singleQuoteStr = "This is also a string";

myVar = 'Adam said, "Hi, Barbara!"';
console.log(myVar); // Adam said, "Hi, Barbara!"
```

### Escape Sequences

[Escape sequences on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#escape_sequences)

| Code | Output          |
| ---- | --------------- |
| `\'` | single quote    |
| `\"` | double quote    |
| `\\` | backslash       |
| `\n` | new line        |
| `\r` | carriage return |
| `\t` | tab             |
| `\b` | word boundary   |
| `\f` | form feed       |

```js
let myStr = "FirstLine\n\t\\SecondLine\nThirdLine";

console.log(myStr);

/* Output:
FirstLine
        \SecondLine
ThirdLine
*/
```

### Concatenation

[Addition on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Addition#content)

```js
let myStr = "I come first. " + "I come second.";
// Notice the space at the end of the first string

console.log(myStr); // I come first. I come second.
```

```js
let myStr = "I come first. ";
myStr += "I come second.";

console.log(myStr); // I come first. I come second.
```

### Constructing Strings with Variables

```js
const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";

console.log(ourStr); // Hello, our name is freeCodeCamp, how are you?
```

```js
const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;

console.log(ourStr); // freeCodeCamp is awesome!
```

### Operations on Strings

[String objects on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Text_formatting#string_objects)

```js
const lastName = "Lovelace";

// Find the length of a string
let lastNameLength = lastName.length;
console.log(lastNameLength); // Value is 8 - word "Lovelace" is 8 characters long

// Use bracket notation to find the first character in a string
let firstLetterOfLastName = lastName[0]; // Index 0 is our first letter
console.log(firstLetterOfLastName); // Value is "L"
```

**_IMPORTANT!_** In bracket notation we start counting from zero (_Zero-based indexing_; this is common for most modern programming languages). That means, for example:

- 1st character is at `[0]`
- 2nd character is at `[1]`
- 3rd character is at `[2]`
- 7th character is at `[6]`
- 30th character is at `[29]`

```js
// Use bracket notation to find the Nth character in a string
let thirdLetterOfLastName = lastName[2]; // Index 2 is our third letter
console.log(thirdLetterOfLastName); // Value is "v"

// Use bracket notation to find the last character in a string
let lastLetterOfLastName = lastName[lastName.length - 1];
// Remember to subtract 1 since we are counting from 0!
console.log(lastLetterOfLastName); // Value is "e"
```

#### String Mutability

In JavaScript, `String` values are immutable, which means that they cannot be altered once created.

```js
// This code will throw an error
let myStr = "Bob";
myStr[0] = "J";
// TypeError: 0 is read-only
```

This does _not_ mean that `myStr` cannot be changed, just that the individual characters of a _string literal_ cannot be changed. The only way to change `myStr` would be to assign it with a new string.

```js
// This code is correct
let myStr = "Bob";
myStr = "Job";
// Value is "Job"
```

## Arrays

[Arrays on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

Arrays can be thought of as lists in JavaScript; an array can hold multiple values, even if they are not the same data type (string, integer, boolean, etc.) within that array.

```js
const sandwich = ["peanut butter", "jelly", "bread", 2, false];
```

### Multi-dimensional Arrays

```js
// Arrays can be nested within other arrays
const teams = [
  ["Bulls", 23],
  ["White Sox", 45],
];
```

### Access Array Data

Much like getting the value of a single character in a string, accessing the full values within an array use square brackets and an index number

```js
const months = ["January", "February", "March"];
console.log(months[0]);  // Zero-indexing applies here as well. This will print "January" in the console.
```

We can access values in a multi-dimensional array as well:

```js
const daysInMonth = [["January", 31], ["February", 28], ["March", 31]];
console.log(daysInMonth[2][0]); // This will print "March" in the console.
console.log(daysInMonth[1][1]); // This will print 28 in the console.
```

### Modify Array Data

```js
let myArray = [2, 3, 4];
console.log(myArray); // Will print the array in console [ 2, 3, 4 ]

// Add element to the end of the array
myArray.push(5);
console.log(myArray); // Will print the new array in console  [ 2, 3, 4, 5 ]

// Remove last element of the array
myArray.pop();
console.log(myArray); // Will print the new array in console  [ 2, 3, 4 ]

// Remove element at the beginning of the array
myArray.shift();
console.log(myArray); // Will print the new array in console  [ 3, 4 ]

// Add element at the beginning of the array
myArray.unshift(2);
console.log(myArray); // Will print the new array in console  [ 2, 3, 4 ]
```

## Data Types

- `number` - represents both integers and decimals

  ```js
  let integer = 2;
  let decimal = 2.0;
  ```

- `string` - represents a sequence of characters enclosed in `""` or `''`

  ```js
  let name = "John Doe";
  let country = 'United States';
  ```

- `boolean` - represents only 2 values, `true` and `false`, which are not enclosed in quotes (`"true"` and `"false"` are strings)

  ```js
  const adult = true;
  ```

- `null` - represents nothing; normally used to specify explicitly that a variable currently doesn't have any value
  
- `undefined` - is automatically assigned to a variable when it is declared but not assigned any value

Use `typeof` to know the type of variable or literal.

  ```js
  let a;                     // declared but not initialized with any value
  console.log(typeof a);     // undefined
  
  a = 1;
  console.log(typeof a);     // number
  
  a = 1.11;
  console.log(typeof a);     // number
  
  a = false;
  console.log(typeof a);     // boolean
  
  a = "hello";
  console.log(typeof a);     // string
  ```

## ES6

### Modify Array Data (ES6)

#### Rest parameter in function parameters

With the rest parameter, it does not matter how many arguments are given in an array, the function will accept it; arguments are "condensed" into one element

```js
function addToArr(...args) {

  return args.filter(arg=>arg>=4);  // filter out all elements greater than or equal to 4
}


console.log(addToArr(1,2,3,4,5))  // the result will be [4,5]

```
  
#### Spread operator

[Spread syntax on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

Expands an array into its individual elements.

```js

const mySpreadArray = [54,2,30,41,5];

console.log(Math.min(...mySpreadArray))         // this example gives back the min of the array, without the ... it would result in NaN.

```

#### Destructuring arrays

Exctract data from an array and assign it to variables.

```js

const myArr = [1,2,3,4,5,6,7,8,9];

// assign the first four elements of the array to the variables a b c and d.

let [a,b,c,d] = myArr;

console.log(a,b,c,d) // result is 1, 2, 3, 4.

// asign the fifth element to the variable e

let [,,,,e] = myArr;    // use commas until desired index.

console.log(e); // result is number 5.

```

### Scopes

```js
function checkScope() {
  let i = 'function scope';
  if (true) {
    let i = 'block scope';
    console.log('Block scope i is:', i);
  }
  console.log('Function scope i is:', i);
  return i;
}

checkScope();

/*
Block scope i is: block scope
Function scope i is: function scope
*/
```

### Prevent object mutation

`const` is not enough to protect data from mutation; you can freeze an object to reject any attempts at changing the object

```js
Object.freeze(obj);
```

### Default parameters for functions

```js
const increment = (number, value = 1) => number + value;

console.log(increment(5, 2)); // 7
console.log(increment(5)); // 6
```

### Arrow functions

```js
const myFunc = function() {
  const myVar = "value";
  return myVar;
}
```

We can use the *arrow function syntax* instead of having to write anonymous functions this way:

```js
const myFunc = () => {
  const myVar = "value";
  return myVar;
}
```

When there is no function body, and only a return value, arrow function syntax allows you to omit the keyword `return` (as well as the brackets):

```js
const myFunc = () => "value";
```

### Template literals

```js
const myDog = {
    name: "Gustavo",
    legs: 4,
    tails: 1
};

console.log(`My dog is called ${myDog.name}, and he has ${myDog.legs} legs and ${myDog.tails} tail`)
```

### Classes

```js
class SpaceShuttle {
  constructor(targetPlanet) {
    this.targetPlanet = targetPlanet;
  }
}
const zeus = new SpaceShuttle('Jupiter');
```

### Modules

```html
<script type="module" src="index.js"></script>
```

A script that uses this `module` type can now use the `import` and `export` features

#### Export

```js
export const add = (x, y) => {
  return x + y;
}d
```

```js
const add = (x, y) => {
  return x + y;
}

export { add };
```

##### Export fallback

Usually, you will use this syntax if only one value is being exported from a file, or to create a fallback value for a file or module

```js
export default function add(x, y) {
  return x + y;
}
```

```js
export default function(x, y) {
  return x + y;
}
```

| Note                                                         |
| ------------------------------------------------------------ |
| You cannot use `export default` with `var`, `let` or `const` |

#### Import

```js
import { add, subtract } from './math_functions.js';
```

Import everything from a file into an object:

```js
import * as myMathModule from "./math_functions.js";
```

##### Import a default export

```js
import add from "./math_functions.js";
```

## Regular Expressions

[Regex on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

```js
let testStr = "JavaScript";
let testRegex = /Script/;
testRegex.test(testStr); // returns true

// Other forms of "Script" will not match
testRegex = /script/;
testRegex.test(testStr); // returns false
```

```js
// Multiple possibilities using OR | operator
let testStr = "Today we are learning JavaScript.";
let testRegex = /HTML|CSS|JavaScript|Ruby/;
testRegex.test(testStr); // returns true
```

### Regex Flags

[Advanced searching with flags on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions#advanced_searching_with_flags)

```js
let testStr = "Repeat, Repeat, Repeat";
let ourRegex = /Repeat/;
testStr.match(ourRegex);
// returns ["Repeat"]

let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);
// returns ["Repeat", "Repeat", "Repeat"]
```

```js
let testStr = "JavaScript, javascript, javaScript, JAVASCRIPT, jAVasCrIPt, JAvAScrIpT";
let ourRegex = /JavaScript/gi;
testStr.match(ourRegex);
// returns all the occurences of the word "javascript" in the string regardless of their cases
```

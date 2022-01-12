# freeCodeCamp JavaScript course notes

## Read me first

[JavaScript course on freeCodeCamp](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/) | [JavaScript Bootcamp playlist](https://www.youtube.com/playlist?list=PLU3RKvMpgrSEswU7f9pg6EYaO1s944CDI)

While it is not strictly necessary, it is a good practice to type the semicolon `;` at the end of each line.

## Comments

```js
// This is a single-line comment

let variableName; // This is also a single-line comment, next to some code

/* And this is a multi-line comment.
let variableName
See? You can even comment out code
so that it doesn't execute! */
```

## Variables, constants

- `var` - **variable**; you can declare (create) it multiple times
- `let` - **variable**; you can declare it only once, but you can change its value later
- `const` - **constant**; you can declare it only once, its value will not change

It is recommended to use `let` for variables, since you won't be able to accidentally declare it multiple times.

```js
let myVariable;             // Declare a variable
        // Use what's called a "camelCase" to name your variables
myVariable = "Hello World"; // Assign a value to a variable
myVariable = 12;            // You can assign numbers without quotation marks
```

```js
var myName = "Andrew";      // Declare a variable
var myName = "Barbara";     // You can declare a "var" multiple times
        // Note that you can't do the same with a "let"
```

```js
const MY_CONSTANT;
/* It is a good practice to name constants using 
what is called a "SCREAMING_SNAKE_CASE", so that 
you can easily tell them apart from variables */
```

```js
myName = myVariable;        // You can assign the value of one variable to another

let decimalValue = 3.59;    // You can assign a decimal value to your variable as well
```

## Console logging

You can print out anything you want to the JavaScript console - a string, a number, a variable, a constant, a mathematical equation, etc.

Very useful for checking the value of a variable

```js
console.log("Hello World");  // Prints "Hello World" to the console
console.log(myVariable);     // Prints the (declared above) number 12 to the console
console.log(5 + 6);          // Prints the number 11
```

## Mathematical operations

```js
let addVar = 5 + 10;     // Value is 15
let subVar = 16 - 9;     // Value is 7
let mulVar = 2 * 12;     // Value is 24
let divVar = 21 / 7;     // Value is 3

addVar++;            // Increment the "addVar" variable - same as adding 1 to it
subVar--;            // Same as above, but we are decrementing - subtracting 1

let myVar = subVar * 5; // Multiply the value of subVar by 5 - we get 35

let remainder = 11 % 3; // Gives the remainder of the division of two numbers
        // Value is 2 (3 * 3 = 9; 11 - 9 = 2)
```

### Prefix and postfix increment/decrement

```js
let a = 1;

// Postfix
console.log(a++);   // First, 'a' is used to print to console, and THEN incremented
        // Above statement prints 1

console.log(a);     // This statement prints 2 (because we incremented it above)

// Prefix
console.log(++a);   // 'a' is incremented first, then the new value of 'a' is printed
        // Above statement prints 3
```

### Compound assignment

```js
let myVar = 1;

myVar += 5;     /* Value is 6
This is the same as:
myVar = myVar + 5 */

myVar -= 2;     /* Value is 4
myVar = myVar - 2 */

myVar *= 2;     /* Value is 8
myVar = myVar * 2 */

myVar /= 4;     /* Value is 2
myVar = myVar / 2 */
```

## Strings

### Quotation marks

```js
// You can escape literal quotes inside your string using a backslash
let myVar = "This is a \"JavaScript\" course.";
console.log(myVar);     // This is a "JavaScript" course.

// You can also use single quotes
let doubleQuoteStr = "This is a string"; 
let singleQuoteStr = 'This is also a string';

myVar = 'Adam said, "Hi, Barbara!"'
console.log(myVar);     // Adam said, "Hi, Barbara!"
```

### Escape sequences

| Code |      Output      |
|------|------------------|
| \'   | single quote     |
| \"   | double quote     |
| \\\\ | backslash        |
| \n   | new line         |
| \r   | carriage return  |
| \t   | tab              |
| \b   | word boundary    |
| \f   | form feed        |

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

```js
let myStr = "I come first. " + "I come second.";
        // Notice the space at the end of the first string

console.log(myStr);     // I come first. I come second.
```

```js
let myStr = "I come first. ";
myStr += "I come second.";

console.log(myStr);     // I come first. I come second.
```

### Constructing strings with variables

```js
const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";

console.log(ourStr);    // Hello, our name is freeCodeCamp, how are you?
```

```js
const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;

console.log(ourStr);    // freeCodeCamp is awesome!
```

### Operations on strings

```js
const lastName = "Lovelace";

// Find the length of a string
let lastNameLength = lastName.length;
console.log(lastNameLength);    // Value is 8 - word "Lovelace" is 8 characters long

// Use bracket notation to find the first character in a string
let firstLetterOfLastName = lastName[0];        // Index 0 is our first letter
console.log(firstLetterOfLastName);             // Value is "L"
```

***IMPORTANT!*** In bracket notation we start counting from zero (*Zero-based indexing*; this is common for most modern programming languages). That means, for example:

- 1st character is at `[0]`
- 2nd character is at `[1]`
- 3rd character is at `[2]`
- 7th character is at `[6]`
- 30th character is at `[29]`

```js
// Use bracket notation to find the Nth character in a string
let thirdLetterOfLastName = lastName[2];        // Index 2 is our third letter
console.log(thirdLetterOfLastName);             // Value is "v"

// Use bracket notation to find the last character in a string
let lastLetterOfLastName = lastName[lastName.length - 1];     
        // Remember to subtract 1 since we are counting from 0!
console.log(lastLetterOfLastName);              // Value is "e"
```

#### String mutability

In JavaScript, `String` values are immutable, which means that they cannot be altered once created.

```js
// This code will throw an error
let myStr = "Bob";
myStr[0] = "J";
// TypeError: 0 is read-only
```

This does *not* mean that `myStr` cannot be changed, just that the individual characters of a *string literal* cannot be changed. The only way to change `myStr` would be to assign it with a new string.

```js
// This code is correct
let myStr = "Bob";
myStr = "Job";
// Value is "Job"
```

## Arrays

```js
// An array can hold multiple values
const sandwich = ["peanut butter", "jelly", "bread", 2];

// You can nest arrays inside other arrays
const teams = [["Bulls", 23], ["White Sox", 45]];
```

TODO: Multi-dimensional arrays

### Modify array data

```js
let myArray = [2, 3, 4];
console.log(myArray);   // Will print the array in console [ 2, 3, 4 ]

// Add element to the end of the array
myArray.push(5);
console.log(myArray);   // Will print the new array in console  [ 2, 3, 4, 5 ]

// Remove last element of the array
myArray.pop();
console.log(myArray);   // Will print the new array in console  [ 2, 3, 4 ]

// Remove element at the beginning of the array
myArray.shift();
console.log(myArray);   // Will print the new array in console  [ 3, 4 ]

// Add element at the beginning of the array
myArray.unshift(2);
console.log(myArray);   // Will print the new array in console  [ 2, 3, 4 ]
```

# freeCodeCamp JavaScript course notes

## Comments

```js
// This is a single-line comment

let variableName // This is also a single-line comment, next to some code

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
var myName = "Barbara";     // You can declare a *var* multiple times
// Note that you can't do the same with a *let*
```

```js
const MY_CONSTANT;
/* It is a good practice to name constants using 
what is called a "SCREAMING_SNAKE_CASE", so that 
you can easily tell them apart from variables */
```

```js
myName = myVariable;        // You can assign the value of one variable to another

let decimalValue = 3.59     // You can assign a decimal value to your variable as well
```

## Mathematical operations

```js
let addVar = 5 + 10     // Value is 15
let subVar = 16 - 9     // Value is 7
let mulVar = 2 * 12     // Value is 24
let divVar = 21 / 7     // Value is 3

addVar++            // Increment the "addVar" variable - same as adding 1 to it
subVar--            // Same as above, but we are decrementing - subtracting 1

let myVar = subVar * 5  // Multiply the value of subVar by 5 - we get 35
```
### Prefix and Postfix increment/decrement
```js
let a = 1;
// postfix
console.log(a++); // a is used first used to print to console and then a is incremented by 1
// Above statement prints 1
console.log(a); // prints 2
// prefix
console.log(++a); // a is incremented first and then new value of a is used to print
// Above statement prints 3
// same applies for -- but decremented by 1
```
### Some methods to change arrays

```js

let myArray =[2,3,4];
console.log(myArray); // will display the array in console [ 2, 3, 4 ]

// remove last element of array with .pop()
myArray.pop();
console.log(myArray); // will display the new array in console  [ 2, 3 ]

// add element to the end of the array with .push()
myArray.push(4);
console.log(myArray);  // will display the new array in console  [ 2, 3, 4 ]

// remove  element at the beginning of the array with .shift()
myArray.shift();
console.log(myArray);   // will display the new array in console  [ 3, 4 ]

// add element at thae beginning of the array with .unshift()
myArray.unshift(2);
console.log(myArray); // will display the new array in console with the 2 readded  [ 2, 3, 4 ]

```

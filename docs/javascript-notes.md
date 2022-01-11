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

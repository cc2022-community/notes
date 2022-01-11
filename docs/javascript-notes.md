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
- `const` - **constant**; you can declare it only once and won't be able to change its value

It is recommended to use `let` for variables, since you won't be able to declare it multiple times.

```js
let myVariable;             // Declare a variable
// Use what's called a "camelCase" to name your variables
myVariable = "Hello World"; // Assign a value to a variable
myVariable = 12;            // You can assign numbers without quotation marks

var myName = "Andrew";      // Declare a variable
var myName = "Barbara";     // You can declare a *var* multiple times
// Note that you can't do the same with a *let*

const MY_CONSTANT;
/* It is a good practice to name constants using 
what is called a "SCREAMING_SNAKE_CASE", so that 
you can easily tell them apart from variables */

myName = myVariable;
```

# Arrow Functions

Arrow functions are like a shorter way to write regular functions.

```jsx
function traditionalFunction(x, y) {
  return x + y;
}

const arrowFunction = (x, y) => x + y;

console.log(traditionalFunction(1, 2)); // 3
console.log(arrowFunction(1, 2)); // 3
```

## Syntax

```jsx
() => expression

param => expression

(param) => expression

(param1, paramN) => expression

() => {
  statements
}

param => {
  statements
}

(param1, paramN) => {
  statements
}
```

## So what are different from traditional functions?

- They don't have their own `this`, `arguments`, or `super`, so they shouldn't be used for certain things.
- You can't make new objects with arrow functions. Trying will cause an error.
- They can't use `yield` or be used to make special kinds of functions.

### Let’s take a look at a quick example

Here is an example of a `sum` function that returns the sum of two parameters:

```jsx
function sum(a, b) {
  return a + b;
}
```

You can execute the `sum` function before declaring the function due to hoisting:

```jsx
sum(1, 2); // 3

function sum(a, b) {
  return a + b;
}
```

Now let’s try with the arrow function

```jsx
sum(1, 2) //Uncaught ReferenceError: Cannot access 'sum' before initialization

const sum = function (a, b) {
  return a + b
}
```

Before we go any further, please take a look at [Named vs. Anonymous Functions](./Named%20vs%20Anonymous%20Functions.md) first.

An *[arrow function expression](https://www.digitalocean.com/community/tutorials/how-to-define-functions-in-javascript#arrow-functions)* is an anonymous function expression written with the “fat arrow” syntax (`=>`).

```jsx
const sum = (a, b) => {
  return a + b
}
```

The arrow functions are not hoisted, so you cannot call them before you declare them. They are also **always anonymous**—there is no way to name an arrow function. If you want to dig deeper, please take a look at the reference.

### References:

[Understanding Arrow Functions in JavaScript  | DigitalOcean](https://www.digitalocean.com/community/tutorials/understanding-arrow-functions-in-javascript)

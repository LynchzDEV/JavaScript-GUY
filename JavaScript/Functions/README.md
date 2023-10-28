# Functions

In JavaScript, functions are like special VIPs. They can be treated like regular things. This means you can put them in a box (variable), send them as a gift (argument) to another friend (function), and even receive them as a gift (return) from that friend. So, you can do a lot of cool stuff with them!

1. **Function Definition and Invocation**: In JavaScript, a function is a piece of code that can be defined once and executed multiple times. It allows you to group a set of related actions and call them by a single name.
2. **Parameterization**: JavaScript functions can be defined with parameters, which act as local variables within the function. These parameters allow you to pass values into the function when it is called, making the function more flexible and reusable.
3. **Functions as Objects**: Functions in JavaScript are objects. This means they can be assigned to variables, passed as arguments to other functions, and even returned from other functions. This feature enables the creation of higher-order functions and makes JavaScript a versatile language.
4. **Function Nesting and Scope Access**: JavaScript functions can be nested within other functions. Nested functions have access to the variables in their outer function's scope, which is known as lexical scoping. This feature enables the creation of closures, where inner functions retain access to the variables of their outer functions even after the outer function has finished execution.

```jsx
// Function Definition and Invocation
function greet(name) {
  console.log(`Hello, ${name}!`);
}
greet("John"); // Output: Hello, John!

// Parameterization
function add(a, b) {
  return a + b;
}
const sum = add(5, 3); // sum will be 8

// Functions as Objects
const myFunction = function () {
  console.log("This is a function assigned to a variable.");
};
myFunction(); // Output: This is a function assigned to a variable.

// Function Nesting and Scope Access
function outerFunction() {
  const outerVariable = "I am from the outer function";

  function innerFunction() {
    console.log(outerVariable);
  }

  innerFunction(); // Output: I am from the outer function
}
outerFunction();
```

[Higher-Order Functions](./Higher-Order%20Functions)

[Arrow Functions](Functions%20078ef94df2244a77b2f4878b1bafbd60/Arrow%20Functions%20272534d3008c4b15998480114106bad9.md)

[Named vs Anonymous Functions](Functions%20078ef94df2244a77b2f4878b1bafbd60/Named%20vs%20Anonymous%20Functions%2041d874f87dd64f809eda66f39d6c35f9.md)

[**Nested Functions**](Functions%20078ef94df2244a77b2f4878b1bafbd60/Nested%20Functions%20f71bc13c61de432cb4697ecf904c6db2.md)

[Closure Functions](Functions%20078ef94df2244a77b2f4878b1bafbd60/Closure%20Functions%202fee34e6a60c417a999630c5b1db4dc8.md)

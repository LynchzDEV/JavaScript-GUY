# Named vs Anonymous Functions

## Named Functions

```jsx
function greeting(name) {
  return `Hello ${name}!`;
}
```

Named functions always look in the format below:

```jsx
function functionoName() {
	...
}
```

## Anonymous Functions

Anonymous functions are functions that are not assigned names. They can take a few different forms.

```jsx
const greeting = function (name) {
  return `Hello ${name}!`;
};

const farewell = (name) => {
  return `Bye ${name}!`;
};
```

Although they do not have names, they can be referenced through the variable they are assigned to.

Once initialized, the anonymous function exists through the variable, but the original function itself is gone and cannot be reused.
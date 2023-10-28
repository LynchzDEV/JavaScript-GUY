# Defining Methods

A function is one of three data types that an object can store, which is referred to as a method in the [Getting Started chapter](Getting%20Started%2046c5a9a5b62143a4ba5156400bd296c4.md).

<aside>
💡 Methods were introduced as a way to include reusable behavior within an object.

</aside>

```jsx
const obj = {
  foo() {
    return 'bar';
  },
};

console.log(obj.foo());
```

![The result of the above code](https://github.com/LynchzDEV/JavaScript-GUY/blob/main/JavaScript/Objects/Defining%20Methods/preview.png)

The result of the above code

## Syntax

```jsx
const obj = {
  foo: function () {
    // …
  },
  bar: function () {
    // …
  },
};
```

### Shorthand

```jsx
const obj = {
  foo() {
    // …
  },
  bar() {
    // …
  },
};
```

### Example Usage

```jsx
const obj = {
  a: "foo",
  b() {
    return this.a;
  },
};
console.log(obj.b()); // "foo"
```

### Method Definitions and Usages in Classes

```jsx
class Car {
  x = 0;

  move() {
    this.x++;
  }
}

const car = new Car();
car.move();
```

### Reference:

[Method definitions - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions#syntax)

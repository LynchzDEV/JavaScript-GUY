# Prototype Chaining

We learned about prototype chaining in the previous chapter, so in this chapter, we'll look more closely at it.

<aside>
💡 **Note:** `Object.getPrototypeOf` might return an unexpected value if you are running using NodeJS. For more details, you can [read this](https://stackoverflow.com/a/51233850).

</aside>

## Before we go any deeper, let’s get to know the must-know methods.

In the previous chapter, we discovered that objects store their superclasses through the `[[prototype]]`**,** but how can we access it?

Normally when we would access the prototype with `myObj.__proto__` but according to [SonarLint `__proto__` should not be used](https://rules.sonarsource.com/javascript/RSPEC-6654/).

To avoid using we can use `Object.getPrototype` and `Object.setPrototype` methods instead.

- `Object.getPrototype(object)` get the prototype of the object.
- `Object.setPrototype(object)` sets the prototype of the object or sets the superclass of the object.

## Now let’s start 😉

```jsx
const myDate = new Date(); // Initialize the 'myDate' object.
let object = myDate; // Create the 'object' variable and set it as a reference to the 'myDate' object.

// Iterate through the prototype chain of the 'myDate' object.
do {
  object = Object.getPrototypeOf(object); // Get the prototype and set the new reference to the prototype.
  console.log(object?.constructor?.name); // Log the name of the prototype.
} while (object);
```

![The result of the above code](Prototype%20Chaining%209469bfb949fb4ff4a49fc21ce8813d98/Screenshot_2023-10-15_at_18.09.26.png)

The result of the above code

As seen in the output, the object created by `new Date()` uses `Date.prototype` as its prototype. The `Date` object, in turn, uses `Object.prototype` as its prototype, and the last one, `Object`, which is the root, doesn't have any prototype.

### Inheritance

```jsx
const obj1 = {};
obj1.x = 1;

const obj2 = Object.create(obj1);
obj2.y = 2;

const obj3 = Object.create(obj2);
obj3.z = 3;

console.log(obj3.x); // 1
console.log(obj3.y); // 2
console.log(obj3.z); // 3
```

As you can see, in JavaScript inheritance also works similarly to class-based OOP; the properties are also inherited to the subclasses.

### ****Checking Subclass Relationship****

```jsx
const myObj = new Array();
console.log(Array.prototype.isPrototypeOf(myObj)); // true
console.log(Date.prototype.isPrototypeOf(myObj)); // false
console.log(Object.prototype.isPrototypeOf(myObj)); // true
```

This code snippet creates an instance `myObj` of the Array class. Then, it checks if `myObj` is a subclass of `Array.prototype`, `Date.prototype`, and `Object.prototype` using the `isPrototypeOf` method.

The outputs show that `myObj` is a subclass of `Array.prototype` and `Object.prototype`, but not of `Date.prototype`.
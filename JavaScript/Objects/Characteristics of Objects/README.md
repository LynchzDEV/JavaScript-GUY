# Characteristics of Objects

Objects are **mutable** and manipulated by reference.

When you assign an object to a new variable or use it as a reference, changes made to one variable also affect the other.

```jsx
const blueBoy = {
  name: 'Chanapol',
  score: 12,
};

const blueGirl = blueBoy;
blueGirl.name = 'Lopanahc';
blueGirl.score = 10;

console.log(blueBoy);
```

![The result of the above code](https://github.com/LynchzDEV/JavaScript-GUY/blob/main/JavaScript/Objects/Characteristics%20of%20Objects/preview.png)

The result of the above code

## ****Compare Objects for Equality****

Normally, when we compare primitive data types, the result should be true if both values are the same.

```jsx
const a = 1;
const b = 1;
console.log(a === b); // true
```

Now, let's apply this logic to objects.

```jsx
const a = { name: 'blue' };
const b = { name: 'blue' };
console.log(a === b); // false
```

As you can see, the result is different, but why?

When you compare objects, you are comparing their memory addresses, not their contents.

## Let’s take a look deeper:

When you use the **`{}`** syntax, you are creating a new object that is stored in a unique memory address.

```jsx
const a = { name: 'blue' }; // Create a new object store in memory address: 0xFA
const b = { name: 'blue' }; // Create a new object stores in memory adress: 0xFB
console.log(a === b); // Compare betweem 0xFA and 0XFB: false
```

## So how can we compare objects?

1. Referential equality: `==`, `===`
    
    ```
    const city1 = { name: 'Tokyo' };
    const city2 = { name: 'Tokyo' };
    
    console.log(city1 == city2); // false
    console.log(city1 === city2); // false
    ```
    
2. Manual comparison of properties values.
    - A simple way to compare objects by content is to read the properties and compare them manually.
    
    ```
    const city1 = { name: 'Tokyo' };
    const city2 = { name: 'Tokyo' };
    
    console.log(city1.name === city2.name); // true
    ```
    
3. Shallow Equality check the properties values for equality.
    - It compares the properties' values of objects at the first level, without considering nested objects or arrays.
    
    ```jsx
    function shallowEquality(object1, object2) {
      const keys1 = Object.keys(object1);
      const keys2 = Object.keys(object2);
    
      if (keys1.length !== keys2.length) {
        return false;
      }
    
      for (let key of keys1) {
        if (object1[key] !== object2[key]) {
          return false;
        }
      }
    
      return true;
    }
    
    const city1 = { name: 'Tokyo' };
    const city2 = { name: 'Tokyo' };
    shallowEquality(city1, city2); // true
    ```
    

### References:

[JavaScript Comparison Operators – How to Compare Objects for Equality in JS](https://www.freecodecamp.org/news/javascript-comparison-operators-how-to-compare-objects-for-equality-in-js/)

[How to Compare Objects in JavaScript](https://dmitripavlutin.com/how-to-compare-objects-in-javascript/)

# Prototype vs Class OOP

<aside>
🚨 The notes in this chapter you will read are summarized from the article below, which I strongly advise you to read.

</aside>

[Why JavaScript is a Prototype-based OOP](https://github.com/LynchzDEV/JavaScript-GUY/blob/main/JavaScript/Objects/Prototype%20vs%20Class%20OOP/preview2.png)

In a class-based OOP, we use classes as a blueprint for creating the objects, whereas in a prototype-based OOP, we can create the objects without first defining their class.

So, if we don’t need a class, how do we inherit properties? Instead, objects inherit from other objects through a prototype property.

### **Prototypes and proto-Properties**

Prototypes play a central role in JavaScript's prototype-based OOP. Each object has a hidden property called **`prototype`**, represented by **`[[Prototype]]`**, which points to another object. This object, referred to as "the prototype of that object," holds the properties and methods that the object inherits.

![Untitled](https://github.com/LynchzDEV/JavaScript-GUY/blob/main/JavaScript/Objects/Prototype%20vs%20Class%20OOP/preview1.png)

This approach allows us to create objects with similar functionality to those in class-based OOPs.

## **How prototype works**

```jsx
const person = {
  name: 'Park',
  age: 18,
};

console.log(person.name); // Park
```

We are accessing the existing properties from the given code, **but what if that property doesn’t exist?**

If the property we are looking for doesn’t exist in the property, the JS engine will try to search `[[prototype]]`, **this process is known as prototype chaining.**

![Untitled](Prototype%20vs%20Class%20OOP%20beb484541224478eb7b9983205d85639/Untitled%201.png)

### Let’s take a look at a quick example:

```jsx
const car = {
  wheelsAmount: 4,
};

const fordMustang = {
  color: 'black',
  brand: 'ford',
};
Object.setPrototypeOf(fordMustang, car);

console.log(fordMustang.wheelsAmount); // 4
```

In this example, the `fordMustang` object inherits from the `car` object using the `Object.setPrototypeOf(object, prototype)` method. When attempting to access the `wheelsAmount` property in the `fordMustang` object, which doesn't exist, the JS Engine looks at `[[prototype]]` and searches the `car` object.

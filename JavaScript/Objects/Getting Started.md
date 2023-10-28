# Getting Started

In JavaScript, objects contain properties, which are key-value pairs. An object can store three types of values:

1. **Primitive**: These are referred to as properties.
2. **Object**: These are also referred to as properties.
3. **Function**: These are called methods.

## How to create an object?

1. Object Literal

- This is the simplest way to create an object.
- You define an object by enclosing key-value pairs in curly braces.
- Example:
    
    ```jsx
    const person = {
      name: "John",
      age: 30,
    };
    ```
    
1. Constructor Function:
    - You can create objects by defining constructor functions.
    - These functions are used to create multiple objects with the same structure.
    - Example:
        
        ```jsx
        function Person(name, age) {
          this.name = name;
          this.age = age;
        }
        const john = new Person("John", 30);
        ```
        
2. `Object.create()`:
    - This method allows you to create a new object with a specified prototype.
    - Example:
        
        ```jsx
        const personPrototype = {
          greet: function() {
            console.log("Hello!");
          }
        };
        const john = Object.create(personPrototype);
        ```
        
3. Class (ES6):
    - ES6 introduced classes, a more modern way to create objects with constructors and methods.
    - Example:
        
        ```jsx
        class Person {
          constructor(name, age) {
            this.name = name;
            this.age = age;
          }
        }
        const john = new Person("John", 30);
        ```
        
4. Factory Functions:
    - These are functions that return objects.
    - Useful for creating multiple objects with shared properties and methods.
    - Example:
        
        ```jsx
        function createPerson(name, age) {
          return {
            name,
            age,
          };
        }
        const john = createPerson("John", 30);
        ```
        
5. Object Constructor:
    - You can create objects using the Object constructor, but it's less commonly used.
    - Example:
        
        ```jsx
        const person = new Object();
        person.name = "John";
        person.age = 30;
        ```
        
    

Some of you might get confused at this point about why JavaScript is so different from Java and the other OOP languages. Let’s get into the details further 👇.

[Prototype vs Class OOP](Prototype%20vs%20Class%20OOP%20beb484541224478eb7b9983205d85639.md)
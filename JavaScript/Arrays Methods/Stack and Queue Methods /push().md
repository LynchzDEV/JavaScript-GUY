# push()

- **Adds one or more elements to the end of an array** and returns the new length of the array.

## Usage

```jsx
array.push(element1, element2, ..., elementN);
```

## Example

**Example 1:** Adding elements to an array

```jsx
let fruits = ['apple', 'banana'];
fruits.push('cherry', 'date');
console.log(fruits); // Output: ['apple', 'banana', 'cherry', 'date']
```

**Example 2:** Adding a single element to an array

```jsx

let numbers = [1, 2, 3];
numbers.push(4);
console.log(numbers); // Output: [1, 2, 3, 4]
```
# shift()

- **Removes the first element** from an array and returns that removed element. This operation modifies the original array.

## Usage

```jsx
let removedElement = array.shift();
```

## Example

**Example 1:** Removing the first element from an array

```jsx
let fruits = ['apple', 'banana', 'cherry'];
let removedFruit = fruits.shift();
console.log(removedFruit); // Output: 'apple'
console.log(fruits); // Output: ['banana', 'cherry']
```

**Example 2:** Removing and using the first element of an array

```jsx
let numbers = [1, 2, 3, 4, 5];
let firstNumber = numbers.shift();
console.log(firstNumber); // Output: 1
console.log(numbers); // Output: [2, 3, 4, 5]
```
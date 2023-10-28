# join()

- Creates and returns a new string by concatenating all the elements in an array. It can be customized to include a specified separator between each element.

## Usage

```jsx
let newString = array.join(separator);
```

## Example

**Example 1:** Joining elements of an array into a string

```jsx
let elements = ['Fire', 'Air', 'Water'];
let result1 = elements.join();
console.log(result1); // Output: 'Fire,Air,Water'
```

**Example 2:** Joining elements of an array with a custom separator

```jsx
let elements2 = ['Fire', 'Air', 'Water'];
let result2 = elements2.join(' - ');
console.log(result2); // Output: 'Fire - Air - Water'
```
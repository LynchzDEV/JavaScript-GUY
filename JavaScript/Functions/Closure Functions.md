# Closure Functions

- A closure is when a function remembers the environment in which it was created, including the variables outside of its scope.
- It allows an inner function to access and use the variables from its outer function even after the outer function has finished running.
- Essentially, it's like a way for a function to retain a connection to its birthplace, so it can always access its 'ancestral' (บรรพบุรุษ) data.

## Example

```jsx
function createCounter() {
  let count = 0;
  return {
    increment: function() {
      count++;
    },
    decrement: function() {
      count--;
    },
    getCount: function() {
      return count;
    }
  };
}

let counter = createCounter();

counter.increment();
counter.increment();
counter.increment();
console.log(counter.getCount()); // Output: 3

counter.decrement();
console.log(counter.getCount()); // Output: 2
```

## References

[Master the JavaScript Interview: What is a Closure?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36)
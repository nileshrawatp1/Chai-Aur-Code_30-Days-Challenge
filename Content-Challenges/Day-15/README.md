# Table of Content

- [Table of Content](#table-of-content)
- [Day 15: Closures](#day-15-closures)
  - [Tasks/Activities](#tasksactivities)
    - [Activity 1: Understanding Closures](#activity-1-understanding-closures)
    - [Activity 2: Practical Closures](#activity-2-practical-closures)
    - [Activity 3: Closures in Loops](#activity-3-closures-in-loops)
    - [Activity 4: Module Pattern](#activity-4-module-pattern)
    - [Activity 5: Memoization](#activity-5-memoization)
  - [Feature Request](#feature-request)
    - [1. Basic Closure Script](#1-basic-closure-script)
    - [2. Counter Closure Script](#2-counter-closure-script)
    - [3. Unique ID Generator Script](#3-unique-id-generator-script)
    - [4. Loop Closure Script](#4-loop-closure-script)
    - [5. Memoization Script](#5-memoization-script)
  - [Achievement](#achievement)

# Day 15: Closures

## Tasks/Activities

### Activity 1: Understanding Closures

**Task 1: Write a function that returns another function, where the inner function accesses a variable from the outer function's scope. Call the inner function and log the result.**

```javascript
// Task 1: Function returning another function (Closure example)
function outerFunction() {
    const outerVariable = "I'm from the outer function";

    return function innerFunction() {
        console.log(outerVariable);
    };
}

const myFunction = outerFunction();
myFunction(); // Output: I'm from the outer function
```

**Task 2: Create a closure that maintains a private counter. Implement functions to increment and get the current value of the counter.**

```javascript
// Task 2: Closure maintaining a private counter
function createCounter() {
    let counter = 0;

    return {
        increment: function() {
            counter++;
        },
        getValue: function() {
            return counter;
        }
    };
}

const counter = createCounter();
counter.increment();
counter.increment();
console.log(counter.getValue()); // Output: 2
```

### Activity 2: Practical Closures

**Task 3: Write a function that generates unique IDs. Use a closure to keep track of the last generated ID and increment it with each call.**

```javascript
// Task 3: Unique ID generator using closure
function createIdGenerator() {
    let lastId = 0;

    return function generateId() {
        lastId++;
        return lastId;
    };
}

const generateId = createIdGenerator();
console.log(generateId()); // Output: 1
console.log(generateId()); // Output: 2
```

**Task 4: Create a closure that captures a user's name and returns a function that greets the user by name.**

```javascript
// Task 4: Closure capturing user's name and greeting
function createGreeter(name) {
    return function() {
        console.log(`Hello, ${name}!`);
    };
}

const greetJohn = createGreeter("John");
greetJohn(); // Output: Hello, John!
```

### Activity 3: Closures in Loops

**Task 5: Write a loop that creates an array of functions. Each function should log its index when called. Use a closure to ensure each function logs the correct index.**

```javascript
// Task 5: Closures in loops to log correct index
function createFunctionArray() {
    const functionArray = [];

    for (let i = 0; i < 5; i++) {
        functionArray.push(function() {
            console.log(i);
        });
    }

    return functionArray;
}

const functionArray = createFunctionArray();
functionArray[0](); // Output: 0
functionArray[1](); // Output: 1
```

### Activity 4: Module Pattern

**Task 6: Use closures to create a simple module for managing a collection of items. Implement methods to add, remove, and list items.**

```javascript
// Task 6: Module pattern using closures
const itemManager = (function() {
    const items = [];

    return {
        addItem: function(item) {
            items.push(item);
        },
        removeItem: function(item) {
            const index = items.indexOf(item);
            if (index > -1) {
                items.splice(index, 1);
            }
        },
        listItems: function() {
            return items.slice();
        }
    };
})();

itemManager.addItem("Item 1");
itemManager.addItem("Item 2");
console.log(itemManager.listItems()); // Output: ["Item 1", "Item 2"]
itemManager.removeItem("Item 1");
console.log(itemManager.listItems()); // Output: ["Item 2"]
```

### Activity 5: Memoization

**Task 7: Write a function that memoizes the results of another function. Use a closure to store the results of previous computations.**

```javascript
// Task 7: Memoization function
function memoize(fn) {
    const cache = {};

    return function(...args) {
        const key = JSON.stringify(args);
        if (cache[key]) {
            return cache[key];
        } else {
            const result = fn(...args);
            cache[key] = result;
            return result;
        }
    };
}

const add = (a, b) => a + b;
const memoizedAdd = memoize(add);
console.log(memoizedAdd(1, 2)); // Output: 3
console.log(memoizedAdd(1, 2)); // Output: 3 (from cache)
```

**Task 8: Create a memoized version of a function that calculates the factorial of a number.**

```javascript
// Task 8: Memoized factorial function
function memoizeFactorial(fn) {
    const cache = {};

    return function(n) {
        if (cache[n]) {
            return cache[n];
        } else {
            const result = fn(n);
            cache[n] = result;
            return result;
        }
    };
}

const factorial = (n) => {
    if (n === 0) {
        return 1;
    }
    return n * factorial(n - 1);
};

const memoizedFactorial = memoizeFactorial(factorial);
console.log(memoizedFactorial(5)); // Output: 120
console.log(memoizedFactorial(5)); // Output: 120 (from cache)
```

## Feature Request

### 1. Basic Closure Script

```javascript
// Basic Closure Script
function createGreeting(name) {
    const message = `Hello, ${name}!`;

    return function() {
        console.log(message);
    };
}

const greetAlice = createGreeting("Alice");
greetAlice(); // Output: Hello, Alice!
```

### 2. Counter Closure Script

```javascript
// Counter Closure Script
function createCounter() {
    let count = 0;

    return {
        increment: function() {
            count++;
        },
        getCount: function() {
            return count;
        }
    };
}

const counter = createCounter();
counter.increment();
counter.increment();
console.log(counter.getCount()); // Output: 2
```

### 3. Unique ID Generator Script

```javascript
// Unique ID Generator Script
function createIdGenerator() {
    let lastId = 0;

    return function() {
        lastId++;
        return lastId;
    };
}

const generateId = createIdGenerator();
console.log(generateId()); // Output: 1
console.log(generateId()); // Output: 2
```

### 4. Loop Closure Script

```javascript
// Loop Closure Script
function createFunctionArray() {
    const functionArray = [];

    for (let i = 0; i < 5; i++) {
        functionArray.push(function() {
            console.log(i);
        });
    }

    return functionArray;
}

const functionArray = createFunctionArray();
functionArray[0](); // Output: 0
functionArray[1](); // Output: 1
```

### 5. Memoization Script

```javascript
// Memoization Script
function memoize(fn) {
    const cache = {};

    return function(...args) {
        const key = JSON.stringify(args);
        if (cache[key]) {
            return cache[key];
        } else {
            const result = fn(...args);
            cache[key] = result;
            return result;
        }
    };
}

const factorial = (n) => {
    if (n === 0) {
        return 1;
    }
    return n * factorial(n - 1);
};

const memoizedFactorial = memoize(factorial);
console.log(memoizedFactorial(5)); // Output: 120
console.log(memoizedFactorial(5)); // Output: 120 (from cache)
```

## Achievement

By the end of these activities, students will:
- Understand and create closures in JavaScript.
- Use closures to maintain private state and create encapsulated modules.
- Apply closures in practical scenarios like generating unique IDs and memoization.
- Use closures in loops to capture and use variables correctly.

# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 5: Functions](#day-5-functions)
  - [Tasks/Activities](#tasksactivities)
    - [Activity 1: Function Declaration](#activity-1-function-declaration)
      - [Task 1: Write a function to check if a number is even or odd and log the result to the console.](#task-1-write-a-function-to-check-if-a-number-is-even-or-odd-and-log-the-result-to-the-console)
      - [Task 2: Write a function to calculate the square of a number and return the result.](#task-2-write-a-function-to-calculate-the-square-of-a-number-and-return-the-result)
    - [Activity 2: Function Expression](#activity-2-function-expression)
      - [Task 3: Write a function expression to find the maximum of two numbers and log the result to the console.](#task-3-write-a-function-expression-to-find-the-maximum-of-two-numbers-and-log-the-result-to-the-console)
      - [Task 4: Write a function expression to concatenate two strings and return the result.](#task-4-write-a-function-expression-to-concatenate-two-strings-and-return-the-result)
    - [Activity 3: Arrow Functions](#activity-3-arrow-functions)
      - [Task 5: Write an arrow function to calculate the sum of two numbers and return the result.](#task-5-write-an-arrow-function-to-calculate-the-sum-of-two-numbers-and-return-the-result)
      - [Task 6: Write an arrow function to check if a string contains a specific character and return a boolean value.](#task-6-write-an-arrow-function-to-check-if-a-string-contains-a-specific-character-and-return-a-boolean-value)
    - [Activity 4: Function Parameters and Default Values](#activity-4-function-parameters-and-default-values)
      - [Task 7: Write a function that takes two parameters and returns their product. Provide a default value for the second parameter.](#task-7-write-a-function-that-takes-two-parameters-and-returns-their-product-provide-a-default-value-for-the-second-parameter)
      - [Task 8: Write a function that takes a person's name and age and returns a greeting message. Provide a default value for the age.](#task-8-write-a-function-that-takes-a-persons-name-and-age-and-returns-a-greeting-message-provide-a-default-value-for-the-age)
    - [Activity 5: Higher-Order Functions](#activity-5-higher-order-functions)
      - [Task 9: Write a higher-order function that takes a function and a number, and calls the function that many times.](#task-9-write-a-higher-order-function-that-takes-a-function-and-a-number-and-calls-the-function-that-many-times)
      - [Task 10: Write a higher-order function that takes two functions and a value, applies the first function to the value, and then applies the second function to the result.](#task-10-write-a-higher-order-function-that-takes-two-functions-and-a-value-applies-the-first-function-to-the-value-and-then-applies-the-second-function-to-the-result)
  - [Feature Request](#feature-request)
    - [1. Even or Odd Function Script](#1-even-or-odd-function-script)
    - [2. Square Calculation Function Script](#2-square-calculation-function-script)
    - [3. Concatenation Function Script](#3-concatenation-function-script)
    - [4. Sum Calculation Arrow Function Script](#4-sum-calculation-arrow-function-script)
    - [5. Higher-Order Function Script](#5-higher-order-function-script)
  - [Achievement](#achievement)

# Day 5: Functions

## Tasks/Activities

### Activity 1: Function Declaration

#### Task 1: Write a function to check if a number is even or odd and log the result to the console.

```javascript
function checkEvenOdd(number) {
  if (number % 2 === 0) {
    console.log(`${number} is even.`);
  } else {
    console.log(`${number} is odd.`);
  }
}

// Example usage:
checkEvenOdd(4); // Output: 4 is even.
checkEvenOdd(7); // Output: 7 is odd.
```

**Explanation:** This function takes a number as input and checks if it is even or odd using the modulus operator `%`. If the remainder is 0, the number is even; otherwise, it is odd.

#### Task 2: Write a function to calculate the square of a number and return the result.

```javascript
function calculateSquare(number) {
  return number * number;
}

// Example usage:
console.log(calculateSquare(5)); // Output: 25
```

**Explanation:** This function takes a number as input and returns its square by multiplying the number by itself.

### Activity 2: Function Expression

#### Task 3: Write a function expression to find the maximum of two numbers and log the result to the console.

```javascript
const findMax = function(a, b) {
  const max = a > b ? a : b;
  console.log(`The maximum of ${a} and ${b} is ${max}.`);
};

// Example usage:
findMax(10, 20); // Output: The maximum of 10 and 20 is 20.
```

**Explanation:** This function expression takes two numbers as input and uses a ternary operator to determine the maximum of the two numbers, then logs the result to the console.

#### Task 4: Write a function expression to concatenate two strings and return the result.

```javascript
const concatenateStrings = function(str1, str2) {
  return str1 + str2;
};

// Example usage:
console.log(concatenateStrings('Hello, ', 'World!')); // Output: Hello, World!
```

**Explanation:** This function expression takes two strings as input and returns their concatenation using the `+` operator.

### Activity 3: Arrow Functions

#### Task 5: Write an arrow function to calculate the sum of two numbers and return the result.

```javascript
const calculateSum = (a, b) => a + b;

// Example usage:
console.log(calculateSum(5, 7)); // Output: 12
```

**Explanation:** This arrow function takes two numbers as input and returns their sum using the `+` operator.

#### Task 6: Write an arrow function to check if a string contains a specific character and return a boolean value.

```javascript
const containsCharacter = (str, char) => str.includes(char);

// Example usage:
console.log(containsCharacter('Hello', 'e')); // Output: true
console.log(containsCharacter('World', 'a')); // Output: false
```

**Explanation:** This arrow function takes a string and a character as input and returns `true` if the string contains the character, otherwise `false`. It uses the `includes` method of the string.

### Activity 4: Function Parameters and Default Values

#### Task 7: Write a function that takes two parameters and returns their product. Provide a default value for the second parameter.

```javascript
function multiply(a, b = 1) {
  return a * b;
}

// Example usage:
console.log(multiply(5, 3)); // Output: 15
console.log(multiply(5));    // Output: 5
```

**Explanation:** This function takes two parameters and returns their product. The second parameter has a default value of 1, so if it is not provided, the function will still return a valid result.

#### Task 8: Write a function that takes a person's name and age and returns a greeting message. Provide a default value for the age.

```javascript
function greet(name, age = 'unknown') {
  return `Hello, my name is ${name} and I am ${age} years old.`;
}

// Example usage:
console.log(greet('Alice', 30)); // Output: Hello, my name is Alice and I am 30 years old.
console.log(greet('Bob'));       // Output: Hello, my name is Bob and I am unknown years old.
```

**Explanation:** This function takes a person's name and age and returns a greeting message. The age parameter has a default value of 'unknown'.

### Activity 5: Higher-Order Functions

#### Task 9: Write a higher-order function that takes a function and a number, and calls the function that many times.

```javascript
function repeatFunction(fn, times) {
  for (let i = 0; i < times; i++) {
    fn();
  }
}

// Example usage:
repeatFunction(() => console.log('Hello!'), 3);
// Output:
// Hello!
// Hello!
// Hello!
```

**Explanation:** This higher-order function takes another function `fn` and a number `times`, and calls `fn` the specified number of times using a `for` loop.

#### Task 10: Write a higher-order function that takes two functions and a value, applies the first function to the value, and then applies the second function to the result.

```javascript
function applyFunctions(fn1, fn2, value) {
  return fn2(fn1(value));
}

// Example usage:
const double = x => x * 2;
const square = x => x * x;

console.log(applyFunctions(double, square, 5)); // Output: 100
```

**Explanation:** This higher-order function takes two functions `fn1` and `fn2`, and a value. It applies `fn1` to the value, then applies `fn2` to the result, and returns the final result.

## Feature Request

### 1. Even or Odd Function Script

```javascript
function checkEvenOdd(number) {
  if (number % 2 === 0) {
    console.log(`${number} is even.`);
  } else {
    console.log(`${number} is odd.`);
  }
}

// Example usage:
checkEvenOdd(4); // Output: 4 is even.
checkEvenOdd(7); // Output: 7 is odd.
```

### 2. Square Calculation Function Script

```javascript
function calculateSquare(number) {
  return number * number;
}

// Example usage:
console.log(calculateSquare(5)); // Output: 25
```

### 3. Concatenation Function Script

```javascript
const concatenateStrings = function(str1, str2) {
  return str1 + str2;
};

// Example usage:
console.log(concatenateStrings('Hello, ', 'World!')); // Output: Hello, World!
```

### 4. Sum Calculation Arrow Function Script

```javascript
const calculateSum = (a, b) => a + b;

// Example usage:
console.log(calculateSum(5, 7)); // Output: 12
```

### 5. Higher-Order Function Script

```javascript
function repeatFunction(fn, times) {
  for (let i = 0; i < times; i++) {
    fn();
  }
}

// Example usage:
repeatFunction(() => console.log('Hello!'), 3);
// Output:
// Hello!
// Hello!
// Hello!
```

## Achievement

By the end of these activities, students will:

- Understand and define functions using function declarations, expressions, and arrow functions.
- Use function parameters and default values effectively.
- Create and utilize higher-order functions.
- Apply functions to solve common problems and perform calculations.
- Enhance code reusability and organization using functions.

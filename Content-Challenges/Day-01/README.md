# Table Of Content

- [Table Of Content](#table-of-content)
- [JavaScript Basics](#javascript-basics)
  - [Day 1: Variables and Data Types](#day-1-variables-and-data-types)
    - [Tasks/Activities](#tasksactivities)
      - [Activity 1: Variable Declaration](#activity-1-variable-declaration)
      - [Activity 2: Constant Declaration](#activity-2-constant-declaration)
      - [Activity 3: Data Types](#activity-3-data-types)
      - [Activity 4: Reassigning Variables](#activity-4-reassigning-variables)
      - [Activity 5: Understanding `const`](#activity-5-understanding-const)
    - [Feature Requests](#feature-requests)
    - [Achievement](#achievement)

# JavaScript Basics

## Day 1: Variables and Data Types

### Tasks/Activities

#### Activity 1: Variable Declaration

**Task 1: Declare a variable using `var`, assign it a number, and log the value to the console.**

```javascript
var numberVar = 42;
console.log(numberVar); // Output: 42
```

**Explanation:**

- `var` is used to declare a variable.
- `numberVar` is assigned the value `42`.
- `console.log(numberVar)` prints the value of `numberVar` to the console.

**Task 2: Declare a variable using `let`, assign it a string, and log the value to the console.**

```javascript
let stringLet = "Hello, World!";
console.log(stringLet); // Output: Hello, World!
```

**Explanation:**

- `let` is used to declare a block-scoped variable.
- `stringLet` is assigned the value `"Hello, World!"`.
- `console.log(stringLet)` prints the value of `stringLet` to the console.

#### Activity 2: Constant Declaration

**Task 3: Declare a variable using `const`, assign it a boolean value, and log the value to the console.**

```javascript
const booleanConst = true;
console.log(booleanConst); // Output: true
```

**Explanation:**

- `const` is used to declare a constant variable that cannot be reassigned.
- `booleanConst` is assigned the value `true`.
- `console.log(booleanConst)` prints the value of `booleanConst` to the console.

#### Activity 3: Data Types

**Task 4: Create variables of different data types (number, string, boolean, object, array) and log each variable's type using the `typeof` operator.**

```javascript
let numberVar = 42;
let stringVar = "Hello, World!";
let booleanVar = true;
let objectVar = { name: "John", age: 30 };
let arrayVar = [1, 2, 3, 4, 5];

console.log(typeof numberVar); // Output: number
console.log(typeof stringVar); // Output: string
console.log(typeof booleanVar); // Output: boolean
console.log(typeof objectVar); // Output: object
console.log(typeof arrayVar); // Output: object
```

**Explanation:**

- Variables of different data types are declared.
- `typeof` operator is used to determine the data type of each variable.
- The data type of each variable is logged to the console.

#### Activity 4: Reassigning Variables

**Task 5: Declare a variable using `let`, assign it an initial value, reassign a new value, and log both values to the console.**

```javascript
let reassignVar = "Initial Value";
console.log(reassignVar); // Output: Initial Value

reassignVar = "New Value";
console.log(reassignVar); // Output: New Value
```

**Explanation:**

- `let` is used to declare a variable `reassignVar` with an initial value `"Initial Value"`.
- The initial value is logged to the console.
- The variable is reassigned a new value `"New Value"`.
- The new value is logged to the console.

#### Activity 5: Understanding `const`

**Task 6: Try reassigning a variable declared with `const` and observe the error.**

```javascript
const constantVar = "Initial Value";
console.log(constantVar); // Output: Initial Value

// Uncommenting the following line will cause an error
// constantVar = "New Value"; // TypeError: Assignment to constant variable.
```

**Explanation:**

- `const` is used to declare a constant variable `constantVar` with an initial value `"Initial Value"`.
- The initial value is logged to the console.
- Attempting to reassign `constantVar` will result in a `TypeError` because `const` variables cannot be reassigned.

### Feature Requests

**1. Variable Types Console Log: Write a script that declares variables of different data types and logs both the value and type of each variable to the console.**

```javascript
let numberVar = 42;
let stringVar = "Hello, World!";
let booleanVar = true;
let objectVar = { name: "John", age: 30 };
let arrayVar = [1, 2, 3, 4, 5];

console.log(`Value: ${numberVar}, Type: ${typeof numberVar}`); // Output: Value: 42, Type: number
console.log(`Value: ${stringVar}, Type: ${typeof stringVar}`); // Output: Value: Hello, World!, Type: string
console.log(`Value: ${booleanVar}, Type: ${typeof booleanVar}`); // Output: Value: true, Type: boolean
console.log(`Value: ${objectVar}, Type: ${typeof objectVar}`); // Output: Value: [object Object], Type: object
console.log(`Value: ${arrayVar}, Type: ${typeof arrayVar}`); // Output: Value: 1,2,3,4,5, Type: object
```

**Explanation:**

- Variables of different data types are declared.
- Both the value and type of each variable are logged to the console using template literals.

**2. Reassignment Demo: Create a script that demonstrates the difference in behavior between `let` and `const` when it comes to reassignment.**

```javascript
let reassignLet = "Initial Value";
console.log(reassignLet); // Output: Initial Value

reassignLet = "New Value";
console.log(reassignLet); // Output: New Value

const reassignConst = "Initial Value";
console.log(reassignConst); // Output: Initial Value

// Uncommenting the following line will cause an error
// reassignConst = "New Value"; // TypeError: Assignment to constant variable.
```

**Explanation:**

- `let` is used to declare a variable `reassignLet` which can be reassigned.
- The initial and new values of `reassignLet` are logged to the console.
- `const` is used to declare a constant variable `reassignConst` which cannot be reassigned.
- Attempting to reassign `reassignConst` will result in a `TypeError`.

### Achievement

By the end of these activities, you will:

- Know how to declare variables using `var`, `let`, and `const`.
- Understand the different data types in JavaScript.
- Be able to use the `typeof` operator to identify the data type of a variable.
- Understand the concept of variable reassignment and the immutability of `const` variables.

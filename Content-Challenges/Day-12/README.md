# Table of Content

- [Table of Content](#table-of-content)
  - [Day 12: Error Handling](#day-12-error-handling)
    - [Activity 1: Basic Error Handling with Try-Catch](#activity-1-basic-error-handling-with-try-catch)
    - [Activity 2: Finally Block](#activity-2-finally-block)
    - [Activity 3: Custom Error Objects](#activity-3-custom-error-objects)
    - [Activity 4: Error Handling in Promises](#activity-4-error-handling-in-promises)
    - [Activity 5: Graceful Error Handling in Fetch](#activity-5-graceful-error-handling-in-fetch)
    - [Feature Request](#feature-request)

## Day 12: Error Handling

### Activity 1: Basic Error Handling with Try-Catch

**Task 1: Write a function that intentionally throws an error and use a try-catch block to handle the error and log an appropriate message to the console.**

```javascript
function throwError() {
  throw new Error("Intentional error");
}

try {
  throwError();
} catch (error) {
  console.error("Error caught:", error.message);
}
```

**Explanation:**

- We define a function `throwError` that explicitly throws an error.
- The `try` block attempts to execute the code within it.
- If an error occurs, it's caught by the `catch` block.
- The error object is accessible within the `catch` block, and its message is logged to the console.

**Task 2: Create a function that divides two numbers and throws an error if the denominator is zero. Use a try-catch block to handle this error.**

```javascript
function divide(numerator, denominator) {
  if (denominator === 0) {
    throw new Error("Division by zero");
  }
  return numerator / denominator;
}

try {
  const result = divide(10, 0);
  console.log(result);
} catch (error) {
  console.error("Error:", error.message);
}
```

**Explanation:**

- The `divide` function checks if the denominator is zero and throws an error if it is.
- The `try` block attempts to call the `divide` function.
- If an error occurs, the `catch` block handles it and logs the error message.

### Activity 2: Finally Block

**Task 3: Write a script that includes a try-catch block and a finally block. Log messages in the try, catch, and finally blocks to observe the execution flow.**

```javascript
try {
  console.log("Inside try block");
  // Some code that might throw an error
} catch (error) {
  console.error("Error caught:", error.message);
} finally {
  console.log("Finally block always executes");
}
```

**Explanation:**

- The `try` block contains code that might throw an error.
- The `catch` block handles any errors that occur in the `try` block.
- The `finally` block always executes, regardless of whether an error occurs or not.

### Activity 3: Custom Error Objects

**Task 4: Create a custom error class that extends the built-in Error class. Throw an instance of this custom error in a function and handle it using a try-catch block.**

```javascript
class CustomError extends Error {
  constructor(message) {
    super(message);
    this.name = "CustomError";
  }
}

function throwCustomError() {
  throw new CustomError("This is a custom error");
}

try {
  throwCustomError();
} catch (error) {
  if (error instanceof CustomError) {
    console.error("Custom error caught:", error.message);
  } else {
    console.error("Unexpected error:", error);
  }
}
```

**Explanation:**

- We create a custom error class `CustomError` that extends the built-in `Error` class.
- We define a function `throwCustomError` that throws an instance of the custom error.
- The `try` block attempts to call `throwCustomError`.
- The `catch` block checks if the error is an instance of `CustomError` and handles it accordingly.

**Task 5: Write a function that validates user input (e.g., checking if a string is not empty) and throws a custom error if the validation fails. Handle the custom error using a try-catch block.**

```javascript
function validateInput(input) {
  if (input === "") {
    throw new InputValidationError("Input cannot be empty");
  }
  return true;
}

try {
  validateInput("");
} catch (error) {
  console.error("Input validation error:", error.message);
}
```

**Explanation:**

- We create a custom error class `InputValidationError`.
- The `validateInput` function checks if the input is empty and throws a `InputValidationError` if it is.
- The `try` block attempts to call `validateInput`.
- The `catch` block handles the `InputValidationError` and logs an appropriate message.

### Activity 4: Error Handling in Promises

**Task 6: Create a promise that randomly resolves or rejects. Use catch() to handle the rejection and log an appropriate message to the console.**

```javascript
function randomPromise() {
  return new Promise((resolve, reject) => {
    const randomValue = Math.random();
    if (randomValue < 0.5) {
      resolve("Promise resolved");
    } else {
      reject("Promise rejected");
    }
  });
}

randomPromise()
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
```

**Explanation:**

- The `randomPromise` function creates a Promise that randomly resolves or rejects.
- We use `.then()` to handle the resolved value and `.catch()` to handle the rejected value.

**Task 7: Use try-catch within an async function to handle errors from a promise that randomly resolves or rejects, and log the error message.**

```javascript
async function handlePromiseError() {
  try {
    const result = await randomPromise();
    console.log(result);
  } catch (error) {
    console.error("Error:", error);
  }
}

handlePromiseError();
```

**Explanation:**

- The `handlePromiseError` function is an async function that uses `await` to wait for the Promise to resolve.
- We use a `try-catch` block to handle potential errors from the Promise.

### Activity 5: Graceful Error Handling in Fetch

**Task 8: Use the fetch API to request data from an invalid URL and handle the error using catch(). Log an appropriate error message to the console.**

```javascript
fetch("https://invalid-api.com")
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((error) => console.error("Fetch error:", error));
```

**Explanation:**

- We use the `fetch` API to make a request to an invalid URL.
- The `.catch()` block handles the network error.

**Task 9: Use the fetch API to request data from an invalid URL within an async function and handle the error using try-catch. Log an appropriate error message.**

```javascript
async function fetchWithErrorHandling() {
  try {
    const response = await fetch("https://invalid-api.com");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Fetch error:", error);
  }
}

fetchWithErrorHandling();
```

**Explanation:**

- We use an async function to handle the fetch request.
- A `try-catch` block is used to catch potential errors from the fetch.

### Feature Request

**1. Basic Error Handling Script:** (See Activity 1)
**2. Custom Error Script:** (See Activity 3)
**3. Promise Error Handling Script:** (See Activity 4)
**4. Fetch Error Handling Script:** (See Activity 5)

**Remember to replace `https://invalid-api.com` with an actual invalid URL.**

I hope this comprehensive response is helpful!

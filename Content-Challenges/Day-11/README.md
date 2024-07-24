# Table of Contect

- [Table of Contect](#table-of-contect)
  - [Day 11: Promises and Async/Await](#day-11-promises-and-asyncawait)
    - [Activity 1: Understanding Promises](#activity-1-understanding-promises)
    - [Activity 2: Chaining Promises](#activity-2-chaining-promises)
    - [Activity 3: Using Async/Await](#activity-3-using-asyncawait)
    - [Activity 4: Fetching Data from an API](#activity-4-fetching-data-from-an-api)
    - [Activity 5: Concurrent Promises](#activity-5-concurrent-promises)
    - [Feature Request](#feature-request)

## Day 11: Promises and Async/Await

### Activity 1: Understanding Promises

**Task 1: Create a promise that resolves with a message after a 2-second timeout and log the message to the console.**

```javascript
function resolvePromise() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Promise resolved!");
    }, 2000);
  });
}

resolvePromise().then((message) => {
  console.log(message);
});
```

**Explanation:**

- We define a function `resolvePromise` that returns a new Promise.
- The Promise takes a resolver function as an argument.
- Inside the resolver, we use `setTimeout` to simulate a 2-second delay.
- After the delay, we call `resolve` with the message 'Promise resolved!'.
- We chain a `.then()` method to the Promise to handle the resolved value.

**Task 2: Create a promise that rejects with an error message after a 2-second timeout and handle the error using .catch().**

```javascript
function rejectPromise() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      reject("Promise rejected!");
    }, 2000);
  });
}

rejectPromise()
  .then((message) => {
    console.log(message); // This will not be executed
  })
  .catch((error) => {
    console.error(error);
  });
```

**Explanation:**

- We define a function `rejectPromise` that returns a new Promise.
- The Promise takes a resolver and a rejector function as arguments.
- Inside the resolver, we use `setTimeout` to simulate a 2-second delay.
- After the delay, we call `reject` with the error message 'Promise rejected!'.
- We chain a `.catch()` method to the Promise to handle the rejected error.

### Activity 2: Chaining Promises

**Task 3: Create a sequence of promises that simulate fetching data from a server. Chain the promises to log messages in a specific order.**

```javascript
function fetchData1() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Data from server 1");
    }, 1000);
  });
}

function fetchData2(data1) {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(`Data from server 2: ${data1}`);
    }, 1500);
  });
}

fetchData1()
  .then((data1) => fetchData2(data1))
  .then((data2) => console.log(data2));
```

**Explanation:**

- We define two functions `fetchData1` and `fetchData2` that return Promises.
- The first Promise resolves with 'Data from server 1' after 1 second.
- The second Promise takes the data from the first Promise as an argument and resolves with a concatenated message after 1.5 seconds.
- We chain the Promises using `.then()` to log the final message.

### Activity 3: Using Async/Await

**Task 4: Write an async function that waits for a promise to resolve and then logs the resolved value.**

```javascript
const resolvePromise = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve('Promise Resolved')
    }, 2000);
  })
}

async function resolveAsync() {
  const result = await resolvePromise();
  console.log("Result: ", result);
}

resolveAsync();
```

**Explanation:**

- We defined a function `resolvePromise` for which the async await will wait for 2 seconds to execute.
- We define an async function `resolveAsync`.
- Inside the function, we use `await` to wait for the `resolvePromise` function to resolve.
- Once resolved, we log the result to the console.

**Task 5: Write an async function that handles a rejected promise using try-catch and logs the error message.**

```javascript
const rejectPromise = () => {
  return new Promise((reject) => {
    reject("error occured")
  })
}

async function handleError() {
  try {
    const result = await rejectPromise();
    console.log(result); // This will not be executed
  } catch (error) {
    console.error(error);
  }
}

handleError();
```

**Explanation:**

- We define a function `rejectPromise` which will reject the promise.
- We define an async function `handleError`.
- We use a `try-catch` block to handle potential errors.
- We await the `rejectPromise` function.
- If the Promise is rejected, the error is caught and logged to the console.

### Activity 4: Fetching Data from an API

**Task 6: Use the fetch API to get data from a public API and log the response data to the console using promises.**

```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1/comments")
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((error) => console.error(error));
```

**Explanation:**

- We use the `fetch` API to make a request to the specified URL.
- We chain `.then()` methods to handle the response.
- The first `.then()` converts the response to JSON.
- The second `.then()` logs the parsed data to the console.
- We use `.catch()` to handle potential errors.

**Task 7: Use the fetch API to get data from a public API and log the response data to the console using async/await.**

```javascript
async function fetchDataFromApi() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts/1/comments");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

fetchDataFromApi();
```

**Explanation:**

- We define an async function `fetchDataFromApi`.
- We use `await` to wait for the fetch request to complete.
- We convert the response to JSON using `await response.json()`.
- We log the parsed data to the console.
- We use a `try-catch` block to handle potential errors.

### Activity 5: Concurrent Promises

**Task 8: Use Promise.all to wait for multiple promises to resolve and then log all their values.**

```javascript

function fetchData1() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve('Data from server 1');
    }, 1000);
  });
}

function fetchData2(string) {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(`Data from server 2: ${string}`);
    }, 1500);
  });
}
 
Promise.all([fetchData1(), fetchData2("data1test")])
  .then((results) => console.log(results))
  .catch((error) => console.error(error));
```

**Explanation:**

- We create an array of Promises using `fetchData1()` and `fetchData2()`.
- We use `Promise.all` to wait for both Promises to resolve.
- The resolved values are passed to the `.then()` method as an array.

**Task 9: Use Promise.race to log the value of the first promise that resolves among multiple promises.**

```javascript
Promise.race([fetchData1(), fetchData2()])
  .then((result) => console.log(result))
  .catch((error) => console.error(error));
```

**Explanation:**

- We create an array of Promises using `fetchData1()` and `fetchData2()`.
- We use `Promise.race` to return the value of the first Promise that resolves.

### Feature Request

**1. Promise Creation Script:** (See Task 1 and Task 2)
**2. Promise Chaining Script:** (See Task 3)
**3. Async/Await Script:** (See Task 4 and Task 5)
**4. API Fetch Script:** (See Task 6 and Task 7)
**5. Concurrent Promises Script:** (See Task 8 and Task 9)

Remember to replace `https://api.example.com/data` with the actual URL of the API you want to use.

**Note:** To run these examples, you'll need a web server or a development environment to handle the fetch requests. You can also use mock data instead of fetching from an actual API for testing purposes.

**I hope this comprehensive response is helpful!**

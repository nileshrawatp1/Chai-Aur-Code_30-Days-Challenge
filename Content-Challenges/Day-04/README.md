# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 4: Loops](#day-4-loops)
  - [Activity 1: For Loop](#activity-1-for-loop)
    - [Task 1: Print numbers from 1 to 10](#task-1-print-numbers-from-1-to-10)
    - [Task 2: Print even numbers from 1 to 20](#task-2-print-even-numbers-from-1-to-20)
  - [Activity 2: While Loop](#activity-2-while-loop)
    - [Task 3: Print numbers from 10 to 1](#task-3-print-numbers-from-10-to-1)
    - [Task 4: Print odd numbers from 1 to 15](#task-4-print-odd-numbers-from-1-to-15)
  - [Activity 3: Do-While Loop](#activity-3-do-while-loop)
    - [Task 5: Print numbers from 1 to 5](#task-5-print-numbers-from-1-to-5)
    - [Task 6: Print multiples of 3 up to 30](#task-6-print-multiples-of-3-up-to-30)
  - [Activity 4: Nested Loops](#activity-4-nested-loops)
    - [Task 7: Print a 5x5 matrix of asterisks](#task-7-print-a-5x5-matrix-of-asterisks)
    - [Task 8: Print a right-angled triangle of asterisks](#task-8-print-a-right-angled-triangle-of-asterisks)
  - [Achievement](#achievement)

# Day 4: Loops

## Activity 1: For Loop

### Task 1: Print numbers from 1 to 10
```javascript
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```
**Explanation**: This for loop initializes `i` to 1, checks if `i` is less than or equal to 10, and increments `i` by 1 after each iteration. It prints the numbers from 1 to 10.

### Task 2: Print even numbers from 1 to 20
```javascript
for (let i = 1; i <= 20; i++) {
  if (i % 2 === 0) {
    console.log(i);
  }
}
```
**Explanation**: This for loop iterates from 1 to 20. Inside the loop, it checks if the number is even using the modulus operator (`%`). If the number is even, it prints the number.

## Activity 2: While Loop

### Task 3: Print numbers from 10 to 1
```javascript
let i = 10;
while (i >= 1) {
  console.log(i);
  i--;
}
```
**Explanation**: This while loop initializes `i` to 10 and continues to loop as long as `i` is greater than or equal to 1. It decrements `i` by 1 after each iteration and prints the numbers from 10 to 1.

### Task 4: Print odd numbers from 1 to 15
```javascript
let i = 1;
while (i <= 15) {
  if (i % 2 !== 0) {
    console.log(i);
  }
  i++;
}
```
**Explanation**: This while loop initializes `i` to 1 and continues to loop as long as `i` is less than or equal to 15. Inside the loop, it checks if the number is odd using the modulus operator (`%`). If the number is odd, it prints the number. It increments `i` by 1 after each iteration.

## Activity 3: Do-While Loop

### Task 5: Print numbers from 1 to 5
```javascript
let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);
```
**Explanation**: This do-while loop initializes `i` to 1 and prints the number. It then increments `i` by 1 and checks if `i` is less than or equal to 5. The loop continues until `i` is greater than 5.

### Task 6: Print multiples of 3 up to 30
```javascript
let i = 3;
do {
  console.log(i);
  i += 3;
} while (i <= 30);
```
**Explanation**: This do-while loop initializes `i` to 3 and prints the number. It then increments `i` by 3 and checks if `i` is less than or equal to 30. The loop continues until `i` is greater than 30.

## Activity 4: Nested Loops

### Task 7: Print a 5x5 matrix of asterisks
```javascript
for (let i = 0; i < 5; i++)
  let row = '';
  for (let j = 0; j < 5; j++) {
    row += '* ';
  }
  console.log(row);
}
```
**Explanation**: This nested for loop prints a 5x5 matrix of asterisks. The outer loop runs 5 times for each row, and the inner loop runs 5 times for each column, appending an asterisk to the `row` string. After the inner loop completes, it prints the `row`.

### Task 8: Print a right-angled triangle of asterisks
```javascript
for (let i = 1; i <= 5; i++) {
  let row = '';
  for (let j = 0; j < i; j++) {
    row += '* ';
  }
  console.log(row);
}
```
**Explanation**: This nested for loop prints a right-angled triangle of asterisks. The outer loop runs from 1 to 5, representing the number of rows. The inner loop runs from 0 to `i`, appending an asterisk to the `row` string. After the inner loop completes, it prints the `row`.

## Achievement
By the end of these activities, students will:
- Implement and understand basic for loops.
- Use while loops to handle conditions.
- Utilize do-while loops for at least one iteration.
- Apply nested loops to solve more complex problems.

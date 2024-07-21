# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 3: Control Structures](#day-3-control-structures)
  - [Activity 1: If-Else Statements](#activity-1-if-else-statements)
    - [Task 1: Check if a number is positive, negative, or zero](#task-1-check-if-a-number-is-positive-negative-or-zero)
    - [Task 2: Check if a person is eligible to vote](#task-2-check-if-a-person-is-eligible-to-vote)
  - [Activity 2: Nested If-Else Statements](#activity-2-nested-if-else-statements)
    - [Task 3: Find the largest of three numbers](#task-3-find-the-largest-of-three-numbers)
  - [Activity 3: Switch Case](#activity-3-switch-case)
    - [Task 4: Determine the day of the week based on a number](#task-4-determine-the-day-of-the-week-based-on-a-number)
    - [Task 5: Assign a grade based on a score](#task-5-assign-a-grade-based-on-a-score)
  - [Activity 4: Conditional (Ternary) Operator](#activity-4-conditional-ternary-operator)
    - [Task 6: Check if a number is even or odd](#task-6-check-if-a-number-is-even-or-odd)
  - [Activity 5: Combining Conditions](#activity-5-combining-conditions)
    - [Task 7: Check if a year is a leap year](#task-7-check-if-a-year-is-a-leap-year)
  - [Feature Request](#feature-request)
    - [1. Number Check Script](#1-number-check-script)
    - [2. Voting Eligibility Script](#2-voting-eligibility-script)
    - [3. Day of the Week Script](#3-day-of-the-week-script)
    - [4. Grade Assignment Script](#4-grade-assignment-script)
    - [5. Leap Year Check Script](#5-leap-year-check-script)
  - [Achievement](#achievement)

# Day 3: Control Structures

## Activity 1: If-Else Statements

### Task 1: Check if a number is positive, negative, or zero
```javascript
function checkNumber(num) {
  if (num > 0) {
    console.log("The number is positive.");
  } else if (num < 0) {
    console.log("The number is negative.");
  } else {
    console.log("The number is zero.");
  }
}

// Example usage:
checkNumber(5);  // Output: The number is positive.
checkNumber(-3); // Output: The number is negative.
checkNumber(0);  // Output: The number is zero.
```
**Explanation**: This function takes a number as input and uses if-else statements to determine if the number is positive, negative, or zero, then logs the result to the console.

### Task 2: Check if a person is eligible to vote
```javascript
function checkVotingEligibility(age) {
  if (age >= 18) {
    console.log("The person is eligible to vote.");
  } else {
    console.log("The person is not eligible to vote.");
  }
}

// Example usage:
checkVotingEligibility(20); // Output: The person is eligible to vote.
checkVotingEligibility(16); // Output: The person is not eligible to vote.
```
**Explanation**: This function checks if a person is eligible to vote based on their age. If the age is 18 or more, it logs that the person is eligible; otherwise, it logs that they are not eligible.

## Activity 2: Nested If-Else Statements

### Task 3: Find the largest of three numbers
```javascript
function findLargest(a, b, c) {
  if (a >= b && a >= c) {
    console.log(`${a} is the largest number.`);
  } else if (b >= a && b >= c) {
    console.log(`${b} is the largest number.`);
  } else {
    console.log(`${c} is the largest number.`);
  }
}

// Example usage:
findLargest(5, 10, 3); // Output: 10 is the largest number.
findLargest(7, 7, 2);  // Output: 7 is the largest number.
```
**Explanation**: This function uses nested if-else statements to compare three numbers and determine the largest one, then logs the result.

## Activity 3: Switch Case

### Task 4: Determine the day of the week based on a number
```javascript
function getDayOfWeek(dayNumber) {
  switch (dayNumber) {
    case 1:
      console.log("Sunday");
      break;
    case 2:
      console.log("Monday");
      break;
    case 3:
      console.log("Tuesday");
      break;
    case 4:
      console.log("Wednesday");
      break;
    case 5:
      console.log("Thursday");
      break;
    case 6:
      console.log("Friday");
      break;
    case 7:
      console.log("Saturday");
      break;
    default:
      console.log("Invalid day number.");
  }
}

// Example usage:
getDayOfWeek(1); // Output: Sunday
getDayOfWeek(5); // Output: Thursday
getDayOfWeek(8); // Output: Invalid day number.
```
**Explanation**: This function uses a switch case to determine the day of the week based on a number (1-7) and logs the corresponding day name. If the number is not between 1 and 7, it logs "Invalid day number."

### Task 5: Assign a grade based on a score
```javascript
function assignGrade(score) {
  switch (true) {
    case (score >= 90):
      console.log("Grade: A");
      break;
    case (score >= 80):
      console.log("Grade: B");
      break;
    case (score >= 70):
      console.log("Grade: C");
      break;
    case (score >= 60):
      console.log("Grade: D");
      break;
    default:
      console.log("Grade: F");
  }
}

// Example usage:
assignGrade(95); // Output: Grade: A
assignGrade(82); // Output: Grade: B
assignGrade(58); // Output: Grade: F
```
**Explanation**: This function uses a switch case to assign a grade based on a score. The switch case checks ranges of scores and logs the corresponding grade.

## Activity 4: Conditional (Ternary) Operator

### Task 6: Check if a number is even or odd
```javascript
function checkEvenOdd(num) {
  const result = (num % 2 === 0) ? "The number is even." : "The number is odd.";
  console.log(result);
}

// Example usage:
checkEvenOdd(4); // Output: The number is even.
checkEvenOdd(7); // Output: The number is odd.
```
**Explanation**: This function uses the ternary operator to check if a number is even or odd and logs the result.

## Activity 5: Combining Conditions

### Task 7: Check if a year is a leap year
```javascript
function isLeapYear(year) {
  if ((year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0)) {
    console.log(`${year} is a leap year.`);
  } else {
    console.log(`${year} is not a leap year.`);
  }
}

// Example usage:
isLeapYear(2020); // Output: 2020 is a leap year.
isLeapYear(1900); // Output: 1900 is not a leap year.
isLeapYear(2000); // Output: 2000 is a leap year.
```
**Explanation**: This function checks if a year is a leap year using multiple conditions: a year is a leap year if it is divisible by 4 but not by 100, unless it is also divisible by 400. It then logs the result.

## Feature Request

### 1. Number Check Script
```javascript
function checkNumber(num) {
  if (num > 0) {
    console.log("The number is positive.");
  } else if (num < 0) {
    console.log("The number is negative.");
  } else {
    console.log("The number is zero.");
  }
}

// Example usage:
checkNumber(5);  // Output: The number is positive.
checkNumber(-3); // Output: The number is negative.
checkNumber(0);  // Output: The number is zero.
```

### 2. Voting Eligibility Script
```javascript
function checkVotingEligibility(age) {
  if (age >= 18) {
    console.log("The person is eligible to vote.");
  } else {
    console.log("The person is not eligible to vote.");
  }
}

// Example usage:
checkVotingEligibility(20); // Output: The person is eligible to vote.
checkVotingEligibility(16); // Output: The person is not eligible to vote.
```

### 3. Day of the Week Script
```javascript
function getDayOfWeek(dayNumber) {
  switch (dayNumber) {
    case 1:
      console.log("Sunday");
      break;
    case 2:
      console.log("Monday");
      break;
    case 3:
      console.log("Tuesday");
      break;
    case 4:
      console.log("Wednesday");
      break;
    case 5:
      console.log("Thursday");
      break;
    case 6:
      console.log("Friday");
      break;
    case 7:
      console.log("Saturday");
      break;
    default:
      console.log("Invalid day number.");
  }
}

// Example usage:
getDayOfWeek(1); // Output: Sunday
getDayOfWeek(5); // Output: Thursday
getDayOfWeek(8); // Output: Invalid day number.
```

### 4. Grade Assignment Script
```javascript
function assignGrade(score) {
  switch (true) {
    case (score >= 90):
      console.log("Grade: A");
      break;
    case (score >= 80):
      console.log("Grade: B");
      break;
    case (score >= 70):
      console.log("Grade: C");
      break;
    case (score >= 60):
      console.log("Grade: D");
      break;
    default:
      console.log("Grade: F");
  }
}

// Example usage:
assignGrade(95); // Output: Grade: A
assignGrade(82); // Output: Grade: B
assignGrade(58); // Output: Grade: F
```

### 5. Leap Year Check Script
```javascript
function isLeapYear(year) {
  if ((year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0)) {
    console.log(`${year} is a leap year.`);
  } else {
    console.log(`${year} is not a leap year.`);
  }
}

// Example usage:
isLeapYear(2020); // Output: 2020 is a leap year.
isLeapYear(1900); // Output: 1900 is not a leap year.
isLeapYear(2000); // Output: 2000 is a leap year.
```

## Achievement
By the end of these activities, students will:
- Implement and understand basic if-else control flow.
- Use nested if-else statements to handle multiple conditions.
- Utilize switch cases for control flow based on specific values.
- Apply the ternary operator for concise condition checking.
- Combine multiple conditions to solve more complex problems.

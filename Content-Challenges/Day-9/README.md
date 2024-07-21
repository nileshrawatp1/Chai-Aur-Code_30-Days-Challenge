# Table Of Content

- [Table Of Content](#table-of-content)
- [Day 9: DOM Manipulation](#day-9-dom-manipulation)
  - [Task 1: Create a new div element with some text content and append it to the body](#task-1-create-a-new-div-element-with-some-text-content-and-append-it-to-the-body)
    - [Explanation](#explanation)
    - [Code](#code)
  - [Task 2: Create a new li element and add it to an existing ul list](#task-2-create-a-new-li-element-and-add-it-to-an-existing-ul-list)
    - [Explanation](#explanation-1)
    - [Code](#code-1)
  - [Task 3: Select an HTML element and remove it from the DOM](#task-3-select-an-html-element-and-remove-it-from-the-dom)
    - [Explanation](#explanation-2)
    - [Code](#code-2)
  - [Task 4: Remove the last child of a specific HTML element](#task-4-remove-the-last-child-of-a-specific-html-element)
    - [Explanation](#explanation-3)
    - [Code](#code-3)
  - [Task 5: Select an HTML element and change one of its attributes](#task-5-select-an-html-element-and-change-one-of-its-attributes)
    - [Explanation](#explanation-4)
    - [Code](#code-4)
  - [Task 6: Add and remove a CSS class to/from an HTML element](#task-6-add-and-remove-a-css-class-tofrom-an-html-element)
    - [Explanation](#explanation-5)
    - [Code](#code-5)
  - [Task 7: Add a click event listener to a button that changes the text content of a paragraph](#task-7-add-a-click-event-listener-to-a-button-that-changes-the-text-content-of-a-paragraph)
    - [Explanation](#explanation-6)
    - [Code](#code-6)
  - [Task 8: Add a mouseover event listener to an element that changes its border color](#task-8-add-a-mouseover-event-listener-to-an-element-that-changes-its-border-color)
    - [Explanation](#explanation-7)
    - [Code](#code-7)
  - [Feature Request: Text Content Manipulation Script](#feature-request-text-content-manipulation-script)
    - [Explanation](#explanation-8)
    - [Code](#code-8)
  - [Feature Request: Element Creation Script](#feature-request-element-creation-script)
    - [Explanation](#explanation-9)
    - [Code](#code-9)
  - [Feature Request: Element Removal Script](#feature-request-element-removal-script)
    - [Explanation](#explanation-10)
    - [Code](#code-10)
  - [Feature Request: Attribute Modification Script](#feature-request-attribute-modification-script)
    - [Explanation](#explanation-11)
    - [Code](#code-11)
  - [Feature Request: Event Handling Script](#feature-request-event-handling-script)
    - [Explanation](#explanation-12)
    - [Code](#code-12)
  - [Achievement](#achievement)

# Day 9: DOM Manipulation

## Task 1: Create a new div element with some text content and append it to the body

### Explanation

In this task, we will create a new `div` element, set its text content, and append it to the `body` of the document.

### Code

```javascript
// Create a new div element
const newDiv = document.createElement("div");

// Set the text content of the new div
newDiv.textContent = "This is a new div element";

// Append the new div to the body
document.body.appendChild(newDiv);
```

## Task 2: Create a new li element and add it to an existing ul list

### Explanation

Here, we will create a new `li` element and add it to an existing `ul` list. We assume there is a `ul` element with an id of `myList` in the HTML.

### Code

```javascript
// Create a new li element
const newLi = document.createElement("li");

// Set the text content of the new li
newLi.textContent = "This is a new list item";

// Find the existing ul element by its id
const ul = document.getElementById("myList");

// Append the new li to the ul
ul.appendChild(newLi);
```

## Task 3: Select an HTML element and remove it from the DOM

### Explanation

In this task, we will select an HTML element by its id and remove it from the DOM.

### Code

```javascript
// Find the element to be removed by its id
const elementToRemove = document.getElementById("elementId");

// Remove the element from the DOM
elementToRemove.remove();
```

## Task 4: Remove the last child of a specific HTML element

### Explanation

We will select a specific HTML element and remove its last child.

### Code

```javascript
// Find the specific HTML element by its id
const parentElement = document.getElementById("parentElementId");

// Remove the last child of the specific element
parentElement.removeChild(parentElement.lastElementChild);
```

## Task 5: Select an HTML element and change one of its attributes

### Explanation

We will select an HTML element and change one of its attributes, such as the `src` attribute of an `img` tag.

### Code

```javascript
// Find the img element by its id
const imgElement = document.getElementById("imageId");

// Change the src attribute of the img element
imgElement.setAttribute("src", "newImageSource.jpg");
```

## Task 6: Add and remove a CSS class to/from an HTML element

### Explanation

We will select an HTML element and add a CSS class to it, then remove the class.

### Code

```javascript
// Find the element by its id
const element = document.getElementById("elementId");

// Add a CSS class to the element
element.classList.add("newClass");

// Remove the CSS class from the element
element.classList.remove("newClass");
```

## Task 7: Add a click event listener to a button that changes the text content of a paragraph

### Explanation

We will add a click event listener to a button. When the button is clicked, it will change the text content of a paragraph.

### Code

```javascript
// Find the button and paragraph elements by their ids
const button = document.getElementById("buttonId");
const paragraph = document.getElementById("paragraphId");

// Add a click event listener to the button
button.addEventListener("click", () => {
  // Change the text content of the paragraph
  paragraph.textContent = "The text content has been changed!";
});
```

## Task 8: Add a mouseover event listener to an element that changes its border color

### Explanation

We will add a mouseover event listener to an element. When the mouse is over the element, it will change its border color.

### Code

```javascript
// Find the element by its id
const element = document.getElementById("elementId");

// Add a mouseover event listener to the element
element.addEventListener("mouseover", () => {
  // Change the border color of the element
  element.style.borderColor = "red";
});
```

## Feature Request: Text Content Manipulation Script

### Explanation

We will write a script that selects an HTML element by its ID and changes its text content.

### Code

```javascript
// Find the element by its id
const element = document.getElementById("elementId");

// Change the text content of the element
element.textContent = "New text content";
```

## Feature Request: Element Creation Script

### Explanation

We will create a script that demonstrates creating a new `div` element and appending it to the body.

### Code

```javascript
// Create a new div element
const newDiv = document.createElement("div");

// Set the text content of the new div
newDiv.textContent = "This is a new div element";

// Append the new div to the body
document.body.appendChild(newDiv);
```

## Feature Request: Element Removal Script

### Explanation

We will write a script that selects an HTML element and removes it from the DOM.

### Code

```javascript
// Find the element to be removed by its id
const elementToRemove = document.getElementById("elementId");

// Remove the element from the DOM
elementToRemove.remove();
```

## Feature Request: Attribute Modification Script

### Explanation

We will create a script that changes the attributes of an HTML element.

### Code

```javascript
// Find the element by its id
const element = document.getElementById("elementId");

// Change an attribute of the element
element.setAttribute("attributeName", "newValue");
```

## Feature Request: Event Handling Script

### Explanation

We will write a script that adds event listeners to HTML elements to change their content or style based on user interactions.

### Code

```javascript
// Find the button and paragraph elements by their ids
const button = document.getElementById("buttonId");
const paragraph = document.getElementById("paragraphId");

// Add a click event listener to the button
button.addEventListener("click", () => {
  // Change the text content of the paragraph
  paragraph.textContent = "The text content has been changed!";
});

// Find the element by its id
const element = document.getElementById("elementId");

// Add a mouseover event listener to the element
element.addEventListener("mouseover", () => {
  // Change the border color of the element
  element.style.borderColor = "red";
});
```

## Achievement

By the end of these activities, students will:

- Select and manipulate DOM elements using JavaScript.
- Create and append new elements to the DOM.
- Remove elements from the DOM.
- Modify attributes and classes of HTML elements.
- Add and handle events to make web pages interactive.

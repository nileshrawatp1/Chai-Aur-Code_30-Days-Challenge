# Table Of Content

- [Table Of Content](#table-of-content)
  - [Day 10: Event Handling](#day-10-event-handling)
    - [Activity 1: Basic Event Handling](#activity-1-basic-event-handling)
    - [Activity 2: Mouse Events](#activity-2-mouse-events)
    - [Activity 3: Keyboard Events](#activity-3-keyboard-events)
    - [Activity 4: Form Events](#activity-4-form-events)
    - [Activity 5: Event Delegation](#activity-5-event-delegation)
    - [Feature Request](#feature-request)

## Day 10: Event Handling

### Activity 1: Basic Event Handling

**Task 1: Add a click event listener to a button that changes the text content of a paragraph.**

```javascript
const button = document.getElementById("myButton");
const paragraph = document.getElementById("myParagraph");

button.addEventListener("click", () => {
  paragraph.textContent = "Button clicked!";
});
```

**Explanation:**

- We select the button and paragraph elements using their IDs.
- We attach a click event listener to the button.
- When the button is clicked, the text content of the paragraph is changed to 'Button clicked!'.

**Task 2: Add a double-click event listener to an image that toggles its visibility.**

```javascript
const image = document.getElementById("myImage");

image.addEventListener("dblclick", () => {
  image.style.display = image.style.display === "none" ? "block" : "none";
});
```

**Explanation:**

- We select the image element using its ID.
- We attach a double-click event listener to the image.
- When the image is double-clicked, its display property is toggled between 'none' and 'block', effectively hiding and showing the image.

### Activity 2: Mouse Events

**Task 3: Add a mouseover event listener to an element that changes its background color.**

```javascript
const element = document.getElementById("myElement");

element.addEventListener("mouseover", () => {
  element.style.backgroundColor = "lightblue";
});
```

**Explanation:**

- We select the element using its ID.
- We attach a mouseover event listener to the element.
- When the mouse moves over the element, its background color is changed to 'lightblue'.

**Task 4: Add a mouseout event listener to an element that resets its background color.**

```javascript
const element = document.getElementById("myElement");

element.addEventListener("mouseout", () => {
  element.style.backgroundColor = ""; // Reset to default
});
```

**Explanation:**

- We select the element using its ID.
- We attach a mouseout event listener to the element.
- When the mouse moves out of the element, its background color is reset to its default value.

### Activity 3: Keyboard Events

**Task 5: Add a keydown event listener to an input field that logs the key pressed to the console.**

```javascript
const input = document.getElementById("myInput");

input.addEventListener("keydown", (event) => {
  console.log("Key pressed:", event.key);
});
```

**Explanation:**

- We select the input field using its ID.
- We attach a keydown event listener to the input field.
- When a key is pressed in the input field, the pressed key is logged to the console.

**Task 6: Add a keyup event listener to an input field that displays the current value in a paragraph.**

```javascript
const input = document.getElementById("myInput");
const paragraph = document.getElementById("myParagraph");

input.addEventListener("keyup", () => {
  paragraph.textContent = input.value;
});
```

**Explanation:**

- We select the input field and paragraph using their IDs.
- We attach a keyup event listener to the input field.
- When a key is released in the input field, the current value of the input is displayed in the paragraph.

### Activity 4: Form Events

**Task 7: Add a submit event listener to a form that prevents the default submission and logs the form data to the console.**

```javascript
const form = document.getElementById("myForm");

form.addEventListener("submit", (event) => {
  event.preventDefault(); // Prevent default form submission

  // Access form data here
  const formData = new FormData(form);
  const data = Object.fromEntries(formData);
  console.log(data);
});
```

**Explanation:**

- We select the form using its ID.
- We attach a submit event listener to the form.
- When the form is submitted, the default behavior is prevented using `event.preventDefault()`.
- We create a FormData object to access the form data and log it to the console.

**Task 8: Add a change event listener to a select dropdown that displays the selected value in a paragraph.**

```javascript
const select = document.getElementById("mySelect");
const paragraph = document.getElementById("myParagraph");

select.addEventListener("change", () => {
  paragraph.textContent = select.value;
});
```

**Explanation:**

- We select the select dropdown and paragraph using their IDs.
- We attach a change event listener to the select dropdown.
- When the selected option changes, the selected value is displayed in the paragraph.

### Activity 5: Event Delegation

**Task 9: Add a click event listener to a list that logs the text content of the clicked list item using event delegation.**

```javascript
const list = document.getElementById("myList");

list.addEventListener("click", (event) => {
  if (event.target.tagName === "LI") {
    console.log(event.target.textContent);
  }
});
```

**Explanation:**

- We select the list using its ID.
- We attach a click event listener to the list.
- When a click event occurs, we check if the clicked element is an LI element. If it is, we log its text content to the console.

**Task 10: Add an event listener to a parent element that listens for events from dynamically added child elements.**

```javascript
const parent = document.getElementById("myParent");

parent.addEventListener("click", (event) => {
  if (event.target.classList.contains("dynamic-child")) {
    console.log("Dynamic child clicked!");
  }
});
```

**Explanation:**

- We select the parent element using its ID.
- We attach a click event listener to the parent element.
- When a click event occurs, we check if the clicked element has the class 'dynamic-child'. If it does, we log a message to the console.

### Feature Request

**1. Click Event Script:**
See Task 1 under Activity 1: Basic Event Handling.

**2. Mouse Events Script:**
See Tasks 3 and 4 under Activity 2: Mouse Events.

**3. Keyboard Events Script:**
See Tasks 5 and 6 under Activity 3: Keyboard Events.

**4. Form Events Script:**
See Tasks 7 and 8 under Activity 4: Form Events.

**5. Event Delegation Script:**
See Tasks 9 and 10 under Activity 5: Event Delegation.

**Remember to replace placeholders like `myButton`, `myParagraph`, etc., with actual IDs of your HTML elements.**

**Additional Notes:**

- You can customize the event handlers to perform different actions based on your specific requirements.
- Consider using event bubbling and capturing for more complex event handling scenarios.
- Explore other event types like focus, blur, resize, scroll, and more to create interactive web applications.

I hope this comprehensive response is helpful!

# JavaScript Syntax Reference Guide

## Objective
Fetch data from the provided API endpoint and display it as a list on the webpage.

**API Endpoint:** `https://dhruvabisht.github.io/endpoint/list.json`
**HTML Boiler Plate:** 'https://dhruvabisht.github.io/endpoint/boilerplatecode.md'

---

## JavaScript Syntax Guide

### 1. Declaring Variables

```javascript
// Constant variable (cannot be reassigned)
const variableName = value;

// Variable that can be reassigned
let variableName = value;
```

---

### 2. Fetching Data from an API

#### Using async/await (Recommended)

```javascript
async function functionName() {
    const response = await fetch(url);
    const data = await response.json();
}
```

#### Key Points:
- `fetch(url)` - Makes an HTTP request to the specified URL
- `await` - Waits for the promise to resolve
- `.json()` - Parses the response body as JSON
- Functions using `await` must be declared with `async`

---

### 3. Error Handling

```javascript
// Check if response is successful
if (!response.ok) {
    console.log(response.status);
    return;
}
```

**Alternative:** Check for response existence
```javascript
if (!response) {
    // Handle error
} else {
    // Process data
}
```

---

### 4. DOM Manipulation

#### Selecting Elements

```javascript
// Get element by ID
const element = document.getElementById('elementId');
```

#### Creating Elements

```javascript
// Create a new HTML element
const newElement = document.createElement('tagName');
```

#### Modifying Elements

```javascript
// Set text content
element.textContent = 'Your text here';

// Append child element
parentElement.appendChild(childElement);
```

---

### 5. Iterating Over Arrays

#### Using forEach

```javascript
array.forEach(function(item) {
    // Do something with each item
});
```

**Arrow function syntax (alternative):**
```javascript
array.forEach((item) => {
    // Do something with each item
});
```

---

### 6. Accessing Object Properties

```javascript
// Dot notation
object.propertyName

// Bracket notation
object['propertyName']
```

---

### 7. Calling Functions

```javascript
// Define function
function myFunction() {
    // function body
}

// Call function
myFunction();
```

---

## Expected Data Structure

The API returns an array of user objects. Each object has properties you'll need to access and display.

**Tip:** Use `console.log(data)` to inspect the structure of the returned data.

---

## Testing Your Code

1. Open the HTML file in a web browser
2. Open Developer Tools (F12)
3. Check the Console tab for any errors
4. Verify that the list items appear on the page

---


## Additional Resources

- [MDN: Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [MDN: async/await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
- [MDN: DOM Manipulation](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents)

---

Good luck! 

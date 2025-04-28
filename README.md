# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript and DOM Manipulation</title>
    <style>
        #dynamicText {
            color: blue;
            font-size: 20px;
        }
    </style>
</head>
<body>

    <h1>Welcome to DOM Manipulation!</h1>
    <p id="dynamicText">This text will change when you click the button.</p>

    <button id="changeTextBtn">Change Text</button>
    <button id="addElementBtn">Add New Element</button>
    <button id="removeElementBtn">Remove Element</button>

    <div id="newElementContainer"></div>

    <script src="script.js"></script>
</body>
</html>

// 1. Change text content dynamically
document.getElementById("changeTextBtn").addEventListener("click", function() {
    document.getElementById("dynamicText").textContent = "The text has been changed!";
});

// 2. Modify CSS styles via JavaScript
document.getElementById("changeTextBtn").addEventListener("click", function() {
    document.getElementById("dynamicText").style.color = "red";
    document.getElementById("dynamicText").style.fontSize = "25px";
});

// 3. Add a new element when a button is clicked
document.getElementById("addElementBtn").addEventListener("click", function() {
    const newElement = document.createElement("p");
    newElement.textContent = "This is a new element added dynamically!";
    document.getElementById("newElementContainer").appendChild(newElement);
});

// 4. Remove an element when a button is clicked
document.getElementById("removeElementBtn").addEventListener("click", function() {
    const container = document.getElementById("newElementContainer");
    if (container.childNodes.length > 0) {
        container.removeChild(container.lastChild);
    } else {
        alert("No element to remove!");
    }
});


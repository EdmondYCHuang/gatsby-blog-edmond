---
title: "use-chatGPT-to-design-web-layout"
date: "2024-11-12T22:40:32.169Z"
description: use-chatGPT-to-design-web-layout.
---


> I want to create a 3-column layout with the interactive functionality. The left Column displays a static image. The middle column contains six buttons arranged vertically, each with descriptive text. The right column shows a different image based on the button clicked.

Step 1: HTML Structure
Here's the HTML setup for the 3-column layout and buttons:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3-Column Layout with Dynamic Images</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <!-- Left Column -->
        <div class="column left-column">
            <img src="default.jpg" alt="Static Image" id="staticImage">
        </div>

        <!-- Middle Column -->
        <div class="column middle-column">
            <button onclick="showImage('image1.jpg')">Button 1</button>
            <button onclick="showImage('image2.jpg')">Button 2</button>
            <button onclick="showImage('image3.jpg')">Button 3</button>
            <button onclick="showImage('image4.jpg')">Button 4</button>
            <button onclick="showImage('image5.jpg')">Button 5</button>
        </div>

        <!-- Right Column -->
        <div class="column right-column">
            <img src="placeholder.jpg" alt="Display Image" id="displayImage">
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
```

Step 2: CSS for Styling and Layout
Create a styles.css file to style the 3-column layout:

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

.container {
    display: flex;
    height: 100vh;
}

.column {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
}

.left-column, .right-column {
    background-color: #f0f0f0;
}

.middle-column {
    background-color: #ddd;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

button {
    margin: 10px 0;
    padding: 10px;
    font-size: 16px;
    cursor: pointer;
}

img {
    max-width: 100%;
    max-height: 100%;
}
```

Step 3: JavaScript for Interactive Image Display
Create a script.js file to handle button clicks and update the displayed image in the right column.

```javascript
function showImage(imageSrc) {
    // Get the image element in the right column
    const displayImage = document.getElementById('displayImage');

    // Update the source of the display image
    displayImage.src = imageSrc;
}
```

Explanation of the Code
HTML:

Each button in the middle column has an onclick event that triggers the showImage function and passes the corresponding image filename as a parameter.
The left column displays a static image, and the right column contains an image element whose src will be dynamically updated.
CSS:

The container is set to display: flex to create a 3-column layout.
The .middle-column is styled to arrange the buttons vertically.
JavaScript:

The showImage function takes an image filename (imageSrc) as a parameter, finds the displayImage element in the right column, and changes its src attribute to display the selected image.


> i hope the middle column width account for 10% of all layout. Left and right columns account for 45% of layout width separately


ChatGPT 說：
ChatGPT
To adjust the column widths so that the middle column occupies 10% of the layout, while the left and right columns each take up 45%, you can modify the CSS flex-basis properties accordingly. This will ensure the desired layout proportions without the need for complex calculations.

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

.container {
    display: flex;
    height: 100vh;
}

.column {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
}

/* Set width for each column */
.left-column {
    flex-basis: 45%;
    background-color: #f0f0f0;
}

.middle-column {
    flex-basis: 10%;
    background-color: #ddd;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.right-column {
    flex-basis: 45%;
    background-color: #f0f0f0;
}

/* Button styling */
button {
    margin: 10px 0;
    padding: 10px;
    font-size: 16px;
    cursor: pointer;
}

/* Image styling */
img {
    max-width: 100%;
    max-height: 100%;
}
```

I hope the button is made of designer style

ChatGPT 說：
ChatGPT
To give the buttons a more designer-styled look, we can add some modern UI touches such as shadows, gradients, subtle animations, and hover effects. This styling will make the buttons look polished and interactive.

```css
/* Button Styling */
button {
    margin: 10px 0;
    padding: 12px 20px;
    font-size: 16px;
    font-weight: bold;
    color: #fff;
    background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

/* Hover and Active Effects */
button:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
}

button:active {
    transform: translateY(1px);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

/* Add focus effect for accessibility */
button:focus {
    outline: 2px solid #2575fc;
}

```
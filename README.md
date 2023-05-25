# Circular Progress Bar

This is a simple guide on how to create a circular progress bar using HTML and CSS.

## Table of Contents

1. Introduction
2. HTML Structure
3. CSS Styling
4. JavaScript 
5. Conclusion

## Introduction

A circular progress bar is a visual element used to represent the progress of a task or process in a circular format. It is a popular choice for displaying progress in web applications. In this guide, we'll go through the steps to create a basic circular progress bar using HTML and CSS.

## HTML Structure

To create a circular progress bar, we'll start by defining the HTML structure. The progress bar will be contained within a parent element, and we'll use a child element to represent the progress indicator.

```html
<div class="container">
  <div class="circular-progress"></div>
</div>
```

In the above code snippet, we have a parent container element with the class "container" and a child element with the class "circular-progress."

## CSS Styling

Next, let's define the CSS styles to create the circular progress bar effect. We'll use CSS to set the dimensions, colors, and animations.

```css
.container{
    display: flex;
    width: 420px;
    padding: 50px 0;
    border-radius: 8px;
    background: #fff;
    row-gap: 30px;
    flex-direction: column;
    align-items: center;
}

.circular-progress{
    position: relative;
    height: 250px;
    width: 250px;
    background: conic-gradient(rgb(186, 2, 8) 3.6deg, #ededed 0deg);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.circular-progress::before{
    content:"";
    position: absolute;
    height: 210px;
    width: 210px;
    background-color: #fff;
    border-radius: 50%;
}
...

In the CSS above, we set the width and height of the circular-progress to 250 pixels. The "border-radius" property is set to 50% to create a circular shape. The background color of the container is set to "#fff" and the circular-progress bar color is set to "rgb(186, 2, 8)".

The progress bar itself is positioned absolutely within the container, and its dimensions match the container's dimensions.

## JavaScript

Here's an example of how you can update the progress bar using JavaScript:

```javascript
let circularProgress = document.querySelector(".circular-progress"),
    progressValue = document.querySelector(".progress-value");

let progressStartValue = 0,
    progressEndValue = 80,
    speed = 100;
...

In the above JavaScript code, we select the progress bar element using its class name and update it based on the "progressValue" variable.

## Conclusion

By following the steps outlined in this guide, you should now have a basic understanding of how to create a circular progress bar using HTML and CSS. Feel free to customize the styles and animations to match your specific requirements.

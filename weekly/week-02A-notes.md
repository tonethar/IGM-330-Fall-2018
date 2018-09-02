# Week 2A - Canvas Affine Transformations

## I. Overview
Today we will: 
- Review:
  - last week's homework
  - JavaScript & DOM concepts from last week
  - how to set up a canvas drawing context, and how to draw rectangles, circles, and lines
- look at how Canvas *tranformations* (translating, rotating, scaling) work


## II. Required Reading & Assignments
* Shape Viewer HW -> [HW-shape-viewer.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-shape-viewer.md)
* Try It! HW -> [HW-try-it.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-try-it.md)
* Study Guide-2 -> [HW-SG-2.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-2.md)

## III. Review of last week's JavaScript concepts
1. When writing JavaScript code in a web browser, what is the essential first step you must take before writing code that accesses HTML elements (i.e DOM elements) that are already on the page?
1. Which DOM method is used (in this course) to get a reference to a *single* HTML page element?
    * What are the possible return values(s) of this method?
1. Which DOM method (used in this course) is able to return references to *multiple* HTML page elements?
1. What are the names of 2 legacy DOM methods that are considered *deprecated* for this course, and we will not be using in any of our  assignments or projects?
1. What does `"use strict"` do? See these articles:
    * https://love2dev.com/blog/javascript-strict-mode/
    * https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode
1. What is the JS keyword used to declare variables that are *block scoped*?
1. What is the JS keyword which declares a variable *globally*, or locally to an entire function (i.e. *function scoped*) regardless of the block it is declared in?
1. Which one of these 2 keywords are we going to use 99.9% of the time in this course when we want to declare a variable?
1. Write a function named `addThem`, that takes 2 arguments named `num1` and `num2`, and returns their sum
    * Now write another function named `addThem2` that works as above, but also gives `num1` and `num2` *default values* of `0`
    * Now write another function named `addThem3` that works the same as `addThem2`, but is instead declared as an ES6 arrow function
1. Write a function named `doStuff` that causes the second paragraph on an HTML page to have a pink background color, and for that paragraph's contents to be replaced with the text "Greetings and Felcitations"
1. Suppose we have a variable named `myButton` that references a DOM button. Write a JS *event handler* that will call function `doStuff` when the button is clicked
1. Now write *event listener* code that will do the same thing for `myButton`

## IV. Canvas Presentation
1. Basic Canvas Review:
  - **Why canvas?**
      - It's a stateful bitmap drawing API that is available on all modern web browsers - it's good to know how these kind of APIs work - as both iOS & Android have similar APIs for drawing
      
  - **Steps to getting a drawing context object**:
      - After the page loads, get a reference to a &lt;canvas> element: `let canvas = document.querySelector('canvas');`
      - Now get a reference to the drawing *context* like this: `let ctx = canvas.getContext('2d');`
      - `ctx` is a new `CanvasRenderingContext2D` object- this object has properties and methods that are listed here: https://www.w3.org/TR/2dcontext/#conformance-requirements
      
  - **How to draw a rectangle**:
      - A) Optionally, `ctx.save()` (i.e. save or "push") the current value of all of the drawing state attributes so that you can easily restore them to their original values later. This also saves the CTM (current transformation matrix), which we will discuss soon
      
      - B) Optionally, set the drawing state attributes (properties) that you wish to have values other than the defaults - for example `ctx.lineWidth`, `ctx.strokeStyle`, `ctx.fillStyle`, `ctx.globalAlpha` - a full list of state properties is here: https://www.w3.org/TR/2dcontext/#the-canvas-state
      
      - C) Create a *path* for the rectangle like this:
      
      `ctx.beginPath();`
      
      `ctx.rect(x,y,width,height);`
      
      `ctx.closePath();`
    
     - D) So we now have a path, but we can't see it. Now we need to stroke and/or fill the rectangular path like so. *Note that the order of these two calls **will** have an effect on the appearance of the drawing*:
     
     `ctx.stroke();`
     
     `ctx.fill();`
     
     - E) Optionally, `ctx.restore()` the drawing context state properties and CTM to their previous values

The final version, which gives us a 100px by 100px yellow rectangle, with a 5 pixel thick (visible) red border, looks like this:

```js
ctx.save();                 // A - optionally, save the drawing state attributes and CTM
ctx.strokeStyle = "red";    // B - optionally, change the values of one or more drawing state attributes
ctx.fillStyle = "yellow";   // B
ctx.lineWidth = "10";       // B
ctx.beginPath();            // C - describe a path
ctx.rect(20,20,100,100);    // C
ctx.closePath();            // C
ctx.stroke();               // D - draw! i.e. make the path visible
ctx.fill();                 // D - swap the order of stroke() and fill() to see what happens to the drawing
ctx.restore();              // E - optionally, restore the saved values of drawing state attributes and CTM
```

\*\* ***Note that the order of steps B and C above does not matter, and could be flipped, and the drawing would look the same.*** \*\*

 - **How to draw a circle**:
     - virtually identical to drawing a rectangle, just replace the path code - `ctx.rect()` - with:
       - `ctx.arc(x, y, radius, startAngle, endAngle, counterclockwise);`
     - here's an example: 
       - `ctx.arc(100, 100, 25, 0, Math.PI * 2, false); // draws a circle at 100,100 with a 25-pixel radius`
 - **How to draw a line**:
     -  just replace the path code - `ctx.rect()` - with:
     
```js
ctx.moveTo(20,100);
ctx.lineTo(620,100);
``` 

2. **Drawing polygons**

3. **Canvas Transformations**



## V. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Transformations

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-01B-notes.md**](week-01B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-02B-notes.md**](week-02B-notes.md)

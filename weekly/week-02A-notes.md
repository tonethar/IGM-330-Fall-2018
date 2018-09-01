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
2. Which DOM method is used (in this course) to get a reference to a *single* HTML page element?
    * What are the possible return values(s) of this method?
3. Which DOM method (used in this course) is able to return references to *multiple* HTML page elements?
4. What are the names of 2 legacy DOM methods that are considered *deprecated* for this course, and we will not be using in any assignments or projects?
5. What does `"use strict"` do? See these articles:
    * https://love2dev.com/blog/javascript-strict-mode/
    * https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode
6. What is the JS keyword used to declare variables that are *block scoped*?
7. What is the JS keyword which declares a variable *globally*, or locally to an entire function (i.e. *function scoped*) regardless of the block it is declared in?
8. Which one of these 2 keywords are we going to use 99.9% of the time in this course when we want to declare a variable?
9. Write a function named `addThem`, that takes 2 arguments named `num1` and `num2`, and returns their sum
    * Now write another function named `addThem2` that works as above, but also gives `num1` and `num2` *default values* of `0`
    * Now write another function named `addThem3` that works the same as `addThem2`, but is instead declared as an ES6 arrow function
10. Write a function named `doStuff` that causes the second paragraph on an HTML page to have a pink background color, and for that paragraph's contents to be replaced with the text "Greetings and Felcitations"
11. Suppose we have a variable named `myButton` that references a DOM button. Write a JS *event handler* that will call function `doStuff` when the button is clicked
12. Now write *event listener* code that will do the same thing for `myButton`

## IV. Presentation
1. Basic Canvas Review:
  - Why canvas? It's a stateful bitmap drawing API - it's good to know how they work - both iOS & Android have similar APIs for drawing
  - Steps to getting a drawing context object
    - After the page loads, get a reference to a &lt;canvas> element
    - Now get a reference to the drawing *context* like this: `let ctx = canvas.getContext('2d')`
    - `ctx` is a new `CanvasRenderingContext2D` object- this object has properties and methods that are listed here: https://www.w3.org/TR/2dcontext/#conformance-requirements
  - Basic drawing of a rectangle:
    1. Optionally, `ctx.save()` (i.e. save or "push") the current value of all of the drawing state attributes so that you can easily `ctx.restore()` them to their original values later
    2. Set drawing state attributes (properties) that you wish to have values other than the defaults - for example `ctx.lineWidth`, `ctx.strokeStyle`, `ctx.fillStyle`, `ctx.globalAlpha` - a full list of state properties is here: https://www.w3.org/TR/2dcontext/#the-canvas-state
    3. Create a path for the rectangle like this:
    
```js
ctx.beginPath();
ctx.rect(*x*,y,width,height);
ctx.closePath();
```
    
  

## V. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Transformations

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-01B-notes.md**](week-01B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-02B-notes.md**](week-02B-notes.md)

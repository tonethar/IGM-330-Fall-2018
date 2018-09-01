# Week 2A - Canvas Affine Transformations

## I. Overview
This week we will: 
- look at how Canvas *tranformations* (translating, rotating, scaling) work
- review how to work with DOM elements like buttons, and how to hook them up to canvas code when an event occurs

## II. Required Reading & Assignments
* Shape Viewer HW -> [HW-shape-viewer.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-shape-viewer.md)
* Try It! HW -> [HW-try-it.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-try-it.md)
* Study Guide-2 -> [HW-SG-2.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-2.md)

### III. Review of last week's JavaScript concepts

1. When writing JavaScript code in a web browser, what is the essential first step you must take before writing code that accesses HTML elements (i.e DOM elements) that are already on the page?
2. Which DOM method is used (in this course) to get a reference to a *single* HTML page element?
  * What are the possible return values(s) of this method?
3. Which DOM method (used in this course) is able to return references to *multiple* HTML page elements?
4. What are the names of 2 legacy DOM methods that are considered *deprecated* for this course, and we will not get using in any assignments or projects?
5. What does `"use strict"` do? See these articles:
  * https://love2dev.com/blog/javascript-strict-mode/
  * https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode
6. What is the JS keyword used to declare variables that are *block scoped*?
7. What is the JS keyword which declares a variable *globally*, or locally to an entire function (i.e. *function scoped*) regardless of the block it is declared in?
8. Which one of these 2 keywords are we going to use 99.9% of the time in this course when we want to declare a variable?
9. Write a function named `addThem`, that takes 2 arguments named `num1` and `num2`, and returns their sum
  * Now write another function named `addThem2` that works as above, but also gives `num1` and `num2` *default values* of `0`
  * Now write another function named `addThem3` that works the same as `addThem2`, but is instead declared as an ES6 arrow function
10. Suppose we have a variable named `myButton` that references a DOM button, write an *event handler* code that will call a function named `doStuff()` when the button is clicked
11. Now write *event listener* code that will do the same thing for `myButton`

## IV. Presentation

## V. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Transformations

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-01B-notes.md**](week-01B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-02B-notes.md**](week-02B-notes.md)

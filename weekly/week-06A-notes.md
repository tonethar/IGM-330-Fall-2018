# Week 6A - JavaScript's *Revealing Module Pattern*

## I. Overview & Presentation
- In the first part of today's demo, we will take a previous demo where all of the JS code is contained in the HTML file and split the code between 3 JS files, which will improve the readability and organization of the code.
  - However, as far as the JavaScript runtime is concerned, all of this code is still intermingled in the global and "script" scopes.
- In the second and third parts of today's demo, we will fix this issue by implementing the ***revealing module pattern***. 
  - This pattern uses multiple IIFEs to first hide away all the code in a file that we wish to be *private* and not visible to the outside, and then to only export those variables and functions that we wish to be *public*.
  
 ## II. Start Files
- The start file for Part I of the presentation is the completed version of the the "Demo - Sprite Literals and Canvas Image Data", we did [Week 4B](https://github.com/tonethar/IGM-330-Fall-2018/blob/master/weekly/week-04B-notes.md) - hopefully you followed along with the demo and have this file.
- If you did not previously follow along in the 4B demo, the original start file is here: https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-canvas-image-data.md - and you will need to watch the Week 4B "Canvas Image Data" videos (linked in mycourses) to get the controls working.
- The start file for Part II of the presentation is here: https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-privacy-with-IIFE.md

## III. Reference
- https://en.wikipedia.org/wiki/Immediately-invoked_function_expression
- https://addyosmani.com/resources/essentialjsdesignpatterns/book/#revealingmodulepatternjavascript
- https://toddmotto.com/mastering-the-module-pattern/


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-05B-notes.md**](week-05B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-06B-notes.md**](week-06B-notes.md)

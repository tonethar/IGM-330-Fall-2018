# Week 9A - Review Exam & ES6 Modules

- Review Exam, and touch on major concepts:
  - canvas API, paths, drawing state properties, drawing state stack
  - manipulating bitmaps for pixel effects
  - web audio routing graph, effect node, destination node, analyzer node, oscillator node
  - JS typed arrays (we used these with both image data and audio data)
  - DOM: did the page load? Event handlers and function *references*
  - Other JavaScript concepts:
    - writing ES5 function declarations and ES6 arrow functions
    - value types v. reference types:
      - immutability of these with *const*
      - changing properties of reference types (extra credit question)
    - variable scope (outside of modules):
      - outside of another function, `function` declarations are **global**, otherwise the function is scoped to the enclosing function
      - `var` is **global** if declared outside of a function, otherwise the variable is scoped to the enclosing function (Chrome debugger call this scope **local**)
      - `let` is **script** scoped if declared outside of a function, otherwise the variable is scoped to the enclosing **block**
      - `const` is the same as `let`
  - Objects: literals, methods, classes
  - Modular code: 
    - use a single IIFE to create scope
    - use multiple IIFEs to create modular code and "public/private" - the *ES5 Revealing Module Pattern*
- New Stuff:
  - ES6 Modules

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-08B-notes.md**](week-08B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-09B-notes.md**](week-09B-notes.md)

# Week 3A - Review recent HW & Build a paint app

## I. Overview
Today we will:
- review [HW-shape-viewer.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-shape-viewer.md) - an important concept is how to pass data *from* HTML elements *to* your JavaScript - there are several approaches that work - we will look at 3 of them:
  - `drawBox()`- pass color data by utilizing `e.target` or `this`
    - BTW - arrow function don't bind their own `this`, it instead binds to its *lexical scope* (aka static scope)
  - `drawBox()`- pass color data inside an anonymous wrapper function
  - `drawBox()`- pass color data via an HTML5 custom data attributes:
    - we briefly covered HTML5 custom data attributes in IGM-230 - see [web-apps-6.md#section7](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-6.md#section7)
- review [HW-try-it.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-try-it.md)
  - to draw the squares, circles, and ploygons, this requires a good understanding of `ctx.translate()`, `ctx.rotate()` and `ctx.scale()` as well as `ctx.save()` and `ctx.restore()`
  - note how we can flip the text along its horizontal or vertical axis with `ctx.scale(-1,1)` or `ctx.scale(1,-1)`
- review [HW-SG-2.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-2.md) - concepts:
  - line caps, line joins, line dashes
  - A gradient specifies a starting color, an ending color, and an area over which color changes. A single gradient can encompass more than one color change
    - linear and radial gradients
  - bezier curves:
      - `ctx.quadraticCurveTo(ctrlX, ctrlY, endX, endY)` draws bezier curves with 1 control point
      - `ctx.bezierCurveTo(ctrlX, ctrlY, ctrlXa, ctrlYa, endX, endY)` draws cubic bezier curves with 2 control points
      - curve building demos
      - animating curves
  
## II. Presentation
- Let's talk about [HW-drawing-app.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-drawing-app.md)

## III. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Transformations


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-02B-notes.md**](week-02B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-03B-notes.md**](week-03B-notes.md)

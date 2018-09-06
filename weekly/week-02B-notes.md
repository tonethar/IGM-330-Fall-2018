# Week 2B - Canvas Affine Transformations

## I. Overview
Today we will:
- review *smiley* HW submissions
- look at how Canvas *tranformations* (translating, rotating, scaling) work
- look at the Canvas drawing state "stack", and use cases for `ctx.save()` and `ctx.restore()`

## II. Required Reading & Assignments
* Try It! HW -> [HW-try-it.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-try-it.md)
* Canvas Procedural Artwork with "Helper" Functions HW -> [HW-canvas-helpers.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-canvas-helpers.md)
* Drawing App HW -> [HW-drawing-app.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-drawing-app.md)


## III. Presentation
1. the current transformation matrix (CTM)
  - `ctx.translate()`
  - `ctx.rotate()`
  - `ctx.scale()`
2. Manipulating the drawing state stack via `ctx.save()` and `ctx.restore`
3. What is the drawing state "stack"? 
  - the drawing state "stack" is a "snapshot" of the current value of drawing attributes and transformations. Here is what is included in it:
  - drawing attributes (i.e. styles or properties):  `strokeStyle, fillStyle, globalAlpha, lineWidth, lineCap, lineJoin, miterLimit, shadowOffsetX, shadowOffsetY, shadowBlur, shadowColor, globalCompositeOperation, font, textAlign, textBaseline`
  - The clipping region - there is a `ctx.clip()` method, and we also saw clipping in action with the "ring" and "donut" we created last time
  - the transformation matrix (translations + rotations + scales via `ctx.translate()`, `ctx.rotate()`, `ctx.scale()`, and ctx.setTransform()`)


## IV. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Transformations


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-02A-notes.md**](week-02A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-03A-notes.md**](week-03A-notes.md)

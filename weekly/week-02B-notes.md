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
1. the **Current Transformation Matrix** (CTM)
  - `ctx.translate()`
  - `ctx.rotate()`
  - `ctx.scale()`
2. Manipulating the drawing state stack via `ctx.save()` and `ctx.restore()`
3. What is the drawing state "stack"? 
  - the drawing state "stack" is a "snapshot" of the current value of drawing attributes and transformations. Here is what is included in it:
    - **drawing attributes** (i.e. styles or properties):  `strokeStyle, fillStyle, globalAlpha, lineWidth, lineCap, lineJoin, miterLimit, shadowOffsetX, shadowOffsetY, shadowBlur, shadowColor, globalCompositeOperation, font, textAlign, textBaseline`
    - The **clipping region** - there is a `ctx.clip()` method, and we also saw clipping in action with the "ring" and "donut" we created last time
    - the **CTM** - *current transformation matrix* (translations + rotations + scales via `ctx.translate()`, `ctx.rotate()`, `ctx.scale()`, and `ctx.setTransform()`)
    
## IV. Demo
1. In **canvas-transforms-demo-start.html**, let's make some drawing changes to just our first green square.  We will see that using `ctx.save()` and `ctx.restore` helps to make this easier

2. Let's next try *translating*, then *scaling*, then *rotating* the squares -  how are the results unexpected? Once again, `ctx.save()` and `ctx.restore` to the rescue!

3. Now now we will create some animation by letting our transformations accumulate over time

![Drawing State Stack](./_images/drawing-stack.jpg)

## V. Demo Start Files

**canvas-transforms-demo-start.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Canvas Transforms Starter</title>
	<style>
	canvas{
		border:1px solid gray;
	}
	</style>
</head>
<body>
	<canvas width="640" height="480">
		Get a real browser!
	</canvas>
	<script>
		'use strict';
		
		init();
	
		function init(){
			let ctx = document.querySelector('canvas').getContext('2d');
		
			// A - all fill operations are now in yellow
				ctx.fillStyle = 'yellow'; 
			
				// B- fill a rectangle with the current fill color
				ctx.fillRect(0,0,640,480); 
			
				// C - set the current font
				ctx.font = 'bold 60pt Verdana'; 
			
				// D - change the current fill color
				ctx.fillStyle = '#44aa44'; 
			
				// E - draw stuff
			 
				//ctx.translate(100,0);
				//ctx.scale(1.2,1.2);
				//ctx.rotate(Math.PI/6);
			
				// square with fillRect() convenience method
				ctx.fillStyle="green";
				ctx.fillRect(100,100,100,100);
			
				// square with rect()
				ctx.fillStyle="blue";
				ctx.beginPath();
				ctx.rect(300,100,100,100);
				ctx.closePath();
				ctx.fill();
			
				// triangle
				ctx.strokeStyle="red";
				ctx.fillStyle="red";
				ctx.lineWidth="5";
				ctx.beginPath();
				ctx.moveTo(500,100);
				ctx.lineTo(550,200);
				ctx.lineTo(450,200);
				ctx.closePath();
				ctx.stroke();
		}
	</script>
</body>
</html>
```



## VI. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Transformations


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-02A-notes.md**](week-02A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-03A-notes.md**](week-03A-notes.md)

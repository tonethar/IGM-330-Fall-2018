# Week 3B - Canvas Bitmaps & Blending Modes

## I. Overview
- Review [HW-canvas-helpers.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-canvas-helpers.md)

## II. Required Reading & Assignments
- [HW - Audio Visualizer - Part I](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-1.md)
- [HW - Audio Visualizer - Part II](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2.md)
- [HW - Audio Visualizer - Part III](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-3.md)

## III. Presentation

1. Drawing Images:
  - we can use canvas to draw bitmap images. The source of the image could be an &lt;img> tag, an `Image()` object, a SVG &lt;image> element, a frame of a &lt;video> element, or another &lt;canvas> element
  - 
2. Blend Modes:


## IV Demo Files

**canvas-image-demo.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Canvas Image Demo</title>
	<style>
		canvas{
			border:1px solid black;
		}
	</style>
</head>
<body>
<canvas width="600" height="600"></canvas>

<script>
	const imageURL = "https://pbs.twimg.com/profile_images/1419014347/Logo_IGM_color_512x512.jpg";

	preloadImage(imageURL,init); 	

	// simple pre-loader that loads 1 image
	// preloadImage(imageURL,callbackFunc);
	function preloadImage(url,callback){
		let img = new Image();
		img.src = url;
		img.onload = _=>{
			callback(img)
		};
		img.onerror = _=>{
			console.log(`Image at url "${url}" wouldn't load! Check your URL!`);
		};
	}
	
	function init(img){
			let ctx = document.querySelector("canvas").getContext("2d");
			ctx.fillStyle = "yellow";
			ctx.fillRect(0,0,600,600);
			
			// 1 - ctx.drawImage(image, dx, dy); // dx = "destination x"
			ctx.drawImage(img,0,0);
			
			// 2 - ctx.drawImage(image, dx, dy, dWidth, dHeight); 
			// use dWidth and dHeight to scale the Image
			// ctx.drawImage(img,0,0,240,240);
				
			// 3 - ctx.drawImage(image, sx, sy, sWidth, sHeight, dx, dy, dWidth, dHeight);
			// use sx, sy, sWidth, sHeight to sample just part of the image
			//ctx.drawImage(img, 304, 140, 200, 200, 20, 20, 250, 250);
			
			// 4 - loop and draw!
			// ctx.translate(150,65);
// 			for(let i=0;i<55;i++){
// 				ctx.drawImage(img, 304, 140, 200, 200, -50, -50, 100, 100);
// 				ctx.translate(110-i*2,0);
// 				ctx.rotate(Math.PI/10);
// 				ctx.scale(.95,.95);
// 			}
	}
</script>
</body>
</html>
```

## V. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Using_images
- https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/drawImage
- https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/globalCompositeOperation


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-03A-notes.md**](week-03A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-04A-notes.md**](week-04A-notes.md)

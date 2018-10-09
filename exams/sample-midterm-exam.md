# Sample IGME-330 Midterm Exam

Note: Some of these JavaScript concepts are reviewed in the IGME-230 JavaScript Web App notes: https://github.com/tonethar/IGME-230-GDD-Spring-2018/blob/master/notes/web-apps-0.md

1. The following code throws the error Uncaught TypeError: Cannot set property 'innerHTML' of null. Why does this error occur and how do you fix it?

```html
<!DOCTYPE html>
<html>
<head>
<title>Example 1</title>
<script>
	function init(){
		let myH1 = document.querySelector("#main");
		myH1.innerHTML="Welcome to my favorite music page";
	}
	
	init();

</script>
</head>
<body>
	<h1 id="main">  This is my my header </ h1>
</body>
</html>
```


2. Explain what `"use strict"` does in JavaScript


3. Write a JavaScript function called multiply that accepts two numbers as arguments. This function will multiply the two numbers together and return the result

- now write this function as an ES6 arrow function


4. Given the following `odds` array, write JS code that will iterate over the `odds` array, add all even numbers to the `evens` array and remove the even numbers from the `odds` array. 
The final version of the `odds` array should only contain odd numbers. The final version of the `evens` array should only contain the even numbers

```js
let  odds  = [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ];
let  evens = [ ];
```

5. Given a page that has a button with an id value of `button1`, write JS code to attach a `click` event to the button. When the button is clicked, the function should print "I was clicked"


6. Given a page that has a select box with the id “dropdown1”, write JS code to attach a change event to the select box. When the dropdown value is changed, your function should print the current value of the dropdown.


7. In the following example, `myNum` is which of the following types of variables? 

```js
<script>
	let myNum = 0; 

	function init(){
		console.log(myNum);
	}
	
	window.onload = init;
</script>
```

A)	Local

B)	Global

C)	Script

D)	Property


8. In the following example, `myNum` is which of the following types of variables? 

```js
<script>
	function init(){
		let myNum = 0;
		console.log(myNum);
	}
	
	window.onload = init;
</script>
```

A)	Local

B)	Global

C)	Script

D)	Property


9. In the following example, myNum is which of the following types of variables? 

```js
<script>
	var obj = {
		myNum: 0
	};
</script>
```

A)	Local

B)	Global

C)	Instance

D)	Property


10.	 What does `Object.seal()` do and when would you use it?


11. What does `Object.freeze()` do and when would you use it?


12. What types of legal values can be put into a standard JS array created with `[ ]` or `new Array()`?


13.	What legal values can be put into a typed array created with `new Uint8Array(1024)`?


**For questions 14 - 17, use this object:**

```js
let obj = {
     x: 5,
  y: 10,
     move: function() {
         	this.x++;
            this.y++;
     }
}
```

14.	 What will be the output of this code?

```js
console.log(obj.speed);
```


15. What will be the output of this code?

```js
obj.speed = 10;
console.log(obj.speed);
```


16. What will be the output of this code?

```js
obj.move();
console.log(obj.x);
```


17.	Write JS code that adds a function called `moveBack()` to `obj` that decreases obj's `x` and `y` values by 1.


18.	 Is this legal or will it cause an error?

```js
const x = {name: "Fred"};
x.name = "Mary";
x = {name: "Jane"};
```


19.	What is an immediately invoked function expression (IIFE – pronounced "iffy") and what is the rimary advantage of using one? 


20.	Write an example of an immediately invoked function expression (IIFE – pronounced "iffy") below. 


21)	What are some advantages of using JavaScript modules? (both ES5 & ES6)














22)	 Convert obj in question #14 above to an ES6 class named Mover. Give it a constructor that takes x and y as values. Give it move() and moveBack() methods.




















23)	 Extend the Mover class with a class named RoadRunner. The RoadRunner constructor accepts x, y and speed arguments. Give it a beepBeep() method that logs out “Beep Beep1” when called. 














24)	 Create an object literal named car that has the properties color, speed and drive. Color should be set to red. Speed should be set to zero. Drive should be a function that changes speed to 55.


















25)	Why did we use a second canvas in the Paint ICE? What is an advantage of having multiple canvases sometimes?








26)	Write a line of code that sets the fill style of canvas to green. Assume the 
 canvas context is in scope and called ctx.





27)	Write a line of code that sets the stroke style of canvas to red. Assume the 
 canvas context is in scope and called ctx.




28)	Write a line of code that draws a 200 wide, 200 high rectangle at 100x, 150y. Assume the canvas context is in scope and called ctx.





29)	Write a line of code that creates a circle in canvas at 100x, 150y that has a radius of 50. Assume the canvas context is in scope called ctx.




 
30)	 Write a line of code that rotates the canvas context by 2 radians. Assume the 
 canvas context is in scope and called ctx.






 
31)	 What do ctx.save() and ctx.restore() do in canvas?




















32)	 Given the following code, what color will the rectangle be on canvas?

let canvas = document.querySelector('canvas');              	
let ctx = canvas.getContext('2d');
 
ctx.fillStyle="blue";
ctx.save();
ctx.fillStyle="red";	
ctx.save();
ctx.fillStyle="black";
ctx.save();
ctx.fillStyle="yellow";

ctx.restore();
ctx.restore();
ctx.fillRect(20,20,100,100);









33)	 What are raster-based images?





34)	What are vector-based images?






35)	Is canvas raster or vector based?






36)	There are five buckets of water. Each bucket can contain 1, 2, 3, 4 or 5 ounces of water. The number of ounces in each bucket is tracked sequentially by the buckets array. Write JS code to find which buckets have at least a 2 ounce difference from the bucket before them AND the bucket after them, then print it out. 

The correct values in this example are 2 and 5. The bucket with 2 ounces has a two ounce difference from the previous bucket (4 ounces) and a three ounce difference from the following bucket (5 ounces). The bucket with 5 ounces has a three ounce difference from the previous bucket (2 ounces) and a four ounce difference from the following bucket (1 ounce).

Your code should work regardless of the numbers in this array, but the correct answer is in this example is 2 and 5. 

let  buckets  = [ 3, 4, 2, 5, 1 ];




37)	 Explain Object.create() and prototypical inheritance



38)	 Explain what Object.assign() does

## HTML5 Canvas Cheatsheet
---

### Canvas Element
##### Attributes

|Name| Default|
|----|--------|
|width| 300|
|height| 150|

##### Usage:

```html
<canvas id="tutorial" width="150" height="150"></canvas>
```

***
##### Methods
|returns| Name |
|-------|------|
|Object |getContext(string contextid)|


##### Usage
```javascript
var canvas = document.getElementById('canvas');
var ctx = canvas.getContext('2d');
```

__More at [MDN][1]__

---
___
### Colors and style
##### Attributes

|Name  |Type|Default|Function|
|------|----|-------|--------|
|fillStyle| any| black|Sets the style used when filling shapes|
|strokeStyle| any| black|Sets the style for shapes' outlines|


##### Usage
```javascript
ctx.fillStyle = "orange";
ctx.strokeStyle = "rgb(255,165,0)";

// Assigning transparent colors to stroke and fill style
ctx.fillStyle = "rgba(255,0,0,0.5)";
ctx.strokeStyle = "rgba(255,0,0,0.5)";
```

__More at [MDN][1]__

***

##### Methods
|returns| Name | Function |
|-------|------|----------|
|void |createLinearGradient(x1, y1, x2, y2)|Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2)|
|void |createRadialGradient(x1, y1, r1, x2, y2, r2)|Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2|
|void |addColorStop(float offset, string color)|Creates a new color stop on the gradient object|

##### Usage

```javascript
var ctx = document.getElementById('canvas').getContext('2d');

// Create gradients
var lingrad = ctx.createLinearGradient(0,0,0,150);
lingrad.addColorStop(0, '#00ABEB');
lingrad.addColorStop(0.5, '#fff');
lingrad.addColorStop(0.5, '#26C000');
lingrad.addColorStop(1, '#fff');

var lingrad2 = ctx.createLinearGradient(0,50,0,95);
lingrad2.addColorStop(0.5, '#000');
lingrad2.addColorStop(1, 'rgba(0,0,0,0)');
```

__More at [MDN][1]__


---

---
### Paths
##### Methods
|returns| Name |Function|
|-------|------|--------|
|void |beginPath()|Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up|
|void |closePath()|Closes the path so that future drawing commands are once again directed to the context.
|void |fill()|Draws a solid shape by filling the path's content area|
|void |stroke()|Draws the shape by stroking its outline|
|void |clip()|
|void |moveTo(x, y)|Moves the pen to the coordinates specified by x and y|
|void |lineTo(x, y)|Draws a line from the current drawing position to the position specified by x and y|
|void|arc(x, y, radius, startAngle, endAngle, anticlockwise)| Draws an arc|
|void|quadraticCurveTo(cp1x, cp1y, x, y)|     Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y|
|void|bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)|     Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y)|

##### Usage

```javascript
var canvas = document.getElementById('canvas');
var ctx = canvas.getContext('2d');

// Quadratric curves example
ctx.beginPath();
ctx.moveTo(75,25);
ctx.quadraticCurveTo(25,25,25,62.5);
ctx.quadraticCurveTo(25,100,50,100);
ctx.quadraticCurveTo(50,120,30,125);
ctx.quadraticCurveTo(60,120,65,100);
ctx.quadraticCurveTo(125,100,125,62.5);
ctx.quadraticCurveTo(125,25,75,25);
ctx.stroke();


// Quadratric curves example
ctx.beginPath();
ctx.moveTo(75,40);
ctx.bezierCurveTo(75,37,70,25,50,25);
ctx.bezierCurveTo(20,25,20,62.5,20,62.5);
ctx.bezierCurveTo(20,80,40,102,75,120);
ctx.bezierCurveTo(110,102,130,80,130,62.5);
ctx.bezierCurveTo(130,62.5,130,25,100,25);
ctx.bezierCurveTo(85,25,75,37,75,40);
ctx.fill();
```

__Draw a triangle__

```javascript
var canvas = document.getElementById('canvas');
var ctx = canvas.getContext('2d');
ctx.beginPath();
ctx.moveTo(75,50);
ctx.lineTo(100,75);
ctx.lineTo(100,25);
ctx.fill();
```

__More at [MDN][1]__

---

---

### Rectangles
##### Methods
|returns| Name | Function |
|-------|------|----------|
|void |clearRect(x, y, width, height)|Draws a filled rectangle|
|void |fillRect(x, y, width, height)|Draws a rectangular outline|
|void |strokeRect(x, y, width, height)|Clears the specified rectangular area|

##### Usage
```javascript
var canvas = document.getElementById('canvas');
var ctx = canvas.getContext('2d');
ctx.fillRect(25,25,100,100);
ctx.clearRect(45,45,60,60);
ctx.strokeRect(50,50,50,50);

```

__More at [MDN][1]__

---

---
### Text
##### Attributes

|Name  |Type|Default|
|------|----|-------|
|font| string| 10px sans-serif|
|textAlign| string| start|
|textBaseline| string| alphabetic|

---

---

####References:

1. [Canvas Tutorials: Mozilla Developer Network][2]

2. [Webmastersucks.com HTML5 Cheatsheet][1]

[1]: http://www.webmastersucks.com/uploads/HTML5_Canvas_Cheat_Sheet.png
[2]: https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Canvas_tutorial?redirectlocale=en-US&redirectslug=Canvas_tutorial
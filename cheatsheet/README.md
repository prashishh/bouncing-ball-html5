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

---
___
### Colors and style
##### Attributes

|Name  |Type|Default|
|------|----|-------|
|fillStyle| any| black|
|strokeStyle| any| black|

***

##### Methods
|returns| Name |
|-------|------|
|void |addColorStop(float offset, string color)|

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
|void| arc(x, y, radius, startAngle, endAngle, anticlockwise)| Draws an arc|


##### Usage

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
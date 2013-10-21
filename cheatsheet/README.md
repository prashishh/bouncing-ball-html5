## HTML5 Canvas Cheatsheet
---

### Canvas Element
##### Attributes

|Name| Default|
|----|--------|
|width| 300|
|height| 150|
***
##### Methods
|returns| Name |
|-------|------|
|Object |getContext(string contextid)|

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
|returns| Name |
|-------|------|
|void |beginPath()|
|void |closePath()|
|void |fill()|
|void |stroke()|
|void |clip()|
|void |moveTo(float x, float y)|
|void |lineTo(float x, float y)|

---

---

### Rectangles
##### Methods
|returns| Name |
|-------|------|
|void |clearRect(float x, float y, float w, float h)|
|void |fillRect(float x, float y, float w, float h)|
|void |stroleRect(float x, float y, float w, float h)|

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

##### Methods
|returns| Name |
|-------|------|
|void |clearRect(float x, float y, float w, float h)|
|void |fillRect(float x, float y, float w, float h)|
|void |stroleRect(float x, float y, float w, float h)|

---

---

####References:

1. [Canvas Tutorials: Mozilla Developer Network][2]

2. [Webmastersucks.com HTML5 Cheatsheet][1]

[1]: http://www.webmastersucks.com/uploads/HTML5_Canvas_Cheat_Sheet.png
[2]: https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Canvas_tutorial?redirectlocale=en-US&redirectslug=Canvas_tutorial
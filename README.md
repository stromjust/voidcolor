![voidcolor](/assets/voidcolor_logo.png)

Voidcolor is a Node.js package created for simulating various color blindness types.

###### Usage:
\
Install package
```
npm install --save voidcolor
```
\
Import package
```javascript
const voidcolor = require('voidcolor');
```
\
__Anopia__\
Simulate complete color blindness
```javascript
let r = 255, g = 50, b = 0;

voidcolor.deuteranopia(r, g, b);
voidcolor.protanopia(r, g, b);
voidcolor.tritanopia(r, g, b);
voidcolor.achromatopsia(r, g, b);
```
\
__Anomaly__\
Simulate partial color blindness\
_0 - normal vision, 1 - complete color_ blindness
```javascript
let r = 255, g = 50, b = 0;
let severity = 0.5;

voidcolor.deuteranomaly(r, g, b, severity);
voidcolor.protanomaly(r, g, b, severity);
voidcolor.tritanomaly(r, g, b, severity);
```

_Note: the return is always {r, g, b} object_

\
Example
```javascript
const voidcolor = require('voidcolor');

const color = voidcolor.deuteranopia(230, 10, 10);

console.log(color.r);
console.log(color.g);
console.log(color.b);
```
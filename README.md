# sidenotes.js
![Bower version](https://img.shields.io/bower/v/sidenotes.js.svg?style=flat)
[![npm version](https://img.shields.io/npm/v/sidenotes.js.svg?style=flat)](https://www.npmjs.com/package/sidenotes.js)
[![Build Status](https://travis-ci.org/bcorreia/sidenotes.js.svg?branch=master)](https://travis-ci.org/bcorreia/sidenotes.js)

Add sidenote capabilities to your page.<br />
[**Demo**](http://bcorreia.com/projects/sidenotes.js/src/demo.html)

---
## Getting Started
You may install sidenotes.js using package managers, or download project [archive](https://github.com/bcorreia/sidenotes.js/archive/master.zip).<br />
Installing via `bower` will bring in the dependencies as well.
```bash
bower install sidenotes.js
npm install sidenotes.js

# sidenotes.min.js           minified version of sidenotes.js
```

## Usage
```javascript
var note = new Sidenotes(document.querySelector('.page'));
```

### Callbacks
```javascript
onBefore: function(event, element) {}   // called before animation starts
                                        // event: open, close
                                        // element: `.sidepanel` node

onAfter: function(event, element) {}    // called after animation ends
                                        // event: open, close
                                        // element: `.sidepanel` node
```

### HTML data-attribute
Add `data-sidenote` attribute to elements within your document.
```html
<!-- example -->
<a href="#" data-sidenote="A feeling of surprise … ">Wonder</a>
```

### CSS
Add prefixes accordingly.
```css
/* required */
.sidenote-open body     { transform: translateX(-400px); transition: transform .5s; overflow-y: hidden; }
.sidenote-close body    { transform: translateX(0); transform .75s; transition: }
.sidenote               { translateX(400px); display: flex; align-items: center; justify-content:center; }

/* recommended */
.sidenote               { position: fixed; right: 0; height: 100vh; width: 400px; border-left:1px solid #333; }
```
---

## License
This software is free to use under the [MIT license](https://github.com/bcorreia/sidenotes.js/blob/master/license.md).

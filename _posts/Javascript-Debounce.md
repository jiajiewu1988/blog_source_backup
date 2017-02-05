---
title: 'Javascript Debounce'
date: 2017-02-04 22:24:33
tags:
---

[David Walsh: Debounce](https://davidwalsh.name/javascript-debounce-function)

**debounce function** is used to optimize web performance when there are events get fired frequently.

A **debounce function** limits the rate which a function can fire.

For example, we can limit an event handler to fire at every interval, instead of the handler getting fired when the event is fired.

Code example from *David Walsh Blog*

``` javascript
// Returns a function, that, as long as it continues to be invoked, will not
// be triggered. The function will be called after it stops being called for
// N milliseconds. If `immediate` is passed, trigger the function on the
// leading edge, instead of the trailing.
function debounce(func, wait, immediate) {
	var timeout;
	return function() {
		var context = this, args = arguments;
		var later = function() {
			timeout = null;
			if (!immediate) func.apply(context, args);
		};
		var callNow = immediate && !timeout;
		clearTimeout(timeout);
		timeout = setTimeout(later, wait);
		if (callNow) func.apply(context, args);
	};
};
```

Example of **debounce function** call:

``` javascript
var myEfficientFn = debounce(function() {
	// All the taxing stuff you do
}, 250);

window.addEventListener('resize', myEfficientFn);
```
In this case, we limit the handler *myEfficientFn* to fire after 250 ms when every *resize* event gets fired, instead of immediately after the *resize* event get caught. 

Therefore, **debounce** function help to improve web performance in such cases.
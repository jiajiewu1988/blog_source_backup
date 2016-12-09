---
title: 'JavaScript: append, appendChild, and innerHTML'
categories:
  - Web
date: 2016-12-08 18:29:11
tags:
---


There are several ways to add nodes to DOM, **jQuery.append**, **Node.appendChild**, and **Node.innerHTML** are 3 major ways that are being used to add nodes to a DOM element.

## append()
[jQuery Documentation](http://api.jquery.com/append/)

*append()* offers a convenient way to insert nodes into DOM object. We can either pass in a string or a DOM element. If passing in a string, the string has to be in valid html or xml format.

*append()* and *appendTo()* perform the same task. **Difference** is the placement of content and target.

Source Code:
```js
append: function() {
    return this.domManip( arguments, function( elem ) {
        if ( this.nodeType === 1 || this.nodeType === 11 || this.nodeType === 9 ) {
            var target = manipulationTarget( this, elem );
            target.appendChild( elem );
        }
    });
}
```

## appendChild()
[MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)

The **Node.appendChild()** method adds a node to the end of the list of children of a specified parent node.

Note that if a node you want to append already exists in DOM, *appendChild()* first removes the node from it's original place, then append it to the new place.

## innerHTML
[MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)

The **Element.innerHTML** property sets or gets the HTML syntax describing the element's descendants.

## append() V.S. appendChild() V.S. innerHTML
*append()* is a extension of *appendChild()* as we can see from *append()*'s source code. *append()* is more flexible because it can take either html string and DOM element. 

<span style="background-color:#ea8b54">*innerHTML* is different from *appendChild()*. Everytime, when the *innerHTML* is changed, browser does a complete rebuild of the content of the target element.</span>

<span style="background-color:#54bbea">*appendChild()* does not cause a complete rebuild of the DOM.</span>

Resources:
- [http://stackoverflow.com/a/2305677/1155155](http://stackoverflow.com/a/2305677/1155155)

## Performance Comparasion
[append, appendChild, and innerHTML benchmark](http://jsben.ch/#/nMElN)



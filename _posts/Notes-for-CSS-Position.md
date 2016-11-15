---
title: Notes for CSS Position
date: 2016-11-14 16:09:29
tags:
- CSS
categories:
- Web
---

## CSS Position Values
- absolute
- relative
- fixed
- static
- sticky (new)

## Browser compatibility for ***sticky*** position
{% asset_img sticky-browser-compatibility.png example %}

## **relative** v.s. **absolute**

Both **relative** and **absolute** are positioned relative to the **nearest positioned ancestor**

**relative** adjusts elements position so they do not overlap each other.

**absolute** does not leave space for the element. Instead, position it at a specific position only relays to its cloest positioned ancestor.


## Reference

[MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
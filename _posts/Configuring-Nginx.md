---
title: Configuring Nginx
date: 2016-12-19 16:32:48
tags:
  - Nginx
categories:
  - Web
---

This is a Study Note of "Nginx Essentials" by ....

### Nginx Directive Value Types

| Value Type     | Format                                | Example of a value |
|----------------|---------------------------------------|--------------------|
| Flag           | [on&#124;off]                         | on, off            |
| Signed integer | -?[0-9]+                              | 1024               |
| Size           | [0-9]+([mM] &#124; [kK])?             | 23M, 12348k        |
| Offset         | [0-9]+([mM] &#124; [kK] &#124; [gG])? | 34G, 256m          |
| Milliseconds   | [0-9]+[yMwdhms]?                      | 30s, 60m           |


---
layout: post
title:  "The HTML5 Canvas Tag"
date:   2019-09-18 05:33:00 -0700
categories: course update
youtubeId: EO6OkltgudE
youtubeId2: k27oMfzx-yo
---

### The Canvas Tag

The HTML5 [Canvas tag](https://www.w3schools.com/tags/tag_canvas.asp) can be used to draw graphics with JavaScript. This is a cool new feature of HTML5, which will not work in older browsers.

Here is a good video to describe how to use this tag:

{% include youtubePlayer.html id=page.youtubeId %}

Another Video that is helpful for this topic can be found here:

{% include youtubePlayer.html id=page.youtubeId2 %}

The interesting part of the Video starts at minute 8:07.

Some Helpful links regarding the Canvas tag can be found here:

* [W3 Schools](https://www.w3schools.com/tags/tag_canvas.asp)
* [W3 Schools updated](https://www.w3schools.com/html/html5_canvas.asp)
* [HTML dot com](https://html.com/tags/canvas/)
* [HTML Canvas Tutorials](https://www.html5canvastutorials.com/tutorials/html5-canvas-element/)

# Special mention of the strokeRect() Method

This will draw a rectangle in a canvas tag with JavaScript

```javascript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.strokeRect(20, 20, 150, 100);
```

The source of this code snippet can be found [here](https://www.w3schools.com/tags/canvas_strokerect.asp).

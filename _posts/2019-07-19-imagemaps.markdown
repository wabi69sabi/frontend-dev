---
layout: post
title:  "How Imagemaps work"
date:   2019-07-19 09:37:00 -0700
categories: course update
---

# Imagemaps are fun

Here are some explanations on the basic mechanics behind imagemaps:

[W3Schools](https://www.w3schools.com/tags/tag_map.asp)

[How to Create](http://www.howtocreate.co.uk/tutorials/html/imagemaps)

In order to create an imagemap these resources are always required:

- an image

- an HTML 'map' tag

- at least one HTML 'area' tag

Each one of these tags has severeal attributes that need to be filled out.

Here is an example:

{% highlight html %}
<img src="example.png" width="145" height="126" alt="Synonym" usemap="#map_name">

<map name="map_name">
  <area shape="rect" coords="0,0,82,126" href="object.htm" alt="Sun">
  <area shape="circle" coords="90,58,3" href="object_two.htm" alt="Mercury">
  <area shape="circle" coords="124,58,8" href="object_three.htm" alt="Venus">
</map>
{% endhighlight %}

### Some links to generate imagemaps

[Image-Maps](https://www.image-maps.com/)

[Imagemap Generator](http://imagemap-generator.dariodomi.de/)

[Image Map Weebly](https://image-map.weebly.com/)

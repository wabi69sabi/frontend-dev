---
layout: post
title:  "Some solutions to the recent JS challenges"
date:   2019-08-25 10:31:00 -0700
categories: course update
youtubeId: eaLKqoB9Fu0
youtubeId2: wiozYyXQEVk
---

### How to access nested values inside a JSON object

We all know what JSON objects look like by now, but here is an additional [link](https://www.shapediver.com/blog/json-objects-explained/) that gives great detail and additional information with examples to JSON objects.

Given the following example:

```javascript
let one = {
	name: "Bo",
	email: "bo@mail.com",
	cars: {
		toyota: "Prius",
		chevy: "corvette"
	}
}
```

I wanted a function that could retrieve the values from the nested ```cars``` object.

Here is one approach that works with simple nested objects:

``` javascript
function retrieve(object, target) {
	if (object[target] != undefined) {
		return object[target];
	} else {
		for ( i = 0; i < Object.keys(object).length; i++) {
			if (object[Object.keys(object)[i]].length === undefined) {
				let temp = object[Object.keys(object)[i]];
				return temp[target];
			}
		}
	}
}
```

But this only works for simple two dimensional Objects. If there are deeper nested objects, a more sophisticated approach is needed.

Here is an example of one such approach:

```javascript
const dig = (obj, target) =>
  target in obj
    ? obj[target]
    : Object.values(obj).reduce((acc, val) => {
        if (acc !== undefined) return acc;
        if (typeof val === 'object') return dig(val, target);
      }, undefined);
```

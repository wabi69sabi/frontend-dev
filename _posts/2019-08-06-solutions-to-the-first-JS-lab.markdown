---
layout: post
title:  "Solutions and explanations to Lab 4 Handout and additional exercises"
date:   2019-08-14 04:13:00 -0700
categories: course update
youtubeId: JfHEtou8qb4
---

# Our first JS funtions

``` javascript
function triangle(x, y) {
    return (x * y)/2;
}

console.log(triangle(3,4));
```

Answer key to number 8 can be found [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Arithmetic).

A list of JS arithmetic operators can be found [here](https://www.w3schools.com/jsref/jsref_operators.asp).

In order to solve number 8 we want to divide any full number by 2 and only if the remainder is equal to zero, should we return true. The way we can achieve this is by using the modulus operator (``` % ```).

This is a video that explains the modulus operator with some examples:

{% include youtubePlayer.html id=page.youtubeId %}

### Solution

``` javascript
function isEven(n) {
  return n % 2 === 0;
}
```

### Age in years, days hours and minutes

``` javascript
function age(year, month, day) {
  var now = new Date();
  var bday = new Date(year, (month - 1), day);
  var age_in_ms = now - bday;
  var seconds = age_in_ms / 1000;
  var minutes = seconds / 60;
  var hours = minutes / 60;
  var days = hours / 24;
  var years = days / 365; // this line is problematic as the accuracy is not 100 percent

  console.log("You are " + Math.floor(years) + " years, \n or " + Math.floor(days) +
    " days, \n or " + Math.floor(hours) + " hours, \n or " + Math.floor(minutes) + " minutes old." );
}
```

### Fibonacci

``` javascript
function fib(n) {
  var a = 0;
  var b = 1;
  console.log(a);
  console.log(b);
  i = 0;
  while (i < n) {
    var c = a + b;
    console.log(c);
    a = b;
    b = c;
    i ++;
  }
}
```

There are many alternative ways to solve Fibonacci, and one of the most basic one is perhaps this approach:

``` javascript
function fib(n) {
  var ar = [0, 1];

  for (var i = 0; i < n; i++) {
    ar.push(ar[i + 1] + ar[i])
  }
  console.log(ar);
}
```

For anyone more interested in the time complexity of Fibonacci in JS, you can read [this](https://medium.com/developers-writing/fibonacci-sequence-algorithm-in-javascript-b253dc7e320e) blog post.

### More Advanced challenges

The sort algorithm was supposed to be sorted without the built in .sort function. So the bubble sort method comes to mind. This is a basic implementation in JS:

``` javascript
function bubbleSort(array) {
  for (var i = (array.length - 1); i >= 0; i--) {
    for (var j = (array.length - i); j > 0; j--) {
      if (array[j] < array[j - 1]) {
        var store = array[j];
        array[j] = array[j - 1];
        array[j - 1] = store;
      }
    }
  }
  return array;
}
```

A good blog post to read regarding this algorithm can be found [here](https://codingmiles.com/sorting-algorithms-bubble-sort-using-javascript/).

The count algorithm can be implemented in various ways, but one good solution is here:

``` javascript
function count(ar) {
  res = {};
  ar.forEach(function(element, i) {
      var temp = 1;
      if (!res[element]) {
        res[element] = [i];
      } else {
        res[element].push(i);
      }
  });
  return res;
}
```

The correct value still needs to be extracted.

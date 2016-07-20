---
layout: post
title: Moving to Arrow Functions
---

Progressing from the old way of looping through an array toward arrow functions.

Old way
{% highlight js %}
var nums = [1, 2, 3, 4, 5, 6],
    dblNums = [];

for (var i = 0, len = nums.length; i < len; i++) {
  dblNums[i] = nums[i] * 2;
}
{% endhighlight %}

Using the map function
{% highlight js %}
var nums = [1, 2, 3, 4, 5, 6],
    dblNums = nums.map(function(n) {
      return n * 2;
    });
{% endhighlight %}

Using an arrow function in the map function
{% highlight js %}
var nums = [1, 2, 3, 4, 5, 6],
    dblNums = nums.map(n => n * 2);
{% endhighlight %}
---
layout: post
title:  Tackling FreeCodeCamp's Basic Algorithm Scripting Challenges
date: 2016-01-20 23:22:00
disqus: y
---

Last time I checked in, I was about halfway through FreeCodeCamp's Javascript teaching exercises. Since then, I've made it all the way to the Basic Algorithm Scripting Challenges. Here are my solutions to the first few of them:

## Reverse a String 

This was pretty straghtforward. You're given a string, and have to reverse it. There is no "reverse string" method in Javascript, but there is a reverse-array method. So you need to turn the string into an array.

To do that, you use the **split()** method and put**''** between the parentheses (no space between them) to denote that you want to the split to take place between characters. At that point, your input string ("hello") would look like **['h','e','l','l','o']**.

You then use the **reverse()** method to reverse the contents of the array (now: **['o','l','l','e','h']**). Finally, use **join()** to merge each of the array elements together into a string. You'll want to put **''** between the parentheses again to indicate that you do not want spaces between the letters.

Here is my solution to **Reverse a String**:

{% highlight ruby %}
function reverseString(str) {
  revStr = str.split('').reverse().join('');
  return revStr;
}
reverseString("hello");
{% endhighlight %}


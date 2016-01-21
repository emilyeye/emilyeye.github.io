---
layout: post
title:  Tackling FreeCodeCamp's Basic Algorithm Scripting Challenges
date: 2016-01-20 23:22:00
disqus: y
---

Last time I checked in, I was about halfway through FreeCodeCamp's Javascript teaching exercises. Since then, I've made it all the way to the Basic Algorithm Scripting Challenges. Here are my solutions to the first few of them:

## Reverse a String 

This was pretty straghtforward. You're given a string, and have to reverse it. There is no "reverse string" method in Javascript, but there is a reverse-array method. So you need to turn the string into an array.

To do that, use the **split()** method and put**''** between the parentheses (no space between them) to denote that you want to split the string between characters. On the flip side of this treatment, your input string ("hello") would look like **['h','e','l','l','o']**.

Then use the **reverse()** method to reverse the contents of the array (now: **['o','l','l','e','h']**). Finally, use **join()** to merge each of the array elements together into a string. You'll want to put **''** between the parentheses again to indicate that you do not want spaces between letters.

Here is my solution to **Reverse a String**:

{% highlight ruby %}
function reverseString(str) {
  revStr = str.split('').reverse().join('');
  return revStr;
}
reverseString("hello");
{% endhighlight %}

## Factorialize a Number

If you're like me and forgot what "factorial" means, check out this brief video:

[![a quick factorial refresher video](http://img.youtube.com/vi/EyQXHRHtTFk/0.jpg)](https://youtu.be/EyQXHRHtTFk "Pre-Calcuulus - what is a factorial")

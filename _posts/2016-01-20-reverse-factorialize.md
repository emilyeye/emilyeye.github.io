---
layout: post
title:  FreeCodeCamp basic algorithm challenges - Reverse a String and Factorialize a Number
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

[![a quick factorial refresher video](http://img.youtube.com/vi/EyQXHRHtTFk/0.jpg)](https://youtu.be/EyQXHRHtTFk "Pre-Calcuulus - what is a factorial").

I chose to solve this challenge with a **while loop** although I suppose a **for loop** could have worked as well. Let me explain how this works using a real example.

4! translates to 1 * 2 * 3 * 4

To do this:
1. Create a variable that increments from 1 up to and including the input number. In my solution below, I use ```i``` for this. (In the example above, this variable will serve as the 1, 2, 3, and 4)
2. Create a variable that holds the current value at each step of the factorial. In my solution below, this is ```factorial```. (In the example above, this variable will hold the value of 1 * 2 (2). After being multiplied by 3, it will store the new value (6). Afer being multiplied by 4, 
3. Multiply ```i``` by ```factorial```, store the product as ```factorial```, increment ```i``` by 1 (one), and repeat until ```i``` is equal to the input number.

Note: You need to start with 1, no matter what, because the result of the factorializing process must equal at least 1. (If you want an explanation of why 0! = 1, [read this](http://mathforum.org/library/drmath/view/57128.html)). So that is why both ```i``` and ```factorial``` (or whatever your variables are called) need to be set at 1 (one), not 0 (zero).

Here is my solution to **Factorialize a Number**:

{% highlight ruby %}
function factorialize(num) {
  var i = 1;
  var factorial = 1;
  while (i <= num) {
    factorial *= i;
    i++;
  }
  return factorial;
}

factorialize(2);
{% endhighlight %}

If this helped you out (or if you have any questions), leave a comment below! Next time, I'll be writing about "Check for Palindromes" and rabbit holes.

---
layout: post
title:  What does a good solution look like? FreeCodeCamp's "Find the longest word" challenge.
date: 2016-01-22 20:00:00
disqus: y
---

I had a fun time with the "Find the longest word in a string" challenge.

## A bad solution that passes the tests

My brain works differently than other people's. Sometimes, that's a good thing. Sometimes not.

Here, take a look at my code. This is the first solution I came up with.

	{% highlight css %}
	#container {
	  float: left;
	  margin: 0 -240px 0 0;
	  width: 100%;
	}
	longestWordLength = function(str) {
		var longestWord = "";
		var arrayedStr = str.split(' '); // add replace method
		
		for (var i = 0; i <= brk.length; i++) {
			if brk[i].length > longestWord.length {
				longestWord = brk[i];
			}
		}
		return longestWord.length;
	}

	longestWordLength("I am a banana");
	{% endhighlight %}
	
You may have come at this challenge from a totally different way, so here is what the code does:
1. 
2. 
3. 
4. 
5. 

### Why this solution works

* **It satisfies the conditions.** The challenge is looking for the biggest word's length, not the biggest word itself, so once you've found the numerical value of each word, you can play with the numbers however you like
* **It's simple.** No troublesome comparisons or loops are needed -- you know that whatever the longest word is, its value will be shifted (or popped, if you prefer).
* **It practices new skills.** The last portion of FreeCodeCamp's JavaScript teaching exercises are very loop-heavy. This solution, in avoiding loops, forces you to learn how the sort() and shift() syntax works.
* **It's creative.** As of the time of this writing, the FreeCodeCamp wiki does not list the above as a possible solution.

Why shift instead of pop?

### Why this solution misses the point

1. **It's _too_ simple.** With this method, there is no way to link word length to the word itself. Once the array elements are converted to numbers, this solution divorces the two necessarily and completely. Below, I'll show what I believe to be a better solution and an adaptation that would allow us to keep the words and lengths associated with one another.

2. **It doesn't really build on the previous algorithm scripting challenges.** The above solution is a departure from what comes before and after this challenge.



## A better solution

I'll just leave this right here...

	{% highlight css %}
	#container {
	  float: left;
	  margin: 0 -240px 0 0;
	  width: 100%;
	}
	longestWordLength = function(str) {
		var longestWord = "";
		var arrayedStr = str.split(' '); // add replace method
		
		for (var i = 0; i <= brk.length; i++) {
			if brk[i].length > longestWord.length {
				longestWord = brk[i];
			}
		}
		return longestWord.length;
	}

	longestWordLength("I am a banana");
	{% endhighlight %}

1. Creates a blank variable longestWord (which will eventually hold our longest word as a string)
2. Takes our string, splits it at the spaces to create an array of individual words, removes all non-letter characters by replacing them with '' (nothing), and assigns the new array to a new variable, arrayedStr.
3. Using a for loop, iterates through each element of our new array
4. Within the for loop, an If statement compares the lengths of the current array element (as determined by the for loop) to the array of the current longest word (again, this variable starts wth a value of "").
4. If the current array element has a longer length than the current longest word, the current array element is assigned to longestWord, replacing the old champion. If the current element isn't longer, nothing happents.

### Why this solution is an improvement

* It satisfies the conditions, in a more flexible way.
* It's still pretty simple, but it's more flexible.
* It practices new skills.
* It builds on the previous algorithm scripting challenges.
* It's a foundation, not an end.


	{% highlight css %}
	#container {
	  float: left;
	  margin: 0 -240px 0 0;
	  width: 100%;
	}
	longestWordLength = function(str) {
		var longestWord = "";
		var arrayedStr = str.split(' '); // add replace method
		
		for (var i = 0; i <= brk.length; i++) {
			if brk[i].length > longestWord.length {
				longestWord = brk[i];
			}
		}
		return longestWord.length;
	}

	longestWordLength("I am a banana");
	{% endhighlight %}
	

## What do you think?

Did this post help you? Confuse you? Do you have a critique or a new perspective? I'd love to hear from you, and might even edit the post to include your feedback.

You can check out my profile on FreeCodeAcademy [here](http://www.freecodecamp.com/emilyeye) to see more of my solutions.
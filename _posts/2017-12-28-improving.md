---
layout: post
title: Improving? + UTF and Unicode...
date: 2017-12-28
---

Today, I finished the Chuck Norris challenge on Codingame. 

I didn't use a new method I could write on today, and even though I solved 100% of the challenge, I have mixed feelings with my performance. I'm proud I did it, but after reviewing the best solutions, I saw that there were methods, and actually higher-order functions I could have used. I knew all the methods & HOF involved. I just didn't think to use them! I mostly used for loops and if statements, resulting in a lengthy solution.

I guess this is a normal stage in the learning process, but it should be temporary. So I'm planning to review the solutions to each of the challenges I've solved there (and should do it also for the already completed Free Code Camp's challenges, especially the difficult ones). Then, when I solve new challenges, I should consider whether I could replace what I plan to do with a HOF. I'm kind of familiar with .filter() because I struggled when I learned about it, but today I simply didn't think about .reduce() and .map()...

Actually today, I learned about codePointAt(), but it turned out it was not relevant for what I was doing. 
Still, I researched a bit to understand the difference between charCodeAt() and codePointAt() See [this discussion on the subject](https://stackoverflow.com/questions/36527642/difference-between-codepointat-and-charcodeat). 

Conclusion is: charCodeAt() returns UTF-16 reference whereas codePointAt() is the unicode. But for most cases in European languages you might not see the difference. It is important when you're working with "non-Basic-Multilingual-Plane characters" (that's how MDN calls them but I don't precisely understand what it means yet, I just guess it refers to a certain type of non-Latin characters.)

This led me to ponder: what's the difference between UTF and Unicode? Well, [read this!!! by Rasmus](http://www.polylab.dk/utf8-vs-unicode.html). 
I'll sum it up as a way to memorize what I've understood. Unicode is a set, or a table, of references, with one reference for each character. what I call reference here is what is actually called "code point", hence the codePointAt() method.
In the other hand, UTF is not a "thing" like a table, it is a process. It's an algorithm that calculate or rather convert 0 and 1 to a string of numbers (or the other way round depending on what you're doing). And this string is the Unicode String.

To remember which is which: UTF stands for "Unicode *Transformation* Format". Transformation => process => algorithm.

---
layout: post
title: Happy Coding Year!
date: 2018-01-01
---

first, a syntactic tip I saw on codewars' best solutions.

For a simple algorithm: 'Return 'Even' if input is even, return 'Odd' if it's odd.'

So you would usually do something like that:

    function even_or_odd(number) {
      if (number % 2 === 0){
      //then you know it's even
      return 'Even';
      }else{
      return 'Odd'}
    }

Well, you can do make it much shorter using *ternary* conditional:

    function even_or_odd(number) {
    return number % 2 ? 'Odd' : 'Even'
    }
    
It works, because non-zero values are TRUE. (Sorry Zero.)
to write it ternary-style, 

* you need a *?* after your condition,
* you need a *:* to separate your two possible result. 
* The first result is the one that has to be returned when the condition is true.

More on ternary [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)

    
============================
    
Back to the mobile end course, I'm seeing the end of it...I've learned to delete an array of photo url from the cache, which involves making the Service worker, the IndexDB and the browser db communicate together. 

Last exercise tomorrow! 

I'll redo all the exercises while taking better notes, because pfiou! that was hard.
    
    

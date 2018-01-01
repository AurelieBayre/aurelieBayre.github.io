---
layout: post
title: Happy Coding Year!
date: 2018-01-01
---

first, a syntactic tip I saw on codewars best solutions.

For a simple algorithm: 'Return 'Even' if input is even, return 'Odd' if it's odd.'

So you would usually do something like that:

    function even_or_odd(number) {
      if (number % 2 === 0){
      //then you know it's even
      return 'Even';
      }else{
      return 'Odd'}
    }

Well, you can do maje it much shorter using *ternary* syntax:

    function even_or_odd(number) {
    return number % 2 ? 'Odd' : 'Even'
    }
    
    It works, because non-zero values are TRUE. (Sorry Zero.)
    
    More on ternary [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)
    
    
    ============================
    
    Back to the mobile end course, I'm seeing the end of it.
    
    

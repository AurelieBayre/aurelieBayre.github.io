---
layout: post
title: End of ES6 lesson 1.
date: 2017-01-03
---

Today, I finished learning about for of loop. Actually yesterday I was blocked on a quiz exersise and I couldn't see where the mistake was. 

the for of looked like that: for (day of days)
but inside the loop, I kept referring to days[day] (as in old loop youu refer to days[i]) and of course it didn't worked! 

because I only needed to write *day*. 

So today I finally saw where the mistake was and I was happy to be able to move on.

What learned: Spread and rest operator: ...

I love it! 
 Spread: if you want spill elements out of an array.
 
 
 Rest: if you want to bunddle up elements into an array.
 
 Spread example:
 
        const series = ['Black Books', 'Mr Bean', 'The Office'];
        console.log(...series); //Black Books Mr Bean The Office
        
Rest example:


        function bunddleStufff (...things){
          // so you see that makes an array
          //and you can loop through that array:
          for(const thing of things){
          console.log(thing);
          }
        }
        bunddleStuff('book','phone', 'purse');
        
    I learned function such as bunddleStuff are called *Variadic* Functions.
    Variadic functions take an indefinite amount of arguments. 
    
    That's all folks!

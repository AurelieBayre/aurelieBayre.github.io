---
layout: post
title: End of ES6 lesson 1.
date: 2017-08-03
---

## Grrrr!!!

Yesterday a guy I had never spoken with asked me via twitter to give him the solution to a coding challenge (for the school I will be going to). Just like that! "give me the solution please". 

Not "Can you explain the problem please?" or "I'm blocked, I did this but it doesn't work, what can I do?"

It has happened on several occasions already. I wonder: do guys only do this with women or do they act like that with other guys too?

The thing is I like helping people, and more precisely, empowering people, and I'm hurt when people just want to take advantage of me. I just don't feel recognized for who I am. That is incredibly impolite.

Someone on twitter shared this quote and I really like it:

> "The capacity to learn is gift; the ability to learn is a skill; the willingness to learn is a choice." - Brian Herbert

Ok, back to code:

## for...of

Today, I finished learning about for of loop. Actually yesterday I was blocked on a quiz exersise and I couldn't see where the mistake was. 

the for of looked like that: for (day of days)
but inside the loop, I kept referring to days[day] (as in old loop youu refer to days[i]) and of course it didn't worked! 

because I only needed to write *day*. 

So today I finally saw where the mistake was and I was happy to be able to move on.

## Spread and rest operator: ...

I love it! 
 
 ### Spread: if you want spill elements out of an array.
 
 
 ### Rest: if you want to bunddle up elements into an array.
 
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

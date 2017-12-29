---
layout: post
title: Back to basics
date: 2017-12-29
---

Jotting down some notes. Some are about very basic things, but well. 

*Augmenting strings*

I thought you had to use concat(), but you can do this and it is actually much faster than concat().

    var message = "hello";
    message += " world";
    console.log(message); //hello world
    
*Math.abs()*

It returns the absolute value of a number. It might be useful, if you want to compare numbers regardless of them being positive or negative.

    Math.abs(3); //3
    Math.abs(-3); //3
      
*Syntactic tip*

Using "or" in a variable you have to return. I saw something like this:

      function twoPossibilities(arr) {
      var result = arr[0] || 'nothing, try again!';
      return result;
      }
      twoPossibilities([]); // nothing, try again!
      twoPossibilies([5, 4, 3, 2, 1]); // 5


So basically, if the array is empty, you're returning O but you don't have to write an if statement.
It's cool, isn't it?
  
*Another way to reate arrays*

you want to create an array, with n elements in it:
  
    Array(n); //will create an array with n empty slots!
  
*fill()*

Alright, first time I encounter that one.

First of all, remember it will modify the object you apply it to. = it is a a *mutable* method.

So, you might want to modify an array from start to end with a specific value.

from an already filled array:

    var stuff = [1, 2, 3];
    stuff.fill('hello') // [ "hello", "hello", "hello" ]

from an empty array:

    Array(2).fill(1); //[ 1, 1 ]

Say you have a program that takes a series of input, and you want to store the input in the array: instead of using push() each time you get an input, you can use fill! I saw that in a solution, but I still don't understand the syntax, so I'm still researching.

Also, you can specify the beginning and the end of fill's action.
for example, say you have a fridge filled with lettuce, spinach and pizza, and you want pizza and nothing else!
    
    var fridge = ['lettuce', 'spinach', 'pizza'];
    fridge.fill('pizza', 0, 2); //[ "pizza", "pizza", "pizza" ]


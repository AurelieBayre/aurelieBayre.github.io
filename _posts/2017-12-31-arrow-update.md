---
layout: post
title: Arrow Update
date: 2017-12-31
---

So, I'm finally updating my syntax to ES6.

First, what's ES6?

> it means: *ECMA Script* Edition 6. Aka ES2015 becasuse it was released in June 2015. 
> ECMA is a standard for script languages. Such as JavaScript.

Oh ok.

But what's ECMA?

> It stands for *E*uropean *C*omputer *M*anufacturers *A*ssociation
> It elaborates standards, not only for script languages, but also for, among many other things: 
> * Office Open XML
> * JSON
> * telecommunication standards
> * optical medias


So it was about time I seriously learned about it!

Below are several commented examples to study arrows.

Yes, I had fun writing some of those examples. I think playing is very important when you've got to learn something.

#### The old way:
    const plusTwo = [1, 2, 3].map(function(num){
      return num + 2;
     })
     //console.log(plusTwo); //[3, 4, 5]


#### The new way:

    //Arrows: forget the curly brackets!!!
    const plus3 = [1, 2, 3].map(
        num => num + 3
     );
    //console.log(plus3); //[4, 5, 6]


#### Self Quiz: write that filter function using arrow syntax: 
~~~~~~
 const animalzzz = ['cat', 'tortoise', 'fly', 'dragonfly', 'human', 'boa'];
 //const short = names.filter(function(name) {
 //  return name.length > 6;
 //});

const short2 = animalzzz.filter(
    name => name.length < 4
 );
//console.log(short2); //['cat, 'fly', 'boa']
~~~~~~

## Storing arrow function in a variable

### only ONE parameter

    const truth = name => console.log(`${name}, you are wonderful.`); 
    //use BACKTICKS!!!
    truth('Aurelie');//awwwww thank you!!!!
     
### zero paramesters or parameters >= 2 parameters : use parentheses

~~~~
const insist = () => console.log('I mean it.');
insist(); //stop it!

const alas = (name, forbidden) => console.log(`${name}. You know you can't have ${forbidden}`);
  //BACKTICKS. Use backticks when you're doing those madlibs.
alas('Aurelie', 'pizza'); //why are you so mean?
~~~~

### Are you already missing curly brackets? Here they are again!
### use them for "body block syntax" = when you have more that one line of code in your function.
   
    const alternative = (option1, option2) => { //the curls are here!!!
    option2 = option2.toUpperCase();
    console.log(`But you can have ${option1}, and what's more, ${option2}!!!`);
    };

    alternative('endive salad', 'keto burgers'); 
    //yeah sure but it's not the same...I miss pizza.

That's all folk! Happy new year!

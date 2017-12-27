---
layout: post
title: Conversion and radices
date: 2017-12-27
---

Yesterday and this morning I had to convert data from one numeric system to another.
first case : convert a number from decimal to binary!

For this, use toString(2). toString() is a method you use on a number and it returns a string. If you convert a radix, then the number will be converted to the corresponding numeric system.
Example:

    var num = 5;
    var binary = num.toString(2);
    console.log(binary); //'101'
  
Now let's say you want to work the other way round. You've got a string, a radix, and you want to convert that string into decimal.
In that case, you use parseInt(). Example with a function I wrote for an empireofcode challenge:

    function convert(strNumber, radix) {
    //this function will return -1 if the string cannot be converted into the indicated system.
     if (radix <= 10 && strNumber.match(/[a-z]/i)) {
        return -1;
    }
    
    var result = parseInt(strNumber, radix);

    if (isNaN(result)) {
      return -1;
    }

    var check = result.toString(radix);

    if (check === strNumber){
    return result;
    }
    else{
     return -1;
     }
    }

---
layout: post
title: Merry Christmas and triangles
date: 2017-12-25
---
Hello!

I hope Santa brought you lots of fun presents.

I'm feeling better. Yesterday I solved a few challenges on Codingame and started their Coders Strike Back competition.

Today: more Codingame, aaaand I'm back on empireofcode.

I solved the Triangle Angles challenge on empireofcode!!! And I must say this is no little thing for me because I haven't done math like this in ages. 

So I learned about the different triangle types and then cosinus and tangent and how to convert them to degrees...

My code NEEDS refactoring. (especially for the cosinus things.) But it's a start and I'm happy! :)
I'm saving it here:

    /*
    input : the length of 3 segments
    output: in ascending order, the angles if it's a triangle. Else, output [0, 0, 0]
    */

    function angles(a, b, c){
	function checkRec(x, y, z) {
		if (Math.pow(x, 2) === Math.pow(y, 2) + Math.pow(z, 2)){
		   return true;
		}
		else{
			return false;
		}
	}
	
	function calcRectAngles(opposite, adjacent){
     	var myTan = Math.atan(opposite/adjacent);
        var angle1 = myTan * (180 / Math.PI);
        angle1 = Math.round(angle1);
        var angle2 = 180 - 90 - angle1;
		 console.log(angle1, angle2);
        var result = [];
        result.push(90, angle1, angle2);
        
         result.sort(function (a, b){
                    return a - b;
                     })
             console.log(result);
             return result;
	}

	
	
	// sort sides in descending order
    		var sortedLength = [];
		for (var i = 0; i <arguments.length; i++) {
			sortedLength.push(arguments[i]);
		}
		sortedLength.sort(function (a,b) {
			return b -a;
		})
	//rule out non-triangle cases.
    	var triangle = ( a + b > c) && (a + c > b) && (c + b > a);    
	if (!triangle){ //not a triangle		
		return [0, 0, 0];
		}
	//so it's a triangle. What sort of triangle?
    	else { //equilateral
            if (a === b && a === c && b === c) {            
            return [60, 60, 60];
            }
		//rectangle/egyptian
           if (checkRec(sortedLength[0], sortedLength[1], sortedLength[2])) {
  	 return calcRectAngles(sortedLength[1], sortedLength[2]);
			}
			
	//ok now we need to calculate for scalene I think? three different sides, three different angles.		
	if (sortedLength[0] !== sortedLength[1] && sortedLength[0] !== sortedLength[2] && sortedLength[1] !== sortedLength[2]){
		var cosA = ((-Math.pow(sortedLength[2], 2)) + Math.pow(sortedLength[1], 2) + (Math.pow(sortedLength[0], 2))) / (2 * sortedLength[1] * sortedLength[0]);
		var cosB = (Math.pow(sortedLength[2], 2) - Math.pow(sortedLength[1], 2) + Math.pow(sortedLength[0], 2)) / (2 * sortedLength[0] * sortedLength[2]);
		var angle1 = (Math.acos(cosA))* (180 / Math.PI);
		angle1 = Math.round(angle1);
		var angle2 = (Math.acos(cosB)) * (180 / Math.PI);
		angle2 = Math.round(angle2);
		var angle3 = 180 - angle1 - angle2;
		var result = []
		result.push(angle1, angle2, angle3)
		result.sort(function (a, b) {
			return a - b;
			});
		return result;
			}
			
		//Ok what if it's isocele?
		if (sortedLength[0] === sortedLength[1] && sortedLength[0] !== sortedLength[2]) {
			//considering the smallest side is ONLY sortedLength[2]!!! BEWARE.
			if (sortedLength[1] === sortedLength[0]) {
			var cosA = (sortedLength[2]/2) / sortedLength[0]
			var angle1 = (Math.acos(cosA))* (180 / Math.PI);
			angle1 = Math.round(angle1);
			var angle2 = 180 - (angle1 * 2);
			return [angle2, angle1, angle1]
			}

		}
		else if (sortedLength[1] === sortedLength[2]) {
			var cosA = (sortedLength[0]/2) / sortedLength[2]
			var angle1 = (Math.acos(cosA))* (180 / Math.PI);
			angle1 = Math.round(angle1);
			var angle2 = 180 - (angle1 * 2);
			return [angle1, angle1, angle2]
		}
			
	    }
	}

    //uncomment to test:
    //angles(395, 295, 295);


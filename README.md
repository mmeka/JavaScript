# JavaScript

# Data types
Data types; operations; value ranges and precisions; scopes
Number.MAX_VALUE, Number.MIN_VALUE
NOTE that anything over 16 digits in decimal value, precision is lost and the number is rounded off.
<number_variable>.toFixed(12);

# Operators
mathematical, logical
===, ==
!==, !=

# DOM manipulation
document, window objects
document.getElementById(), document.queryForSelectedEleements()
window.location.href, window.location.hostname, window.location.path, window.location.reload(true)
hostory.forward(), history.back(), history.go(2); // to jump forward and backward thru history

# Math library
Math.floor(Math.random()*10)+1)
Math.max(...array1)
Math.max(num1, num2, ...)

# String function
parseInt("10")
parseFloat("10.13")
Number("9")
"string".length
Whitespace characters
Character encoding
Escape characters
Regular Expressions
indexOf()
.split(" ")
.slice(startIndex)
.slice(startIndex, endIndex)
.substr(startIndex, numberOfChars)
.replace(stringToReplace, replacement)
.charAt(index)

# Date library

# Objects
For loop to loop thru properties in an object.

# Arrays
.length
.toString()
.splice()
.valueOf() // to perform toString
.join(<delimiter_value>) // to print all elements as a string with a deliiter
delete array[index]
.sort() // NOTE that sort() works only on strings to sort in alphabetical order. How to reverse sort?
.sort(array,function(x,y){return x-y;})
.concat(<second_array>)
.pop()
.push(element1, element2, ...)
.shift() // deletes first element and moves remaining items forward
.unshift(element) // add element(s) to the beginning and moves remaining items backward

# Functions
function wrapperFunction(function, value) {
  return function(value);
}
Masterize recursion

# New object creation
this, new, constructors

# Console

# Debugging

# Alerts
alert();
var value = prompt("message", default_value);

# Event handling
<a href="JavaScript:void(0)" />
function getChar(event) {
  if(event.which==null) { // For IE browser
    return String.fromCharCode(event.keyCode);
  } else if(event.which==null) { // For any browser other than IE
    return String.fromCharCode(event.which);
  } else {
    return null;
  }
}
var char = getChar(event || window.event); if(!char) return false;

document.body.onmousemove = function(e) {
  var posX = e.pageX;
  var posY = e.pageY;
  if(posX==undefined) {
    posX = e.clientX + document.body.scollLeft + document.documentElement.scrollLeft;
    posY = e.clientY + document.body.scollTop + document.documentElement.scrollTop;
  }
  rvar coordinates = {"positionX": posX, "positionY": posY};
}


# References
https://developer.mozilla.org/en-US/docs/Web/JavaScript
https://www.youtube.com/watch?v=fju9ii8YsGs&t=252s (Derek Benas fundamentals)

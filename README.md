# JavaScript

# Data types
Data types; operations; value ranges and precisions; scopes
Number.MAX_VALUE, Number.MIN_VALUE
NOTE that anything over 16 digits in decimal value, precision is lost and the number is rounded off.
<number_variable>.toFixed(12);

let vs var vs const in scoping? how to we define these scoping for properties inside an object?

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
"regex".test(value)


# Date library

# Objects
Pass-in-by reference.  How to deep copy the objects?
For loop to loop thru properties in an object.
delete object.property
if(object.hasOwnProperty(property)){} // to check for property defined in object, not prototype
if(property in object) {}
if(typeof object[property]!=='function'){}

Constructor#1
function Customer(name, age) {
  console.log('this' + this);
  this.name = name;
  this.age = age;
  this.sayHello = function() {
    console.log('Hello '+this.name);
  }
}
var cust1 = new Customer("customer name", 12); // when called with 'new' keyword, 'this' represents that class and also 'return this;' happens automatically. When 'new' isn't used, 'this' represents Window object.
NOTE that in order to create a static property, shared across all the objects of type Customer, use Customer.prototype.sharedValue1=false;
Customer.prototype.toString = function() { // say hello };

Factory pattern
function createCircle(radius) {
  return {
    radius: radius,
    draw: function() {
      console.log('hiiii);
    }
  };
}
let circle = createCircle(190);


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
How to deep copy the arrays?

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
  var coordinates = {"positionX": posX, "positionY": posY};
}

// on page load
function() {
  var mie = navigator.appname == 'Microsoft Internet Explorer';
  if(!mie) {
    document.captureEvent(Event.MOUSEMOVE);
    document.captureEvent(Event.MOUSEDOWN);
  }
  document.onmousemove = movepos;
  document.onmousedown = mouseDown;
  var positionX = 0;
  var positionY = 0;
  function movepos(e) {
    if(!mie) {
      positionX = e.pageX;
      positionY = e.pageY;
    } else {
      positionX = e.clientX + document.body.scrollLeft;
      positionY = e.clientY + document.body.scrollTop;
    }
    return true;
  }

}();

# References
https://developer.mozilla.org/en-US/docs/Web/JavaScript
https://www.youtube.com/watch?v=fju9ii8YsGs&t=252s (Derek Benas fundamentals)

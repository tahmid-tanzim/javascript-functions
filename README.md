JavaScript Functions
1. What is a Function?
A function is a series of statements that are grouped together into a special package in JavaScript.

2. Function Basics:
Defined with the function keyword
Functions have to be declared
Function name optional	
Function Parameters/Arguments (comma separated)
Function statements
The return statement
Invoking a function

3. Function Declarations:
Traditional Declarations: 
The Function body {}
Name identifier don’t use keywords, check names ~> http://goo.gl/M3f1V7
Comma separated Parameters/Arguments


Definition Expressions:
Assigning functions to expressions
Anonymous functions
Names can be useful
More flexible than expressions
Can be invoked immediately
Can initialize values immediately
Useful when needed once


4. Invoking functions traditionally:
Function Invocation Patterns (First two are most common): 
Functions
Methods
Constructors
Call & Apply methods
Receive arguments & this
Traditional Invocation ~> this parameter bound to global object




5. Using functions as objects:
Methods: a method is nothing more then a function that has been assigned as a property of an object.
What’s an object: an object is nothing more then one of JavaScript’s many data types.
Variables var a = 2; (number | string | boolean)
Lists / Arrays var myList = (‘Hello World’, false, 5);
Objects are flexible ~> can hold any data types / other objects / functions


Invoking Functions as methods: 
The this argument points to the object
Invoke the function using dot notation
the binding of this happens at the invocation time


6. Invoking instances through the constructor: 
Functions can construct objects using the new keyword.
new creates a new instance of the object.
Each new instance has it’s own set of properties.
this argument points to the instance of the object
Constructor names are capitalized.


7. Expanding objects through prototype: If we want to expand the functionality of a constructor by adding a method, We can do that through that constructors prototype object. 

JavaScript is known as Prototypal Inheritance language
Every object can be based on another.
prototype object gives you access.
Multiple objects can inherit a same functionality
All objects inherit properties
Declarations inherit from Function
Function constructor inherits from Object



console.dir(firstStudent)
console.dir(dept)

8. Understanding Call & Apply invocation:
Indirect invocation
Define the value of this argument
Control: this & arguments
Call passes a value, Apply passes an array


9. Using the arguments parameter:
List of elements passed
An Array like object
Numerical index arguments[x]
We can get the arguments.length
We can loop through arguments
Can’t use all array methods


10. Returning values:
Returns an expression
Sort of optional ->By default undefined return
Only in function body
Return sends something back to the caller
Stops execution of the function
We can have more than one return statement
Can return anything like other function or object or nothing
Return statements is auto semicolon insertion


11. Using anonymous closures:
All functions are considered objects in Javascript



12. Understanding variable scope and hoisting:

13. Creating and namespacing modules:
Modules let you reuse code across apps
Namespacing protects variables
Return statement communicates back

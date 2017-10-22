# JavaScript Functions
## 1. What is a Function?
A function is a series of statements that are grouped together into a special package in JavaScript.

## 2. Function Basics:
- Defined with the *function* keyword
- Functions have to be declared
- Function *name* optional	
- Function Parameters/Arguments (comma separated)
- Function statements
- The *return* statement
- Invoking a function

## 3. Function Declarations:
- #### Traditional Declarations: 
    - The Function body {}
    - Name identifier don’t use *keywords*, check names ~> http://goo.gl/M3f1V7
    - Comma separated Parameters/Arguments
        ```javascript 
        // 1. Traditional Declaration
        function plus_01(a, b) {
            let sum = a + b; 
            return sum;
        }
        
        console.log(plus_01(5, 7));
        ```

- #### Definition Expressions:
    - Assigning functions to expressions
    - Anonymous functions
    - Names can be useful
    - More flexible than expressions
    - Can be invoked immediately
    - Can initialize values immediately
    - Useful when needed once
         ```javascript
         // 2. Definition Expressions
         const plus_02 = function(a, b) {
            return console.log(a + b);
         }(10, 25);
         ```

## 4. Invoking functions traditionally:
- #### Function Invocation Patterns (First two are most common): 
    - Functions
    - Methods
    - Constructors
    - Call & Apply methods
- #### Receive *arguments* & *this*
- #### Traditional Invocation ~> *this* parameter bound to global object
     ```javascript
     // 3. Traditional function invocation with arguments & this
     function plus_03(a, b) {
         return (
             console.log(a + b),
             console.log(this),
             console.log(arguments)
         );
     }
        
     plus_03(5, 8);
     ```

## 5. Using functions as objects:
- #### Methods: a method is nothing more then a function that has been assigned as a property of an object.
    - What’s an object: an object is nothing more then one of JavaScript's many data types.
    - Variables var a = 2; (number | string | boolean)
    - Lists / Arrays var myList = ('Hello World', false, 5);
    - Objects are flexible ~> can hold any data types / other objects / functions
        ```javascript
        /*
        4. What an object looks like
             - Start with curly braces
             - Flexible properties        
        */
        const info = {
            id: 1234,
            name: "Tahmid Tanzim",
            active: true,
            links: { 
                blog: "http://blog.something.com",
                email: "tahmid.tanzim@gmail.com"
            }
        };
        ```

- #### Invoking Functions as methods: 
    - The *this* argument points to the object
    - Invoke the function using dot notation
    - the binding of *this* happens at the invocation time
        ```javascript
        // 5. Invoking functions as methods    
        const calc = {
            status: "In Progress",
            plus: function (a, b) {
                return (
                    console.log(this);
                    console.log(a + b);
                    console.log(arguments);
                    console.log(this.status);
                );
            }
        };
        
        calc.plus(2, 5);
        ```

## 6. Invoking instances through the constructor: 
- Functions can construct objects using the *new* keyword.
- *new* creates a new instance of the object.
- Each new instance has it’s own set of properties.
- *this* argument points to the instance of the object
- Constructor names are capitalized.
     ```javascript
    // 6. Invoking instance through the constructor    
    const Student = function () {
        let name;
        let age;
        
        /* If we call within an object will refer that object 
        otherwise will refer to global object */
        return console.dir(this);
    };
    
    // 1st instance of Student object is firstStudent
    const firstStudent = new Student; // `this` refers to Student object.
    firstStudent.name = "Jack";
    firstStudent.age = 15;
    
    // 2nd instance of Student object is secondStudent
    const secondStudent = new Student; // `this` refers to Student object.
    secondStudent.name = "Tom";
    secondStudent.age = 19;        
    
    console.log(Student());
    console.log(firstStudent.name);
    console.log(secondStudent.name);
     ```


## 7. Expanding objects through prototype: If we want to expand the functionality of a constructor by adding a method, We can do that through that constructors prototype object. 

JavaScript is known as Prototypal Inheritance language
Every object can be based on another.
prototype object gives you access.
Multiple objects can inherit a same functionality
All objects inherit properties
Declarations inherit from Function
Function constructor inherits from Object



console.dir(firstStudent)
console.dir(dept)

## 8. Understanding Call & Apply invocation:
Indirect invocation
Define the value of this argument
Control: this & arguments
Call passes a value, Apply passes an array

## 9. Using the arguments parameter:
List of elements passed
An Array like object
Numerical index arguments[x]
We can get the arguments.length
We can loop through arguments
Can’t use all array methods

## 10. Returning values:
Returns an expression
Sort of optional ->By default undefined return
Only in function body
Return sends something back to the caller
Stops execution of the function
We can have more than one return statement
Can return anything like other function or object or nothing
Return statements is auto semicolon insertion

## 11. Using anonymous closures:
All functions are considered objects in Javascript

## 12. Understanding variable scope and hoisting:

## 13. Creating and namespacing modules:
Modules let you reuse code across apps
Namespacing protects variables
Return statement communicates back

# Context, scope & hosting

Scope is function-based while context is object-based. In other words, scope pertains to the variable access of a function when it is invoked and is unique to each invocation. Context is always the value of the this keyword which is a reference to the object that “owns” the currently executing code.

Execution Contexts: A wrapper to help manage the code that is running. The wrapper can  
contain things beyond what you've written in your code.

Scope on the other hand defines the way JavaScript resolves a variable at run time. There is only two scopes in JavaScript -- global and function scope. Moreover, it also deals with something called "scope chain" that makes closures possible.

Global: means not inside a function.

Creation Phase a.k.a. Global Execution Context when running code at the base level, the  
JS engine will automattically do the following:

1. Creates a global object. Your code will sit inside of this global object.
2. Creates a special variable called, "this". At the global level, "this" would equal the
   Global \(window\) Object.
3. A reference or link to the outer environment if there is one.
4. Hoisting, which setups up functions and creates a list of variables \(but sets them all to
   "undefined"\). Example code is below.
5. Then JS will run your code line by line \(which includes adding values to variables, thus
   replacing the "undefined".

Name/Value Pair: A name which maps to a unique value. And a value can be more  
name/value pairs. Those are called objects.

Object: A collection of name/value pairs.

All variables are setup initially as undefined in js.

Scope, ES6, And let

Scope: is where your variable is available in your code. And if it's truly the same variable, or  
a new copy.

let & const does not hoist the variable to the top of the block

Objects and the Dot  
What values \(or properties\) can an object have?  
1. Primitive type  
2. Another object  
3. A function \(or a "method" when sitting in the object\)  
JS will build a set of references \(or addresses\) to link a core object and it's properties and  
keep it memory.

Object literal: is a comma-separated list of name-value pairs wrapped in curly braces. This  
is considered a faster approach to creating objects.

Namespace: is a container for variables and functions. It keeps variable names from being  
overwritten. JS does not specifically use namespaces like other languages do, but we can  
do something like it using object notations

Functions are Objects

Function Statements and Function Expressions  
Expression: is a unit of code that results in a value. It doesn't have to save to a variable.  
Functions do the work, expressions returns a value.  
What is the difference between a function statement and function expression?  
This is a function statement:  
function greet\(\) {  
console.log\('hi'\);  
}  
Section 4: Objects and Functions  
15  
This function statement does not result in a value. JS runs through and says, "ok, I'll commit  
this to memory, but I won't do anything with it until you tell me."

//

This is a function expression:  
var anonymousGreet = function\(\) {  
console.log\('hi'\);  
}

Notice that this function does not have a name. It is called an anonymous function. How  
do we invoke this function?

var anonymousGreet = function\(\) {  
console.log\('hi'\);  
}  
anonymousGreet\(\);

The parenthesis invoke the function.

//

Immediately Invoked Functions Expressions \(IIFEs\)  
IIFE is when you invoke a function immediately after creating it. You can do this by adding  
parenthesis at the end of your function.

Closures are functions that refer to independent \(free\) variables \(variables that are used  
locally, but defined in an enclosing scope\). In other words, these functions 'remember' the  
environment in which they were created.

call\(\), apply\(\), and bind\(\)


Functions in js are values or First Class Function. This means it can be asigned to a variable or passed as parameter.

Function hoisting only works with function declaration and not with function expression.

Every function creates a new execution context and then it executes the code line by line. After the execution finished, this execution context is poped up from the **execution stack**

###Function scope

Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined. In other words, a function defined in the global scope can access all variables defined in the global scope. A function defined inside another function can also access all variables defined in its parent function and any other variable to which the parent function has access.


###In JavaScript a function can be declared using several ways:

1. Function declaration

A function declaration is made of function keyword, followed by an obligatory function name, a list of parameters in a pair of parenthesis (para1, ..., paramN) and a pair of curly braces {...} that delimits the body code

It is easy to confuse the function declaration and function expression. They look very similar, but produce functions with different properties.

An easy to remember rule: the function declaration in a statement always starts with the keyword function. Otherwise it's a function expression

Some JavaScript environments can throw a reference error when invoking a function whose declaration appears within blocks {...} of if, for or while statements.

2. Function expression

Expression: is a unit of code that results in a value. It doesn't have to save to a variable. 

The function expression creates a function object that can be used in different situations:

Assigned to a variable as an object count = function(...) {...}
Create a method on an object sum: function() {...}
Use the function as a callback .reduce(function(...) {...})

3. Shorthand method definition

Shorthand method definition can be used in a method declaration on object literals and ES6 classes. You can define them using a function name, followed by a list of parameters in a pair of parenthesis (para1, ..., paramN) and a pair of curly braces { ... } that delimits the body statements.

4. Arrow function

The function declared using a fat arrow has the following properties:

The arrow function does not create its own execution context, but takes it lexically (contrary to function expression or function declaration, which create own this depending on invocation)
The arrow function is anonymous: name is an empty string (contrary to function declaration which have a name)
arguments object is not available in the arrow function (contrary to other declaration types that provide arguments object)

5. Generator function
6. Function constructor

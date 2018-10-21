####Hosting Process

1. Stores every function to memory, in their entirety.

2. Stores every variable names to memory, but not the value! Instead JS will set a
placeholder called undefined.

3. JS engine will begin executing every line of code, which includes assigning values to
variables.

Hoisting and var
Variables declared with var are hoisted to the top of the enclosing function scope. If the variable is accessed before declaration, it evaluates to undefined.

Hoisting and let
let variables are registered at the top of the block. But when the variable is accessed before declaration, JavaScript **throws an error: ReferenceError: <variable> is not defined**. From the declaration statement up to the beginning of the block the variable is in a temporal dead zone and cannot be accessed.

Hoisting and const
Constants const are registered at the top of the block. 
The constants cannot be accessed before declaration because of the temporal dead zone. When accessed before declaration, JavaScript **throws an error: ReferenceError: <constant> is not defined**.

const hoisting has the same behavior as the variables declared with let statement 


Hoisting and function declaration
Hoisting in a function declaration allows to use the function anywhere in the enclosing scope, even before the declaration. In other words, the function can be called from any place of the current or inner scopes (no undefined values, temporal dead zones or reference errors).

Hoisting and class
The class variables are registered at the beginning of the block scope. But if you try to access the class before the definition, JavaScript **throws ReferenceError: <name> is not defined**. So the correct approach is first to declare the class and later use it to instantiate objects.
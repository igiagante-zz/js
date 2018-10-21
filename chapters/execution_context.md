The javsacript engine creates a Global Execution Context every time you run some Javascript code.

**Execution Context** is a fancy word for describing the environment in which your Javascript code runs.

####Types of Execution Context

There are three types of execution context in JavaScript.

* Global Execution Context: This is the default or base execution context. The code that is not inside any function is in the global execution context. It performs two things: it creates a global object which is a window object (in case of browsers) and sets the value of this to equal to the global object. There can only be one global execution context in a program.

* Functional Execution Context: Every time a function is invoked, a brand new execution context is created for that function. Each function has its own execution context, but it’s created when the function is invoked or called. There can be any number of function execution contexts.

* Eval Function Execution Context 

####How is the Execution Context created?

Up until now, we have seen how the JavaScript engine manages the execution context, Now let’s understand how an execution context is created by the JavaScript engine.

The execution context is created in two phases: 1) **Creation Phase** and 2) **Execution Phase.**

###The Creation Phase
Before any JavaScript code is executed, the execution context goes through the creation phase. Three things happen during the creation phase:

* Value of this is determined, also known as **This Binding**.
* Lexical Environment component is created.
* Variable Environment component is created.

Now, within the Lexical Environment, there are two components: (1) the **environment record** and (2) a **reference to the outer environment.**

1. The **environment record** is the actual place where the variable and function declarations are stored.
2. The **reference to the outer environment** means it has access to its outer lexical environment.

There are two types of lexical environment:

1. A global environment (in a global execution context) is a Lexical Environment which does not have an outer environment. 
The global environment’s outer environment reference is null. It has global object (window object) and its associated methods and properties (eg. array methods) inside the environment record as well as any user-defined global variables, and the value of this refers to the global object.

2. A function environment, in which the user-defined variables inside the function are stored in the environment record. And the reference to the outer environment can be the global environment, or an outer function environment that contains the inner function.

For function environment, the environment record also contains an arguments object that contains mapping between indexes and arguments passed to the function and the length(number) of the arguments passed into the function


There are also two types of environment record:

1. Declarative environment record stores variables, functions, and parameters. A function environment contains declarative environment record.

2. Object environment record is used to define association of variables and functions appeared in the global execution context. A global environment contains object environment record.


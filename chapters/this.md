#### Function invocation

### `this` in function invocation

  `this` is the **global object** in a function invocation

  `this` is undefined in a function invocation in **strict mode**


### `this` in an inner function

* A common trap with the function invocation is thinking that this is the same in an inner function as in the outer function. 
* The context of the inner function depends only on invocation, but not on the outer function's context.

#### Method invocation

A method is a function stored in a property of an object.

It is important to distinguish function invocation from method invocation, because they are different types. The main difference is that method invocation requires a property accessor form to call the function (obj.myFunc() or obj['myFunc']()), while function invocation does not (myFunc()).

### `this` in method invocation

`this` is the object that owns the method in a method invocation

Ff the method is called without an object, then a function invocation happens: where this is the global object window or undefined in strict mode

Constructor invocation
Constructor invocation is performed when new keyword is followed by an expression that evaluates to a function object

#### Constructor invocation

Constructor invocation is performed when **new** keyword is followed by an expression that evaluates to a function object, an open parenthesis 

### `this` in constructor invocation

`this` is the newly created object in a constructor invocation

#### Indirect invocation

Indirect invocation is performed when a function is called using myFun.call() or myFun.apply() methods.

### `this` in indirect invocation

`this` is the first argument of .call() or .apply() in an indirect invocation

#### Bound function

A bound function is a function connected with an object. Usually it is created from the original function using .bind() method. The original and bound functions share the same code and scope, but different contexts on execution.

Contrary to .apply() and .call() methods, which invokes the function right away, the .bind() method only returns a new function that it supposed to be invoked later with a pre-configured this.

### `this` in bound function

`this` is the first argument of .bind() when invoking a bound function

The role of .bind() is to create a new function, which invocation will have the context as the first argument passed to .bind(). It is a powerful technique that allows to create functions with a predefined this value.

#### Arrow function

`this` is the enclosing context where the arrow function is defined

The arrow function doesn't create its own execution context, but takes this from the outer function where it is defined.


Because the function invocation has the biggest impart on this, from now on do not ask yourself:

`Where is this taken from?`

but do ask yourself:

`How is the function invoked?`

For an arrow function ask yourself:

`What is this where the arrow function is defined?`
#####Creation Phase a.k.a. Global Execution Context 

When running code at the base level the JS engine will automattically do the following:

1. Creates a global object. Your code will sit inside of this global object.
2. Creates a special variable called, "this". At the global level, "this" would equal the
   Global \(window\) Object.
3. A reference or link to the outer environment if there is one.
4. Hoisting, which setups up functions and creates a list of variables \(but sets them all to
   "undefined"\). Example code is below.
5. Then JS will run your code line by line \(which includes adding values to variables, thus
   replacing the "undefined".

> All variables are setup initially as undefined in js.

![Hoisting](./images/hoisting.png "Hoisting")
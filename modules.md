#CommonJS,  AMD (Asynchronous Module Definition)

In JavaScript, the word "modules" refers to small units of independent, reusable code. 
Modules help in keeping the units of code for a project both cleanly separated and organized.

##Ways to create modules:
- The Module pattern (public/private methods and variables inside a single object, thus shielding particular parts from the global scope)
-	Object literal notation (object is described as a set of comma-separated name/value pairs enclosed in curly braces)
-	AMD modules
-	CommonJS modules
-	ECMAScript Harmony modules

JavaScript Harmony will introduce native modules into JavaScript. Until then, there are two competing standards for modules: AMD and CJS Modules.

AMD is designed for browser environments and CommonJS is targeted at server-side environments.

##AMD 
- AMD (Asynchronous Module Definition) format provides a solution for modular JavaScript;
- both the module and dependencies can be asynchronously loaded. 
- Scope: it avoids the need to worry about globals, supports named modules, doesn't require server transformation to function 

**define method** for module definition and a **require method** for handling dependency loading. 

define is used to define named or unnamed modules based using the following signature:
```
define(
    module_id /*optional*/,
    [dependencies] /*optional*/,
    definition function /*function for instantiating the module or object*/
);
```
**require** is used to load code in a top-level JavaScript file or within a module should we wish to dynamically fetch dependencies. An example of its usage is:
```
// Consider "foo" and "bar" are two external modules
// In this example, the "exports" from the two modules
// loaded are passed as function arguments to the
// callback (foo and bar) so that they can similarly be accessed
 
require(["foo", "bar"], function ( foo, bar ) {
        // rest of your code here
        foo.doSomething();
});
```

##CommonJS - A Module Format Optimized For The Server

CommonJS module is a reusable piece of JavaScript which exports specific objects made available to any dependent code. Unlike AMD, there are typically no function wrappers around such modules (so we won't see define here for example).

CommonJS modules  contain two primary parts:
- a free variable named exports which contains the objects a module wishes to make available to other modules 
- a require function that modules can use to import the exports of other modules.
```
// package/lib is a dependency we require
var lib = require( "package/lib" );
 
// behaviour for our module
function foo(){
    lib.log( "hello world!" );
}
 
// export (expose) foo to other modules
exports.foo = foo;
```

##Script Loaders - RequireJS

- Dynamically load scripts after page load.
- Optimization tools (like the RequireJS optimizer) to concatenate scripts is recommended for deployment

"RequireJS is a JavaScript file and module loader. 
It is optimized for in-browser use, but it can be used in other JavaScript environments, like Rhino and Node. Using a modular script loader like RequireJS will improve the speed and quality of your code."

Loading AMD Modules Using RequireJS
```
require(["app/myModule"],
 
    function( myModule ){
        // start the main module which in-turn
        // loads other modules
        var module = new myModule();
        module.doStuff();
});
```

#Resources
- [Learning JavaScript Design Patterns by Addy Osmani](http://addyosmani.com/resources/essentialjsdesignpatterns/book/#modulepatternjavascript)
- [http://requirejs.org/](http://requirejs.org/)
- [AMD versus CJS. What’s the best format?](http://unscriptable.com/2011/09/30/amd-versus-cjs-whats-the-best-format)
- [Understanding JavaScript Modules](https://spring.io/understanding/javascript-modules)

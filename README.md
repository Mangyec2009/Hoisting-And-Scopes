# What is ***Scope*** in **JavaScript**?

JavaScript has the following kinds of scopes:

+ Global Scopes: the default scope for all code running in script mode.
+ Function Scope: The scope created with a function.
+ Block Scope: This scope restricts the variable that is declared inside a specific block, from access by the outside of the block.
+ Module Scope: The scope for code running in module mode.

![](./Pictures/2.png)

If you create one scope inside each another, outer scope will be Globalscope for the insider scope.

You can get data from global scope inside any other scopes, but you cant get data from block or function scopes in global scope.

# What is ***hoisting*** in **JavaScript**?

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

Hoisting in JavaScript is a behavior in which a function or a variable can be used before declaration.

We can do hoisting only in 2 cases:
1. If it is declaration function
2. It is var variables.

One small issue is here, that if you use var initial value forever will be "undefined".

But we can't do it to let and const variables, cuz initial value will be TDZ error - "uninitializated".

TDZ - Temporal Dead Zone
A variable declared with let or const cannot be accessed until it is declared within its scope.

```JavaScript
    let a = 45, b = 23;
    let sum=add(a,b);
    console.log(sum);

    function add(a, b){
        return a + b;
    }

    68  <---------  Output
```
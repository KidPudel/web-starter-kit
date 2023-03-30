In JavaScript, both `let` and `var` are used to declare variables, **_but they have different scoping rules_**.

# `var`
`var` declares a variable globally or locally to a function, but not to a block.   
Variables declared with `var` are **hoisted**, which means that they are moved to the top of their scope and initialized with a value of `undefined` before the code is executed.

For example:

```javascript
function myFunction() {
  var x = 10;
  if (true) {
    var x = 20; // same variable as above
    console.log(x); // 20
  }
  console.log(x); // 20
}
```

> In the example above, the variable `x` is declared twice using `var`, **_but it refers to the same variable, which means that the second assignment overwrites the first one_**.  

# `let`
`let`, on the other hand, declares a **_block-scoped variable, which means that it is only accessible within the block where it is defined_**.  
Variables declared with `let` are **not hoisted**, which means that they cannot be accessed before they are declared.

For example:

```javascript
function myFunction() {
  let x = 10;
  if (true) {
    let x = 20; // different variable than above
    console.log(x); // 20
  }
  console.log(x); // 10
}
```
> In the example above, the variable `x` is declared twice using `let`, but they refer to different variables because they are declared within different blocks.

# In summary
`var` is function-scoped and hoisted, while `let` is block-scoped and not hoisted.   
You should use `let` when you need a variable that is only accessible within a block, and `var` when you need a variable that is accessible within a function or globally.

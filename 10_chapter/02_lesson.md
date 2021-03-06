**WDI Fundamentals Unit 10**

---

# Functions

When you write software you may find yourself writing the same kind of code over and over again. You are about to learn to how to write code that can be re-used. Instead of repeating the same code, you will write re-usable code. To do this you will use **functions**! Functions are _abilities_ (or actions)! Functions must be _defined_ to be used. They must be _called_ to be used; and when they are called, they may _return_ a value to you. Let's define your first function.

## Defining JavaScript Functions

To create a new function, we must *declare* it as we would a variable.  A **function expression** typically looks like this:

```javascript
var nameOfMyFunction = function(x) {
  // Body of the function 'nameOfMyFunction';
}
```

As you can see, the first line begins with `nameOfMyFunction` followed by the word `function`, which is how we'd like to refer to that function later.

Next, we write a list of the input values we'd like to use, enclosed in parentheses and separated by commas. These values are called **parameters** of the function.  Above, we only used one parameter, `x`.

Finally, we write the body of our function, enclosed by a pair of curly braces (`{}`).

We'll focus on using **function expression** for these lessons. Let's look at an example:

Let's look at an example:

```javascript
var tripleIt = function(x) {
  return 3 * x;
}
```

This function takes one parameter – `x`. The body of the function consists of one statement that says to return the parameter of the function (that is, `x`) multiplied by 3.

This is the first time we're seeing a `return` statement – it does exactly what it sounds like it does. `return` gives back the output of the function.

###Naming Functions

Function names should describe what the function does as best as possible, and a general rule of thumb is to keep the name short and simple.

You may have noticed how we capitalize names in JavaScript using the **camelCase** style. Remember that identifiers *(how we name things)* can't use spaces between them.

To make it easier to read a name like `nameofmyfunction`, capitalize the first letter of each word (e.g. `nameOfMyFunction` – see the resemblance to a three-humped camel?)

Examples of naming functions:

- **bad**:  `thisfunctioncalculatestheperimeterofarectangle` (no camelCase, too verbose)
- **bad**:  `my new function` (contains spaces)
- **bad**:  `myNewFunction` (doesn't explain what it does!)
- **good**: `calculatePerimeter` (describes what it does, short, and uses camelCase)


## Calling JavaScript Functions

Declaring a function does not execute the instructions we include in its body. After declaring, we've simply given the function a name and specified how it should work when it is given a set of parameters.

To actually *evaluate* a function, we have to **call** that function as follows:

```javascript
nameOfMyFunction();
```

In the case of `var tripleIt = function(x)`, if we wanted to call the function by passing the value 4, we would write:

```javascript
tripleIt(4)
```

> **NOTE**: The number `4` used when the function is called is known as an **argument**.

The function would execute its statements and evaluate to the value `12`.

Just like a variable, we can use the return value of this function in any expression. For example:

```javascript
var a = tripleIt(1);                         // a === 3
var b = 100 * tripleIt(4);                   // b === 1200
var c = 200 + (tripleIt(20) / tripleIt(10)); // c === 202
```
## Other Ways to Define Your Functions

Function expressions is only one way to define a function in JavaScript. Functions can actually be defined in several ways. Another common method is **function declarations**, which is a function that you can call later in your code. It typically looks like this:

```javascript
function nameOfMyFunction (x) {
  // Body of the function 'nameOfMyFunction';
}
```

But don't worry about this right now. We'll focus on function expressions for now!


### Test Yourself

Suppose that we've defined the function 'glorp' as follows:

```javascript
var glorp = function(someNumber) {
  return someNumber * 5 - 3;
}
```

What will each of the following expressions evaluate to?

* glorp(10)
* 2 * (glorp(5) + 10)
* glorp(1 + 2)
* glorp(glorp(1))

Test your answers in JSBin by copying the function definition into the editor, clicking the 'play' button, and typing each of these expressions into the console.

>**Note**  JavaScript follows order of operations for mathematical expressions. When mathematical operations occur certain operators will be evaluated first. Code inside of a `()` will execute first; then multiplication and division; followed by addition and subtraction. [Further Reading](https://www.mathsisfun.com/operation-order-pemdas.html).

---

## The Return Statement

As mentioned above, `return` specifies the value of the function when it's executed. It has another important job - it tells the function to immediately stop whatever it's doing.

Consider the following program:

```javascript
var doAThing = function(x) {
  if (x > 10) {
    return x + 10;
  }
  return x;
}
```

If `x` is greater than 10, the computer will run the `if` statement and hit that first `return` statement (`x + 10`).

This will *immediately end the function* - that second `return` statement won't be reached.

### Test Yourself

Where will the function stop if `x` is 5? 10? 20? What value will be returned in each case?

```javascript
var categorize = function(x) {
  if (x < 8) {
    return 8;
  }
  x += 3;
  if (x < 15) {
    return x;
  }
  return 100;
}
```

---

[Here's another exercise for you](04_exercise.md) - give it a shot.

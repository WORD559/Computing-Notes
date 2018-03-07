# Programming Paradigms #

A programming paradigm is a style of programming.
Different types of programming need to be tackled in different ways.

## Procedural Programming ##

"Recipe" approach to solving problems. Very straightforward.

## Object-Oriented ##

Models parts of the problem as objects, which have properties and methods.

## Declarative ##

States what needs to be done.
(an example of this is SQL)

## Functional Programming ##

- A functional program describes a series of functions.
- Each function takes in some data as arguments and returns an output.
- Functional programming has a lot in common with mathematics.
- Functional programming is not useful for certain procedures, like making tea.

Functional programming is not totally different from other paradigms which also use functions. However, there are differences, particularly in things which do not happen in functional programming.

### Domain and Co-domain ###

The domain is a set from which the function's input is chosen.

The co-domain is a set from which the function's output is chosen.

A function is a mapping from set of inputs to a set of outputs.

For example, when the domain is -10 to 10, the co-domain of x*x is 0 to 100.

### Types and Typeclasses ###

Functional languages use types, such as: Integer, float, bool, char, etc.

Typeclasses are sets of types. E.g.: `Typeclass Num includes Integer, Float, Double`

Take for example the function `sumOfTwo x y = x + y`

This function would be valid to use for different types. For example, x and y could be int and float. You can choose not to give an explicit type to enable versatility, but you can also limit it to certain types.

### Function Types ###

A function f has a function type:

`f: A -> B`

The function type is A -> B where A is the argument type and B is the result type.

### First Class Objects ###

First class objects:

 - can appear in expressions
 - can be assigned to a variable
 - can be assigned as an argument 
 - can be returned in a function call

Examples: Int, Bool, Float, Char, String, and *Functions*

### Statelessness ###

When you execute a procedural program such as in Python, the computer's memory changes state as it goes along. However, in functional programming, the values of variables cannot change. They are immutable and the program is said to be stateless.

The only thing that a function can do in functional programming is calculate something and return a result. This means there are no side effects. 

A consequence of not being able to change the value of an object is that every time a function is called with the same parameters it will always return the same result. A simple function can be proved to be correct and then used to build more complex functions.

### Function Application ###

Consider a function `add3Integers x y z = x + y + z`

The process of giving particular inputs to a function is called function application. Thus, `add3Integers 3 4 5` represents the application of the function `add3Integers` to the arguments `3`, `4` and `5`. Although we would say that `add3Integers` takes three arguments, it only takes one.

`add3Integers: Int -> Int -> Int -> Int`

This is more accurately written: 

`add3Integers: Int -> (Int -> (Int -> Int))`

So `add3Integers` takes in `3` and applies itself, which creates a function that takes one parameter (`4`) and adds 2. This creates a new function that takes a parameter (`5`) and adds 6.

Each additional argument creates a new function which is applied to the argument.

### Partial Function Application ###

This can be exploited.

Take the function `add x y = x + y`, `add :: Int -> Int -> Int`

Remember that if we type `add 6 4` a function language does `(add 6) 4`

We can use this to simplify functions by fixing or binding an argument. In this case we can define a function: `addSix = add 6`, `addSix :: Int -> Int`

Then `addSix 10` becomes the same as `add 6 10`

This is useful if we only want to pass partial arguments.

### Higher Order Functions ###

A function is higher-order if it takes a function as an argument and/or returns a function as a result.

For example:

 - `map`. Takes a list and the function to be applied to the list made by applying the function to each element of the old list.
 - `filter`. Takes a list and a predicate and returns the elements in the list that satisfy the predicate.
 - `fold` (or `reduce`). Reduces a list to a single value using recursion by applying an operation to each value.

### Heads and tails ###

A list is a collection of elements of a similar type, such as integers, characters, strings, enclosed in square brackets.
A list is composed of a head and a tail. The head is the first element of the list and the tail is the remainder of the list.

```
listA = [1,2,3]
head listA --> 1
tail listA --> [2,3]
```

`null(list)` returns `True` if the list is empty.


To prepend a single element to a list we can use a colon.

`5:[1,2,3] --> [5,1,2,3]`

We can also add a list to an exissting list with `++`

`[5,2]++[1,2,3] --> [5,2,1,2,3]`


To append we use `++` to add a list to the end

`[1,2,3] ++ [4,5] --> [1,2,3,4,5]`


`Length` is used to get the length of the list.


To concatenate two or more lists, we can use concat, which concatenates the elements in the lists to return one element.

## Paradigm Support ##

Many languages support multiple paradigms.
E.g. Python, Delphi, VB all support proceduraland object-oriented.

Others support a single paradigm.
SQL supports declarative.
Haskell supports functional.




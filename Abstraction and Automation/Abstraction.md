# Abstraction #

Computer science is about using mathematical principles to solve problems. It is NOT about how to use a spreadsheet, word processor, graphics package, etc. It involves learning to think computationally and applying the principles of abstraction.

What information is relevant to solving a particular problem?

What computations need to be performed in order to solve the problem?

How can we be sure the problem has been solved?

- Information hiding is one aspect of abstraction that is very useful in all kinds of simulation problems in which the real world is modelled
- All the details that do not contribute to the essential characteristics of the problem are omitted
- The London Underground map is a good example of information hiding
    - The train lines can be seen as this is the important information
    - The surface of London cannot be seen as this isn't too relevant

## Problem Abstraction ##

This involves removing all the details until the problem reduces to one which has already been solved.

- Abstraction is a key feature of programming languages such as Python, Java, and VB.
- Using abstraction, the algorithms used to solve a problem are far removed from the actual machine code instructions that have to be carried out

## Procedural Abstraction ##

- Procedural abstraction is used to keep the actual values used in a computation separate from the overall design.
- In simple terms, this involves writing procedures and passing parameters
- A car dealer might use a procedure for displaying a particular model of car, and pass parameters for colour, number of doors, how many wheels, etc.

## Functional Abstraction ##

- When you call a function to calculate a square root, or generate a random number, abstraction is taken one stage further.
- Using a function does not require you to know anything about how the computation is carried out.
- You simply have to know how to call the function and what parameters to pass.

## Data Abstraction ##

- The data or information that is relevant to solving a problem may be in the form of an abstract data structure such as an array, stack, or queue.
- A stack, for example, is a data structure that allows items to be added to or removed from the top.
- It could be implemented as an array and a pointer to the top of the stack - items do not need to actually be removed from the array or sorted within it.
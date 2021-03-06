# Big O Notation #

Big O is to do with time complexity of an algorithm.

- O(n!)
- O(1)
- O(n)
- O(n^2)
- O(n^3)
- O(2^n)
- O(log2(n))
- O(nlog2(n))

There are some things that are intractible problems, such as factorising a number.


O(1) refers to a program where every line is only run once, much like a formula

O(n) refers to a program where the lines are run n times, for example in a single loop

## Polynomial Time ##

(just about okay!)

O(n^2) refers to a program where the lines are run n^2 times, like a double nested loop. A bubble sort would be O(n^2).

O(n^3), triple nested loop.

------------------

O(n!) refers to a factorial algorithm. Factorial time algorithms are generally intractible.

## Exponential Time ##

O(2^n)

O(log2(n)) could be a binary search, as the time only increases by 1 if your dataset is doubled.

O(n(log2(n))) could be a merge sort.
# Algorithms #

**Problem: Calculate paint required**

- What inputs would you need?
- What decisions does the painter need to make?
- Think out the sequence of instructions, starting with:
    Input the dimensions of the room.
- Use statements like
    Input, calculate, output, add, subtract, multiply, divide
- Or maths symbols like +, -, *, /

1. Measure the width of the walls.
2. Measure the height of the walls.
3. Calculate height * width and store it to area.
4. Until window_width = 0:
5. Measure the width of the window.
6. Measure the height of the window.
7. Area = Area -(window_width * window_height)

When writing pseudocode, try and stick to some sort of de facto standard. Make sure that whatever you're doing in your code is easily understandable and can't be misinterpreted.

Pseudocode is the first thing you should be doing. Your final code should be based on your pseudocode. This applies irl too --you won't be employed if you don't do it properly.

Data types do not necessarily have to be specified in pseudocode. You could avoid doing it so long as it is clear what the code is doing, but depending on what the pseudocode will be used for and the language it will be used in, it may be advisable to put them in.

**A good algorithm:**

- Has clear and precisely stated steps that produce the correct output for any set of valid inputs
- Should not allow for invalid inputs
- Must always terminate at some point
- Should execute efficiently
- Should be designed in such a way that other people will be able to understand and modify it

**Tools for designing algorithms:**

- Hierarchy Charts -useful for identifying the major task, and breaking these down into subtasks
- Flowcharts -useful for getting down initial ideas for individual subroutines
- Pseudocode -will translate easily into program code

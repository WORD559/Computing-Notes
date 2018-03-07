# Variable Scope #

A variable is in scope when it is able to be accessed.

- A subroutine may have its own variables.
- These are known as local variables.
- A global variable is defined in the main program and can be used in any subroutine called from the main program
- When you use a name on the left hand side of an assignment statement in a subroutine, a local variable is automatically created.
- A local variable can only be used in that subroutine, therefore the scope of a local variable is the subroutine in which it is declared, and does not exist outside the subroutine.

Advantages of local variables:

- There is no chance of accidentally changing a variable in the main program that is used in a subroutine or vice versa.
- Keep your subroutines self-contained!
    - Pass any values that are needed from the main program as arguments.
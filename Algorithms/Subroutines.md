# Subroutines #

A subroutine is a set of instructions with a name.

	SUB GoodBye()
		Print "It has been nice meeting you."
	END SUB
	Sub Hello()
		Print "Hello, how are you today?"
	END SUB
	Hello()
	Print "I am a computer program."
	GoodBye()

Output:

    "Hello, how are you today?
    I am a computer program.
    It has been nice meeting you."

- Program execution starts at the first statement in the main program
- Program flow will jump to the subroutine when called
- When the subroutine has finished, the program will continue from where it was called
- Procedures and functions are types of subroutine
    - A function is a subroutine that returns one or more values
    - In some programming languages all subroutines are referred to as functions even if no value is returned.
- Programming languages come with many built-in functions to perform common tasks
- Programming languages also come complete with libraries of pre-defined subroutines
    - The module library has to be imported at the start of the program
    - For example, in Python:
	    ```
        import random
        x = random.randint(1,6)
	    ```
- Parameters in parentheses are used to pass data to a subroutine
    - For example:
	    ```
        SUB multiply(x,y)
        print "The product is: ", x*y
        ENDSUB
        multiply(2,5)
		```
    - The order of the parameters in parentheses IS important.

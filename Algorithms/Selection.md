# Selection #

Program flow is controlled by evaluating a boolean condition.

A boolean condition evaluates to True/False.

If the condition is true then one or more statements are executed. If it is not true, the statements are skipped and it moves on to the next condition. 

Relational Operators:

- `<` less than
- `>` greater than
- `<=` less than or equal to
- `>=` greater than or equal to
- `=` equal to (`==` in python)
- `<>` not equal to (`!=` in python)

----------------

Complex boolean expressions can be made with AND, OR, and NOT.

AND will only return true if both conditions are true.

OR returns true if one of the conditions are true.

NOT reverses the outcome of an expression.

----------------

If a condition fails, we can use ELSE, which will execute the statements if the conditions are not met.

Some languages have a CASE statement.

For example:

	CASE choice OF
	    A : OUTPUT "You chose a"
	    B : OUTPUT "You chose b"
	ELSE
	    OUTPUT "You chose none."

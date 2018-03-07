# Testing #

- What is the purpose of testing?
- How would you go about testing someone else's program?
- What would you describe as a good or successful test?
- Do you need to know how the program works, in order to test it properly?

The purpose of testing software is to reveal errors. It is notto prove that the system works most of the time. A good test is one which shows up an error.

You don't need to know how to program works in most instances -you just need to know what it's supposed to do.

## Stages of Testing ##

- Module testing -make sure each subroutine works correctly
- Program testing -make sure each program in the system works correctly
- System testing -make sure the whole system works as expected, and does what the original specification required

## Designing a Test Plan ##

- Test data has to be carefully selected
- It should include normal (typical) data, boundary data and erroneous data
- Suppose you are testing a module which allows a user to set a password. The password must be at least 8 characters long, mustinclude both uppercase and lowercase, at least one numeric character, and no spaces.
- You would choose normal test data, data that scrapes by validity, and data that should not work.
- A test plan needs to have the following columns:

|Test|Number|Test Data|Purpose of test|Expected Outcome|Actual Outcome|
|----|------|---------|---------------|----------------|--------------|
|1   |      |         |               |                |              |
|2   |      |         |               |                |              |
|3   |      |         |               |                |              |


- Hand-tracing is useful for:
    - Figuring out how an algorithm works
    - Finding out why an algorithm is not working properly
- It is recommended to put any loop conditions at the start of your trace table

|Count|n|a|b |
|-----|-|-|--|
|1    |5|4|13|
|2    |5|3|11|
|3    |5|2|9 |
|4    |5|1|7 |
|5    |5|0|5 |

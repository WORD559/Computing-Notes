# Instruction Sets and Addressing Modes #

In this chapter, we will learn:

- How to use mnemonics to write code using assembly language.
- The difference between immediate and direct addressing.
- How to use different types of operation codes; data transfer, arithmetic operation, logical operations and branch operations.
- There are three main types of programming language: machine code, assembly language, and high-level languages.
- At machine code level, programming is carried out by directly manipulating 0s and 1s.
- The next level up is to use assembly language, which is made up of mnemonics.
- In order to write assembly code, you need to be familiar with the mnemonics that can be used and this will depend on what processor is being used.
- Each processor will have an instruction set, which is either RISC or CISC.
- An instruction set is the pattern of 1s and 0s that a particular processor recognises as commands, along with their associated meanings.
- A typical assembly language statement consists of four parts:
    - An opcode
    - Two operands
    - A comment
- An example is `CMP r1, #10` 'compare the value in register 1 with the value 10'.
- The opcode is a mnemonic consisting of 3 to four characters.
- The mnemonic's letters typically help to explain what it does. For example, ADD, MOV, CMP.
- The number of operands following an operation code and the way they are interpreted depends on what sort of code it is.
- The use of `#` indicates the addressing mode. In the example above, it is immediate addressing, meaning that the data that follows is the actual data item.
- Comments are optional, but help explain what the code is doing.

Data transfer operations move data from various places, e.g. `MOV`, `STA`, `LDA`.

Arithmetic operations do arithmetic, e.g. `ADD`, `SUB`, `NEG`.

Logical operations are used for comparisons and logic, e.g. `CMP`

Bitwise functions compare each bit to the corresponding bit in another string of equal length.

Branching functions allow you to jump to other bits of code, e.g. `BRA`, `BNE`

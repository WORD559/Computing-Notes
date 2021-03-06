# Backus-Naur Form #

Backus-Naur Form (BNF) is a context-free language. It is useful because it allows it to represent patterns that RegEx would otherwise be unable to represent, for example infinite-length patterns. 

## Syntax ##

`<phrase> ::= _expression_ |...`

- `<>` is a Non-Terminal
- `::=` is defined as
- `_expression_` is a terminal

Terminals can only be on the right hand side of the expression.

`{}` in Extended BNF can be used to represent 0 or more instances of something.

## Examples ##

As an example, defining a digit in BNF would be done by:

`<Digit> ::= 0|1|2|3|4|5|6|7|8|9`

An integer can then be defined as:

`<Integer> ::= <Digit> | <Digit><Integer>`

We define it this way due to the fact that an integer can have an unlimited number of digits.

### Defining a name ###

```
<Name> ::= <FirstName>{ <MiddleName>} <LastName>
<FirstName> ::= <String>
<MiddleName> ::= <String>
<LastName> ::= <String>
<String> ::= <Letter>|<Letter><String>
```

### Defining a Binary Palindrome ###

```
<Palindrome> ::= 0|1|00|11|0<Palindrome>0|1<Palindrome>1
```

This works by building up the palindrome from a "base case". Every binary palindrome will be built up from 0, 1, 00, or 11. Every binary palindrome will be built up from this core

### Defining an Address in BNF ###

```
<Address> ::= <House>
              <Town>
			  <County>
			  <Postcode>
<House> ::= <HouseNo.> <Street> | <HouseName> <Street>
```

etc.

# Parse Trees #

Take an example that represents natual language.

```
<sentence> ::= <noun phrase><verb phrase><noun phrase>
<noun phrase> ::= <preposition><article><noun> | <article><noun>
<verb phrase> ::= <verb> | <adverb><verb>
<article> ::= The | the | a | an | A | An
<preposition> ::= in | on | at | of
<noun> ::= cat | mat | fire | front | mouse
<verb> ::= sat | lay | ate | caught | slept
<adverb> ::= slowly | quickly | happily
```

And the sentence `The cat sat on the mat`

We can represent this in trees that categorise the different parts of the input.

```


<article>  <noun>     <verb> <preposition> <article>  <noun>
The        cat        sat        on        the        mat
```

# Syntax Diagrams #

We can also represent the syntax with a syntax diagram.

- Circle = Terminal element
- Square = Non-terminal element
- Square with a line going back into itself = Repeating element

`<INTEGER> ::= <DIGIT> | <DIGIT><INTEGER>` could be represented as:


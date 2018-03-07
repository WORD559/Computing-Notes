# Finite State Machines #

- It is not a machine in the sense of some mechanical thing with moving parts
- It is an abstract representation of how something changes from one state to another in response to a condition or event.

----------------

- The machine can only be in one state at a time
- It can change from one state to another in response to an event or condition; this is called a transition
- The FSM is defined by a list of its states and the conditions for each transition.
    - There can be outputs linked to the FSM's state, but we will be considering FSMs with no output

## Example - A turnstile ##

- It can be in one of two states: locked or unlocked
- Inserting a ticket unlocks the turnstile
- Pushing through the turnstile locks the turnstile again

[Turnstile Diagram](turnstile.jpg)

## Finite State Automaton ##

- A FSM which has no output is known as a finite state automaton
- It has a start state and a set of end or accept states
- If the automaton can reach a final state, it is said to accept the input
- Starting in an initial state, the automaton processes a sequence of symbols and follows it to the target state
- The symbols depend on the application - they usually represent events

## Notation ##

- A circle represents a state
- A circle with an arrow pointing to it represents a start state
- A circle with another circle inside is an end/accept state
- A curved line is a transition

## Recognising a Language ##

- A finite state system accepts a string if there is a path from the start state to the end or accept state labelled by the symbols C1...Cn
- The language recognised by the FSM consists of all the strings accepted by it

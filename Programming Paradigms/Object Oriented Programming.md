# Procedural Programming #

A program consists of:

- step-by-step instructions
- calls to subroutines
- local and global variables

# Object Oriented Program #

The world is viewed as a collection of objects.

- person
- goat
- event
- data structure, for example a queue or stack

In object oriented programming, the program consists of objects. Each object has its own data (attributes) and operations (methods). Objects interact with each other. All processing is done by objects.

## Classes ##

Classes act like blueprints for objects. It defines the attributes and methods for the common characteristics and behaviours of an object.

A constructor is used to create objects based on the class.

They are similar to records -- a record is a set of attributes, but without methods.

## Encapsulation ##

Encapsulation is a fundamental principle in object oriented programming.
All attributes and methods are wrapped into a single entity.

This is used for information hiding.

An object's attributes attributes are hidden (private/protected) and can only be accessed via the object's methods. Methods are required to set (setters) and retrieve (getters) an object's attributes. To interact with an object, its methods must be accessible (public).

In Python, everything is public by default. You can protect a variable by starting its name with a single underscore OR a double underscore at the beginning and end. Protecting a variable encourages people not to edit it, but it can still be seen easily.

Making it private renders it technically still public, but harder to find. It will be identified as `object._<classname><var name>`. This encourages you even further not to edit it, but you still can anyway.

## Dot Notation ##

Dot notation is used for accessing methods and attributes.

`<class identifier>.<attribute/method identifier>`

For example:

- `Animal.size`
- `Animal.feed()`


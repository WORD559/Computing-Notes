# Object-Oriented Programming #

## Procedural Programming ##

A program consists of:

- step-by-step instructions
- calls to subroutines
- local and global variables

## Object Oriented Program ##

The world is viewed as a collection of objects.

- person
- goat
- event
- data structure, for example a queue or stack

In object oriented programming, the program consists of objects.

Each object has its own data (attributes) and operations (methods).

Objects interact with each other.

All processing is done by objects.

### Classes ###

Classes act like blueprints for objects. It defines the attributes and methods for the common characteristics and behaviours of an object.

A constructor is used to create objects based on the class.

They are similar to records --a record is a set of attributes, but without methods.

### Encapsulation ###

Encapsulation is a fundamental principle in object oriented programming.

All attributes and methods are wrapped into a single entity.

This is used for information hiding.

An object's attributes attributes are hidden (private/protected) and can only be accessed via the object's methods.

Methods are required to set (setters) and retrieve (getters) an object's attributes.

To interact with an object, its methods must be accessible (public).

In Python, everything is public by default.

You can protect a variable by starting its name with a single underscore OR a double underscore at the beginning and end.

Protecting a variable encourages people not to edit it, but it can still be seen easily.

Making it private renders it technically still public, but harder to find. It will be identified as object._<classname><var name>

This encourages you even further not to edit it, but you still can anyway.

### Dot Notation ###

Dot notation is used for accessing methods and attributes.

<class identifier>.<attribute/method identifier>

For example:
```
Animal.size
Animal.feed()
```

### Inheritance ###

This is the act of creating a new class based on an existing class (superclass)

The new class is a subclass of the superclass.

The subclass inherits all the attributes and methods of the superclass, but you can extend them with your own attributes and methods.

For example, Animalcould be a superclass, and Tigerand Lioncan be subclasses. All animals have certain attributes, but tigers and lions are not the same and have their own individual attributes.

An example in Python:

```
class Animal(object):
    def __init__(self,s,n):
		self.state = s
		self.size = n
	def feed(self):
		self.size += 1
		print "Fed."
class Tiger(Animal):
	def feed(self):
		self.size += 2
		print "Fed a big meal!"
```

In VB.NET, the superclass must have its attributes protected, notprivate! Otherwise the subclass won't be able to access these attributes!

### Polymorphism and Overriding ###

Polymorphism -a method in a class hierarchy can behave differently in each class.

This is achieved through overriding. A method with the same identifier in the superclass can be redefined or extended in the subclass.

To do this in VB.NET, the method has to be declared as overrideable.

|Member is accessible...|Public|Private|Private|
|---------------------------|----------|-----------|-----------|
|**Within defining class**  |Yes   |Yes    |Yes    |
|**Via inheritance**        |Yes   |Yes    |No     |
|**Via a reference to an object of the class**|Yes|Only if it is a subclass/in the same package(varies based on language)|No|

### Class Diagrams ###

Public = +

Private = -

Protected = #

|Animal            |
|------------------|
|#state: String    |
|#size: Integer    |
|+ feed()          |
|+ getState() String|
|+ getState() Integer|

|Fish              |Duck            |
|------------------|----------------|
|-maxSize: Integer |                |
|+setMaxSize()     |                |
|+feed()           |+feed()         |
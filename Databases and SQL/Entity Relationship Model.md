# Entity Relationship Model #

- Produce a data model from given data requirements for a simple scenario involving multiple entities
- Produce entity descriptions representing a data model in the form
    Entity(Attribute1,Attribute2...)
- Produce entity relationshp diagrams representing a data model


Suppose you are going to design a new system for a company selling subscriptions for online revision guides.

Where do you start?

One of the first things you need to do is look at the data

What entities are involved?

- An entity is a categriy of object, person, even or thing of interest about which data needs to be recorded
- What entities are there in a system that will keep records of subscriptions for revision guides?
    - Customer
    - Product
    - Subscription
    - If there is data to be stored about it, potentially the company as well

The company is normally the domain.

Other entities could include the author, subject, etc.

## Writing an entity description ##

- This will be a database system called RevisionSubs
- Each entity in the database has attributes
- The entity descriptions can be written in this format:
    - Customer(custID, title, firstname, surname, email)
    - Product(productID, title, subject, level, price)
    - Subscription(subID, startDate, endDate)

Each entity needs an identifier that uniquely identifies each record. This is known as the primary key.

If there is no natural attribute for a primary key, one should be introduced.

Sometimes two or more attributes are needed to uniquely define a record. For example, in a customer order consisting of many different order lines, each order line may be uniquely identified by the two attributes orderNumber and orderLine.

orderNumber, orderLine is a composite primary key.

## Relationships between entities ##

- The three entities are linked or related.
- There are three possible ways in which two entities may be related:
    - one-to-one		e.g. Husband and Wife
    - one-to-many		e.g. Mother and child, school and pupil
    - many-to-many		e.g. Actor and Film, Recipe and Ingredient

## Entity Relationship Diagrams ##

An entity relationship (E-R) diagram is a graphical way of representing the relationships between entities

Husband------Wife    One-to-one

School------<Pupil   One-to-many

Actor>------<Film    Many-to-many

## Database Structure ##

- Each entity is represented by a table
- Tables in a relational database are commonly referred to as relations
- A database contains one or more relations
- A relation has rows, each row containing one record
- The columns in the relation each contain one field (i.i. attribute) belonging to the records

In order to create a relationship between customer and subscription, we need to inclufe custID in the entity description of Subscription

ProductID also needs to be included in the entity description of Subscription

custID and productID are foreign keys in the Subscription entity

A foreign key is an attribute that creates a join between two tables (relations). It is the primary key in the first relation


## Many to Many Relationships ##

Many-to-many relationships are awkward to create, as you would need multiple columns to store multiple shared records. A better way to do this is to create a link table.

Take, for example, a gym.

One table would contain members with memberID private key, one table would contain multiple classes with classID private key. Multiple customers can enroll in multiple classes, however, so we would create a link table to represent this.
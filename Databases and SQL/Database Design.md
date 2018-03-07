# Database Design #

The average idiot will likely create a flat-file database.

This makes many-to-many relationships pretty much impossible.

Normalisation is a process used to come up with the best possible design for a database. Tables should be organised so that data is not duplicated in the same table or in different tables. The structure should allow complex queries to be made.

A table is in first normal form (1NF) if it contains no repeating attributes or groups of attributes. All attributes must be atomic -- a single attribute cannot consist of two data items such as forename and surname (this would make it difficult or impossible to sort on surname).

A table is in second normal form (2NF) if it is in first normal form and contains no partial dependencies. This can only occur if the primary key is a composite key.

A table is in third normal form (3NF) if it is in second normal form and contains no non-key dependencies.
"All attributes are dependant on the key and nothing but the key."

# Advantages of Normalisation #

- Easier to maintain and change a normalised database.
- No unnecessary duplication of data.
- Data integrity is maintained - if a person changes address, for example, the update only needs to be made to one table, as there are no duplicates to be updated.
- Having smaller tables with fewer fields means faster searches and savings in storage.
- Referential integrity - things aren't held in one big table, which helps prevent accidental deletion by requiring all references be changed before the data can be deleted.
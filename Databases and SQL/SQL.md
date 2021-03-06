# SQL #

## Creating a table ##

```
CREATE TABLE tblProduct
(
ProductID CHAR(4) NOT NULL PRIMARY KEY,
Description VARCHAR(20) NOT NULL,
Price CURRENCY
)
```

The datatypes must be explicity stated. Things like "NOT NULL" make a field non-optional, and "PRIMARY KEY" makes it the primary key.

Common datatypes include:

 - CHAR(n) : Character string of fixed length n
 - VARCHAR(n) : Character string of variable length, max length n
 - BOOLEAN : TRUE or FALSE
 - INTEGER, INT : Integer
 - FLOAT(n,d) : Floating point with maximum number of digits n and d numbers after the decimal point
 - DATE : Day, month, year
 - TIME : Hour, minute, second
 - CURRENCY: Formats numbers for the currency in your region

## Altering a table ##

The `ALTER TABLE` statement is used to add, delete, or modify columns in an existing table.

To add a new column:

```
ALTER TABLE tblProduct
ADD QtyInStock
```

To delete a column:

```
ALTER TABLE tblProduct
DROP QtyInStock
```

To change the datatype:

```
ALTER TABLE tblProduct
MODIFY COLUMN QtyInStock FLOAT(10,2) NOT NULL
```

## Data ##

`INSERT INTO` is used to insert a new record into a table.

If we had, for example:

```
ProductID CHAR(4) NOT NULL PRIMARY KEY,
Description VARCHAR(20) NOT NULL,
Price CURRENCY
```

We would do:

```
INSERT INTO tblProduct (ProductID,Description,Price) VALUES ("A345","Pink Rabbit",7.50)
```

You don't need to specify the field names if you are adding data to all fields in order.

You use `UPDATE` to modify records.

```
UPDATE tblProduct
SET Description = "Red Rabbit"
WHERE ProductID = "A345"
```

`DELETE FROM` is used to delete a record in a table.

E.g.:

```
DELETE FROM Product
WHERE ProductID = "A345"
```

This would delete the record with primary key "A345".
# Big Data #

Big data is defined as data that is too large that it does not fit on a single server and is generally unstructured.

Examples:

 - The NHS
 - Passport control to find patterns in border crossings
 - CCTV operators
 - The police

## Big Data Analytics ##

Big Data Analytics can seek out patterns. 

Online shopping is a common example. Often there is value in exploring relationships between connected entities in a dataset.

## Characteristics of Big Data ##

Volume:

 - Big Data is too bigggg to be handled by one server.
 - In the UK, there were 3.5 billion card purchases in one quarter of 2016
 - Google processes more than 3 billion search queries every day

Velocity:

 - Smartphones, sensor networks, and CCTV all create large volumes of data, continuously.
 - The value and use of the data may require a response in the range of milliseconds to seconds.

Variety:

 - Big data comes in many forms; structured, unstructured, text, audio and image
 - 60 million photos uploaded to Instagram daily
 - 48 hours of video are uploaded to YouTube every minute

## Big Data and Functional Programming ##

Functional Programming is useful for processing big data

 - Data structures are immutable, so the data isn't accidentally modified
 - Statelessness, so the program's behaviour does not depend on the order in which functions are called
 - Higher-order functions such as `map` and `fold` allow functions to be input as arguments

`map` applies a function recursively and returns a new list

`fold` applies a function recursively and returns a value

`map` and `fold` operations can be efficiently parallelised. This allows many processors to work simultaneously on parts of a dataset without affecting other parts.

## Fact-Based model ##

Traditional data processing involving relational databases does not suit either the volume of variety of the Bigge Data.

The fact-based model captures a single piece of information, such as sensor location or employer.
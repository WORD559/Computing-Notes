# Fields, Records and Files #

- A fileconsists of a number of records
- A record contains a number of fields, each holding an item of data
- A record is a data structure consisting of a number of fields which can all be of different data types
- Some languages do not have an equivalent data type.
- With text files, the only data type used is a string, and no user-defined data types are used

-----------------

- A file can be a binaryor textfile.
- A textfile may have several text fields, typically separated by commas, line ach record
- A binaryfile can contain records with different types of field such as string, integer, real, Boolean, etc.
- Text files can be opened, created, read, and manipulated with any text editor, and would typically have fields separated by commas, and written one line at a time.
- It is good programming practice to close a file one you have finished writing to it --if you need it later, it is okay to reopen it!

-----------------

- In one sense, all files are "binary" since they are all a collection of bytes consisting of 0s and 1s
- When we talk about binary files, we are referring to the way that the file is opened and processed
- This is different from the way a text file is processed.
- Binary files contain bytes
- Bytes may represent, for example, integers, floating point numbers, characters, part of an image
- So long as you know how to interpret the data in a binary file, you can read it.
- The file has to be opened in binary mode. In Python this is accomplished by "wb", "rb", and "ab"
- Typically, you will need to define a structure for the data to be written to the binary file.
    - Python has a predefined module, struct.pack, to encode data into a binary format for output.
- Text files are convenient because you can read and manipulate them with a text editor, but they can only store a string of characters. Sometimes you need to store a more complex record structure and read it back with the fields intact.
- A record can store any mix of data types in one unit of data which can be written to a file and read back.
- It is possible to read the binary data representing, for example, a .jpg file and copy it to a new file
- You can read the entire file into memory with one read statement, but if it is a large file, this will cause a memory overflow error
- The solution is to set a buffer size of say 50,000 bytes and fill the buffer, write it, refill, and so on.
- This is fairly uncommon nowadays, but you need to know about it.

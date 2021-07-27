# Programming-Note

## What are advantages and disadvantages of indexing in database?
### Advantages

Speed up SELECT query
Helps to make a row unique or without duplicates(primary,unique) 
If index is set to fill-text index, then we can search against large string values. for example to find a word from a sentence etc.

###Disadvantages

Indexes take additional disk space.
indexes slow down INSERT,UPDATE and DELETE, but will speed up UPDATE if the WHERE condition has an indexed field.  INSERT, UPDATE and DELETE becomes slower because on each operation the indexes must also be updated. 

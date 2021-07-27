# DB-Note
## Indexing in Databases 
Indexing is a way to optimize the performance of a database by minimizing the number of disk accesses required when a query is processed. It is a data structure technique which is used to quickly locate and access the data in a database.

Indexes are created using a few database columns.

- The first column is the ###### Search key that contains a copy of the primary key or candidate key of the table. These values are stored in sorted order so that the corresponding data can be accessed quickly.
###### Note: The data may or may not be stored in sorted order.
- The second column is the Data Reference or Pointer which contains a set of pointers holding the address of the disk block where that particular key value can be found.

## What are advantages and disadvantages of indexing in database?
### Advantages

Speed up SELECT query
Helps to make a row unique or without duplicates(primary,unique) 
If index is set to fill-text index, then we can search against large string values. for example to find a word from a sentence etc.

### Disadvantages

Indexes take additional disk space.
indexes slow down INSERT,UPDATE and DELETE, but will speed up UPDATE if the WHERE condition has an indexed field.  INSERT, UPDATE and DELETE becomes slower because on each operation the indexes must also be updated. 

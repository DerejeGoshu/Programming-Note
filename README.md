# DB-Note
## Indexing in Databases 
Indexing is a way to optimize the performance of a database by minimizing the number of disk accesses required when a query is processed. It is a data structure technique which is used to quickly locate and access the data in a database.

Indexes are created using a few database columns.

- The first column is the **Search key** that contains a copy of the primary key or candidate key of the table. These values are stored in sorted order so that the corresponding data can be accessed quickly.
###### Note: The data may or may not be stored in sorted order.
- The second column is the **Data Reference** or **Pointer** which contains a set of pointers holding the address of the disk block where that particular key value can be found.


###### The indexing has various attributes:

- **Access Types**: This refers to the type of access such as value based search, range access, etc.
- **Access Time**: It refers to the time needed to find particular data element or set of elements.
- **Insertion Time**: It refers to the time taken to find the appropriate space and insert a new data.
- **Deletion Time**: Time taken to find an item and delete it as well as update the index structure.
- **Space Overhead**: It refers to the additional space required by the index

## What are advantages and disadvantages of indexing in database?
### Advantages

Speed up SELECT query
Helps to make a row unique or without duplicates(primary,unique) 
If index is set to fill-text index, then we can search against large string values. for example to find a word from a sentence etc.

### Disadvantages

Indexes take additional disk space.
indexes slow down INSERT,UPDATE and DELETE, but will speed up UPDATE if the WHERE condition has an indexed field.  INSERT, UPDATE and DELETE becomes slower because on each operation the indexes must also be updated. 

## Stored Procedures vs Functions vs Views
## Stored Procedures
- A **stored procedure** is a set of pre-compiled Structured Query Languages (SQL), so it can be reused and shared by multiple programs. It can access or modify data in a database.
- **Stored procedures** are one of numerous mechanisms of encapsulating database logic in the database. They are similar to regular programming language procedures in that they take arguments, do something, and sometimes return results and sometimes even change the values of the arguments they take when arguments are declared as output parameters. You will find that they are very similar to stored functions in that they can return data; however stored procedures can not be used in queries. Since stored procedures have the mechanism of taking arguments declared as OUTPUT they can in theory return more than one output.
## Views
 **Views** are similar to inline table valued function - they allow you centralize a query in an object that can be easily called from other queries. The results of the view can be used as part of that calling query, however parameters can't be passed in to the view.

**Views** also have some of the security benefits of a stored procedure; they can be granted access to a view with a limited subset of data from an underlying table that those same users don't have access to.

**Views** also have some performance advantages since they can have indexes added to them, essentially materializing the result set in advance of the view being called (creating faster performance). If considering between an inlined table function and a view, if you don't need to parameterize the input, a view is usually the better option.
## Funcion
A **Funcion**  is a database object in SQL Server. Basically, it is also a set of SQL statements that accept only input parameters and produce output in a single value form or tabular form.

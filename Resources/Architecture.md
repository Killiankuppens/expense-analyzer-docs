# Design pattern

## Creational Patterns

### Abstract Factory

Produce families of related objects without specifying their croncrete classes.


### Builder

Construct complex objects step by step.

# Micro-service architecture

Can be a good idea if we have multiple DBs and want to decouple services.

# Monolithic architecture

Project should start with this kind of architecture as it is a "simple" application.
If the project expands to multiple applications (Mobile + Web) and more DBs, the architecture should change to a micro-services architecture to have decoupling between the 

# Database

## One-To-Many relationship

If we have multiple elements in a column like a list (example: "Biology, Math"), the design violates the first principle of database normalization [1NF (First Normal Form)](https://www.lifewire.com/normalizing-your-database-first-1019733).
Another design might be to add a second record which will lead to redundancies of multiple records, this will violate the [2NF (Second Normal Form)](https://www.lifewire.com/full-functional-dependency-1019753).

We should break the table into two and link them with a FK, it will avoid any redundancies on the PK and implements one-to-many relationship.

## Choosing indexes

For small tables, sequential checking is faster due to the overhead of keeping an index => might not be useful at the start of the application.

When you define an index on the column of a databse table, the dbms(Database Management System) is essentially creating another 'table' with the data of that particular column sorted, allowing quicker search time.
In our case, the an index on the "counterpart_acc_id" might be useful.

### how to choose the column to define the index on

Make a list of all the queries your application is making to the particular table and figure out which column is the most commonly used WHERE clause or JOIN ON clause. 

[Real example of the benefits indexes can give](https://medium.com/the-software-firehose/how-to-choose-a-table-index-for-your-sql-database-d47715a35f34)

## Run PostgreSQL with PgAdmin on Podman
https://dev.to/pr0pm/run-postgresql-pgadmin-in-pods-using-podman-386o

## Retrieve the amounts for a specific time period

There is 2 possibilities for this to happen, we either :
 - Create a DTO to contain the amounts of all the operations (total, incoming, coming out) and also the operations a OperationSummary array
 - Just return the total of the operations in the current OperationSummary => if done this way, functionalities are set in stone/no possibility of amelioration without refactor it
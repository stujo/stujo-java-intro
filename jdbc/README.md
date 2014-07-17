# JDBC

##JDBC Connections (Java Platform)
* Know how to connect your application to a database with JDBC
*
* Know how to execute SQL statements:
 * CREATE TABLE, SELECT, INSERT, UPDATE, DELETE, DROP TABLE
* autoCommit - Basic Transactions
* close ``Connection`` when done (if you opened it)
* [Batching Statements](http://viralpatel.net/blogs/batch-insert-in-java-jdbc/)

## Exercise
* __EXERCISE:__
* A project which reads a CSV File from disk and imports some of the data into a database
* [DataSource](http://docs.oracle.com/javase/6/docs/api/javax/sql/DataSource.html)
* When the file is imported a second time existing records are updated and new records are added
* [OpenCSV](http://viralpatel.net/blogs/java-read-write-csv-file/)
* [Via Maven](http://mvnrepository.com/artifact/net.sf.opencsv/opencsv/2.3)
* Get it working without batching first and then add batch queries
* __CHECKPOINT:__ Connect to a Database
* __CHECKPOINT:__ Query a Database

# JDBC Review


### Exercise
* __EXERCISE:__
* A project which reads a CSV File from disk and imports some of the data into a sqlite database
* Use Maven to get the driver
```
		<dependency>
			<groupId>org.xerial</groupId>
			<artifactId>sqlite-jdbc</artifactId>
			<version>3.7.15-M1</version>
			<scope>compile</scope>
		</dependency>
```
* [https://github.com/boundlessgeo/sqlite-jdbc](https://github.com/boundlessgeo/sqlite-jdbc)

* Example Source Data is Auto Dealership Listings:

```
Year,Make,Model,Description,Price
```

  * [Source Data](http://en.wikipedia.org/wiki/Comma-separated_values#Example)

* [OpenCSV](http://viralpatel.net/blogs/java-read-write-csv-file/)
  * [Via Maven](http://mvnrepository.com/artifact/net.sf.opencsv/opencsv/2.3)

* __BONUS:__ Get it working without batching first and then add batch queries
* __BONUS:__ When the file is imported a second time existing records are updated and new records are added
* __CHECKPOINT:__ Connect to a Database
* __CHECKPOINT:__ Query a Database

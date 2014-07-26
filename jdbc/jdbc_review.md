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

```
VIN,Year,Make,Model,Description,Price
ASBVSDSA,1997,Ford,E350,"ac, abs, moon",3000.00
UYASGC6D,1999,Chevy,"Venture ""Extended Edition""","",4900.00
WGTADSGA,1999,Chevy,"Venture ""Extended Edition, Very Large""",,5000.00
OPACUSUA,1996,Jeep,Grand Cherokee,"MUST SELL! air, moon roof, loaded",4799.00
UYASGC6D,1999,Chevy,"SALE! Venture ""Extended Edition""","",4800.00
```

* [OpenCSV](http://viralpatel.net/blogs/java-read-write-csv-file/)
  * [Via Maven](http://mvnrepository.com/artifact/net.sf.opencsv/opencsv/2.3)

* __BONUS:__ Get it working without batching first and then add batch queries
* __BONUS:__ When the file is imported a second time existing records are updated and new records are added
* __CHECKPOINT:__ Connect to a Database
* __CHECKPOINT:__ Query a Database

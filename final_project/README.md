# Final Project

When you have completed all phases you will have a Java Application which performs these tasks (in order):
* Loads _stock_level.csv_ into a inventory system, in a persistent database of your choice
* The order is read from a JSON file (_order.json_)
* An ``Order`` object from the read data
* The ``OrderManager`` ``process``es the order as follows:
 * Tests that the items are in stock in a database by calling the ``InventoryManager``'s ``stockLevel(productId)``
 * If the stock on hand is >= the required quantity for the line item then
   * Decrements the stock level by calling the ``InventoryManager``'s ``decrementStock(productId)``
 * Otherwise it marks the ``LineItem`` as out_of_stock (all or nothing for each line item)
* Once the order and all the line items have been processed:
* The ``Order`` is passed to the ``ReceiptPrinter`` and a nicely formatted reciept is printed (_reciept.txt_)
* Exports _stock_level_updated.csv_ to the file system with the updated stock levels read from the database

##Background Topics
###CSV Parsing
* [opencsv](http://opencsv.sourceforge.net/)
```
    <dependency>
      <groupId>net.sf.opencsv</groupId>
      <artifactId>opencsv</artifactId>
      <version>2.3</version>
    </dependency>
```

###JSON
/articles/java/json-1973242.html)
* Strings in Switch were only added in java 7 :(
* [json.org](http://json.org/java/)
```
    <dependency>
      <groupId>org.json</groupId>
      <artifactId>json</artifactId>
      <version>20140107</version>
      <scope>compile</scope>
    </dependency>
```
* [The Object Model API vs The Streaming API](http://www.oracle.com/technetwork

###Logging API
* [java.util.logging]()
* ``mLogger = Logger.getLogger(App.class.getName());``
* See boxes/jsonweather

###DbUnit
* Help test your database code with DbUnit
* [Getting Started](http://dbunit.sourceforge.net/howto.html)
* Allows importing of data and schemas easily
```
    <dependency>
      <groupId>org.dbunit</groupId>
      <artifactId>dbunit</artifactId>
      <version>2.5.0</version>
      <scope>test</scope>
    </dependency>
```

###H2 Database
* Simple in memory database very useful for testing!
* ``static final String JDBC_DRIVER = org.h2.Driver.class.getName();``
* ``static final String JDBC_URL = "jdbc:h2:mem:inventory;DB_CLOSE_DELAY=-1";``
```
    <dependency>
      <groupId>com.h2database</groupId>
      <artifactId>h2</artifactId>
      <version>1.4.179</version>
      <scope>test</scope>
    </dependency>
```

##Sample Data
###Sample Stock Data
_stock_level.csv_
```
PRODUCT_ID,STOCK_LEVEL
12,3
14,2
13,2
```

###Sample Input
_order.json_
```
{
"timestamp":"20140709194738",
"store":{"id":"42", "name":"San Francisco" },
"customer":{ "first_name":"Bob", "last_name":"Williams", "rewards_number":"Y18123AS"},
"items":[
  { "id":"12", "name":"Flat Screen TV", "price":500, "quantity":1 },
  { "id":"14", "name":"Playstation 4", "price":399, "quantity":1 },
  { "id":"13", "name":"Playstation Controller", "price":29, "quantity":4 }
]
}
```

###Sample Output
_reciept.txt_
```
  Bob Williams (Y18123AS)
  San Francisco (42)
  July 9th, 2014
  ---------------
  $500.00 - SOLD: 1 @ Flat Screen TV
  $399.00 - SOLD: 1 @ Playstation 4
  OUT_OF_STOCK: 4 @ Playstation Controller
  --------------
  Order Total: $899.00
  --------------
  Thank you for your business

```

##Expectations
* Create a populate a local database with data from a CSV file (_stock_level.csv_)
* Write Unit Tests for the components
* Package the Application into Executable Jar File format (Research Required)
* Takes two command line arguments
  * orderfile - The file to read
  * recieptfile - The file to write
* Reads in _orderfile_ (_order.json_) JSON File (representing a customer order)
  * Find and use an available Parser
* Creates Order Related Objects Based on the JSON File Contents
  * Order ? and what else might you need?
* Writes out _receiptfile_ a nicely formatted receipt describing the order
* Has JUnit tests
   * Unit tests: for functional Units
   * Try you hand at an integration test
* Bonus: Using Logging

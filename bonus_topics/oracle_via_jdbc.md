# Oracle via JDBC

* [Maven?](http://stackoverflow.com/questions/1074869/find-oracle-jdbc-driver-in-maven-repository#1074971)
* [System Dependency](http://stackoverflow.com/questions/1074869/find-oracle-jdbc-driver-in-maven-repository#9779295)
* [Get Drivers](http://www.oracle.com/technetwork/database/features/jdbc/index-091264.html)
* Loading the Driver

```
try {
   Class.forName("oracle.jdbc.driver.OracleDriver");
}
catch(ClassNotFoundException ex) {
   System.out.println("Oracle JDBC Driver Unavailable");
   System.exit(1);
}
```

* Getting the Connection

```
String URL = "jdbc:oracle:thin:@hostname:port Number:databaseName";
String USER = "scott";
String PASS = "tiger"
Connection connection = DriverManager.getConnection(URL, USER, PASS);
```

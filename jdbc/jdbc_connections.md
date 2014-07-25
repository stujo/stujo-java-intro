# JDBC Connections

* How to connect your application to a database with JDBC Connection
* Load / auto register the driver and then request a connection from the DriverManager with a valid URL

* [Tutorial](http://www.tutorialspoint.com/jdbc/jdbc-db-connections.htm)

* close ``Connection`` when done (if you opened it)


* Derby Example:

Example from __boxes/triplecrown__


```
private static final String JDBC_EMBEDDED_DRIVER = "org.apache.derby.jdbc.EmbeddedDriver";
private static final String JDBC_DRIVER          = JDBC_EMBEDDED_DRIVER;
private static final String DB_URL               = "jdbc:derby:directory:races";

```

```
  static Connection createConnection() {
    try {
      // Load the Class Manually
      // This registers it with the driver manager
      Class.forName(JDBC_DRIVER).newInstance();
      // Get a connection
      return DriverManager.getConnection(dbURL + ";create=true");
    } catch (SQLException e) {
      e.printStackTrace();
    } catch (InstantiationException e) {
      e.printStackTrace();
    } catch (IllegalAccessException e) {
      e.printStackTrace();
    } catch (ClassNotFoundException e) {
      e.printStackTrace();
    }
    return null;
  }

```

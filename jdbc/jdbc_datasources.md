# JDBC DataSources

* Application often run in containers which have configured ``DataSource``s so this is most commmon, but you can configure your own

* SQLite Example:

Example from __boxes/checkout__
```
final SQLiteConfig config = new SQLiteConfig();
final SQLiteDataSource ds = new SQLiteDataSource(config);
ds.setUrl("jdbc:sqlite:" + props.getProperty("dburl", "db/checkout.db"));

// now use the ds to get a connection

```

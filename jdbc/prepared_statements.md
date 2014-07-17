# Prepared Statements

```
  void update(final Connection conn, final String tableName)
      throws SQLException {
    final PreparedStatement prepStmt = conn.prepareStatement("UPDATE "
        + tableName + " SET NAME = ? WHERE ID = ?");
    prepStmt.setString(1, getProductName());
    prepStmt.setLong(2, getId());
    prepStmt.executeUpdate();
    prepStmt.close();
  }
```

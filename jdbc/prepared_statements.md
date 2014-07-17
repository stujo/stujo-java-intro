# Prepared Statements


Getting IDs back
```
 void insert(final Connection conn, final String tableName)
      throws SQLException {
    PreparedStatement prepStmt = null;
    ResultSet generatedKeys = null;

    try {

      prepStmt = conn.prepareStatement("INSERT INTO " + tableName + SQL_INSERT,
          Statement.RETURN_GENERATED_KEYS);
      prepStmt.setString(1, getProductName());
      prepStmt.setInt(2, getStockLevel());

      final int affectedRows = prepStmt.executeUpdate();
      if (affectedRows == 0) {
        throw new SQLException("Creating inventory failed, no rows affected.");
      }

      generatedKeys = prepStmt.getGeneratedKeys();
      if (generatedKeys.next()) {
        mId = generatedKeys.getLong(1);
      } else {
        throw new SQLException(
            "Creating inventory failed, no generated key obtained.");
      }
    } finally {
      if (generatedKeys != null) {
        try {
          generatedKeys.close();
        } catch (final SQLException logOrIgnore) {
        }
      }
      if (prepStmt != null) {
        try {
          prepStmt.close();
        } catch (final SQLException logOrIgnore) {
        }
      }
    }
  }
``

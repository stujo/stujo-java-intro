# Executing SQL



* Know how to execute SQL statements:
 * CREATE TABLE, SELECT, INSERT, UPDATE, DELETE, DROP TABLE


```
    // Declare outside of try so we can close it in finally
    Statement stmt = null;
    String query = "SELECT ID, NAME FROM EMPLOYEE";

    try {
        stmt = con.createStatement();
        ResultSet rs = stmt.executeQuery(query);
        while (rs.next()) {
            int id = rs.getInt("ID");
            String name = rs.getString("NAME");
            System.out.println(nae + " : " + id);
        }
    } catch (SQLException e ) {
        e.printStackTrace();
    } finally {
        if (stmt != null) { stmt.close(); }
    }

```

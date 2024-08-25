### MIT App Inventor MySQL Extension Documentation

The Advanced MySQL Extension for MIT App Inventor provides comprehensive tools for managing MySQL databases. It includes a variety of methods for handling tables, columns, indexes, and executing queries with advanced options. Below is a detailed explanation of each block's functionality and usage.

---

#### 1. Add Columns Block
![Add Columns Block](https://i.postimg.cc/YqsTtPQ1/Add-Columns-Block.png)

**Description:**  
Adds new columns to an existing table in the MySQL database. You need to specify the table name and a list of columns with their respective data types (e.g., 'age INT', 'email VARCHAR(100)').

**Parameters:**
- **tableName**: The name of the table where new columns will be added (Type: text).
- **columns**: A list of column definitions including their names and data types (Type: list).

#### 2. Create Index Block
![Create Index Block](https://i.postimg.cc/rwR3s997/Create-Index-Block.png)

**Description:**  
Creates an index on one or more columns of a table to improve query performance.

**Parameters:**
- **tableName**: The name of the table on which the index will be created (Type: text).
- **indexName**: The name of the index to be created (Type: text).
- **columns**: A list of columns that the index will be based on (Type: list).

#### 3. Create Table Block
![Create Table Block](https://i.postimg.cc/9f3S7q80/Create-Table-Block.png)

**Description:**  
Creates a new table in the MySQL database with specified columns and a primary key.

**Parameters:**
- **tableName**: The name of the new table to be created (Type: text).
- **columns**: A list of column definitions including names and data types (Type: list).
- **primaryKey**: The primary key column of the new table (Type: text).

#### 4. Delete Rows Block
![Delete Rows Block](https://i.postimg.cc/fbxPjTpK/Delete-Rows-Block.png)

**Description:**  
Deletes specific rows from a table based on a condition (e.g., 'id = 1' to delete rows where the `id` is 1).

**Parameters:**
- **tableName**: The name of the table from which rows will be deleted (Type: text).
- **whereClause**: The condition to specify which rows to delete (Type: text).

#### 5. Drop Index Block
![Drop Index Block](https://i.postimg.cc/3xPMFqRK/Drop-Index-Block.png)

**Description:**  
Drops an index from a table. This action removes the index, which may affect the performance of certain queries.

**Parameters:**
- **tableName**: The name of the table from which the index will be dropped (Type: text).
- **indexName**: The name of the index to be dropped (Type: text).

#### 6. Drop Table Block
![Drop Table Block](https://i.postimg.cc/Tw6ZZWgF/Drop-Table-Block.png)

**Description:**  
Deletes a table by its name. The specified table must exist; otherwise, no action is taken.

**Parameters:**
- **tableName**: The name of the table to be dropped (Type: text).

#### 7. Execute Query Block
![Execute Query Block](https://i.postimg.cc/sX4tyDJX/Execute-Query-Block.png)

**Description:**  
Executes a MySQL query and returns the result in JSON format. It can handle `SELECT` queries (returns rows) and other types of queries (returns the number of affected rows).

**Parameters:**
- **query**: The MySQL query to execute (Type: text).

#### 8. Execute Transaction Block
![Execute Transaction Block](https://i.postimg.cc/gjc10FMK/Execute-Transaction-Block.png)

**Description:**  
Executes a transaction with multiple queries. All queries are executed as a batch, and if any query fails, the transaction is rolled back to maintain data integrity.

**Parameters:**
- **queries**: A list of MySQL queries to be executed as a transaction (Type: list).

#### 9. Get Column Data Types Block
![Get Column Data Types Block](https://i.postimg.cc/HnSRcZR1/Get-Column-Data-Types-Block.png)

**Description:**  
Retrieves the data types of columns in a specified table, which helps understand the structure of the table.

**Parameters:**
- **tableName**: The name of the table whose column data types are to be retrieved (Type: text).

#### 10. Get Columns Block
![Get Columns Block](https://i.postimg.cc/m2D0f41L/Get-Columns-Block.png)

**Description:**  
Retrieves column names from a table based on the row position. The position is zero-based (e.g., position 0 retrieves the first row).

**Parameters:**
- **tableName**: The name of the table from which column names are to be retrieved (Type: text).
- **position**: The position of the row to retrieve column names from (Type: number).

#### 11. Get Row Count Block
![Get Row Count Block](https://i.postimg.cc/1RMLjXt7/Get-Row-Count-Block.png)

**Description:**  
Gets the total number of rows in a specified table, which can help determine the size of the table.

**Parameters:**
- **tableName**: The name of the table for which the row count is to be determined (Type: text).

#### 12. Get Rows Block
![Get Rows Block](https://i.postimg.cc/nzKtz1nn/Get-Rows-Block.png)

**Description:**  
Retrieves all rows from a specified table and returns the result in JSON format, including all rows of the table.

**Parameters:**
- **tableName**: The name of the table from which rows are to be retrieved (Type: text).

#### 13. Get Tables Block
![Get Tables Block](https://i.postimg.cc/LXFp2WKy/Get-Tables-Block.png)

**Description:**  
Retrieves a list of all table names in the database and returns a list of table names as a `YailList`.

**Parameters:**
- None

#### 14. Rename Table Block
![Rename Table Block](https://i.postimg.cc/MK3JvHJf/Rename-Table-Block.png)

**Description:**  
Renames a table in the database, which is useful for reorganizing the database schema or correcting table names.

**Parameters:**
- **oldName**: The current name of the table to be renamed (Type: text).
- **newName**: The new name for the table (Type: text).

#### 15. Table Exists Block
![Table Exists Block](https://i.postimg.cc/Mpc2RwzP/Table-Exists-Block.png)

**Description:**  
Checks if a table exists in the database. It is useful to verify if a table is available before performing operations on it.

**Parameters:**
- **tableName**: The name of the table to check for existence (Type: text).

#### 16. Update Table Block
![Update Table Block](https://i.postimg.cc/1z6kCKnD/Update-Table-Block.png)

**Description:**  
Updates specific columns in a table with new values. The `whereClause` specifies which rows to update (e.g., 'id = 1').

**Parameters:**
- **tableName**: The name of the table to be updated (Type: text).
- **columns**: A list of column names to be updated (Type: list).
- **values**: A list of new values for the specified columns (Type: list).
- **whereClause**: A condition to specify which rows to update (Type: text).

---

### Events

#### 1. On Columns Retrieved Block
![On Columns Retrieved Block](https://i.postimg.cc/wM6YssBL/On-Columns-Retrieved-Block.png)

**Description:**  
Triggered when columns from a table are retrieved, providing the column names as a list.

**Parameters:**
- **columns**: A list of column names retrieved from the table (Type: list).

#### 2. On Query Failed Block
![On Query Failed Block](https://i.postimg.cc/8ctQdPF3/On-Query-Failed-Block.png)

**Description:**  
Triggered when any MySQL operation fails, providing an error message describing the failure.

**Parameters:**
- **errorMessage**: A text description of the error that occurred (Type: text).

#### 3. On Query Success Block
![On Query Success Block](https://i.postimg.cc/HW2g13S2/On-Query-Success-Block.png)

**Description:**  
Triggered when a query is executed successfully, providing the result of the query or the number of affected rows.

**Parameters:**
- **value**: The result of the query or the number of rows affected by the query (Type: text).

#### 4. On Rows Retrieved Block
![On Rows Retrieved Block](https://i.postimg.cc/ZK5hb32h/On-Rows-Retrieved-Block.png)

**Description:**  
Triggered when all rows from a table are retrieved, providing the result as a JSON string.

**Parameters:**
- **value**: A JSON string containing all rows retrieved from the table (Type:

 text).

#### 5. On Success Block
![On Success Block](https://i.postimg.cc/L69mJGqw/On-Success-Block.png)

**Description:**  
Triggered when any MySQL operation is successful, providing a success message describing the operation.

**Parameters:**
- **successMessage**: A text message indicating the success of the operation (Type: text).

#### 6. On Tables Retrieved Block
![On Tables Retrieved Block](https://i.postimg.cc/DzXhVTDJ/On-Tables-Retrieved-Block.png)

**Description:**  
Triggered when all table names are retrieved, providing the table names as a list.

**Parameters:**
- **tables**: A list of all table names retrieved from the database (Type: list).

---

### Properties

#### 1. Password Block
![Password Block](https://i.postimg.cc/MK9qVtVT/Password-Block.png)

**Description:**  
Sets the password for the MySQL database connection.

#### 2. Server URL Block
![Server URL Block](https://i.postimg.cc/W1tjnrw7/Server-Url-Block.png)

**Description:**  
Sets the server URL for the MySQL database. Example: `jdbc:mysql://localhost:3306/mydatabase`.

#### 3. User Name Block
![User Name Block](https://i.postimg.cc/K8Vbsz9h/User-Name-Block.png)

**Description:**  
Sets the username for the MySQL database connection.

---

This documentation was generated using [Riad Developer Documentation Generator](https://riaddeveloper.000.pe).

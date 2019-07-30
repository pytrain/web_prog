<center>
  <h1>PHP - Database Interactions</h1>
</center>

## Databases
---

The most popular database to coincide with PHP is MySQL. This is a tabular record-keeping storage device that duplicates the function of formatted binary files. MySQL is a database type that runs as a database server that PHP connects to, retrieves/inserts data within the database, and then the connection is closed. If we parallel this with a file:

| File | Database |
|------|----------|
| `fopen($filename, 'r')` | `mysqli_connect($servername, $username, $password)` |
| `fread($filename, filesize($filename))` | `mysqli_query($conn, $sql)` |
| `fclose()` | `mysqli_close($conn)` |

Here, we see that a file is opened, read data, and then close the file. Then, for the database, we connect to the server, read data via a query, and then close the connection. The two are somewhat synonymous.

## A database example
---

Since we did not install phpMyAdmin or MySQL itself, we need to work online to play with a demo database. There is a service that is online available for us to use instead of local development (I don't believe it will allow you to save your code though.).

### Connect to a database
1. Navigate to the following url in a new browser tab/window: [http://phpfiddle.org/lite](http://phpfiddle.org/lite)
2. Click the "Run" button to see the sample code run in the "Window" tab.
3. Now, we need to change this in order to connect to their provided sample MySQL database.
4. Under the "Editor" tab, remove all the HTML code above the PHP code.
5. Change the PHP code to be:
   ```php
   $server = "localhost";
   $user = "xfiddlec_user";
   $pass = "public";
   $db = "xfiddlec_max";

   // Connect to database server and specific database
   $conn = mysqli_connect($server, $user, $pass, $db);

   // Check that connection was succesful
   if (!$conn) {
       die("Connection failed: " . mysqli_connect_error());
   }
   echo "Connected successfully<br><br>";
   ```
6. Run this code and verify that the connection was successful. This allows us to connect to the hosted demo server. (**Note:** I do not recommend storing your credentials in variables within your PHP code.
7. Once we connect, let's ensure we close the connection as well. Add the following at the below the echo statement:
   ```
   mysqli_close($conn);
   ```
8. Now, if we want to "see" what data is in a database, we need to modify the code between connecting and closing the database connection.

**Note:** We can create databases, tables, and insert data into these tables, but we will not cover this in this lecture.

### Retrieving data
1. Let's use a sample SQL statement to select one record from the provided database within the MySQL database server:
   ```php
   // Once connected, retrieve a single entry
   // Here, xfiddlec_max is the table name of the databse xfiddlec_max
   $sql = "SELECT * FROM xfiddlec_max LIMIT 1";
   $result = mysqli_query($conn, $sql);

   // process record(s)
   $row = mysqli_fetch_assoc($result);
   if ($result->num_rows > 0) {
       // output data of each row
       while($row = $result->fetch_assoc()) {
           print_r($row + "<br>");
       }
   } else {
       echo "0 results";
   }
   ```
2. Notice the output array. We have the following entry in the database table:

    | id | firstname | lastname | email | reg_date |
    |----|-----------|----------|-------|----------|
    |  1 | OpenIDM   | Platform for building enterpri | | 2016-09-30 11:21:15 |
3. Let's modify that `print_r` to be an echo instead with a formatted output:
   ```php
   echo "id: " . $row["id"]. " - Name: " . $row["firstname"]. " " . $row["lastname"]. "<br>";
   ```
4. Modify the SQL statement to obtain all the IDs in the table.
   ```sql
   SELECT id FROM xfiddlec_max
   ```
5. Notice there is only one ID. Let's insert one.
   ```php
   $sql = "INSERT INTO xfiddlec_max (firstname, lastname, email) VALUES ('John', 'Doe', 'john@example.com');";
   $result = mysqli_query($conn, $sql);

   if (mysqli_query($conn, $sql)) {
       echo "New record created successfully<br><br>";
   } else {
       echo "Error: " . $sql . "<br>" . mysqli_error($conn);
   }
   ```
6. Modify the SQL statement to obtain only unique IDs in the table.
   ```sql
   SELECT distinct id FROM xfiddlec_max
   ```

So, from this simple example, we can continue working with this database to retrieve data or insert data from/to the database.

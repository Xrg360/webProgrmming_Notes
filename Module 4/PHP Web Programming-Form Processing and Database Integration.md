
## Module Overview
- **Topic**: Form Processing, Business Logic, and MySQL Integration
- **Core Objectives (CO3)**: Apply PHP's superglobal arrays, manage cookies and sessions, and integrate with MySQL.

---

## PHP Form Processing
- PHP handles form input through **superglobal arrays**:
  - **`$_POST`**: Retrieves data sent via HTTP POST requests, suitable for sensitive data (e.g., passwords).
  - **`$_GET`**: Collects data sent via HTTP GET requests, visible in URL, limited in character count (~100).
- **Example Usage**: Accessing form data in PHP:
  ```php
  $phone = $_POST["phone"];  // Fetches input from a form field named "phone"
  ```

## Cookies and Sessions
- **Cookies**:
  - Small files stored on the user's device by the server, used to persist user-specific data between sessions.
  - **Syntax**: `setcookie(name, value, expire, path)`
  - **Example**: Creates a cookie "valid" that lasts for one day:
    ```php
    setcookie("valid", "true", time() + 86400);
    ```
  - To delete a cookie, set an expiration date in the past:
    ```php
    setcookie("valid", "", time() - 3600);
    ```
- **Sessions**:
  - Server-stored session data, identified by a **Session ID**.
  - **Usage**:
    - `session_start()`: Initializes or resumes a session.
    - **Example**:
      ```php
      session_start();
      $_SESSION["username"] = "exampleUser";
      ```

## MySQL Database Integration
- **Connecting PHP to MySQL**:
  - Requires **MySQLi** or **PDO** for PHP 5 and above.
  - **Syntax**:
    ```php
    $mysqli = mysqli_connect("hostname", "username", "password", "database");
    ```
- **Basic Operations**:
  - **INSERT**: Adds data to the database.
  - **SELECT**: Retrieves data, supports both procedural and object-oriented methods.
  - **UPDATE**: Modifies existing records, typically used with a WHERE clause.
  - **DELETE**: Removes records from a table.

### Sample Queries
1. **Insert Data**:
   ```php
   $sql = "INSERT INTO users (name, email) VALUES ('John', 'john@example.com')";
   $conn->query($sql);
   ```
2. **Select Data**:
   ```php
   $result = $conn->query("SELECT * FROM users");
   while($row = $result->fetch_assoc()) {
       echo $row["name"];
   }
   ```

## Dynamic Content with PHP
- **Self-submitting Forms**: Use PHP to dynamically validate, retain, and process form data.
  - **Example**:
    ```php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        // Process form data
    }
    ```
- **Error Handling**:
  - Check each form input field for errors and provide real-time feedback.
  - Display error messages inline to guide user corrections.

---

### Reference Code for Form Data Processing
- **Storing User Information in Database**:
  ```php
  if (isset($_POST["submit"])) {
      $name = $_POST["name"];
      $email = $_POST["email"];
      $query = "INSERT INTO mailing_list (name, email) VALUES ('$name', '$email')";
      if ($conn->query($query)) {
          echo "Successfully saved.";
      }
  }
  ```

### Important Notes
- Avoid **`mysql_*` functions** as they are deprecated. Use **MySQLi** or **PDO** instead for security and future-proofing.

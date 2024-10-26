1. Write an equivalent php statement corresponding to the following
	1. declare an associative array (mark) to store the key value pair 
		1. Ram 40
		2. Alice 20
		3. Raj 45
		4. Mary 35
	2. Modify the value associated with the key "Ram" to '50'.
	3. Sort the Array and print the sorted key value pair.
2. Design a HTML form for entering a number by the user write a php code to display a message indicating whether the number is +ve or -ve while clicking on the submit button.
3. Write the php form handling program to perform user registration of any website with a minimum of 5 diff fields and insert the data into a mysql table after establishing necessary connections with the db.

### 1. Equivalent PHP Statement:

```php
<?php
$mark = array(
    "Ram" => 40,
    "Alice" => 20,
    "Raj" => 45,
    "Mary" => 35
);

$mark["Ram"] = 50;

ksort($mark); 

foreach ($mark as $key => $value) {
    echo "$key => $value\n";
}
?>
```

### 2. HTML Form and PHP Code to Check Positive or Negative:

```html
<!DOCTYPE html>
<html>
<body>

<form method="post" action="">
    Enter a number: <input type="number" name="number">
    <input type="submit" name="submit" value="Check">
</form>

<?php
if (isset($_POST['submit'])) {
    $num = $_POST['number'];
    
    if ($num > 0) {
        echo "$num is a positive number.";
    } elseif ($num < 0) {
        echo "$num is a negative number.";
    } else {
        echo "$num is zero.";
    }
}
?>

</body>
</html>
```

### 3. PHP Form Handling Program for User Registration:

**HTML Form:**
```html
<!DOCTYPE html>
<html>
<body>

<form method="post" action="register.php">
    First Name: <input type="text" name="first_name"><br>
    Last Name: <input type="text" name="last_name"><br>
    Email: <input type="email" name="email"><br>
    Username: <input type="text" name="username"><br>
    Password: <input type="password" name="password"><br>
    <input type="submit" name="submit" value="Register">
</form>

</body>
</html>
```

**PHP Registration Code (`register.php`):**
```php
<?php
if (isset($_POST['submit'])) {
    $first_name = $_POST['first_name'];
    $last_name = $_POST['last_name'];
    $email = $_POST['email'];
    $username = $_POST['username'];
    $password = $_POST['password'];

    $conn = new mysqli('localhost', 'root', '', 'students');

    if ($conn->connect_error) {
        die("Connection failed: " . $conn->connect_error);
    }

    $sql = "INSERT INTO users (first_name, last_name, email, username, password)
            VALUES ('$first_name', '$last_name', '$email', '$username', '$password')";

    if ($conn->query($sql) === TRUE) {
        echo "Registration successful!";
    } else {
        echo "Error: " . $sql . "<br>" . $conn->error;
    }

    $conn->close();
}
?>
```

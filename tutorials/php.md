### Question:
Create an associate array to store 15 items and with the help of array functions update,add,delete and sort the array and also use foreach statement
___
**Code:**

```php
<!DOCTYPE html>
<html>
<body>

<?php
$items = array(
    "item1" => "a1",
    "item2" => "a2",
    "item3" => "a3",
    "item4" => "a4",
    "item5" => "a5",
    "item6" => "a6",
    "item7" => "a7",
    "item8" => "a8",
    "item9" => "a9",
    "item10" => "a10",
    "item11" => "a11",
    "item12" => "a12",
    "item13" => "a13",
    "item14" => "a14",
    "item15" => "a15"
);

$items["item5"] = "changed";  
$items["item16"] = "changed item 16";
unset($items["item10"]);  
asort($items);
foreach ($items as $key => $value) {
    echo "$key => $value<br>";
}
?>

</body>
</html>
```

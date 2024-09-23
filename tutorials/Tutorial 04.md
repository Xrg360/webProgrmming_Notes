
1. create an array flower and add 3 flowers to it (2)
2. use push() and pop() to add and delete an element
3. use shift() and unshift()
4. use splice() to add elements in between

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Array Operations</title>
</head>
<body>
    <script>
        // 1. Create an array flower and add 3 flowers to it
        let flower = [];
        flower.push(prompt("Enter the name of the first flower:"));
        flower.push(prompt("Enter the name of the second flower:"));
        flower.push(prompt("Enter the name of the third flower:"));
        alert("Initial flowers: " + flower.join(", "));

        // 2. Use push() to add an element and pop() to delete the last element
        flower.push(prompt("Enter a flower to add at the end:"));
        alert("After adding a flower at the end: " + flower.join(", "));
        flower.pop();
        alert("After removing the last flower: " + flower.join(", "));

        // 3. Use shift() to remove the first element and unshift() to add a new element at the beginning
        flower.shift();
        alert("After removing the first flower: " + flower.join(", "));
        flower.unshift(prompt("Enter a flower to add at the beginning:"));
        alert("After adding a flower at the beginning: " + flower.join(", "));

        // 4. Use splice() to add elements in between
        let index = prompt("At which index do you want to add flowers (0, 1, 2...)?");
        let flower1 = prompt("Enter the first flower to add:");
        let flower2 = prompt("Enter the second flower to add:");
        flower.splice(index, 0, flower1, flower2);
        alert("After adding flowers at index " + index + ": " + flower.join(", "));
    </script>
</body>
</html>
```


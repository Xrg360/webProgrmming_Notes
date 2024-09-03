### 1. Set text color to your favourite color for `p` elements

```css
p {
    color: #4A90E2;
}
```

### 2. Set text color to blue for the element with `id="paragraph"`

```css
#paragraph {
    color: blue;
}
```

### 3. Set text color to green for elements with `class="css"`

```css
.css {
    color: green;
}
```

### 4. Set text color to orange and center align the text for `p`, `h1`, `h2`, and `h4` elements

```css
p, h1, h2, h4 {
    color: orange;
    text-align: center;
}
```

### 5. Use the universal selector to apply the same styling

```css
* {
    color: orange;
    text-align: center;
}
```

### HTML CODE:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Styling Tutorial</title>
    <link rel="stylesheet" href="styles.css"> 
</head>
<body>
    <h1>My Heading</h1>
    
    <p>This is a paragraph styled with my color.</p>
    
    <p id="paragraph">This paragraph has an ID and is styled with the color blue.</p>
    
    <p class="css">This paragraph has a class and is styled with the color green.</p>
    
    <h2>Subheading</h2>
    <h4>Another Subheading</h4>
    <p>Another paragraph</p>
</body>
</html>

```
1. List the order of precedence of levels of style and organize a sample a webpage for providing "KTU B-tech honours regulation 2019" for KTU and use embedded style sheet to apply minimum 5 styles
2. Organize a webpage for the event "Techfest 2024" at your campus and use inline stylesheet and external style sheets to apply a minimum 5 styles
3. Display the text content of p tag with 2 diff tags:
	1. style 1: text in blue colour, heading in red, right aligned with font style of italics and font size of 20.
	2. style 2: text in green colour, bg in yellow colour with font style of times new roman and font size of 14.
	and write the equivalent css code for style 1 and 2

### 1. Order of Precedence of Levels of Style

The order of precedence for CSS styles is as follows:
1. Inline styles
2. Embedded styles (Internal styles)
3. External styles
4. Browser default styles

#### Sample Webpage for "KTU B-tech Honours Regulation 2019" with Embedded Style Sheet

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KTU B-tech Honours Regulation 2019</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f0f0f0;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
            font-size: 2em;
        }
        h2 {
            color: #2980b9;
            text-align: center;
            font-size: 1.5em;
        }
        p {
            color: #2c3e50;
            margin: 20px;
            text-align: justify;
        }
        a {
            color: #e74c3c;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <h1>KTU B-tech Honours Regulation 2019</h1>
    <h2>Overview</h2>
    <p>The Kerala Technological University (KTU) has laid down specific regulations for the B-tech honours program for the academic year 2019. This document provides a comprehensive overview of the regulations and requirements for students pursuing the B-tech honours program.</p>
    <h2>Eligibility</h2>
    <p>To be eligible for the B-tech honours program, students must meet certain academic criteria, including a minimum GPA and completion of specific prerequisite courses.</p>
    <h2>More Information</h2>
    <p>For more details, visit the <a href="https://ktu.edu.in">KTU official website</a>.</p>
</body>
</html>
```

### 2. Webpage for "Techfest 2024" Using Inline and External Stylesheets

#### HTML (index.html)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Techfest 2024</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header style="background-color: #34495e; color: white; text-align: center; padding: 20px;">
        <h1>Techfest 2024</h1>
    </header>
    <section>
        <h2 style="color: #2980b9;">Event Details</h2>
        <p>Join us for Techfest 2024 at our campus. A celebration of technology and innovation, featuring workshops, competitions, and guest speakers.</p>
    </section>
    <footer>
        <p style="text-align: center;">&copy; 2024 Techfest</p>
    </footer>
</body>
</html>
```

#### External CSS (styles.css)

```css
body {
    font-family: 'Helvetica', sans-serif;
    background-color: #ecf0f1;
    margin: 0;
    padding: 0;
}
h2 {
    font-size: 1.8em;
    text-align: center;
}
p {
    font-size: 1em;
    line-height: 1.5;
    margin: 20px;
}
footer {
    background-color: #34495e;
    color: white;
    padding: 10px 0;
}
```

### 3. Display the Text Content of `<p>` Tag with Two Different Styles

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text Styles</title>
    <link rel="stylesheet" href="styles1.css">
    <link rel="stylesheet" href="styles2.css">
</head>
<body>
    <div class="style1">
        <p class="text1">This is a paragraph with style 1.</p>
    </div>
    <div class="style2">
        <p class="text2">This is a paragraph with style 2.</p>
    </div>
</body>
</html>
```

#### CSS for Style 1 (styles1.css)

```css
.text1 {
    color: blue;
    text-align: right;
    font-style: italic;
    font-size: 20px;
}
.text1::before {
    content: "Heading: ";
    color: red;
    display: block;
}
```

#### CSS for Style 2 (styles2.css)

```css
.text2 {
    color: green;
    background-color: yellow;
    font-family: 'Times New Roman', Times, serif;
    font-size: 14px;
}
```

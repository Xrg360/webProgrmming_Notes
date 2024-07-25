	Rohit Babu George S6 CSE-B
#### 1. Write the equivalent HTML code to implement the following in a web page:

1. An image titled “flower.jpg” with proper attributes to set height, width, and message text.
```html
<html>
<head>
    <title>Picture with Caption</title>
</head>
<body>
    <img src="flower.jpg" alt="A regular flower" width="550" height="430">
    <p>This is a typical flower</p>
</body>
</html>
```
2. Unordered list with values tea, coffee, and milk.
```html
<html>
<head>
    <title>Unordered List</title>
</head>
<body>
    <ul>
        <li>Tea</li>
        <li>Coffee</li>
        <li>Milk</li>
    </ul>
</body>
</html>
```

#### 2. Explain the following HTML tags with proper examples.

1. `<textarea>`
- The `<textarea>` tag defines a multi-line text input control.
- The `<textarea>` element is often used in a form, to collect user inputs like comments or reviews.
```html
<html>
<head>
    <title>Sample Form</title>
</head>
<body>
    <form>
        <label for="feedback">Feedback:</label><br>
        <textarea id="feedback" name="feedback" rows="4" cols="50"></textarea>
    </form>
</body>
</html>
```

2. `<span>`
	- The `<span>` tag is an inline container used to mark up a part of a text, or a part of a document.
```html
<html>
<head>
    <title>Span Tag Example</title>
</head>
<body>
    <p>This text contains a <span class="highlight">highlighted</span> segment.</p>
</body>
</html>
```

3. `<tr>`
- The `<tr>` tag defines a row in an HTML table.

```html
<html>
<head>
    <title>Table Row Example</title>
</head>
<body>
    <table border="1">
        <tr>
            <th>First Name</th>
            <th>Last Name</th>
        </tr>
        <tr>
            <td>Jane</td>
            <td>Smith</td>
        </tr>
    </table>
</body>
</html>
```

4. `<form>`
- The `<form>` tag is used to create an HTML form for user input.
```html
<html>
<head>
    <title>Sample Form</title>
</head>
<body>
    <form action="/submit_form" method="post">
        <label for="fullname">Full Name:</label><br>
        <input type="text" id="fullname" name="fullname"><br><br>
        <label for="useremail">Email:</label><br>
        <input type="email" id="useremail" name="useremail"><br><br>
        <input type="submit" value="Send">
    </form>
</body>
</html>
```

5. `<a>`
- The `<a>` tag defines a hyperlink, which is used to link from one page to another.
```html
<html>
<head>
    <title>Link Example</title>
</head>
<body>
    <p>Check out the <a href="https://www.example.com" target="_blank">Example Website</a>.</p>
</body>
</html>
```
#### 3. Design a webpage that displays the following table.
```html
<html>
    <head>
        <title>Automobile Brands and Models</title>
        <style>
            table, th, td {
                border: 1px solid black;
            }
        </style>
    </head>
    <body>
        <h1>Automobile Brands and Models</h1>
        <table>
           <tr>
                <th>Brand</th>
                <th>Model</th>
           </tr>
            <tr>
                <td>Dodge</td>
                <td>Challenger</td>
            </tr>
            <tr>
                <td>Maruti</td>
                <td>Swift</td>
            </tr>
            </tr>
            <tr>
                <td rowspan="2">Jeep</td>
                <td>Wrangler</td>
            </tr>
            <tr>
                <td>Fusion</td>
            </tr>
            </tr>
           <tr>
                <td rowspan="2">Ford</td>
                <td>Fiesta</td>
            </tr>
            <tr>
                <td>Escape</td>
            </tr>
          <tr>
                <td>BMW</td>
                <td>5 Series</td>
            </tr>
        </table>
    </body>
    </html>
````

#### 4. Write down the general format of an HTTP request and an HTTP response. What is the purpose of the following HTTP headers? Also, identify whether they are included with an HTTP header/response or both.


#### 5. Why do you call MIME as an extension feature? Justify with suitable statements.

>[!info] MIME Extension Feature
> MIME (Multipurpose Internet Mail Extensions) is called an extension feature because it extends the format of email to support text in character sets other than ASCII, as well as attachments like audio, video, images, and application programs.

#### 6. Discuss URIs and URLs.

>[!abstract] URIs vs URLs
> - **URI (Uniform Resource Identifier):** A string of characters used to identify a resource.
> - **URL (Uniform Resource Locator):** A subset of URI that provides a means to access a resource by specifying its location.

| **Aspect**       | **URI**                                          | **URL**                                          |
|------------------|--------------------------------------------------|--------------------------------------------------|
| **Definition**   | Uniform Resource Identifier                      | Uniform Resource Locator                         |
| **Purpose**      | Identifies a resource either by location, name, or both | Specifically identifies the location of a resource |
| **Components**   | Scheme, authority, path, query, fragment         | Scheme, authority, path, query, fragment         |
| **Example**      | `mailto:example@example.com`                     | `https://www.example.com/index.html`             |
| **Types**        | Includes URLs and URNs                           | A type of URI that provides a means to locate the resource |
| **Usage**        | Used to identify any resource in a unique manner | Used to locate a specific resource on the web    |
| **Specificity**  | Can be more general                              | Always specific to the location                  |

#### 7. Define MIME? List any two features offered by MIME to email services.

>[!note] MIME Definition and Features
> - **MIME (Multipurpose Internet Mail Extensions):** A standard that extends the format of email to support non-text attachments.
> - **Features:**
>   1. Supports multimedia content (images, audio, video).
>   2. Allows for attachments of files in email.

#### 8. What is the purpose of the attributes `autoplay`, `src`, and `controls` when used with the `<audio>` tag?

Audio Tag Attributes
 - **autoplay:** Automatically starts playing the audio as soon as it is loaded.
 - **src:** Specifies the source file of the audio.
 - **controls:** Provides audio controls like play, pause, and volume.

#### 9. How will you navigate between sections in the same web page? Illustrate with an appropriate example.

```html
<html>
<head>
    <title>Navigation Example</title>
</head>
<body>
    <h2>Navigation Example</h2>
    <p><a href="#section1">Go to Section 1</a></p>
    <p><a href="#section2">Go to Section 2</a></p>
    <h3 id="section1">Section 1</h3>
    <p>This is section 1.</p>
    <h3 id="section2">Section 2</h3>
    <p>This is section 2.</p>
</body>
</html>
```

#### 10 Create an HTML form for registering to a job site which includes fields to enter your name, address, email, contact number, a date picker to include your date of birth, radio buttons to select your sex, checkboxes to show your area of interest, a selection list to input your experience with a submit and reset button. All fields must be labelled appropriately.

```html
<html>
<head>
    <title>Job Site Registration</title>
</head>
<body>
    <h2>Register</h2>
    <form action="/submit_registration" method="post">
        <label for="name">Name:</label><br>
        <input type="text" id="name" name="name"><hr>
        <label for="address">Address:</label><br>
        <textarea id="address" name="address" rows="4" cols="50"></textarea><hr>
        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email"><hr>
        <label for="contact">Contact Number:</label><br>
        <input type="tel" id="contact" name="contact"><hr>
        <label for="dob">Date of Birth:</label><br>
        <input type="date" id="dob" name="dob"><hr>
        <label>Sex:</label><br>
        <input type="radio" id="male" name="sex" value="male">
        <label for="male">Male</label><br>
        <input type="radio" id="female" name="sex" value="female">
        <label for="female">Female</label><hr>
        <label>Area of Interest:</label><br>
        <input type="checkbox" id="development" name="interest" value="development">
        <label for="development">Development</label><br>
        <input type="checkbox" id="design" name="interest" value="design">
        <label for="design">Design</label><hr>
        <label for="experience">Experience:</label><br>
        <select id="experience" name="experience">
            <option value="fresher">Fresher</option>
            <option value="1-3">1-3 years</option>
            <option value="3-5">3-5 years</option>
            <option value="5+">5+ years</option>
        </select><hr>
        <input type="submit" value="Submit">
        <input type="reset" value="Reset">
    </form>
</body>
</html>
```

#### 11. Give the syntax to create hyperlinks in HTML. List any 3 target attributes and their purpose associated with hyperlinks. Also, how will you identify an active link, visited link, and unvisited link?

>[!example] Hyperlink Syntax
>  :)
>```html
><a href="url" target="target">link text</a>
>```

- **Target Attributes:**
  - `_blank`: Opens the linked document in a new window or tab.
  - `_self`: Opens the linked document in the same frame as it was clicked (default).
  - `_parent`: Opens the linked document in the parent frame.

>[!info] Link Identification
> - **Active link:** Styled using `:active` pseudo-class.
> - **Visited link:** Styled using `:visited` pseudo-class.
> - **Unvisited link:** Styled using `:link` pseudo-class.

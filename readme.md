# HTML and CSS fundamentals

## Web Development Basics

1. **Clients & Servers**

   - A **client** is a device (like your phone or computer) that requests information from a website.

   - A **server** is a powerful computer that stores website data and sends it to clients when requested.

   > **Example:** When you type a website address (`www.google.com`) into your browser, your device **client** **requests** the page from a **server**, which then sends back the webpage as the **response**.

2. **Static vs. Dynamic Websites**

   - **Static Websites:** These show the same content to everyone and don’t change unless the developer manually updates them.

   > **Example:** A basic personal portfolio website.

   - **Dynamic Websites:** These update content based on user interaction or data from a database.

   > Example: Facebook, Amazon (where content changes based on users).

3. **Frontend vs. Backend**

   - **Frontend (Client-side):** Everything users see and interact with in their browser.

   - **Backend (Server-side):** The logic, database, and server operations that make the website function.

4. **Core Technologies**

   - **Frontend Technologies:**

     - **HTML** – Defines the **structure** (headings, paragraphs, buttons).
     - **CSS** – **Styles** the website (colors, fonts, layout).
     - **JavaScript** – Adds **interactivity** (buttons, animations, pop-ups).

   - **Backend Technologies:**

     - `Python`, `JavaScript` (`Node.js`), `PHP`, `Java`, `Ruby`, etc.

     - `MySQL`, `PostgreSQL`, `MongoDB` (store and manage data).

     - `Apache`, `Nginx`, cloud platforms like `AWS`.

---

## Fundamentals of HTML

### HTML

- HTML (**HyperText Markup Language**) is the standard language for creating web pages.

- It defines the structure of a webpage using elements.

- HTML documents are composed of tags that define different parts of a webpage, such as headings, paragraphs, links, images, and more.

- HTML files have a `.html` extension and can be viewed in any web browser.

### HTML Document Structure

Basic structure of a HTML document:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Welcome to HTML</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

`<!DOCTYPE html>`: Declares the document type as HTML5.

`<html>`: The root element of the HTML document.

`<head>`: Contains meta information such as the title and links to stylesheets.

`<title>`: Defines the title of the webpage (appears in the browser tab).

`<body>`: Contains all the visible content of the page.

### HTML Elements & Tags

HTML consists of **elements** enclosed in **tags**:

Types of Tags are

- **Opening Tag:** Used to start an element. Example: `<p>`

- **Closing Tag:** Ends an element. Example: `</p>`

- **Self-closing Tags (Void Elements):** These tags do not require a closing tag. Example: `<br />`, `<img />`, `<input />`

### Common HTML elements and attributes

```html
<!-- Headings -->

<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>

<!-- Text Elements -->
<p>Paragraph</p>
<strong>Bold Text</strong>
<em>Italic Text</em>
<mark>Highlighted Text</mark>
<small>Small Text</small>
<del>Strikethrough Text</del>
<ins>Underlined Text</ins>
<sub>Subscript Text</sub>
<sup>Superscript Text</sup>
<blockquote>Blockquote for citing sources</blockquote>

<!-- Lists -->
<ul>
  <li>Unordered List Item</li>
</ul>
<ol>
  <li>Ordered List Item</li>
</ol>

<!-- Links -->
<a href="https://example.com">Click Here</a>

<!-- Images -->
<img src="image.jpg" alt="Description" width="200" height="100" />

<!-- Tables -->
<table border="1">
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
  </tr>
</table>

<!-- Forms and Inputs -->
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required />

  <label for="gender">Gender:</label>
  <select id="gender" name="gender">
    <option value="male">Male</option>
    <option value="female">Female</option>
    <option value="other">Other</option>
  </select>

  <input type="submit" value="Submit" />
</form>

<!-- Semantic Elements -->

<header>
  <h1>Website Header</h1>
</header>

<nav>
  <a href="#">Home</a>
  <a href="#">About</a>
</nav>

<section>
  <main>
    <h2>About Us</h2>
    <p>Details about our company.</p>
  </main>

  <aside>
    <article>
      <h3>Related Information</h3>
      <p>Objects such as a computer or phone or something.</p>
    </article>
  </aside>
</section>

<figure>
  <img src="image.jpg" alt="A meaningful description" />
  <figcaption>Image Caption</figcaption>
</figure>

<footer>
  <p>&copy; 2025 My Website</p>
</footer>
```

Semantic HTML was introduced after HTML5, before which everything was contained in `<div>`**Everything**`</div>` to make up the layout of webpages. Developers used multiple `<div>` elements with classes and IDs to style and organize content, making the code harder to read and maintain. With the introduction of semantic elements, web pages became more structured, improving accessibility, readability, and SEO ranking.

This change makes the code more meaningful and improves its interpretation by browsers, search engines, and assistive technologies.

---

## Fundamentals of CSS

- **C**ascading **S**tyle **S**heets

- CSS describes the **visual style and presentation** of the **content written in HTML**

- CSS consists of countless **properties** that developers use to format the content: properties about font, text, spacing, layout etc.

### **CSS Syntax**

```css
selector {
  property: value;
}
```

- **Selector:** Specifies the HTML element(s) to style.

- **Declaration:** A property-value pair inside curly brackets.

- **Property:** Defines what aspect of the element to style (e.g., color, font-size).

- **Value:** Specifies how the property should be applied (e.g., red, 20px).

`Example:`

```css
p {
  font-size: 18px;
  color: blue;
}
```

### **The 3 ways to apply CSS**

1. **Inline CSS** - applies styles directly within an HTML element

```html
<p style="color: blue; font-size: 20px;">This is a blue paragraph.</p>
```

2. **Internal CSS** - defined within a `<style>` tag inside the `<head>` section of the HTML document

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         p {
           color: green;
           font-size: 18px;
         }
       </style>
     </head>
     <body>
       <p>This is a green paragraph.</p>
     </body>
   </html>
   ```

3. **External CSS** - written in an external `.css` file which is linked using the `<link>` tag in the `<head>` section of the HTML document.

   ```html
   <!-- Linking the external file -->
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="styles.css" />
     </head>
     <body>
       <p>This paragraph is styled with an external CSS file.</p>
     </body>
   </html>
   ```

   ```css
   /* External CSS file  */
   p {
     color: red;
     font-size: 16px;
     font-weight: bold;
   }
   ```

### **CSS Selectors**

Let us get to know about how to choose elements from the document to style by using various types of CSS selectors, in an incrementing order of their specificities/priority.

- **Universal Selector (\*)**

  Selects all elements in the document and inherits all properties, even those which do not get inherited, to every element of the document.

  Least specificity.

  ```css
  * {
    margin: 0;
    padding: 0;
  }
  ```

- **Type/Element Selector**

  Selects all elements of a specific type (tag name).

  ```css
  h1 {
    color: blue;
  }
  ```

- **Class Selector (.)**

  Selects elements with a specific class name.

  Classes can be applied to multiple elements and are commonly used in real-world applications for reusable styles.

  ```css
  .intro {
    font-size: 20px;
    color: green;
  }
  ```

  _Usage in HTML:_

  ```html
  <p class="intro">This is an introduction paragraph.</p>
  ```

- **ID Selector (#)**

  Selects a unique element by its ID.

  IDs should be unique within a document and are more specific than class selectors.

  ```css
  #main-title {
    font-size: 30px;
    font-weight: bold;
  }
  ```

  _Usage in HTML:_

  ```html
  <h1 id="main-title">Welcome to CSS</h1>
  ```

- **Descendant Selector**

  Selects elements that are inside a specific parent element.

  ```css
  div p {
    color: purple;
  }
  ```

  _Usage in HTML:_

  ```html
  <div>
    <p>This paragraph inside a div will be purple.</p>
  </div>
  ```

- **Adjacent Selector**

  This selects the adjacent sibling elements and is denoted by a `+` sign.

  siblings are the elements present inside of a same parent element.

  ```css
  /* Select all paragraphs which come just after an h2 element */
  h2 + p {
    color: red;
  }

  h2 + p::first-letter {
    font-size: 40px;
  }
  ```

- **Pseudo-classes**

  Pseudo-classes define a special state of an element.

  ```css
  /* Style first child of a parent element*/
  p:first-child {
    font-weight: bold;
  }

  /* Style last child of a parent element*/
  p:last-child {
    font-style: italic;
  }

  /* Style nth child of a parent element*/
  li:nth-child(2) {
    color: orange;
  }

  /*---------------------------------------------------------------
    Pseudo classes are most commonly used to style hyperlinks in the same order as given below and it is good practice to keep the link & visited together and the hover and active together. But we can use them anyhow we like. 
   ---------------------------------------------------------------*/

  /* Style unvisited links */
  a:link {
    color: blue;
  }

  /* Change color when hovered */
  a:hover {
    color: red;
  }

  /* Style visited links */
  a:visited {
    color: purple;
  }

  /* Style when an element is active */
  button:active {
    background-color: yellow;
  }
  ```

- **Pseudo Elements**

  Pseudo elements can select elements that are not actual HTML elements such as first-letter or first-line of a paragraph or text

  and

  also used to create fake first children elements without adding them in our HTML document which is commonly used to add cosmetic styles such as small tags or labels.

  ```css
  /* change font style of the first letter of heading */
  h1::first-letter {
    font-style: normal;
  }

  /* change color to red of every paragraphs first line */
  p::first-line {
    color: red;
  }

  /* Create a cosmetic style by faking an element that is automatically the first child of the element on which we use the ::after pseudo element 
  Points to remember
    - always need to have a content
    - inline by nature
  
  */
  h2 {
    position: relative;
  }

  h2::after {
    content: "TOP";
    background-color: #ffe70e;
    color: #444;
    font-size: 16px;
    font-weight: bold;
    display: inline-block;
    padding: 5px 10px;
    position: absolute;
    top: -10px;
    right: -25px;
  }
  ```

- **The !important Keyword**

  - The !important rule is used to override all other declarations, regardless of specificity.

  - It should be used sparingly as it can make debugging styles difficult.

  ```css
  /* Important keyword in CSS has the highest priority */
  p {
    font-size: 18px !important;
  }
  ```

### **Common CSS Properties**

- **Text Properties**

  - will inherit automatically

  ```css
  p {
    font-size: 10px;
    font-family: sans-serif;
    font-style: italic;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    line-height: 1.5;
  }
  ```

- **Color Properties**

  - 3 common notations
    - `rgb` - red, green and blue with values from **0** to **255** creating **16.8 million** colors
    - `rgba` - red, green and blue with a alpha value for transperency
    - `hexadecimal` - values ranging from **0** to **15** with last value noted as **f**

  ```css
  div {
    color: #fff;
    background-color: rgb(0, 0, 0);
  }
  ```

- **Dimension Properties**

  - Can use percentage as value to cover only that percent of the parent element.

  ```css
  div {
    width: 100%;
    height: 500px;
  }
  ```

- **Shorthand Properties**

  - One property defining the values of multiple properties

  ```css
  div {
    border-top: 5px solid #000;
    border-bottom: 5px solid #000;
    border-left: 5px solid #000;
    border-right: 5px solid #000;
    border: 5px solid #000; /* border will define all*/

    text-decoration-line: underline;
    text-decoration-color: #1098ad;
    text-decoration-style: dotted;
    text-decoration: dashed underline #1098ad; /* text-decoration will define all */

    padding-left: 10px;
    padding-right: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
    padding: 10px; /* padding will define all */

    margin-left: 10px;
    margin-right: 10px;
    margin-top: 10px;
    margin-bottom: 10px;
    margin: 10px; /* margin will define all */
  }
  ```

### **The CSS Box Model**

Every HTML element is a rectangular box, and the CSS Box Model defines how the element's size is calculated:

- **Content** - The actual text or images inside the element.

- **Padding** - Space between the content and the border.

- **Border** - The boundary surrounding the padding.

- **Margin** - Space outside the border, separating the element from others.

```css
div {
  width: 200px;
  height: 100px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
}

/*

## How Calculation Is Done According To The CSS BOX MODEL ## 

Width = left border + left padding + content width + right padding + right border   
Height = top border + top padding + content height + bottom padding + bottom border   

*/
```

### **Positioning Model in CSS**

The CSS Positioning Model defines how elements are positioned in a document.

- **Static Positioning** `default`

  Elements are placed in the normal document flow.

  ```css
  div {
    position: static;
  }
  ```

- **Relative Positioning**

  Moves an element relative to its normal position.

  ```css
  div {
    position: relative;
    top: 20px;
    left: 10px;
  }
  ```

- **Absolute Positioning**

  Moves an element relative to its nearest positioned ancestor.

  ```css
  div {
    position: absolute;
    top: 50px;
    left: 50px;
  }
  ```

- **Fixed Positioning**

  Positions an element relative to the viewport (remains fixed even on scroll).

  ```css
  div {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
  }
  ```

- **Sticky Positioning**

  Behaves like relative until it reaches a defined position, then sticks.

  ```css
  div {
    position: sticky;
    top: 10px;
  }
  ```

### **Inheritance in CSS**

- Some properties are inherited by **default**, such as text properties (**color**, **font-family**, **visibility**).

- Other properties, like **width**, **height**, **border**, and **margin**, are **not** **inherited**.

- The `body` selector is often used to apply **global styles** to the document since text-related properties will be inherited by child elements.

- The `universal (\*)` selector can also be used to enforce consistency across all elements and apply a **global reset** for **margin** and **padding** commonly.

- You can control inheritance using:

  - `inherit` (forces inheritance)

  - `initial` (resets to default)

  - `unset` (removes inheritance if inherited, otherwise resets to default)

```css
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: sans-serif;
  font-weight: 300;
  color: #333;
}

div {
  color: inherit;
}
```

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

     - **HTML** – Defines the structure (headings, paragraphs, buttons).
     - **CSS** – Styles the website (colors, fonts, layout).
     - **JavaScript** – Adds interactivity (buttons, animations, pop-ups).

   - **Backend Technologies:**

     - \*\* \*\* Python, JavaScript (Node.js), PHP, Java, Ruby, etc.

     - \*\* \*\* MySQL, PostgreSQL, MongoDB (store and manage data).

     - \*\* \*\* Apache, Nginx, cloud platforms like AWS.

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

# HTML and CSS fundamentals

## Web Development Basics

### 1. Clients & Servers

- A **client** is a device (like your phone or computer) that requests information from a website.

- A **server** is a powerful computer that stores website data and sends it to clients when requested.

  > **Example:** When you type a website address (`www.google.com`) into your browser, your device **client** **requests** the page from a **server**, which then sends back the webpage as the **response**.

### 2. Static vs. Dynamic Websites

- **Static Websites:** These show the same content to everyone and don’t change unless the developer manually updates them.

  > **Example:** A basic personal portfolio website.

- **Dynamic Websites:** These update content based on user interaction or data from a database.

  > Example: Facebook, Amazon (where content changes based on users).

### 3. Frontend vs. Backend

- **Frontend (Client-side):** Everything users see and interact with in their browser.

- **Backend (Server-side):** The logic, database, and server operations that make the website function.

### 4. Core Technologies

#### **Frontend Technologies:**

- **HTML** – Defines the **structure** (headings, paragraphs, buttons).
- **CSS** – **Styles** the website (colors, fonts, layout).
- **JavaScript** – Adds **interactivity** (buttons, animations, pop-ups).

#### **Backend Technologies:**

- `Python`, `JavaScript` (`Node.js`), `PHP`, `Java`, `Ruby`, etc.

- `MySQL`, `PostgreSQL`, `MongoDB` (store and manage data).

- `Apache`, `Nginx`, cloud platforms like `AWS`.

---

## Fundamentals of HTML

### 1. HTML?

- HTML (**HyperText Markup Language**) is the standard language for creating web pages.

- It defines the structure of a webpage using elements.

- HTML documents are composed of tags that define different parts of a webpage, such as headings, paragraphs, links, images, and more.

- HTML files have a `.html` extension and can be viewed in any web browser.

### 2. HTML Document Structure

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

### 3. HTML Elements & Tags

HTML consists of **elements** enclosed in **tags**:

Types of Tags are

- **Opening Tag:** Used to start an element. Example: `<p>`

- **Closing Tag:** Ends an element. Example: `</p>`

- **Self-closing Tags (Void Elements):** These tags do not require a closing tag. Example: `<br />`, `<img />`, `<input />`

### 4. Common HTML elements and attributes

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

### 5. Semantic HTML

Semantic HTML was introduced after HTML5, before which everything was contained in `<div>`**Everything**`</div>` to make up the layout of webpages. Developers used multiple `<div>` elements with classes and IDs to style and organize content, making the code harder to read and maintain. With the introduction of semantic elements, web pages became more structured, improving accessibility, readability, and SEO ranking.

This change makes the code more meaningful and improves its interpretation by browsers, search engines, and assistive technologies.

---

## Fundamentals of CSS

- **C**ascading **S**tyle **S**heets

- CSS describes the **visual style and presentation** of the **content written in HTML**

- CSS consists of countless **properties** that developers use to format the content: properties about font, text, spacing, layout etc.

### 1. CSS Syntax

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

### 2. The 3 ways to apply CSS

#### **Inline CSS**

Applies styles directly within an HTML element

```html
<p style="color: blue; font-size: 20px;">This is a blue paragraph.</p>
```

#### **Internal CSS**

defined within a `<style>` tag inside the `<head>` section of the HTML document

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

#### **External CSS**

Written in an external `.css` file which is linked using the `<link>` tag in the `<head>` section of the HTML document.

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

### 3. CSS Selectors

Let us get to know about how to choose elements from the document to style by using various types of CSS selectors, in an incrementing order of their specificities/priority.

#### **Universal Selector (\*)**

Selects all elements in the document and inherits all properties, even those which do not get inherited, to every element of the document.

Least specificity.

```css
* {
  margin: 0;
  padding: 0;
}
```

#### **Type/Element Selector**

Selects all elements of a specific type (tag name).

```css
h1 {
  color: blue;
}
```

#### **Class Selector (.)**

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

#### **ID Selector (#)**

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

#### **Descendant Selector**

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

#### **Adjacent Selector**

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

#### **Pseudo-classes**

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

#### **Pseudo Elements**

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

#### **The !important Keyword**

- The !important rule is used to override all other declarations, regardless of specificity.

- It should be used sparingly as it can make debugging styles difficult.

```css
/* Important keyword in CSS has the highest priority */
p {
  font-size: 18px !important;
}
```

### 4. Common CSS Properties

#### **Text Properties**

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

#### **Color Properties**

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

#### **Dimension Properties**

- Can use percentage as value to cover only that percent of the parent element.

```css
div {
  width: 100%;
  height: 500px;
}
```

#### **Shorthand Properties**

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

### 5. The CSS Box Model

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

### 6. Positioning Models in CSS

The CSS Positioning Model defines how elements are positioned in a document.

#### **Static Positioning** `default`

Elements are placed in the normal document flow.

```css
div {
  position: static;
}
```

#### **Relative Positioning**

Moves an element relative to its normal position.

```css
div {
  position: relative;
  top: 20px;
  left: 10px;
}
```

#### **Absolute Positioning**

Moves an element relative to its nearest positioned ancestor.

```css
div {
  position: absolute;
  top: 50px;
  left: 50px;
}
```

#### **Fixed Positioning**

Positions an element relative to the viewport (remains fixed even on scroll).

```css
div {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
```

#### **Sticky Positioning**

Behaves like relative until it reaches a defined position, then sticks.

```css
div {
  position: sticky;
  top: 10px;
}
```

### 7. Inheritance in CSS

- Some properties are inherited by **default**, such as text properties (**color**, **font-family**, **visibility**).

- Other properties, like **width**, **height**, **border**, and **margin**, are **not** **inherited**.

- The `body` selector is often used to apply **global styles** to the document since text-related properties will be inherited by child elements.

- The `universal (\*)` selector can also be used to enforce consistency across all elements and apply a **global reset** used for **margin** and **padding** commonly, also used for **box-sizing** for better control of the box-model measurements.

- You can control inheritance using:

  - `inherit` (forces inheritance)

  - `initial` (resets to default)

  - `unset` (removes inheritance if inherited, otherwise resets to default)

```css
/* global reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box; /* --> see the floats section for detail */
}

/* inheritance to text properties to make our code future ready for changes */
body {
  font-family: sans-serif;
  font-weight: 300;
  color: #333;
}

div {
  color: inherit;
}
```

## Layouts: Floats, Flexbox, and CSS Grid Fundamentals

One of the main application of CSS is to build Layouts of webpages.

### 1. Layout

- Layout is the way text, images and other content is placed and arranged on a webpage, to make the webpage or website visually beautiful and making the content more readable, organized and attractive.

- Layout gives the page a visual structure, into which we place our content.

- **Building a Layout:** arranging page elements into a visual structure, instead of simply having them placed one after another (Normal Flow).

The two types of layouts are

#### **Page layout**

Laying out the big pieces of content inside of a webpage or website.

#### **Component layout**

These bigger page layout are themselves made up of components which also need to be arranged in some kind of layout.

### 2. The 3 ways of Building Layouts

#### **Floats**

##### **The float property**

The **float property** is the **old way of creating layouts** and is getting outdated very fast. Even though **float property** is **not a positioning scheme**, it is used to **take elements out of the flow** similar to absolute positioning. The common difference between both is that -

- Absolute positioning removes the element from the document flow and has no effect on surrounding elements.

- Floated elements are also removed from flow, but can still affect surrounding content (like text wrapping around an image), though they are not affected by surrounding content.

##### **Using float property**

Before using floats we need to make sure that

- the **widths** of our elements are properly set to **fit the actual layout** that **we are going for**. This will make sure that the **elements do not overflow** or jump out of the container element.

> A very common practice to make this task a little easier is to add a global reset of the box-model so that it does not behave in a weird way due to its natural order of calculation of widths and heights.
>
> ```css
> /* A Global Reset used to control the weird default behaviour of the box model in CSS */
> * {
>   box-sizing: border-box;
> }
> ```

To float an element we just set the **float property** to either of one value - **left** or **right**.

`Example :-`

```css
.child-el--1 {
  float: left;
}
.child-el--2 {
  float: right;
}
```

##### **Clearing floats**

**Collapsing elements :** If we float all child elements of a parent element this will collapse the height of the parent element as there will practically be no element inside of the parent element so to fix this problem of **callapsing elements** we usually **clear floats**.

- **clear floats**

  In the empty parent element add a empty div with a clear class **.clear** with clear property at a value of both to clear both floats left and right in any case.

  ```css
  .clear {
    clear: both;
  }
  ```

But, this method was very impractical as if there were multiple elements with collapsed height adding so many divs unnescessarily would be a very bad idea producing a cluttered code base.

- **clearfic hack**

  The **clearfix hack** method was a fix to the previous method of an empty div and was used widely for many years.

  - Add a clearfix class on the collapsing element
  - The clearfix class will contain a after or before pseuodo element
    - content will be empty
    - clear both floats
    - element must be a block level element

  ```css
  .cleearfix::after {
    content: "";
    clear: both;
    display: block;
    /* By default pseudo elements are inline elements */
    /* Clearing floats really works on only a block level element */
  }
  ```

#### **Flexbox**

- Flexbox is a **set of related CSS Properties** for building **1 Dimension layouts**.

- The main idea behind flexbox is that **empty space** inside a container element can be **divided by its child elements**.

- flexbox also makes it easy to **automatically align items** to one another inside a parent container, **both horizontally and vertically**.

- Flexbox **solves common problems** such as **vertical centering** and **creating equal-height columns**.

To start with flexbox we just need to set the **display property to flex** on a container element which contains some child elements in it.
Imediately all the child elements are side by side without using floats and these elements are called **flex-items** as they are the **child elements of the flex container**.

```css
.container {
  display: flex;
}
```

- **Horizontally** each flex item **occupies exactly the space necessary** for its content.

- **Vertically** things are different. **Vertically by default** all the **flex items** are as tall as the tallest item or say they are **stretched**.

##### **Terminologies:**

- **`Flex-container :`** element on which we want to use flexbox is called a flex-container.
- **`Flex-items :`** all the direct children of a flex-container are flex-items.
- **`Main-axis :`** the direction in which the flex-items are laid out is the main-axis.
- **`Cross-axis :`** The other perpendicular direction is the cross-axis.
  - Axis are important as we can change their direction and align elements along the axis, so we need to know which axis we are dealing with.

##### **Cheatsheet for flexbox properties**

![Flexbox Properties Cheatsheet](./The%20Code%20Magzine/imgs/flexbox-cheatsheet.png)

`99%` of most common problems can be solved using these properties.

#### **CSS Grid**

**CSS grid** is the most modern way of building **2-dimensional layouts**, and also the most complete one. It is also the **easiest way** to build layouts atleast if we only use the fundamentals.

- CSS Grid is a **set of CSS properties** that web developers can use **to build 2-dimensional layouts**.

- The main idea behind it was that now we could **divide a container element into rows and columns** that we could **then fill with it's child elements**. And a lot of stuff is possible here.

  - **Span** elements across multiple rows and columns.
  - **Overlap** different elements.

- Css grid is used in 2-dimensional contexts allowing us to write a lot **less nested HTML and easier to read CSS**.

- CSS grid completely **revolutionized CSS**.

- **CSS grid** is not to replace **flexbox** instead they both work together perfectly and are meant to go **hand-in-hand**.

##### **Use of CSS Grid**

- To get started with a **simple grid** we need to set the **display** property to **grid** on the container element. The child elements of this **grid-container** are called the **grid-items**.

  ```css
  .container {
    display: grid;
  }
  ```

- Now we can create/define the **columns** and **rows** using the properties **grid-template-column** and **grid-template-row** respectively. As soon as we create some columns the grid-items will be displayed in columns and rows, and So, as many rows will be created automatically as necessary. These automatically created rows are called the **implicit rows** whereas if we define them ourselves they are called as **explicit rows**.

  ```css
  .container {
    grid-template-column: 150px 150px;
    grid-template-row: 50px 50px;
  }
  ```

##### **Terminologies**

- **`Grid-container :`** This is where everything happens and we create a grid container by setting it's display property to grid.

- **`Grid-items :`** All the child elements of the grid container are called grid-items.

- **`Row-axis :`** horizontal

- **`Column-axis :`** vertical

  Unlike flexbox we cannot change the direction of these axis and this makes it more easier to work with CSS grid.

- **`Grid-lines :`** Divide up the grid and seperate the columns and rows. these grid lines are numbered from 1 to the number of columns/rows + 1. These are used to place a grid-item in a specific place in the grid according to the column and rows.

- **`Grid-cells :`** All the areas created by the intersection of both the grid lines for the columns and the rows are grid cells. grid cells are always created but they do not always need to be filled.

- **`Gutters/Gaps :`** So the spaces between grid items we create are the gutters or gaps.

- **`Grid-tracks :`** So a grid column or a row is also called a grid-track.And we call these tracks because these concepts are a bit more about the space itself and not about the grid items.

##### **Sizing**

- There are **various units** that are available to use while defining the **columns/rows**.

  - `px`
  - `fr`
  - `%`
  - `auto`

- There is also the **repeat function** which makes creating multiple columns rows more easy if they are of the same unit value.

  ```css
  /* px (pixels unit value) */
  .container {
    grid-template-column: 150px 250px;
    grid-template-row: 100px 150px;
  }

  /* fr (fractional unit value) */
  .container {
    grid-template-column: 1fr 1fr 1fr 1fr;
    grid-template-row: 2fr 1fr;
  }

  /* % (percentage unit value) */
  .container {
    grid-template-column: 25% 25% 20% 20% 10%;
    grid-template-row: 60% 40%;
  }

  /* auto (auto unit value) */
  .container {
    grid-template-column: auto 1fr 1fr auto;
    grid-template-row: 2fr auto 1fr;
  }

  /* repeat function */
  .container {
    grid-template-column: repeat(4, 1fr);
  }
  ```

- We can also define the **gap** property similar to flexbox which is the **only way to define space between grid items**. Earlier it was called **grid-gap** but they removed the grid prefix after gap property was also added to flexbox.

  ```css
  .container {
    gap: 20px;
  }
  ```

- The column and row gaps can be defined seperately too.

  ```css
  .container {
    column-gap: 20px;
    row-gap: 40px;
  }
  ```

- grid items are stretched by default.

##### **Placing and Spanning**

- The **grid-lines** are used to **place grid-items** in specific places in the grid by defining the properties **grid-column** and **grid-row** as shown below.

  ```css
  .child-el-1 {
    grid-column: 2/3;
    grid-row: 1/2;
  }
  ```

- grid-items can also span multiple grid-cells by either using **grid-line numbers** or **span keyword**.

  ```css
  .child-el-2 {
    grid-column: 2 / span 2;
    grid-row: 1 / span 3;
  }
  ```

- There is also a trick of using the **negative number** to span till the end of the grid which works due to the grid lines defined by both positive and negative values in opposite directions.

  ```css
  .child-el-2 {
    grid-column: 1/-1;
    grid-row: 2/-1;
  }
  ```

> There are **dev-tools** in the browser itself that highlight the **grid lines** marked with their respective numbers starting from **1** to **number of columns + 1**.

##### **Aligning Grid-items and Tracks**

Aligning grid-items is a little different in css grid than in flexbox, because **we can align both the tracks inside the container** and **the grid-items inside the tracks**.

- **Aligning tracks inside grid-container** is done by **align-content** and **justify-content** for vertical and horizontal alignment respectively.

  ```css
  .container {
    align-content: center;
    justify-content: center;
  }
  ```

- **Aligning items inside the tracks or cells** can be done using the **align-items** and **justify-items** for vertical and horizontal alignment respectively.

  ```css
  .container {
    align-items: center;
    justify-items: center;
  }
  ```

##### **Cheatsheet for CSS grid properties**

![Flexbox Properties Cheatsheet](./The%20Code%20Magzine/imgs/grid-cheatsheet.png)

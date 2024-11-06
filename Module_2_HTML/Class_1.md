### **Introduction to HTML**

**Objective:** Understand the basics of HTML structure and create your first HTML document.

#### 1. What is HTML?

HTML (HyperText Markup Language) is the standard language for creating webpages. It uses tags to structure and organize content so that browsers know how to display it.

- **Tags** are the building blocks of HTML, usually written as `<tag>content</tag>`.
- HTML documents are plain text files with the `.html` extension.

#### 2. Basic HTML Structure

An HTML document has a specific structure:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Webpage</title>
  </head>
  <body>
    <h1>Welcome to My Webpage</h1>
    <p>This is my first paragraph in HTML.</p>
  </body>
</html>
```

- **`<!DOCTYPE html>`**: Declares the document as HTML5. It helps browsers understand the type of document they’re reading.
- **`<html>`**: The root element that contains all HTML content.
- **`<head>`**: Contains metadata (information about the document, like the title or links to stylesheets).
- **`<title>`**: Sets the page title that appears in the browser tab.
- **`<body>`**: Contains the content that displays on the webpage (text, images, links, etc.).

#### 3. Creating Your First HTML Document

1. **Open a Text Editor**: Use a text editor like Notepad, VS Code, or Sublime Text.
2. **Write Your HTML Code**: Copy the code above and paste it into your text editor.
3. **Save Your File**: Save it as `index.html`.
4. **Open in a Browser**: Double-click the file to open it in a web browser. You should see a page with a heading and a paragraph.

#### 4. Practice Task

1. Change the `<title>` content to "My Awesome Webpage" and refresh your browser to see the updated title.
2. Inside the `<body>`, add a second paragraph using the `<p>` tag: `<p>This is another paragraph!</p>`

---

### **Essential Tags and Structure**

**Objective:** Learn the most commonly used HTML tags for structuring text and practice creating formatted content.

#### 1. Headings and Paragraphs

Headings and paragraphs are the basic building blocks of text content on a webpage.

- **Headings**: There are six levels, from `<h1>` (largest) to `<h6>` (smallest). Typically, `<h1>` is used for main headings, and other levels are used for subheadings.
  
  ```html
  <h1>This is a Main Heading</h1>
  <h2>This is a Subheading</h2>
  <h3>This is a Smaller Subheading</h3>
  ```

- **Paragraphs**: Use the `<p>` tag for paragraphs. Paragraphs are block elements, so they automatically add space above and below.

  ```html
  <p>This is a paragraph in HTML. It’s used to write blocks of text.</p>
  ```

#### 2. Text Formatting Tags

HTML offers various tags to style and emphasize text. Here are some of the most commonly used ones:

- **Bold text**: `<strong>` or `<b>`
  
  ```html
  <p>This is <strong>important</strong> text.</p>
  ```

- **Italic text**: `<em>` or `<i>`
  
  ```html
  <p>This text is <em>emphasized</em>.</p>
  ```

- **Small text**: `<small>`
  
  ```html
  <p>This text is in <small>smaller size</small>.</p>
  ```

- **Line Breaks**: `<br>` creates a single line break. It’s a self-closing tag, meaning it doesn’t need a closing `</br>`.

  ```html
  <p>This is a line.<br>This is a new line.</p>
  ```

#### 3. Example: Creating a Structured HTML Document

Here’s an example combining these tags:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>HTML Basics</title>
  </head>
  <body>
    <h1>Introduction to HTML</h1>
    <p>HTML is the language for creating webpages. It's easy to learn and essential for web development.</p>

    <h2>Why Learn HTML?</h2>
    <p>HTML is <strong>fundamental</strong> to building websites. It structures text, images, and multimedia content.</p>

    <h2>Basic Text Formatting</h2>
    <p>Here’s some <em>emphasized text</em> and <small>small text</small>.</p>

    <p>This is the end of the document.<br>Thank you for reading!</p>
  </body>
</html>
```

#### 4. Practice Task

1. Create a new HTML file and include at least:
   - One `<h1>` and one `<h2>` heading.
   - A few paragraphs with **bold** and *italic* text.
2. Add line breaks using `<br>` in one of the paragraphs.

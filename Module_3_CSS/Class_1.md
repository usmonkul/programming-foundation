## Module 3: CSS - Styling the Web

CSS (Cascading Style Sheets) is what makes web pages look good! It lets you control things like colors, fonts, layout, and responsiveness.  Let's dive in and learn how to style your HTML with CSS.

### Linking CSS to HTML

Before you can start styling, you need to connect your CSS code to your HTML document. There are three main ways to do this:

**1. External Stylesheet (Recommended)**

This is the best way for larger projects. You create a separate `.css` file and link it to your HTML using the `<link>` tag in the `<head>` section.

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Styled Page</title>
  <link rel="stylesheet" href="style.css"> 
</head>
<body>
  </body>
</html>
```

* `rel="stylesheet"` tells the browser this is a CSS file.
* `href="style.css"` specifies the path to your CSS file.

**2. Internal Stylesheet**

You can write CSS directly in your HTML within `<style>` tags in the `<head>`.

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Styled Page</title>
  <style>
    /* CSS code goes here */
  </style>
</head>
<body>
  </body>
</html>
```

**3. Inline Styles**

You can add CSS directly to an HTML element using the `style` attribute.

```html
<p style="color: blue; font-size: 18px;">This is a blue paragraph.</p>
```

While this works, it's not ideal for larger projects because it mixes your HTML and CSS.

### CSS Syntax

CSS rules have a simple structure:

```css
selector {
  property: value;
  property: value; 
}
```

* **Selector:**  Targets the HTML element(s) you want to style (e.g., `p`, `h1`, `div`).
* **Property:**  The style attribute you want to change (e.g., `color`, `font-size`).
* **Value:** The specific setting for the property (e.g., `blue`, `16px`).

### Selectors

Selectors are how you tell CSS which elements to style. Here are some common types:

* **Element Selector:** Targets all elements of a specific type.

   ```css
   p { 
     color: red; 
   } 
   ```

* **ID Selector:** Targets a specific element with a unique `id` attribute.

   ```css
   #my-paragraph { 
     font-weight: bold; 
   }
   ```

* **Class Selector:** Targets all elements with a specific `class` attribute.

   ```css
   .highlight { 
     background-color: yellow; 
   }
   ```

### Styling Text

* **`color`:** Sets the text color.

   ```css
   p {
     color: blue; /* You can use color names or hex codes like #0000FF */
   }
   ```

* **`font-family`:** Sets the font.

   ```css
   h1 {
     font-family: Arial, sans-serif; 
   }
   ```

* **`font-size`:** Sets the font size.

   ```css
   p {
     font-size: 16px; /* You can use pixels (px), ems (em), or percentages (%) */
   }
   ```

* **`font-weight`:** Sets the font weight (boldness).

   ```css
   strong {
     font-weight: bold; 
   }
   ```

* **`text-align`:** Aligns text (left, center, right).

   ```css
   h2 {
     text-align: center;
   }
   ```

### Colors and Backgrounds

* **`color`:**  As mentioned above, styles text color.
* **`background-color`:**  Sets the background color of an element.

   ```css
   body {
     background-color: #f0f0f0; 
   }
   ```

* **`background-image`:**  Adds a background image.

   ```css
   div {
     background-image: url("image.jpg"); 
   }
   ```

### Important Considerations

* **Comments:** Use comments (`/* comment here */`) to explain your CSS code.
* **Specificity:** When multiple CSS rules target the same element, the more specific rule wins.
* **Inheritance:** Some CSS properties are inherited by child elements from their parents.
* **The Box Model:**  Understand how padding, borders, and margins affect the size and spacing of elements.
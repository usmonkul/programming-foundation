## Module 3: CSS - Styling the Web (Continued)

This tutorial builds on the CSS basics from the previous lesson. We'll explore more advanced styling concepts to give you greater control over the layout and appearance of your web pages.

### The CSS Box Model

Every HTML element is treated as a rectangular box with the following components:

* **Content:**  The actual content of the element (text, images, etc.).
* **Padding:**  The space between the content and the border.
* **Border:**  A line that surrounds the padding and content.
* **Margin:**  The space outside the border.

```css
div {
  width: 200px;
  padding: 20px;   /* 20px padding on all sides */
  border: 2px solid black; 
  margin: 30px;   /* 30px margin on all sides */
}
```

You can control each side of the box individually:

```css
div {
  margin-top: 10px;
  padding-left: 15px;
  border-bottom: 1px dashed red;
}
```

Understanding the box model is crucial for controlling the spacing and layout of your elements.

### Positioning

CSS provides several ways to position elements on a page:

* **Static (default):** Elements flow normally in the document.
* **Relative:**  Positioned relative to its normal position.

   ```css
   .box {
     position: relative;
     top: 20px;  /* Moves the box 20px down from its normal position */
     left: 10px; /* Moves the box 10px to the right */
   }
   ```

* **Absolute:** Positioned relative to its nearest positioned ancestor (or the document if none).

   ```css
   .container {
     position: relative; /* Makes this a positioned ancestor */
   }

   .box {
     position: absolute;
     top: 50px; 
     right: 20px;
   }
   ```

* **Fixed:** Positioned relative to the browser window. Stays in place even when scrolling.

   ```css
   .navbar {
     position: fixed;
     top: 0;
     width: 100%; 
   }
   ```

### Adding Fonts

You can use custom fonts from services like Google Fonts:

1. **Choose your font:**  Go to Google Fonts (fonts.google.com) and select the fonts you want.
2. **Get the link:** Google Fonts provides a `<link>` tag to include in your HTML `<head>`.
3. **Use the font in your CSS:**

   ```html
   <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">  
   ```

   ```css
   body {
     font-family: 'Roboto', sans-serif;
   }
   ```


**1. Obtain the Font Files**

* **Find the font:** You'll need the font files in formats like `.woff`, `.woff2`, `.ttf`, and/or `.otf`. These are typically included when you download a font from a source like Google Fonts (even if you're not using their hosting) or purchase a font from a foundry.
* **Organize your files:** Create a `fonts` folder within your website's directory to store your font files. This keeps things organized.

**2. Use the `@font-face` Rule**

The `@font-face` rule in CSS allows you to define a custom font and specify where the browser can find the font files.

```css
/* my-font.css */
@font-face {
  font-family: 'MyCoolFont'; /* Give your font a name */
  src: url('fonts/MyCoolFont.woff2') format('woff2'),
       url('fonts/MyCoolFont.woff') format('woff'),
       url('fonts/MyCoolFont.ttf') format('ttf'); 
  font-weight: normal; /*  Optional: Specify weights (normal, bold, etc.) */
  font-style: normal;  /* Optional: Specify styles (normal, italic) */
}
```

* **`font-family`:**  This defines the name you'll use to refer to the font in your CSS.
* **`src`:** This tells the browser where to find the font files.
    * `url()`:  Specifies the path to the font file.
    * `format()`:  Indicates the font file format. Include multiple formats for better browser compatibility.

**3. Apply the Font**

Now you can use the font like any other in your CSS:

```css
body {
  font-family: 'MyCoolFont', sans-serif; 
}

h1 {
  font-family: 'MyCoolFont', cursive;
}
```

**Important Considerations:**

* **File Paths:**  Make sure the paths to your font files in the `src` property are correct relative to your CSS file.
* **Browser Compatibility:**  Include multiple font formats (`.woff2`, `.woff`, `.ttf`) for broader browser support.
* **Licensing:**  Ensure you have the proper licenses to use the fonts you're embedding.
* **Performance:**  Loading many large font files can impact page load speed. Optimize your font files (e.g., using tools like FontForge or online font optimizers) and consider only loading the weights and styles you need.

**Example with Google Fonts (Downloaded):**

1. **Download:** Download the font family you want from Google Fonts.
2. **Extract:** Extract the downloaded ZIP file into your `fonts` folder.
3. **`@font-face`:**

   ```css
   @font-face {
     font-family: 'Roboto';
     src: url('fonts/Roboto-Regular.ttf') format('truetype'); 
     font-weight: normal;
   }

   @font-face {
     font-family: 'Roboto';
     src: url('fonts/Roboto-Bold.ttf') format('truetype');
     font-weight: bold;
   }
   ```

4. **Use it:**

   ```css
   h1 {
     font-family: 'Roboto', sans-serif;
     font-weight: bold;
   }
   ```

By following these steps, you can add unique and personalized fonts to your website, giving it a distinct style and enhancing its visual appeal.


### CSS Units

* **px (pixels):** Fixed units, good for precise control but not always responsive.
* **% (percentage):** Relative to the parent element. Useful for responsive layouts.
* **em:** Relative to the font size of the *parent* element.
* **rem:** Relative to the font size of the *root* element (usually the `<html>` element). Great for consistent sizing and accessibility.

```css
p {
  font-size: 16px;   /* Fixed size in pixels */
  line-height: 1.5em; /* Line height is 1.5 times the parent's font size */
  width: 50%;      /* Width is 50% of the parent's width */
  margin-bottom: 2rem; /* Margin is 2 times the root font size */
}
```

**Other Units:**

* **vw (viewport width):** Percentage of the viewport width.
* **vh (viewport height):** Percentage of the viewport height.

### Important Notes

* **Experiment:**  The best way to learn CSS is to experiment! Try different properties and values to see how they affect your web page.
* **Developer Tools:**  Use your browser's developer tools (right-click and "Inspect") to examine CSS, make live changes, and troubleshoot issues.
* **Keep Learning:**  CSS is a vast and powerful language. Continue exploring resources and tutorials to expand your skills.

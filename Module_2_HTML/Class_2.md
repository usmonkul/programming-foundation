### **Lists and Links**

**Objective:** Learn how to create different types of lists and add links to other pages or resources.

#### 1. Creating Lists

HTML allows us to create both ordered and unordered lists. Lists are useful for organizing items like navigation menus, instructions, or bullet points.

- **Ordered List**: An ordered list (`<ol>`) is a numbered list, with each item marked in sequence.

  ```html
  <h2>Ordered List Example</h2>
  <ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
  </ol>
  ```

- **Unordered List**: An unordered list (`<ul>`) is a bulleted list. It doesn’t follow a sequence.

  ```html
  <h2>Unordered List Example</h2>
  <ul>
    <li>Item one</li>
    <li>Item two</li>
    <li>Item three</li>
  </ul>
  ```

- **Nested Lists**: You can nest lists within lists by placing one list inside another `<li>` item.

  ```html
  <h2>Nested List Example</h2>
  <ul>
    <li>Main item
      <ul>
        <li>Sub-item one</li>
        <li>Sub-item two</li>
      </ul>
    </li>
    <li>Main item two</li>
  </ul>
  ```

#### 2. Adding Links

Links are created using the `<a>` tag. They allow you to navigate to other web pages or files.

- **Basic Link**: To link to another webpage, use the `<a>` tag with the `href` attribute. The `href` (hypertext reference) is the URL of the page you’re linking to.

  ```html
  <p>Visit the <a href="https://www.example.com">Example website</a> for more information.</p>
  ```

- **Open Link in a New Tab**: You can make a link open in a new tab by adding `target="_blank"` to the `<a>` tag.

  ```html
  <p>Visit the <a href="https://www.example.com" target="_blank">Example website</a> in a new tab.</p>
  ```

- **Linking to an Email Address**: You can create a mail link with `mailto:`. When clicked, it opens the user’s default email app.

  ```html
  <p>Email us at <a href="mailto:info@example.com">info@example.com</a></p>
  ```

#### 3. Example: Combining Lists and Links

Here’s an example that combines what we’ve learned about lists and links:

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Lists and Links</title>
</head>
<body>
  <h1>My Favorite Websites</h1>
  <p>Here are some websites I visit frequently:</p>
  
  <ul>
    <li><a href="https://www.example.com" target="_blank">Example</a></li>
    <li><a href="https://www.wikipedia.org">Wikipedia</a></li>
    <li><a href="https://www.github.com">GitHub</a></li>
  </ul>
</body>
</html>
```

#### 4. Practice Task

1. Create an ordered list of three of your favorite books or movies.
2. Create an unordered list of three websites you frequently visit, and add links to each one using the `<a>` tag.

---

### **Images and Media**

**Objective:** Learn to insert and configure images, as well as explore the basics of adding multimedia.

#### 1. Adding Images

To add an image, use the `<img>` tag. This tag has important attributes like `src` (source) and `alt` (alternative text).

- **Basic Image Tag**: The `src` attribute points to the image file, and `alt` describes the image for accessibility (e.g., screen readers).

  ```html
  <img src="image.jpg" alt="A description of the image">
  ```

- **Image Attributes**: You can add width and height to specify the image size.

  ```html
  <img src="image.jpg" alt="A description of the image" width="200" height="100">
  ```

- **Image from URL**: You can link to an image on another website by using the full URL in `src`.

  ```html
  <img src="https://www.example.com/image.jpg" alt="An example image">
  ```

#### 2. Linking Images

You can make an image clickable by wrapping it inside an `<a>` tag.

```html
<a href="https://www.example.com">
  <img src="image.jpg" alt="Clickable image" width="150">
</a>
```

#### 3. Using Multimedia

HTML5 makes it easy to add audio and video to a webpage.

- **Adding Audio**: Use the `<audio>` tag with the `controls` attribute to add a play/pause option.

  ```html
  <audio controls>
    <source src="audio-file.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>
  ```

- **Adding Video**: Use the `<video>` tag, and similar to audio, add the `controls` attribute for play/pause functionality.

  ```html
  <video width="320" height="240" controls>
    <source src="video-file.mp4" type="video/mp4">
    Your browser does not support the video element.
  </video>
  ```

#### 4. Example: Adding Images and Multimedia

Here’s an example that combines images, audio, and video on a single page.

```html
<!DOCTYPE html>
<html>
<head>
  <title>Images and Multimedia</title>
</head>
<body>
  <h1>Welcome to My Media Page</h1>
  
  <h2>My Favorite Image</h2>
  <img src="image.jpg" alt="A beautiful landscape" width="300">
  
  <h2>Listen to My Favorite Song</h2>
  <audio controls>
    <source src="song.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>
  
  <h2>Watch a Cool Video</h2>
  <video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    Your browser does not support the video element.
  </video>
</body>
</html>
```

#### 5. Practice Task

1. Add an image to your webpage. Use the `alt`, `width`, and `height` attributes to control its appearance.
2. Add an audio file using the `<audio>` tag and a video file using the `<video>` tag. Make sure both elements have `controls` so you can play/pause them.

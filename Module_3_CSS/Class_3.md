## Module 3: CSS - Styling the Web (Continued)

### Flexbox: A Deep Dive

Flexbox is a one-dimensional layout model that provides a flexible and efficient way to arrange items within a container.

**Basic Setup**

Remember, you need a flex container and flex items to use Flexbox:

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```

```css
.container {
  display: flex; /* Activate flexbox for the container */
}
```

### Flex Container Properties

These properties apply to the parent element (flex container):

* **`display: flex;`:**  Makes the element a flex container.
* **`flex-direction`:** Sets the main axis (direction of items).

   ```css
   .container {
     flex-direction: row;    /* Default: horizontal */
     flex-direction: column;  /* Vertical */
     flex-direction: row-reverse; /* Reverse horizontal */
     flex-direction: column-reverse; /* Reverse vertical */
   }
   ```

* **`justify-content`:** Aligns items along the main axis.

   ```css
   .container {
     justify-content: flex-start;  /* Align to start */
     justify-content: flex-end;    /* Align to end */
     justify-content: center;      /* Center items */
     justify-content: space-between; /* Space between items */
     justify-content: space-around;  /* Space around items */
     justify-content: space-evenly; /* Even space between and around */
   }
   ```

* **`align-items`:** Aligns items along the cross axis (perpendicular to the main axis).

   ```css
   .container {
     align-items: flex-start; /* Align to start of cross axis */
     align-items: flex-end;   /* Align to end of cross axis */
     align-items: center;     /* Center on cross axis */
     align-items: stretch;   /* Stretch to fill container (default) */
     align-items: baseline;  /* Align items to their baselines */
   }
   ```

* **`flex-wrap`:**  Controls whether items wrap onto multiple lines.

   ```css
   .container {
     flex-wrap: nowrap; /* Default: single line */
     flex-wrap: wrap;   /* Wrap onto multiple lines */
     flex-wrap: wrap-reverse; /* Wrap in reverse order */
   }
   ```

* **`align-content`:**  Aligns multiple lines of flex items along the cross axis (only works with `flex-wrap: wrap`).

   ```css
   .container {
     align-content: flex-start; /* Align lines to start */
     align-content: flex-end;   /* Align lines to end */
     align-content: center;     /* Center lines */
     align-content: space-between; /* Space between lines */
     align-content: space-around;  /* Space around lines */
     align-content: stretch;   /* Stretch lines to fill container */
   }
   ```

* **`gap`:**  Sets the gap between flex items.

   ```css
   .container {
     gap: 10px;     /* 10px gap between all items */
     gap: 10px 20px; /* 10px gap between rows, 20px between columns */
     row-gap: 15px;  /* Gap between rows */
     column-gap: 25px; /* Gap between columns */
   }
   ```


### Flex Item Properties

These properties apply to the child elements (flex items):

* **`order`:**  Changes the order of items.

   ```css
   .item-1 { order: 2; } /* This item will appear second */
   .item-2 { order: 1; } /* This item will appear first */
   ```

* **`flex-grow`:**  Controls how much an item grows to fill available space.

   ```css
   .item-1 { flex-grow: 2; } /* Grows twice as much as others */
   ```

* **`flex-shrink`:** Controls how much an item shrinks when space is limited.

   ```css
   .item-2 { flex-shrink: 0; } /* Prevents shrinking */
   ```

* **`flex-basis`:** Sets the initial size of an item before free space is distributed.

   ```css
   .item-3 { flex-basis: 200px; } /* Initial width of 200px */
   ```

* **`flex`:** Shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.

   ```css
   .item { flex: 1 0 200px; } /* Equivalent to flex-grow: 1; flex-shrink: 0; flex-basis: 200px; */
   ```

* **`align-self`:** Overrides the container's `align-items` for an individual item.

   ```css
   .item-3 { align-self: flex-end; } /* Aligns this item to the end of the cross axis */
   ```


**Important Notes**

* **Browser Support:** Flexbox is well-supported in modern browsers.
* **Practice:** The best way to learn Flexbox is through hands-on practice. Experiment with different properties to see how they work.
* **Developer Tools:** Use your browser's developer tools to inspect flex containers and items, and to experiment with Flexbox properties in real-time.

With this comprehensive guide, you're well-equipped to create dynamic and responsive layouts using the power of Flexbox!

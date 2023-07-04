# CSS Tutorial

CSS (Cascading Style Sheets) is a language used to describe how HTML elements will be styled.

## CSS Syntax

A CSS rule-set consists of a selector and a declaration block:

    selector {
      property: value;
    }

- `selector`: This targets the HTML element that you want to style.
- `property`: The attribute of the HTML element you want to change.
- `value`: The new style you want to apply to the property.

Example:

    h1 {
      color: blue;
    }

This will apply a blue color to all `<h1>` headings.

## How to Add CSS

There are three ways of inserting a style sheet:

### Inline CSS

Inline CSS is used to style a specific HTML element. The style is added directly to the start tag of the element using the `style` attribute.

Example:

    `<h1 style="color:blue;">`This is a Blue Heading`</h1>`

### Internal CSS

Internal CSS is used to define a style for a single HTML page. The style is added within the `<style>` element inside the `<head>` section.

Example:

    `<head>`
    `<style>`
    body {background-color: powderblue;}
    h1   {color: blue;}
    p    {color: red;}
    `</style>`
    `</head>`

### External CSS

External CSS is used when the style is defined in a separate file. This file should be saved with a .css extension. The .css file should be linked in the HTML file using the `<link>` element.

Example:

In your HTML file:

    `<head>`
    `<link rel="stylesheet" href="styles.css">`
    `</head>`

And in "styles.css":

    body {background-color: powderblue;}
    h1   {color: blue;}
    p    {color: red;}


## CSS Selectors

Selectors are the part of CSS ruleset. CSS selectors select HTML elements according to its id, class, type, attribute etc.

There are several different types of selectors in CSS:

- **Element Selector**: The element selector selects the HTML element by name.

  ```
  p {
    text-align: center;
    color: red;
  }
  ```
- **ID Selector**: The id selector uses the id attribute of an HTML element to select a specific element. The id of an element should be unique within a page, so the id selector is used to select one unique element.

  ```
  #myID {
    text-align: center;
    color: red;
  }
  ```
- **Class Selector**: The class selector selects HTML elements with a specific class attribute. It is possible for multiple elements to share the same class.

  ```
  .myClass {
    text-align: center;
    color: red;
  }
  ```

## CSS Box Model

All HTML elements can be considered as boxes. The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.

- **Content**: The content of the box, where text and images appear.
- **Padding**: A transparent area around the content (inside the box), padding is affected by background color of the box.
- **Border**: A border that goes around the padding and content.
- **Margin**: A transparent area around the border.

## CSS Colors

CSS supports a wide variety of colors. These include predefined color names (like `red`, `blue`, `green`), HEX values, RGB, RGBA, HSL, and HSLA values.

    p {
      color: red;  /* color name*/
      color: #ff0000;  /* HEX color */
      color: rgb(255, 0, 0);  /* RGB color */
      color: rgba(255, 0, 0, 0.3);  /* RGBA color */
      color: hsl(0, 100%, 50%);  /* HSL color */
      color: hsla(0, 100%, 50%, 0.3);  /* HSLA color */
    }

## CSS Units

CSS has several different units for expressing length. Some of the units are:

- `px` - pixels (a dot on the computer screen)
- `%` - percent
- `em` - the current font size
- `rem` - the font size of the root element
- `vw` / `vh` - percent of viewport's width / height
- `cm`, `mm`, `in`, `pt`, `pc` - absolute length units

## CSS Positioning

The position property specifies the type of positioning method used for an element:

- `static`: HTML elements are positioned static by default.
- `relative`: The element is positioned relative to its normal position.
- `fixed`: The element is positioned relative to the browser window.
- `absolute`: The element is positioned absolutely to its first positioned parent.
- `sticky`: The element is positioned based on the user's scroll position.

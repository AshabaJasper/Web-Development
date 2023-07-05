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

  Continued:

  ## The Box Model

  In CSS, each element is viewed as a rectangular box. This is often referred to as the "Box Model", and it consists of: margins, borders, padding, and the actual content.


  - **Content**: This is the actual content of the box, where text and images appear.
  - **Padding**: Clears an area around the content. The padding is transparent.
  - **Border**: A border that goes around the padding and content.
  - **Margin**: Clears an area outside the border. The margin is transparent.

    div {
    width: 300px;
    border: 25px solid green;
    padding: 25px;
    margin: 25px;
    }

  ## Margin and Padding

  - **Margin** is used to create space around elements, outside of any defined borders. It's specified with the `margin` property, and it can have one, two, three, or four values.

    div {
    margin: 10px; /* All sides */
    /* OR */
    margin: 10px 20px; /* Top & Bottom | Right & Left */
    /* OR */
    margin: 10px 20px 30px; /* Top | Right & Left | Bottom */
    /* OR */
    margin: 10px 20px 30px 40px; /* Top | Right | Bottom | Left */
    }
  - **Padding** works very similar to margin, but it's used to create space within the element.

    div {
    padding: 10px; /* All sides */
    /* OR */
    padding: 10px 20px; /* Top & Bottom | Right & Left */
    /* OR */
    padding: 10px 20px 30px; /* Top | Right & Left | Bottom */
    /* OR */
    padding: 10px 20px 30px 40px; /* Top | Right | Bottom | Left */
    }

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

## CSS Backgrounds

CSS allows you to set the background color and image of an element.

- **Background Color**: Use the `background-color` property to specify the background color of an element.

  ```css
  body {
    background-color: lightblue;
  }
  ```
- **Background Image**: Use the `background-image` property to specify a background image for an element.

  ```css
  body {
    background-image: url("image.jpg");
  }
  ```

## CSS Text and Fonts

CSS properties allow you to change the style and layout of text.

- **Font Family**: The `font-family` property specifies the font for an element.

  ```css
  p {
    font-family: "Times New Roman", Times, serif;
  }
  ```
- **Font Size**: The `font-size` property sets the size of the text.

  ```css
  p {
    font-size: 16px;
  }
  ```
- **Text Color**: The `color` property specifies the color of the text.

  ```css
  p {
    color: red;
  }
  ```
- **Text Alignment**: The `text-align` property is used to set the horizontal alignment of a text.

  ```css
  p {
    text-align: center;
  }
  ```

## CSS Pseudo-classes

A pseudo-class is used to define a special state of an element. For example, it can be used to:

- Style an element when a user mouses over it
- Style visited and unvisited links differently
- Style an element when it gets focus

  ```css
  a:hover {
    color: orange;
  }
  ```

## CSS Pseudo-elements

A pseudo-element is used to style specified parts of an element. For example, it can be used to:

- Style the first letter, or line, of an element
- Insert content before, or after, the content of an element

  ```css
  p::first-letter {
    font-size: 200%;
    color: blue;
  }
  ```

## CSS Transitions

CSS transitions allows you to change property values smoothly, over a given duration. For example:

    ```css
    div {
      width: 100px;
      transition: width 2s;
    }

    div:hover {
      width: 200px;
    }
    ```

This is still not all of CSS. There's still a lot more to learn about CSS, such as animations, flexbox, grid, etc. Continue exploring!


## CSS Flexbox

Flexbox is a one-dimensional layout method for laying out items in rows or columns. Items flex to fill additional space and shrink to fit into smaller spaces.

    .container {
      display: flex;
    }

    .item {
      flex: 1;  /* Grow and shrink to fill space */
    }

## CSS Grid

CSS Grid Layout is a two-dimensional layout system, with rows and columns. It's perfect for designing interfaces.

    .container {
      display: grid;
      grid-template-columns: auto auto auto;  /* Three equal columns */
    }

## CSS Transforms

The transform property applies a 2D or 3D transformation to an element. This property allows you to rotate, scale, move, skew, etc., elements.

    img {
      transform: rotate(20deg);
    }

## CSS Transitions

Transitions enable you to define the transition between two states of an element. Different states may be defined using pseudo-classes like :hover or :active, or dynamically set using JavaScript.

    div {
      transition: all 2s;
    }

## CSS Animations

Animations are made up of two components, a style describing the CSS animation and a set of keyframes that indicate the start and end states of the animation’s style, as well as possible intermediate waypoints along the way.

    @keyframes my-animation {
      from {background-color: red;}
      to {background-color: yellow;}
    }

    div {
      animation-name: my-animation;
      animation-duration: 5s;
    }


## Responsive Design and Media Queries

Responsive design is an approach where your design adapts to different screen sizes. One major aspect of it is "media queries", which allow you to apply different styles for different media types/devices.

    @media screen and (max-width: 600px) {
      body {
        background-color: lightblue;
      }
    }

## SASS/SCSS

SASS (Syntactically Awesome Style Sheets) and its superset SCSS (Sassy CSS) are CSS pre-processors. They let you use features that don't exist in CSS yet like variables, nesting, mixins, inheritance, and more.

    $primary-color: blue;

    body {
      color: $primary-color;
    }

## CSS Variables (Custom Properties)

CSS Variables, also known as custom properties, allow you to store a value in one place, then reuse it elsewhere in your CSS.

    :root {
      --primary-color: blue;
    }

    body {
      color: var(--primary-color);
    }

## Pseudo-elements (::before and ::after)

Pseudo-elements are used to style certain parts of a document. For example, you can use the ::before and ::after pseudo-elements to insert content onto a page.

    p::before {
      content: "Read this -";
    }

## Advanced CSS Selectors

Advanced CSS selectors like attribute selectors, :nth-child, :nth-of-type, etc., allow for more precise selection of elements to style.

    /* Attribute selector */
    input[type="text"] {
      width: 200px;
    }

    /* nth-of-type selector */
    p:nth-of-type(2) {
      color: blue;
    }

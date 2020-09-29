# Basic CSS Notes

## Changing the Color of Text
Each individual element has a style attribute that you can modify to change the color of text.
Use the color property within the style attribute in order to do this.

For example, changing the color of an h2 element:
```html
<h2 style="color: blue;"> Your text here </h2>
```

It is good practice to end inline style declarations with a semi color (;).

## Use CSS Selectors to Style Elements
There is a more efficient way of changing the color of elements (and much more) using selectors.
Selectors target specific element types and change the color for all elements of that type which allows you to change the color of multiple text tags without doing it individually.

We do this by creating a style block and creating selectors for specific elements within it.

```html
<style>
    p {
        color: red;
    }
</style>
```

In the above example, we are making all text within paragraph tags have the color red.

## Use a CSS Class to Style Elements
Classes are styles you can use for several different tags. Rather than targeting all paragraph tags for example, you can choose which paragraph tags take on that style.

```html
<style>
    .blue-text {
        color: blue;
    }
</style>
```

Now we can apply this to any element we want:

```html
<h2 class="blue-text"> Your text here </h2>
<p> Your paragraph text here </p>
```

Notice how the blue-text class was given to the header tag but not the paragraph tag. If we wanted the paragraph tag to have the same style then we can do so by giving it the blue-text class.

## Change the Font Size of an Element
Font size is another property we can change using CSS selectors. To do this, simply add the ``font-size`` property to the chosen selector and give a new font size in px measurement.

```html
<style>
    .blue-text {
        color: blue;
        font-size: 30px;
    }
</style>
```

## Set the Font Family of an Element
This is another property we can change using CSS selectors. It is used in the same way as the color and font size properties.

```html
<style>
    .blue-text {
        color: blue;
        font-size: 30px;
        font-family: sans-serif;
    }
</style>
```

Now every element with the blue-text class will be blue, have a font size of 30 px, and the font style of sans-serif.

## Import a Google Font
Sometimes we want to use different fonts for our website. We can do this by importing the font into our html document.
Google has a free library of web fonts [Google Fonts](https://fonts.google.com).
To import a google font, copy the fonts URL from the library and paste it into your HTML at the top of the page using a link tag.

For example, we will import the Lobster Font.
```html
<!--
Importing the lobster font.
-->
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">

<main>
    <h1>Website Title</h1>
    <p>Some example text</p>
</main>
```

We can use element selectors in order to actually apply the font to the element we wish:

```html
<style>
    h2 {
        font-family: Lobster;
    }
</style>
```

Now all h2 elements will use the Lobster font.

## Specify How Fonts Should Degrade
Sometimes browsers will not have the font style you want your html to use so we pick how the fonts should degrade.
This means that if your first choice of font isn't available, then the CSS will use your second choice of font style.

Degrading goes like this:

```html
<style>
    h2 {
        font-family: Lobster, monospace;
    }
</style>
```

Now if the Lobster font is unavailable, the monospace font will be used.

## Size Your Images
Selectors have the ``width`` property that allows us to adjust the width of images using the px (pixel) measurement.
To do this, make a style sheet as normal and for the image you want to adjust, create a new class with the property of width and a value assigned to it.

```html
<style>
    .larger-image {
        width: 500px;
    }
</style>
```

## Add Borders Around Your Elements
We can also adjust the borders of images using border classes and their properties. Such properties include border-color, border-width, and border-styles.

```html
<style>
    .thin-red-border {
        border-color: red;
        border-width: 5px;
        border-style: solid;
    }
</style>
```

Now if were to apply this to an element, it would take on these properties.

## Add Rounded Corners
Borders also have the border-radius property which we can change.

```html
<style>
    .thin-red-border {
        border-color: red;
        border-width: 5px;
        border-style: solid;
        border-radius: 3px;
    }
</style>
```

We can also use percentages when changing the border-radius property:

```html
<style>
    .thin-red-border {
        border-color: red;
        border-width: 5px;
        border-style: solid;
        border-radius: 50%;
    }
</style>
```

## Give Background Color
This is another property of style sheets which you can add. An example would be:

```html
<style>
    .green-background {
        background-color: green;
        }
</style>
```

## Set the ID of an Element
HTML elements can have ids which you can use as selectors for styling. It is convention to have every id attribute be unique (don't give more than one element the same id).
Here is an example of giving an id to an element:

```html
<h2 id="unique-identifier">Hello World</h2>
```

## Using ID Attributes to Style an Element
Now that we have given an id to an element, we can make changes to the style that element takes on within our style sheet:

```html
<style>
    #one {
        background-color: green;
        color: blue
    }
</style>

<h2 id='one'>Hello World</h2>
```

The h2 element will have a green background color and its font will be blue.
You should note that ids have higher precedence than classes.

## Adjust the Padding of an Element
There are three important properties that control the space around each element: Padding, Border, and Margin

**Padding:**
Controls the amount of space between the elements content and its border. Increasing the padding means creating more space between the content and border. 
You can adjust any of the following: padding (constant for all sides), padding-right, padding-left, padding-top, padding-bottom.

```html
<style>
    .blue-box {
        padding: 10px;
    }
</style>
```

## Adjust the Margin of an Element
An elements margins control the amount of space between its border and surrounding elements. You can adjust any of the following: margin (constant for all sides), margin-bottom, margin-top, margin-right, margin-left.

```html
<style>
    .blue-box {
        padding: 10px;
        margin: 3px;
    }
</style>
```

This example only shows constant margins but you can change any of the previously listed margins.
If you set an elements margin to a negative value, the element will grow larger.

## Use Clockwise Notation to Specify the Padding or Margin of an Element
This is a faster way of adjusting specific margins (bottom/top, right/left). Using clockwise notation allows you to declare these all in one line like:

```html
<style>
    .blue-box {
        padding: <padding-top-size> <padding-right-size> <padding-bottom-size> <padding-left-size>;
        margin: <margin-top-size> <margin-right-size> <margin-bottom-size> <margin-left-size>;
    }
</style>
```

You would have to specify the sizes obviously.

## Use Attribute Selectors to Style Elements
Previously we have been adding ``class`` and ``id`` attributes to elements we want to specifically style. These are class and id selectors. There are also other types of selectors we can use to style elements. 
``[attr=value]`` selectors can be given a specific attribute and its corresponding value to be used in style sheets.

For example, if we wanted to style all elements with the type attribute with the value of radio, we would do so as follows:

```html
<style>
    [type="radio"] {
        margin: 20px, 30px, 40px, 50px;
    }
</style>
```

Similarly we can do this for all elements of type 'checkbox' etc.

## Understand Absolute vs Relative Units
We have primarily been using px units as a form of measurement for a lot of our css properties. There are other length units as well.

The two main types of units are absolute and relative units. 

Absolute: Physical units of length; in (inches), mm (millimeters)
Relative: Units (em or rem) which are relative to another length value. Example: em is based on the size of an elements font. Setting the font-size property using em, it is relative to the parent font-size

```html
<style>
    [type="radio"] {
        margin: 1.5em;
    }
</style>
```

## Style the HTML Body Element
Every HTML page has a ``body`` element which we can make a style sheet for as any other element:

```html
<style>
    body {
        background-color: black;
    }
</style>
```

Now the entire page will be black (dark mode!)

## Inherit Styles from the Body Element
You can style your body element just like all other elements but the difference here is that other elements will inherit the style of the body element.

For example: If we had a body background-color of black and a color of white, then the text within the body element will be white.

```html
<style>
    body {
        background-color: black;
        color: white;
    }
</style>

<body>
    <h1> Hello World </h1>
</body>
```

Now the background of the page will be black and the color of the h1 text will be white.

## Prioritize One Style Over the Other
Sometimes elements will receive multiple styles. You will need to be able to prioritize which style the elements take on.

Here is the order of precendence for styles (most important to least):
1. inline style rules
2. embedded styles
3. external style sheet rules
4. browser default rules

If we have something like this: 

```html
<style>
    body {
        background-color: black;
        font-family: monospace;
        color: green;
    }
  
  .pink-text {
        color: pink;
    }
</style>

<h1 class='pink-text'>Hello World!</h1>
```

The h1 element will have a pink font color.

## Override Styles in Subsuquent CSS
If an element has more than 1 class, the class that comes last in the style tag is the one that takes precendence. So if we had a blue-text style class written after the pink-text class, the blue-text will be the style that is followed:

```html
<style>
    body {
        background-color: black;
        font-family: monospace;
        color: green;
    }
  
    .pink-text {
        color: pink;
    }

    .blue-text {
        color: blue;
    }
</style>

<h1 class='pink-text blue-text'>Hello World!</h1>
```

The order in which the classes are within the HTML element does not matter i.e class='blue-text pink-text' would still produce blue colored h1 element.

## Override Class Declarations by Styling ID Attributes
If we were to style the same h1 element by using its tag, the style of the id style sheet will be used instead. For example:

```html
<style>
    body {
        background-color: black;
        font-family: monospace;
        color: green;
    }
  
    .pink-text {
        color: pink;
    }

    .blue-text {
        color: blue;
    }
    #hello-word {
        color: red;
    }
</style>

<h1 id='hello-word' class='pink-text blue-text'>Hello World!</h1>
```

Now this will make the h1 element have a red font color.

## Override Class Declarations with Inline Styles
Inline styles have precedence over all other styles:

```html
<style>
    body {
        background-color: black;
        font-family: monospace;
        color: green;
    }
  
    .pink-text {
        color: pink;
    }

    .blue-text {
        color: blue;
    }
    #hello-word {
        color: red;
    }
</style>

<h1 style="color: yellow;" id='hello-word' class='pink-text blue-text'>Hello World!</h1>
```

Now the h1 element will have a yellow font color.

## Use Hex Code for Specific Colors
Hexadecimals are base 16 numbers (16 distinct symbols). 
We have the digits 0-9 and the letters A-F.
Together you can use these to represent a number in hexadecimal form. 

In CSS we use 6 hexadecimal digits to represent colors, two each for red, green, and blue. 
For example: #000000 is black.

Some hex codes can be shortened to just 3 digits like red: #F00

## Use RGB Values to Color Elements
RGB values are given by rgb(x, y, z) where 0 <= x, y, z <= 255. When x = y = z = 0, you have black and when x = y = z = 255, you have white.

## Use CSS Variables to Change Several Elements at Once
Variables can be used to change multiple values at once but only actually changing one thing.

You declare variables using with the form ``--<variable-name>`` within style tags.
For Example:

```html
<style>
    .variable-storage {
        --fox-face-color: white;
        --fox-leg-color: red;
    }
</style>
```

To use these variables in other style classes you must use ``var(--<variable-name>)`` for the property which you wish to change. You can also add a fallback.

```html
<style>
    .variable-storage {
        --fox-face-color: white;
        --fox-leg-color: red;
    }

    .fox-face {
        color: var(--fox-face-color, blue)
    }
</style>
```

To make use of these variables we will often define them within :root style class. This makes them available yearly

```html
<style>
    :root {
        --fox-face-color: white;
        --fox-leg-color: red;
    }

    .fox-face {
        color: var(--fox-face-color, blue)
    }
</style>
```
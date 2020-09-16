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
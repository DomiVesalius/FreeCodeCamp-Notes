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
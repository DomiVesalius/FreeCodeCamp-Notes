# Applied Visual Design Notes

## Create a Visual Balance using the text-align Property
CSS can be used to align text in different places using the text-align property. We have four options:

1. text-align: justified -> causes all lines of text except the last one to meet the right and left edges of the line box
2. text-align: right -> right-aligns the text
3. text-align: left -> left-aligns the text (this is the default)
4. text-align: center -> centers the text

Here is an example. Say we have an h1 element with the class of page-title and we want to center it on the page:

```html
<style>
    .page-title {
        text-align: center;
    }
</style>

<h1 class='page-title'> Wikipedia </h1>
```

## Adjust the Height and Width of of an Element
Every element has the height and width property that can easily be changed in the style sheet.

```html
<style>
    img {
        height: 220px;
        width: 400px;
    }
</style>
```

This will give all image elements a height of 220px and a width of 400px.

## Use the strong tag to make text bold
To make text you can use the strong tag. Using the strong tag on individual elements is the same as applying ``font-weight: bold;`` to the element.

Example One:

```html
<h1> The following word will be bold: <strong> bruh </strong></h1>
```

Example Two:
```html
<style>
    #ronen {
        font-weight: bold;
    }
</style>

<h1 id='ronen'> This entire sentence will be bolded </h1>
```

## Use the u Tag to Underline Text
The u tag is used to underline text. Using the u tag is the same as applying ``text-decoration: underline;`` to the element.

Example One:

```html
<h1> The following word will be underlined: <u> bruh </u> </h1>
```

Example Two:

```html
<style>
    .over-load {
        text-decoration: underline;
    }
</style>

<h1 class='over-load'> This entire sentence will be underlined.</h1>
```

## Use the em Tag to Italicize Text
The em tag is used to emphasize/italicize text. This can also be done by applying ``font-style: italic;`` to the element.


```html
<style>
    .rover {
        font-style: italic;
    }
</style>

<h1> The following word will be italicized: <em> Zelda </em> </h1>

<h2 class='rover'> This entire sentence will be italicized</h2>
```

## Use the s Tag to Strikethrough Text
The s tag is used to put a line through the middle of text. This is the same as applying ``text-decoration: line-through;`` to the element.

```html
<style>
    .deleted {
        text-decoration: line-through;
    }
</style>

<h1> The following word will have a line through it: <s> Strikethrough text </s></h1>

<h2 class='deleted'> This entire sentence will have a line through it. </h2>
```

## Create a Horizontal Line Using the hr Element
The hr tag is used to add a horizontal line across the width of the element it is nested within. Note that it is a self closing tag:

```html
<h1> Google <hr> <h2>
```
This will make a horizontal line appear across the width of the h2 element.

## Adjust the background-color Property of Text
You are able to add a ``background-color`` property to the element holding the text you want to emphasize.
In order to use this you have to use rgba() rather than hex codes or normal rbg(). 

rgba(x, y, z, w) where x is red, y is green, z is blue, and w is the level of opacity. 0<= x, y, z <= 255 and 0 <= w <= 1.
w = 0 fully transparent and w = 1 is fully opaque.

```html
<style>
    h1 {
        background-color: rgba(45, 45, 45, 0.1);
    }
</style>

<h1> Google </h1>
```

## Adjust the Size of a Header Versus a Paragraph Tag
The font size of header tags should generally be larger than the font size of paragraph tags.
You use the ``font-size`` property to adjust the size of the text in an element.

Example:

```html
<style>
    h4 {
        font-size: 25px;
    }
</style>

<h4> I'm not creative enough to think of new sentences. This sentence will have a font size of 25 pixels. </h4>
```

## Add a box-shadow to a Card-like Element
``box-shadow`` property applied one or more shadows to an element. It takes a total of 5 values:
1. offset-x: how far to push the shadow horizontally from the element
2. offset-y: how far to push the shadow vertically from the element
3. blur-radius: what parts of the shadow are blurred
4. spread-radius: How far the shadow is spread
5. color: The color of the shadow

Note that the ``blur-radius`` and ``spread-radius`` values are optional.

Multiple box-shadows can be created by using commas to separate properties of each box-shadow element:

```html
<style>
    .thumbnail {
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0,0,0,0.23);
    }
</style>
```

## Adjust the Opacity of an Element
A value of 1 is opaque, 0 is fully transparent, 0.5 is half see-through.
It is applied to the entire element.

```html
<style>
    .links {
        opacity: 1;
    }
</style>
```

## Use the text-transform Property to Make Text Uppercase
This property is used to adjust the appearance of text. It's convenient to make sure text on webpages appear consistently without having to change the text content of the actual elements.
``text-transform`` can take the following values:
1. lowercase
2. uppercase
3. capitalize
4. initial (the original value)
5. inherit (use the text-transform value from the parent element)
6. none (use the original text)

## Font: size and weight
Text elements have the ``font-size`` and ``font-weight`` properties. Font size is obvious but ``font-weight`` controls how thick and thin characters are in a section of text.

## Set the line-height of Paragraphs
This property changes the height of each line in a block of text ie the amount of vertical space that each line of text gets.

## Adjust the Hover State of an Anchor Tag
The styling of an anchor tag can be changed in its hover state using the ``:hover`` pseudo-class selector.

```html
<style>
    a:hover {
        color: red;
    }
</style>
```

Now every time an anchor tag is hovered over, it will change its color to red.
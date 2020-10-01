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
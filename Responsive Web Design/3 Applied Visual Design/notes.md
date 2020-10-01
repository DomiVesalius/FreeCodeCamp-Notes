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
To make text you can use the strong tag. Using the strong tag on individual elements is the same as applying font-weight: bold; to a style sheet.

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
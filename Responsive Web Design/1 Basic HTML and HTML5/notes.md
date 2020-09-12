# Basic HTML and HTML5

## Heading Tags
There are 6 different types of heading tags ranging from h1 to h6.
h1 tags are the largest while h6 tags are the smallest.
To create a heading, choose the appropriate heading tag and do the following:

```html
<h1>textGoesHere</h1>

<h2>textGoesHere</h2>

<h3>textGoesHere</h3>

<h4>textGoesHere</h4>

<h5>textGoesHere</h5>

<h6>textGoesHere</h6>
```

# Paragraphs

You can also use paragraph elements (p) for paragraph sentences. It's syntax is just like the header tags; an opening and closing tag.

```html
<p>
    This is a paragraph tag. These are the preferred tags for long groups of sentences as opposed to heading tags. Make sure to use these when appropriate.
</p>
```

## HTML5 Tags: Main

HTML5 allows for more tags that are usefull when making large media dense websites.
A few examples are:
    1. main
    2. header
    3. footer
    4. nav
    5. video
    6. article
    7. section
Using these tags will bring more structure to the website you are building which makes your code easier to read.

Often we will use the 'main' tag which is helpful for search engines and developers in finding the main content of your page.
We can nest several tags within the main tag to do this.

```html
<main>
    <h1>Hello World</h1>
    
    <p>
        This is the main content of this webpage.
    </p>
</main>
```

## Adding Images

A lot of the time you want your website to have a lot of media such as pictures. HTML makes this very easy since it has a tag for just that.

We can use the 'img' (which is self closing) to add images to our website. Within the img tag we need to provide a source (src) which is a link 
to the picture.
A lot of the time we want to improve accessibility which is why we must use an 'alt' tag which provides a brief description of the image.
In some cases, we do not want to use the 'alt' tag but it is still best practice to have an empty alt tag instead of no alt tag.

```html
<img src='https://i.ytimg.com/vi/tMkURmaHKgs/maxresdefault.jpg' alt="Kakashi from the anime 'Naruto'">
```

## Anchor Elements

It's often usefull to be able to direct the user to content that does not exist within your webpage (perhaps on another website such as a wikipedia article.).
To do this we must use anchor elements (a) which are a non self-closing tag. We can use it as follows given the link you want to refer to:

```html
<p>
    For more information check out the <a href="https://en.wikipedia.org/wiki/HTML_element#Anchor">wikipedia article.</a>
</p>
```
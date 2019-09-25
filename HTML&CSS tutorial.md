HTML and CSS tutorial
====

## The world wide web
A Website is simply a collection of Webpages located on a same domain.
```
web -> website -> web page
```
<dl>
<dt>Web</dt> <dd>The part of the Internet that uses the HTTP protocol.</dd>
<dt>Webpage</dt> <dd> A document written in HTML.</dd>
<dt>Website </dt> <dd>
A collection of Webpages on the same domain.</dd>
<dt>Browser</dt>
<dd>A program that can open Webpages in order to display them.</dd></dl>

## A web browser
Remember that an HTML document can be opened in 2 ways:
```
by a text editor who sees the source code
by a browser who interprets the source code
```
list of editor
- [ ] Notepad ++
- [x] sublime text

# HTML basics
## HTML syntax
HTML stands for HyperText Markup Language:
```
HyperText            means that it uses the HTTP part of the Internet
Markup               means the code you write is annotated with keywords
Language             means it can be read by both a human and a computer
```
What you see in 
```
angle brackets < and > 
```
are HTML tags. They define where something starts and where it ends.

Each of them carry a specific meaning. In this case, p stands for paragraph.
They usually go in pairs:
```
the opening tag <p> defines the start of the paragraph
the closing tag </p> defines its end
```
The only difference between an opening and closing tag is the slash / that precedes the name of the tag.

### Where to write HTML
You’ve probably come across *simple text files*, those that have a .txt extension.
For such a text file to become an HTML document (instead of a text document), you need to use an *.html extension*.

Remember:
```
use a text editor like Notepad++ to create HTML documents
use a browser like Firefox to open HTML documents
```
### Attributes
Attributes act like extra information tied to an HTML element. They are *written within an HTML tag*. As such, they are not displayed by the browser either.

There are 16 HTML attributes that can be used on any HTML element. All of them are *optional*.
```
<a href="https://www.mozilla.com/firefox">Download Firefox</a>
```
Some HTML elements have *obligatory attributes*. 
For example, when inserting an image, you have to provide the location of the image, using the src (source) attribute
```
<img src="#" alt="Description of the image">
```

### Comments
They will be ignored by the browser, and are only useful for us humans who write the code.

A comment starts with 
```
<!-- and ends with -->.
```
```
<!-- This sentence will be ignored by the browser -->
<p>Hello World!</p>
```
### Self-enclosing elements
Some HTML elements only have an *opening tag*:
```
<br> <!-- line-break -->
<img src="https://placehold.it/50x50" alt="Description"> <!-- image -->
<input type="text"> <!-- text input -->
```
## HTML Block and Inline
<strong>Block</strong> elements are meant to structure the main parts of your page, by dividing your content in coherent blocks.<br>
block elements like:
  
```
paragraphs                                                                  <p>
lists: unordered (with bullet points) <ul> or ordered lists (with numbers)  <ol>
headings: from 1st level <h1> to 6th level headings                         <h6>
articles                                                                    <article>
sections                                                                    <section>
long quotes                                                                 <blockquote>
```
  
Inline elements are meant to *differentiate* part of a text, to give it a particular function or meaning. 
Inline elements usually comprise a single or few words.
inline elements like:
```
links                                               <a>
emphasised words                                    <em>
important words                                     <strong>
short quotes                                        <q>
abbreviations                                       <abbr>
```
### Other types of HTML elements
There are several exceptions to the block/inline elements, but the ones you will most often encounter are:
```
list items for the                                                          <li>
table, table rows, table cells for <table>, <tr> and <td> respectively
```
## HTML Hierarchy
An HTML document is like a *big family tree*, with parents, siblings, children, ancestors, and descendants.

It comes from the ability to **nest** HTML elements within one another.

### Depth
Because child elements can themselves contain other child elements, it’s possible to write a deeper hierarchy within an HTML document.

Our above paragraph could be part of a blog article:
```
<article>
  <h1>Famous football quotes</h1>
  <p> Sir <strong>Alex Ferguson</strong> once said about Filipo Inzaghi:<q>"That lad must have been born offside"</q>.</p>
  <p> When criticized by John Carew, <strong>Zlatan Ibrahimovic</strong> replied: <q>"What Carew does with a football, I can do with an orange"</q>. </p>
  <p><strong>George Best</strong> said <q>"I spent a lot of money on booze, birds and fast cars. The rest I just squandered."</q> when asked about his lifestyle.</p>
</article>
```

## HTML Semantics
### Structure elements: organizing your page
Here’s what a typical webpage could include:
```
<header>       as the first element of the page, that can include the logo and the tagline.
<nav>          as a list of links that go to the different pages of the website.
<h1>           as the title of the page.
<article>      as the main content of the page, like a blog post.
<footer>       as the last element of the page, located at the bottom.
```
### Text elements: defining your content
nside these structure elements, you usually find text elements meant to define the purpose of your content.

You’ll mainly use:
```
<p> for paragraphs
<ul> for (unordered) lists
<ol> for (ordered) lists
<li> for individual list items
<blockquote> for quotes
```

### Inline elements: distinguishing your text
There are a lot of inline elements available, but you’ll usually come across the following:
```
<strong> for important words
<em> for emphasized words
<a> for links
<small> for less important words
<abbr> for abbreviations like W3C
```
### Generic elements
When apparently no semantic element seems suited for your content but you still want to insert an HTML element (either for grouping or styling purposes), you can settle for one of the two generic elements:
```
<div> for block-level elements
<span> for inline elements
```
Although these HTML elements don’t actually mean anything, they will come in handy when we’ll start using CSS.

### Don’t overthink semantics
There are about 100 semantic HTML elements to choose from.
[All the form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)


## HTML formatting
```
Tabulations, 
empty lines, 
successive spaces, 
and line-breaks,
```
are dismissed by the computer, and are all converted into a single space.

There aren’t specific rules concerning HTML formatting, but there are implicit conventions, specifically:
```
use tabulations                        to help visualize how HTML elements are nested
put opening and closing tags           of block-level elements on their own line
write inline elements                  on one line (including opening and closing tags)
```

## A valid HTML document
```
correct: a valid document is correctly displayed by the browser
debugging: invalid HTML code can trigger bugs hard to target
maintenance: a valid document is easier to update later, even by someone else
```
### Doctype
To tell the browser that the HTML document is an HTML 5, just start your document with the following line
```
<!DOCTYPE html>
```

### The html element

Apart from the doctype line, all your HTML document must be wrapped inside an `<html>` element:
```
<!DOCTYPE html>
<html>
  <!-- The rest of your HTML code is here -->
</html>
```
The html is technically the ancestor of all HTML elements.

### The head
```
<head>
  <title>My fabulous blog</title>
</head>
```
Other HTML elements can appear in the `<head>`, and only in the head:
```
<link>
<meta>
<style>
```































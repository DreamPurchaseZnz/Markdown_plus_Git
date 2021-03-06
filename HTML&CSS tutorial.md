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

### `<body>`
While the `<head>` only contains metadata not meant to be displayed anywhere (apart from the `<title>`), the `<body>` element is where we write all our content. Everything inside the `<body>` will be displayed in the browser window.

### A complete valid HTML document
Combining all these requirements, we can write a simple and valid HTML document:
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>MarkSheet</title>
    <meta name="description" content="A simple HTML and CSS tutorial">
  </head>
  <body>
    <p>Hello World!</p>
  </body>
</html>
```
# Html Content
## Links

In HTML, links are inline elements written with the <a> tag.

The href attribute (hypertext reference) is used to define the target of the link (where you navigate to when you click).
```
 <a href="https://www.google.com">Google</a>.
```
It renders like:
 <a href="https://www.google.com">Google</a>.

There are 3 types of target you can define.
```
anchor targets, to navigate within the same page
relative URLs, usually to navigate within the same website
absolute URLs, usually to navigate to another website
```

Anchor target to navigate within the same page. By prepending 
```
your href with #
```
 you can target an HTML element with a specific id attribute.

For example, 
```
<a href="#footer">
```
will navigate to the 
```
<div id="footer"> 
```
within the same HTML document. This type of href is often used to navigate back to the top of the page.

## Images
Images use the 
```
<img> element, 
```
which is a self-closing element (it only has an opening tag).
```
width and height
```
## Table
Building a table in HTML requires a specific structure:
```
open a <table>
add rows with <tr>
add regular cells with <td> or heading cells with <th>
```
`<thead>`, `<tfoot>` and `<tbody>` are collections of rows. As such, they are direct children of `<table>` and direct parents of one or more `<tr>`. In short, they add one level of hierarchy.

`<thead>` and `<tfoot>` are used as a summary of the columns.
```
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Lennon</td>
      <td>Rhythm Guitar</td>
    </tr>
    <tr>
      <td>Paul McCartney</td>
      <td>Bass</td>
    </tr>
    <tr>
      <td>George Harrison</td>
      <td>Lead Guitar</td>
    </tr>
    <tr>
      <td>Ringo Starr</td>
      <td>Drums</td>
    </tr>
  </tbody>
</table>

```

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Instrument</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Lennon</td>
      <td>Rhythm Guitar</td>
    </tr>
    <tr>
      <td>Paul McCartney</td>
      <td>Bass</td>
    </tr>
    <tr>
      <td>George Harrison</td>
      <td>Lead Guitar</td>
    </tr>
    <tr>
      <td>Ringo Starr</td>
      <td>Drums</td>
    </tr>
  </tbody>
</table>

Although we’ve added a `<tfoot>` before the `<tbody>`, it still appears at the end.

It comes from the fact that the `<tbody>` can contain a lot of rows. But the browser wants to render the foot before receiving all of the (potentially numerous) rows of data. That’s why the `<tfoot>` is first in the code.
  
You can merge columns or rows by using
```
the rowspan and colspan respectively.
```
Keep in mind that in order to merge columns you need to use the rowspan attribute, as it allows to span a column across several rows

## HTML forms
But the Web understands that a user is sometimes required to provide his own input. These types of interaction include:
```
signing up and logging in to websites
entering personal information (name, address, credit card details…)
filtering content (by using dropdowns, checkboxes…)
performing a search
uploading files
```

To accomodate for these needs, HTML provides interactive form controls:
```
text inputs (for one or multiple lines)
radio buttons
checkboxes
dropdowns
upload widgets
submit buttons
```
```
<input type="text">
<!-- A checkbox -->
<input type="checkbox">
<!-- A radio button -->
<input type="radio">
```
<input type="text">
<!-- A checkbox -->
<input type="checkbox">
<!-- A radio button -->
<input type="radio">

The `<form>` is a block-level element thats defines an interactive part of a webpage. As a result, all form controls (like `<input>`, `<textarea>` or `<button>`) must appear within a `<form>` element.

Two HTML attributes are required:
```
action contains an address that defines where the form information will be sent
method can be either GET or POST and defines how the form information will be sent
```
Usually, the form information is sent to a server. How this data will then be processed goes beyond the scope of this tutorial.
```
Text	<input type="text">	             Allows any type of character
Email	<input type="email">	           Might display a warning if an invalid email is entered
Password	<input type="password">	     Shows dots as characters
Number	<input type="number">	         Up/Down keyboard keys can be used
Telephone	<input type="tel">	         Can trigger an autofill 

Multiple line text	
<textarea></textarea>	                  Can be resized
```
```

<form action="/signup" method="POST">
  <p>
    <label>Title</label>
    <label>
      <input type="radio" name="title" value="mr">
      Mr
    </label>
    <label>
      <input type="radio" name="title" value="mrs">
      Mrs
    </label>
    <label>
      <input type="radio" name="title" value="miss">
      Miss
    </label>
  </p>
  <p>
    <label>First name</label>
    <input type="text" value="first_name">
  </p>
  <p>
    <label>Last name</label>
    <input type="text" value="last_name">
  </p>
  <p>
    <label>Email</label>
    <input type="email" value="email">
  </p>
  <p>
    <label>Phone number</label>
    <input type="tel" value="phone">
  </p>
  <p>
    <label>Password</label>
    <input type="password" value="password">
  </p>
  <p>
    <label>Confirm your password</label>
    <input type="password" value="password_confirm">
  </p>
  <p>
    <label>Country</label>
    <select>
      <option>Canada</option>
      <option>France</option>
      <option>Germany</option>
      <option>Italy</option>
      <option>Japan</option>
      <option>Russia</option>
      <option>United Kingdom</option>
      <option>United States</option>
    </select>
  </p>
  <p>
    <label>
      <input type="checkbox" value="terms">
      I agree to the <a href="/terms">terms and conditions</a>
    </label>
  </p>
  <p>
    <button>
      Sign up
    </button>
  </p>
</form>
```
<form action="/signup" method="POST">
  <p>
    <label>Title</label>
    <label>
      <input type="radio" name="title" value="mr">
      Mr
    </label>
    <label>
      <input type="radio" name="title" value="mrs">
      Mrs
    </label>
    <label>
      <input type="radio" name="title" value="miss">
      Miss
    </label>
  </p>
  <p>
    <label>First name</label>
    <input type="text" value="first_name">
  </p>
  <p>
    <label>Last name</label>
    <input type="text" value="last_name">
  </p>
  <p>
    <label>Email</label>
    <input type="email" value="email">
  </p>
  <p>
    <label>Phone number</label>
    <input type="tel" value="phone">
  </p>
  <p>
    <label>Password</label>
    <input type="password" value="password">
  </p>
  <p>
    <label>Confirm your password</label>
    <input type="password" value="password_confirm">
  </p>
  <p>
    <label>Country</label>
    <select>
      <option>Canada</option>
      <option>France</option>
      <option>Germany</option>
      <option>Italy</option>
      <option>Japan</option>
      <option>Russia</option>
      <option>United Kingdom</option>
      <option>United States</option>
    </select>
  </p>
  <p>
    <label>
      <input type="checkbox" value="terms">
      I agree to the <a href="/terms">terms and conditions</a>
    </label>
  </p>
  <p>
    <button>
      Sign up
    </button>
  </p>
</form>











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
Some HTML elements only have an opening tag:
```
<br> <!-- line-break -->
<img src="https://placehold.it/50x50" alt="Description"> <!-- image -->
<input type="text"> <!-- text input -->
```














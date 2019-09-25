# Markdown_plus_Git
[Learn the ropes](https://www.markdownguide.org/basic-syntax)
[Table Generator:http://www.tablesgenerator.com/markdown_tables](http://www.tablesgenerator.com/markdown_tables)

### window software
MarkdownPad and ghost writer

## Basic syntax
### headings

To create a heading, add number signs (#) in front of a word or phrase

```
Markdown                       HTML:
# Heading level 1              <h1> Heading level 1</h1>
```

Alternate Syntax:

Alternatively, on the line below the text, add *any number* of == characters for heading level 1 or -- characters for heading level 2.

```
Heading level 1             
===============            <h1>Heading level 1</h1>

Heading level 2
---------------            <h2>Heading level 2</h2>
```
<h3> Paragraphs </h3>

<p>To create paragraphs, use a *blank line* to separate one or more lines of text.</p>
 You should not indent paragraphs with spaces or tabs

```
MarkDown:                           HTML
I really like using Markdown.       <p>I really like using Markdown.</p>
(blank line)
```
### line breaks
To create a line break (),    
```
<br>
```
end a line with two or more spaces, and then type return.
### Emphasis

You can add emphasis by making text bold or italic.
```
<strong> </strong>                   **text**
<em> </em>                           *text*
<strong><em> </em></strong>          ***text***
```
### Blockquotes
To create a blockquote, add a > in front of a paragraph.
```
> text

> text
>
> paragraph
```
Blockquotes can contain multiple paragraphs. Add a > on the blank lines between the paragraphs.
Blockquotes can be nested. Add a >> in front of the paragraph you want to nest
```
>
>>
>>>
```
Blockquotes with Other Elements
```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

### List
You can organize items into ordered and unordered lists.

#### Ordered Lists
```
1. First item
2. Second item
3. Third item
4. Fourth item	
<ol>
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
<li>Fourth item</li>
</ol>
```
#### Unordered Lists
To create an unordered list, add 
```
dashes (-),                     <ul> <li></li>   </ul>
asterisks (*), or 
plus signs (+) 
```
in front of line items. Indent one or more items to create a nested list.

#### Adding Elements in Lists
To add another element in a list while preserving the continuity of the list, 
indent the element **four spaces or one tab**, as shown in the following examples.
```
*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.
```
  
#### Code
To denote a word or phrase as code, enclose it in tick marks.
```
`code`
<code>nano</code>.
```
`code`
<code>nano</code>.
#### Horizontal Rules
To create a horizontal rule,  
```
use three or more 
asterisks(***), 
dashes (---), or 
underscores (___) 
```
on a line by themselves.

#### URLs and Email Addresses
To quickly turn a URL or email address into a link, enclose it in angle brackets.
```
<https://www.markdownguide.org>
<fake@example.com>
```
### Images
To add an image, add an exclamation mark (!), followed by alt text in brackets, and the path or URL to the image asset in parentheses. You can optionally add a title after the URL in the parentheses.
```
![Philadelphia's Magic Gardens. This place was so cool!]                  alt
(/assets/images/philly-magic-gardens.jpg "Philadelphia's Magic Gardens")  path and title
```
##### Linking Images
To add a link to an image, enclose the Markdown for the image in brackets, and then add the link in parentheses.
```
[  ![]()  ]()
```
### Escaping Characters
To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash (\) in front of the character

<h2>Extended syntax</h2>
### Availability
Extended syntax **isn’t available in all Markdown applications**. You’ll need to check whether or not the lightweight markup language your application is using supports extended syntax. If it doesn’t, it may still be possible to enable extensions in your Markdown processor.

### Table

To add a table, use three or more hyphens *(---)* to create each column’s header, and use pipes *(|)* to separate each column. You can optionally add pipes on either end of the table.

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

```

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

##### Alignment:
You can align text in the columns to the left, right, or center by adding a *colon (:)* to the left, right, or on both side of the hyphens within the header row.
```
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

##### Formatting text in tables
You can format the text within tables. For example, you can add 
```
links, code (words or phrases in tick marks (`) only, not code blocks), and emphasis.
```
You can’t add 
```
headings, blockquotes, lists, horizontal rules, images, or HTML tags
```
### Fenced Code Blocks
The basic Markdown syntax allows you to create code blocks by indenting lines by four spaces or one tab. If you find that inconvenient, try using fenced code blocks. Depending on your Markdown processor or editor, you’ll use 
```
three tick marks (```) or three tildes (~~~) 
```
on the lines before and after the code block. The best part? You don’t have to indent any lines!

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
##### Syntax Highlighting
To add syntax highlighting, specify a language next to the tick marks before the fenced code block.
```
three tick ``` + language（json,python,java）

```

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
### Footnotes

To create a footnote reference, add a caret and an identifier inside brackets 
```
([^1])
```
Identifiers can be numbers or words, but they can’t contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself — in the output, footnotes are numbered sequentially.<br>
Add the footnote using another caret and number inside brackets with a colon and text 
```
([^1]: My footnote.)
```
You don’t have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.


```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.
```
Results is:

Here's a simple footnote,[^1] and here's a longer one.[^bignote]
[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.
Conlusion: it doesn't work

###  Heading IDs {#custom-id}

 To add a custom heading ID, enclose the custom ID in curly braces on the same line as the heading.
``` 
### My Great Heading {#custom-id}         <h3 id="custom-id">My Great Heading</h3>
```

#### linking heading IDs
You can link to headings with custom IDs in the file by creating a *standard link* with a number sign (#) followed by the custom heading ID

```
[Heading IDs](#heading-ids)	             <a href="#heading-ids">Heading IDs</a>	
```
return [Heading IDs title](#heading-ids)

Conclusion: it doesn't work

### Definition lists
To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition
```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

Conclusion: it doesn't work
```
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>
```
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>

### Strikethrough
To strikethrough words, use two tilde symbols \
```
(~~) 
```
before and after the words.
```
I Sad a lie: ~~I LOVE YOU~~
```
I Sad a lie: ~~I LOVE YOU~~

### Task Lists











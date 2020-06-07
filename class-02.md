# Basics of HTML, CSS & JS

## Structural markup

The elements that you can use to describe both headings and paragraphs.

### Headings

HTML headings are titles or subtitles that you want to display on a webpage.
`<h1>` defines the most important heading. `<h6>` defines the least important heading.

```
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Paragraphs

A paragraph always starts on a new line, and is usually a block of text.

`<p>This is a paragraph.</p>`

### Bold & Italic

**Bold**

The HTML `<b>` element defines bold text, without any extra importance.

`<b>This text is bold</b>`

_Italic_

The HTML `<i>` element defines italic text, without any extra importance.

`<i>This text is italic</i>`

### Subscript & Superscript

The `<sub>` tag defines subscript text. Subscript text appears half a character below the normal line.

The `<sup>` tag defines superscript text. Superscript text appears half a character above the normal line.

### Line break & Horizontal Rules

The `<br>` tag inserts a single line break.

The `<hr>` element is most often displayed as a horizontal rule that is used to separate content (or define a change) in an HTML page.

## Semantic Markup

### Strong & Emphasis

The `<strong>` tag is used to define text with strong importance. The content inside is typically displayed in **bold**.

The `<em>` tag is used to define emphasized text. The content inside is typically displayed in _italic_.

### Quotations

The `<blockquote>` tag indicates that the enclosed text is an extended quotation.

The `<q>` tag defines a short quotation.

### Abbreviations & Acronyms

The `<abbr>` tag defines an abbreviation or an acronym, like "HTML", "CSS", "Mr.", "Dr.", "ASAP", "ATM".

### Citation & Definitions

The `<cite>` tag defines the title of a creative work (e.g. a book, a poem, a song, a movie, a painting, a sculpture, etc.).

The `<dfn>` tag stands for the "definition element", and it specifies a term that is going to be defined within the content.

### Auther Details

The `<address>` tag defines the contact information for the author/owner of a document or an article.

### Changes to content

The `<ins>` tag defines a text that has been inserted into a document. Browsers will usually underline inserted text.

The `<del>` tag defines text that has been deleted from a document. Browsers will usually strike a line through deleted text.

The `<s>` tag specifies text that is no longer correct, accurate or relevant. The text will be displayed with a line through it.

## Introducing CSS

Css works by associating rules with Html elements. These rules specify how the element should be displayed.
a Css rule conatins to parts, selector and a decleration.

![css rule](assets/image3.png)

Css rule can have more than one decleration. And any decleration contain two parts: property and value

![css rule](assets/Image4.png)

### Using ExternaL Css

The best practise of using css is to include all the rules in external file with .css extention and link it on your document using this tag

`<link href="css/styles.css" type="text/css" rel="stylesheet" />`

- **href** :This specifies the path to the CSS file (which is often placed in a folder called css or styles).
- **type**: This attribute specifies the type of document being linked to. The value should be text/css.
- **rel**: This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.

### Using Internal Css

You can also use css inside the head tag of your document by adding the css rules within `<style>` tag

```
<head>
<title>Using Internal CSS</title> <style type="text/css">
body {
font-family: arial; background-color: rgb(185,179,175);}
h1 {
color: rgb(255,255,255);}
    </style>
  </head>
```

### Css selectors 

its the way to select the element or elements that we wish to apply some css rules on it.
there is many types of selectors. See this table.

Selector | Example | description
--------- | --------- | ---------
.class | .intro | Selects all elements with class="intro"
#id	| #firstname | Selects the element with id="firstname"
/* | /* | Selects all elements
element | p | Selects all `<p>` elements
element,element,..	| div, p | Selects all `<div>` elements and all `<p>` elements

### How css ruLes cascade ?

There are 4 rules that govirn this:

- **Sort by Importance**

If there are any conflicts in your css, there is an order of importance in which some selectors are more important than others:
an ID will win out over a class
a class will win out over a tag

- **Sort by weight**

The styles are checked in the following order, each subsequent style sheet has a greater weight than the previous.

Default: Browser
User: Style Sheet
Author: Style Sheet - Linked
Author: Style Sheet - Embedded in the head of the web page
Author: Style Sheet - Inline within the body of the web page

- **Sort by Specificity**

Determines how specific the rule is

```
#content{
color: #333
}

#content p{
color: #f00
}

#content p em{
color: #f00
}
#content  p em{ color: #foo}
```
This rule wins out because it is the most specific of the three.

- **Sort by Order**

f two rules have the same properties, specificy and values the one that appears later in the css will be the one that the browser uses but:
! importance has more weight than anything else regardless of its position within the style sheet;
```
p em{
color: #f00 !important;
}
```

### Inheritance in css

Inheritance is the mechanism by which certain properties are passed on from a parent element down to its children, in the same fashion as genetics: if parents have blue eyes, their children will probably also have blue eyes.

Not all CSS properties are inherited, because it does not make sense for some of them to be. For instance, margins and width are not inherited
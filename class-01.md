# Introductory HTML and JavaScript

##  How the web works ?

Let’s start with the most obvious way of using the internet: You visit a website like google.com.
The moment you enter this address in your browser and you hit ENTER, a lot of different things happen:

1. The URL gets resolved
2. Contact the (DNS) servers
3. Obtain the IP address associated with the requested domain name.
4. A Request is sent to the server of the website
5. The response of the server is parsed
6. The page is rendered and displayed

![web](assets/image1.png)

## Structure

### HTML
It is refer to hyper text mark up langauge. You have to know it is not a programming language instead it is a way of structuring data on the web using special write to do this purpose. In HTML we wrap every piece of data in tags that tags define how to present thies information. Tags it has two brakets and a charters between them like <p>data</p> each tag has an opening and closeing and every tag has it purpose. The opening tags can carry attributes, which tell us more about the content of that element. and every attribue has a name and value.

**Check this image to see how we structue data using html**
![Html](https://help.madcapsoftware.com/flare2017r3/Content/Resources/Images/Flare/page_structure_example.png)

* The `<html>` element is the root element of an HTML page
* The `<head>` element contains meta information about the HTML page
* The `<title>` element specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)
* The `<body>` element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs,  images, hyperlinks, tables, lists, etc.
* The `<h1>` element defines a large heading
* The `<p>` element defines a paragraph

## Extra Markup
### DOCTYPES
The `<!DOCTYPE html>` declaration is used to inform a website visitor's browser that the document being rendered is an HTML document. While not actually an HTML element itself, every HTML document should being with a DOCTYPE declaration to be compliant with HTML standards.
### Comments in HTML
You can add comments to your HTML source by using the following syntax:

`<!-- Write your comments here -->`

### ID attribute
The id attribute specifies a unique id for an HTML element (the value must be unique within the HTML document).
The id attribute is most used to point to a style in a style sheet, and by JavaScript (via the HTML DOM) to manipulate the element with the specific id.

`<h1 id="myHeader">Hello World!</h1>`

### Class attribute
The class attribute in HTML is used to set one or more classnames for an element. With the specified class name you can work it through CSS and point in a stylesheet.

```
<!DOCTYPE html>
<html>
<head>
<style>
h2.demo {
   color: orange;
   background-color: black;
}
</style>
</head>
<body>
<h1>Resources</h1>
   <h2 class="demo">Text Tutorials</h1>
   <h2 class="demo">Video Tutorials</h1>
   <h2 class="demo">Interview Questions and Answers</h1>
   <h2 class="demo">Online Quiz</h1>
</body>
</html>
```

### Block Elements
A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).

Example:

`<div>Hello World</div>`


### Inline Elements
An inline element does not start on a new line and only takes up as much width as necessary.

Example:

`<span>Hello World</span>`

### Grouping text & Elements in a block
The `<div>` element does not inherently represent anything. Instead, it's used to group content so it can be easily styled using the class or id attributes.

Example:
```
<div class="warning">
    <img src="/media/examples/leopard.jpg"
         alt="An intimidating leopard.">
    <p>Beware of the leopard</p>
</div>
```

### Grouping text & Elements inline
Spans are similar to divs, except they are inline elements. You might use them to group words together, since words appear inline and not each on their own line.

Example:

`<p>Note: this is an editorial piece and does not reflect the official opinion of the <span>Sun Journal.</span></p>`




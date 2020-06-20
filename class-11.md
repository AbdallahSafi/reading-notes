# Images

### ControllIng sIzes of Images In css

You can control the size of an image using the width and height properties in CSS.

```html
<img src="images/magnolia-large.jpg" class="large" alt="Magnolia" />
<img src="images/magnolia-medium.jpg" class="medium" alt="Magnolia" />
<img src="images/magnolia-small.jpg" class="small" alt="Magnolia" />
```

```css
img.large { width: 500px; height: 500px;}
img.medium { width: 250px; height: 250px;}
img.small { width: 100px; height: 100px;}
```

### How to align and float images on your website ?

**Image alignment**

- Floating images right with text wrapping
In this example, we include the image tag in our HTML file, but identify the image with an ID (“hp”).

```html
<img src="hp.jpg" alt="" width="200" height="200" id="hp"/>
```

The formatting code is called from a separate CSS file, which includes the float:right rule, plus some additional spacing, courtesy of the margin rule.

```css
#hp  {
float: right;    
 margin: 0 0 0 15px;
}
```

![image](https://hostpapasupport.com/knowledgebase/wp-content/uploads/2017/11/6-600x119.png)


- Floating images left with text wrapping

With the image correctly tagged in the HTML file, you can simply edit the CSS rule to experiment with alternative layouts.

```css
#hp  {
float: left;    
 margin: 0 15px 0 0;
}
```

![image](https://hostpapasupport.com/knowledgebase/wp-content/uploads/2017/11/7-600x118.png)

- No float

Use the float:none rule to simply display the image where it is placed in the text, without any wrapping. You can retain the margin rule (if desired) for spacing.

```css
#hp  {
float: none;    
 margin: 0 15px 0 0;
}
```

![image](https://hostpapasupport.com/knowledgebase/wp-content/uploads/2017/11/8-600x132.png)

- Clearing floats

One important, additional requirement when floating images is the correct use of the clear rule. Floated images (and other web elements) will overlap one another if you do not “clear” the float. Be sure to use the clear rule after each section in which an image is floating.

![image](https://hostpapasupport.com/knowledgebase/wp-content/uploads/2017/11/9-600x167.png)


```css
.div2 {
     border: 1px solid red;
     clear: both;
}
```

**Centering the image using CSS**

```html
<img src="paris.jpg" alt="Paris" class="center">
```

```css
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
```

- Background Image

Set a background-image for the `<body>` element:

```css
body {
 background-image: url("paper.gif");
 background-color: #cccccc;
}
```

- Background Repeat 

Repeat a background-image only vertically:

```css
body {
  background-image: url("paper.gif");
  background-repeat: repeat-y;
}
```

- Background Attachment 

A background-image that will not scroll with the page (fixed):

```css
body {
  background-image: url("img_tree.gif");
  background-repeat: no-repeat;
  background-attachment: fixed;
}
```

- Background Position

The background-position property in CSS allows you to move a background image (or gradient) around within its container.

```css
html {
  background-position: 100px 5px; 
}
```


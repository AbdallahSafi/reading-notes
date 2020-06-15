# CSS layout

every single element on a web page is a block. Literally a rectangle of pixels. This is easy to understand when you set the element to display: block; or if that element is block-level by default like a `<div>`. This means you can set a width and a height and that element will respect that. But elements that are display: inline;, like a `<span>` by default, are also rectangles, they just flow onto the page differently, lining up horizontally as they can.

**Block-level elements**
start on a new line

Examples include:
`<h1> <p> <ul> <li>`

**Inline elements**
flow in Between surrounding text Examples include:

`<img> <b> <i>`

**Normal Flow**

If you take an HTML webpage which has no CSS applied to change the layout, the elements will display in normal flow.

![normal flow](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/deeb1d28-d06d-4c1f-90c6-de2597d3f6c1/block-inline.png)

You can benfit of this normal flow to structure your page but If you want more control you may move away from the normal flow.


**Positioning**

Remove an element from normal flow or shift it around from its place in normal flow, you can use the position property in CSS.

*RELATIVE POSITIONING*

If an item has position: relative then the reference point is the place it would normally be in normal flow.

```css
.item {
    position: relative;
    bottom: 50px;
}
```


*ABSOLUTE POSITIONING*

Set position: absolute on an item and it will be removed completely from normal flow.

You can then use offset values for the properties top, left, bottom and right to move the box from that position to where you want it to be.

```css
.item {
    position: absolute;
    top: 20px;
    right: 20px;
}
```

*FIXED POSITIONING*

Something with position: fixed will be positioned in most cases relative to the viewport, and removed from document flow so that no space is reserved for it.

```css
.item {
    position: fixed;
    top: 20px;
    left: 100px;
}
```

*STICKY POSITIONING*

Setting position: sticky on an element will cause the element to scroll with the document just as it would in normal flow, however, once it reaches a certain point in relation to the viewport (using the usual offsets) it “sticks” and starts to act like position: fixed.

```css
.item {
    position: sticky;
    top: 0;
}
```


**Floats**

Floats are used to shift a box to the left or right, allowing content to display wrapped around it.

```css
.item {
    float: left;
}
```


**What are floats used for?**

Aside from the simple example of wrapping text around images, floats can be used to create entire web layouts.

![float](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/web-text-wrap.png?resize=540%2C270&ssl=1)


Floats are also helpful for layout in smaller instances. Take for example this little area of a web page. If we use float for our little avatar image, when that image changes size the text in the box will reflow to accommodate:

![float](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/web-layout.png?resize=540%2C240&ssl=1)


**CLearing FLoats**

Once you have floated an element, all of the following elements will wrap around that floated element until they wrap underneath and normal flow continues. If you want to prevent that, you need to clear the float.

``` css
.clear {
    clear: both; 
}
```

**Liquid Layouts**

All containers on the page have their widths defined in percents – meaning that they are completely based on the viewport rather than the initial containing block. A liquid layout will move in and out when you resize your browser window.

**Fixed-width layouts**

All containers on the page have their widths defined in pixels or other fixed units. They are completely independent of the viewport. A fixed layout will not move in and out when you resize your browser window.

**Layout grids**
Grids set consistent proportions and spaces between items which helps to create a professional looking design.

![grid](https://www.bitdegree.org/learn/storage/media/images/f2804b75-5393-4504-bad9-fec3f56dfb94.png)

**CSS frameworks**

CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.
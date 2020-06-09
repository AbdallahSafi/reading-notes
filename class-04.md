# HTML Links, CSS Layout, JS Functions

## HTML Links

HTML links are hyperlinks.You can click on a link and jump to another document.
When you move the mouse over a link, the mouse arrow will turn into a little hand.

Hyperlinks are defined with the HTML `<a>` tag:

`<a href="https://www.google.com/html/">Google</a>`

![links](assets/image10.png);

**Linking to a page in the same website**

```html
<p> <ul>
<li><a href="index.html">Home</a></li>
 <li><a href="about-us.html">About</a></li>
 <li><a href="movies.html">Movies</a></li>
 <li><a href="contact.html">Contact</a></li>
</ul> </p>
```

**Directory structure**

On a larg projects you should organize your code in files and folders with good name convention

![structure](assets/image11.png);

**Relative URL**

Relative URLs can be used when linking to pages within your own website. They provide a shorthand way of telling the browser where to find your files

| Relative Link Type | Example                                          |
| ------------------ | ------------------------------------------------ |
| Same Folder        | `<a href="reviews.html">Reviews</a>`             |
| Child Folder       | `<a href="music/listings.html">Listings</a>`     |
| Grandchild Folder  | `<a href="movies/dvd/reviews.html"> Reviews</a>` |
| Parent Folder      | `<a href="../index.html">Home</a>`               |
| Grandparent Folder | `<a href="../../index.html">Home</a>`            |

**Email Linking**

Mailto link is a type of HTML link that activates the default mail client on the computer for sending an e-mail.

`<a href="mailto:name@email.com">Link text</a>`

**Open links in a new window**

You can use target attrbut to target your link to another window.

`<a href="http://www.imdb.com" target="_blank"> Internet Movie Database</a>`

**Linking to a specifice part of a page**

Here you must use an Id for that part you want the link to go to. See the Example

```html
<h2 id="interlude">Interlude</h2>
<a href="#interlude">Interlude</a>
```

If you want to go to a specfice part pf other page just include the #id after the link

`<a href="http:/www.htmlandcssbookcom/#bottom">`

# CSS Layout

**Normal Flow**

If you take an HTML webpage which has no CSS applied to change the layout, the elements will display in normal flow.

![normal flow](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/deeb1d28-d06d-4c1f-90c6-de2597d3f6c1/block-inline.png)

You can benfit of this normal flow to structure your page but If you wnat more control you may move away from the normal flow.

**Floats**

Floats are used to shift a box to the left or right, allowing content to display wrapped around it.

```css
.item {
    float: left;
}
```

![float](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/5be62853-b56c-4a56-8764-8814fa5c48d5/float-background.png)

**CLearing FLoats**

Once you have floated an element, all of the following elements will wrap around that floated element until they wrap underneath and normal flow continues. If you want to prevent that, you need to clear the float.

``` css
.clear {
    clear: both; 
}
```

*Note*: the most common when clearing floats is to set the overflow property to have a value other than the default visible.

```css
.container {
    overflow: auto;
}
```

**Positioning**

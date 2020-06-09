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


Relative Link Type | Example
------------------ | ------------------
Same Folder | `<a href="reviews.html">Reviews</a>`
Child Folder | `<a href="music/listings.html">Listings</a>`
Grandchild Folder | `<a href="movies/dvd/reviews.html"> Reviews</a>`
Parent Folder | `<a href="../index.html">Home</a>`
Grandparent Folder | `<a href="../../index.html">Home</a>`

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
# LOCAL STORAGE FOR WEB APPLICATIONS


 The operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state.

 Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data.

- thereby slowing down your web application by needlessly transmitting the same data over and over
- thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
- Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful

## A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5

- Microsoft invented DHTML Behaviors (userData) allows web pages to store up to 64 KB of data per domain.
- In 2002, Adobe introduced “Flash cookies.” it allows Flash objects to store up to 100 KB of data per domain.
- In 2007, Google launched Gears, Gears can store unlimited amounts of data per domain in SQL database tables.
-  HTML5 set out to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.

## INTRODUCING HTML5 STORAGE

- HTML5 Storage it’s a way for web pages to store named key/value pairs locally, within the client web browser.
- This data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you.
- Unlike cookies, this data is never transmitted to the remote web server.
- The latest version of pretty much every browser supports HTML5 Storage.

To detect support for HTML5 Storage.
```javascript
if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```

## USING HTML5 STORAGE

- HTML5 Storage is based on named key/value pairs.

```javascript
var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
```

- could be rewritten to use square bracket syntax instead:

```javascript
var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;
```

- Removing the value for a given named key

```javascript
interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};
```

- Property to get the total number of values in the storage area

```javascript
interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};
```

## TRACKING CHANGES TO THE HTML5 STORAGE AREA

- The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called.

```javascript
if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};
```

## LIMITATIONS IN CURRENT BROWSERS

- “5 megabytes” is how much storage space each origin gets by default.



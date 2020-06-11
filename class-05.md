# HTML Images; CSS Color & Text

## Images

### Adding Image

Images can be easily inserted at any section in an HTML page. To insert image in an HTML page, use the <img> tags. It is an empty tag, containing only attributes since the closing tag is not required.

![image](https://www.tutorialspoint.com/assets/questions/images/167928-1516185173.jpg)

```html
<img src="/html/images/test.png" alt="Simply Easy Learning" width="200" height="80">
 ```
### Aligning image
 
You can align image using align attribute

`<img src="images/bird.gif" alt="Bird" width="100" height="100" align="top" />`

You have four choices for alignment : top, bottom, left, right

**Note**: 
- Images with png formate is the best suit for screen displays.
- Images with vsg format are vector based and it is the ultimate choice when using logo or icons in your website.
- Images created for web should be saved at a resolution of 72ppi for optimization purpose.

### Figure and Figure caption

You can use `<figur>` tag to inclue a captions for the image element.

Example:

```html
<figure>
<img src="images/otters.jpg" alt="Photograph of
two sea otters floating in water"> <br />
<figcaption>Sea otters hold hands when they sleep so they don't drift away from each other.</figcaption>
</figure>
```





## CSS Color
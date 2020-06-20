# Images

### ControllIng sIzes of Images In css

You can control the size of an image using the width and height properties in CSS.

```html
<img src="images/magnolia-large.jpg" class="large" alt="Magnolia" />
<img src="images/magnolia-medium.jpg" class="medium" alt="Magnolia" />
<img src="images/magnolia-small.jpg" class="small" alt="Magnolia" />
```

```css
img.large {
  width: 500px;
  height: 500px;
}
img.medium {
  width: 250px;
  height: 250px;
}
img.small {
  width: 100px;
  height: 100px;
}
```

### How to align and float images on your website ?

**Image alignment**

- Floating images right with text wrapping
  In this example, we include the image tag in our HTML file, but identify the image with an ID (“hp”).

```html
<img src="hp.jpg" alt="" width="200" height="200" id="hp" />
```

The formatting code is called from a separate CSS file, which includes the float:right rule, plus some additional spacing, courtesy of the margin rule.

```css
#hp {
  float: right;
  margin: 0 0 0 15px;
}
```

![image](https://hostpapasupport.com/knowledgebase/wp-content/uploads/2017/11/6-600x119.png)

- Floating images left with text wrapping

With the image correctly tagged in the HTML file, you can simply edit the CSS rule to experiment with alternative layouts.

```css
#hp {
  float: left;
  margin: 0 15px 0 0;
}
```

![image](https://hostpapasupport.com/knowledgebase/wp-content/uploads/2017/11/7-600x118.png)

- No float

Use the float:none rule to simply display the image where it is placed in the text, without any wrapping. You can retain the margin rule (if desired) for spacing.

```css
#hp {
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
<img src="paris.jpg" alt="Paris" class="center" />
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

- Gradients & background-image

```css
body {
  background: #eb01a5;
  background-image: url("IMAGE_URL"); /* fallback */
  background-image: url("IMAGE_URL"), linear-gradient(#eb01a5, #d13531); /* W3C */
}
```

# Practical information

Search Engine Optimization (SEO)

![image](https://moz.imgix.net/learn/guides/Mozlows-01-outline.svg?auto=format&ch=Width&fit=max&q=50&s=e088165a17e355b8186964266ef71ca5)

earch engine optimization is the process of optimizing web pages and their content to be easily discoverable by users searching for terms relevant to your website. The term SEO also describes the process of making web pages easier for search engine indexing software, known as "crawlers," to find, scan, and index your site.

- Why Should You Care About SEO ?

Many people search for specific products and services with the intent to pay for these things. These searches are known to have commercial intent, meaning they are clearly indicating with their search that they want to buy something you offer.

- SEO Keyword Research & Keyword Targeting Best Practices

The first step in search engine optimization is to determine what you’re actually optimizing for. This means identifying terms people are searching for, also known as “keywords,” that you want your website to rank for in search engines like Google.

- How many people are coming to your site?

The overview page gives you a snapshot of the key information you are likely to want to know. In particular, it tells you how many people are coming to your site.

### Domain names & Hosting

- Domain name is the address of your website that people type in the browser’s URL bar to visit your website.

- Web hosting is the place where all the files of your website live. It is like the home of your website where it actually lives.

### FTP & third Party tools

The File Transfer Protocol (FTP) is a standard network protocol used for the transfer of computer files between a client and server on a computer network.

File Transfer Protocol (FTP) is both easy to use and a robust solution. It enables you to visualize your file structure, and access advanced options for each file within an intuitive interface. Plus, there are plenty of free FTP tools available.

## HTML5 audio and video

HTML5 features include native audio and video support without the need for Flash.

The HTML5 `<audio>` and `<video>` tags make it simple to add media to a website. You need to set src attribute to identify the media source and include a controls attribute so the user can play and pause the media.

- Embedding Video

Here is the simplest form of embedding a video file in your webpage −

```html
<video src="foo.mp4" width="300" height="200" controls>
  Your browser does not support the <video>element.</video>
</video>
```

most commonly used video formats are −

_Ogg_ − Ogg files with Thedora video codec and Vorbis audio codec.

_mpeg4_ − MPEG4 files with H.264 video codec and AAC audio codec.

**Video Attribute Specification**

The HTML5 video tag can have a number of attributes to control the look and feel and various functionalities of the control −

| Attribute  | Description                                                                                             |
| ---------- | ------------------------------------------------------------------------------------------------------- |
| autoplay   | the video will automatically begin to play back as soon as it can do                                    |
| autobuffer | the video will automatically begin buffering even if it's not set to automatically play.                |
| controls   | it will allow the user to control video playback, including volume, seeking, and pause/resume playback. |
| height     | This attribute specifies the height of the video's display area, in CSS pixels.                         |
| loop       | will allow video automatically seek back to the start after reaching at the end.                        |
| preload    | the video will be loaded at page load, and ready to run                                                 |
| poster     | This is a URL of an image to show until the user plays or seeks.                                        |
| src        | The URL of the video to embed. This is optional;                                                        |
| width      | This attribute specifies the width of the video's display area, in CSS pixels.                          |

- Embedding Audio

HTML5 supports `<audio>` tag which is used to embed sound content in an HTML or XHTML document as follows.

```html
<audio src="foo.wav" controls autoplay>
  Your browser does not support the <audio>element.</audio>
</audio>
```

**Audio Attribute Specification**

The HTML5 audio tag can have a number of attributes to control the look and feel and various functionalities of the control −

Attribute |  Description
-------- | -----------
autoplay | the audio will automatically begin to play back as soon as it can do so without stopping to finish loading the data.	
autobuffer | the audio will automatically begin buffering even if it's not set to automatically play.
controls |  it will allow the user to control audio playback, including volume, seeking, and pause/resume playback.	
loop | will allow audio automatically seek back to the start after reaching at the end.	
preload |  he audio will be loaded at page load, and ready to run. Ignored if autoplay is present.	
src | The URL of the audio to embed. This is optional


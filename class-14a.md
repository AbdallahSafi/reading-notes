# Transforms

- The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

```javascript
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

## 2D Transforms

- Two-dimensional transforms work on the x and y axes.

### 2D Rotate

- The rotate value provides the ability to rotate an element from 0 to 360 degrees.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

### 2D Scale

- Allows you to change the appeared size of an element.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
7 .box-1 {
  transform: scale(0.75);
}
.box-2 {
  transform: scale(1.25);
}
```

- It is possible to scale only the height or width of an element using the scaleX and scaleY values.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
```

```css
.box-1 {
  transform: scaleX(0.5);
}
.box-2 {
  transform: scaleY(1.15);
}
.box-3 {
  transform: scale(0.5, 1.15);
}
```

### 2D Translate

- The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
```

```css
.box-1 {
  transform: translateX(-10px);
}
.box-2 {
  transform: translateY(25%);
}
.box-3 {
  transform: translate(-10px, 25%);
}
```

### 2D Skew

- skew, is used to distort elements on the horizontal axis, vertical axis, or both.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
```

```css
.box-1 {
  transform: skewX(5deg);
}
.box-2 {
  transform: skewY(-20deg);
}
.box-3 {
  transform: skew(5deg, -20deg);
}
```

## Combining Transforms

- It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
.box-1 {
  transform: rotate(25deg) scale(0.75);
}
.box-2 {
  transform: skew(10deg, 20deg) translateX(20px);
}
```

## Transform Origin

- As previously mentioned, the default transform origin is the dead center of an element, both 50% horizontally and 50% vertically. To change this default origin position the transform-origin property may be used.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
<figure class="box-4">Box 3</figure>
```

```css
.box-1 {
  transform: rotate(15deg);
  transform-origin: 0 0;
}
.box-2 {
  transform: scale(0.5);
  transform-origin: 100% 100%;
}
.box-3 {
  transform: skewX(20deg);
  transform-origin: top left;
}
.box-4 {
  transform: scale(0.75) translate(-10px, -10px);
  transform-origin: 20px 50px;
}
```

## Perspective

- In order for three-dimensional transforms to work the elements need a perspective from which to transform.

```html
<figure class="box">Box 1</figure>
<figure class="box">Box 2</figure>
<figure class="box">Box 3</figure>
```

```css
.box {
  transform: perspective(200px) rotateX(45deg);
}
```

### Perspective Depth Value

- The perspective value can be set as none or a length measurement.

## 3D Transforms

## 3D Rotate

- With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
```

```css
.box-1 {
  transform: perspective(200px) rotateX(45deg);
}
.box-2 {
  transform: perspective(200px) rotateY(45deg);
}
.box-3 {
  transform: perspective(200px) rotateZ(45deg);
}
```

## 3D Scale

- By using the scaleZ three-dimensional transform elements may be scaled on the z axis.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
.box-1 {
  transform: perspective(200px) scaleZ(1.75) rotateX(45deg);
}
.box-2 {
  transform: perspective(200px) scaleZ(0.25) rotateX(45deg);
}
```

## 3D Translate

- Elements may also be translated on the z axis using the translateZ value.

<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
.box-1 {
  transform: perspective(200px) translateZ(-50px);
}
.box-2 {
  transform: perspective(200px) translateZ(50px);
}
```

## 3D Skew

Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale.

## Transform Style

To allow nested elements to transform in their own three-dimensional plane use the transform-style property with the preserve-3d value.

```html
<div class="rotate three-d">
  <figure class="box">Box 1</figure>
</div>
<div class="rotate">
  <figure class="box">Box 2</figure>
</div>
```

```css
.rotate {
  transform: perspective(200px) rotateY(45deg);
}
.three-d {
  transform-style: preserve-3d;
}
.box {
  transform: rotateX(15deg) translateZ(20px);
  transform-origin: 0 0;
}
```

# Transitions & Animations

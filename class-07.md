# Domain Modeling

The process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain.

## Define a constructor and initialize properties

To define the same properties between many objects, you'll want to use a constructor function.

```javascript
var EpicFailVideo = function (epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
};

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);
```

This is object-oriented programming in JavaScript at its most fundamental level.

- The new keyword instantiates (i.e. creates) an object.
- The constructor function initializes properties inside that object using the this variable.
- The object is stored in a variable for later use.

# HTML Tables

The HTML tables allow to arrange data like text, images, links, other tables.

The HTML tables are created using the `<table>` tag in which the `<tr>` tag is used to create table rows and `<td>` tag is used to create data cells. The elements under `<td>` are regular and left aligned by default

```html
<table>
  <tr>
    <td>Row 1, Column 1</td>
    <td>Row 1, Column 2</td>
  </tr>

  <tr>
    <td>Row 2, Column 1</td>
    <td>Row 2, Column 2</td>
  </tr>
</table>
```

![img](assets/image17.png)

## Table Heading

Table heading can be defined using `<th>` tag.

```html
<table>
  <tr>
    <th>Name</th>
    <th>Salary</th>
  </tr>
  <tr>
    <td>Ramesh Raman</td>
    <td>5000</td>
  </tr>

  <tr>
    <td>Shabbir Hussein</td>
    <td>7000</td>
  </tr>
</table>
```

![img](assets/image18.png)

## Cell padding and Cell spacing Attributes

There are two attributes called cellpadding and cellspacing which you will use to adjust the white space in your table cells. The cellspacing attribute defines space between table cells, while cellpadding represents the distance between cell borders and the content within a cell.

````html
<table border="1" cellpadding="5" cellspacing="5">
  <tr>
    <th>Name</th>
    <th>Salary</th>
  </tr>
  <tr>
    <td>Ramesh Raman</td>
    <td>5000</td>
  </tr>
  <tr>
    <td>Shabbir Hussein</td>
    <td>7000</td>
  </tr>
</table>
```
````

## Colspan and Rowspan Attributes

You will use colspan attribute if you want to merge two or more columns into a single column. Similar way you will use rowspan if you want to merge two or more rows.

```html
<table border="1">
  <tr>
    <th>Column 1</th>
    <th>Column 2</th>
    <th>Column 3</th>
  </tr>
  <tr>
    <td rowspan="2">Row 1 Cell 1</td>
    <td>Row 1 Cell 2</td>
    <td>Row 1 Cell 3</td>
  </tr>
  <tr>
    <td>Row 2 Cell 2</td>
    <td>Row 2 Cell 3</td>
  </tr>
  <tr>
    <td colspan="3">Row 3 Cell 1</td>
  </tr>
</table>
```

## Table Header, Body, and Footer

The three elements for separating the head, body, and foot of a table are −

- `<thead>` − to create a separate table header.

- `<tbody>` − to indicate the main body of the table.

- `<tfoot>` − to create a separate table footer.

````html
<table border="1" width="100%">
  <thead>
    <tr>
      <td colspan="4">This is the head of the table</td>
    </tr>
  </thead>

  <tfoot>
    <tr>
      <td colspan="4">This is the foot of the table</td>
    </tr>
  </tfoot>

  <tbody>
    <tr>
      <td>Cell 1</td>
      <td>Cell 2</td>
      <td>Cell 3</td>
      <td>Cell 4</td>
    </tr>
  </tbody>
</table>
```
````

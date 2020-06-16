# Forms and JS Events

## HTML Forms

### What is HTML Form ?

HTML Form is a document which stores information of a user on a web server using interactive controls. An HTML form contains different kind of information such as username, password, contact number, email id etc.

The form tag is used to create an HTML form.

```html
<!DOCTYPE html>
<html>
  <body>
    <form>
      Username:<br />
      <input type="text" name="username" />
      <br />
      Email id:<br />
      <input type="text" name="email_id" />
      <br /><br />
      <input type="submit" value="Submit" />
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-13-at-9.52.09-PM.png)

### Text Field in HTML Forms :

The text field is a one line input field allowing the user to input text. Text Field input controls are created using the “input” element with a type attribute having value as “text”.

```html
<!DOCTYPE html>
<html>
  <h3>Example Of Text Field</h3>
  <body>
    <form>
      <label for="EMAIL ID">Email Id:</label><br />
      <input type="text" name="Email id" id="Email id" />
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-13-at-10.03.09-PM.png)

### Password Field in HTML Forms :

Password fields are a type of text field in which the text entered is masked using asterisk or dots for prevention of user identity from another person who is looking onto the screen. Password Field input controls are created using the “input” element with a type attribute having value as “password”.

```html
<!DOCTYPE html>
<html>
  <h3>Example of Password Field</h3>
  <body>
    <form>
      <label for="user-password">Password: </label><br />
      <input type="password" name="user-pwd" id="user-password" />
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-13-at-10.10.26-PM.png)

### Radio Buttons in HTML Form :

Radio Buttons are used to let the user select exactly one option from a list of predefined options. Radio Button input controls are created using the “input” element with a type attribute having value as “radio”.

```html
<!DOCTYPE html>
<html>
  <h3>Example of Radio Buttons</h3>
  <body>
    <form>
      SELECT GENDER
      <br />
      <input type="radio" name="gender" id="male" />
      <label for="male">Male</label><br />
      <input type="radio" name="gender" id="female" />
      <label for="female">Female</label>
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-14-at-3.08.52-AM.png)

### Checkboxes in HTML Form :

Checkboxes are used to let the user select one or more options from a pre-defined set of options. Checkbox input controls are created using the “input” element with a type attribute having value as “checkbox”.

```html
<!DOCTYPE html>
<html>
  <h3>Example of HTML Checkboxes</h3>
  <body>
    <form>
      <b>SELECT SUBJECTS</b>
      <br />
      <input type="checkbox" name="subject" id="maths" />
      <label for="maths">Maths</label>
      <input type="checkbox" name="subject" id="science" />
      <label for="sceince">Science</label>
      <input type="checkbox" name="subject" id="english" />
      <label for="english">English</label>
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-13-at-10.22.57-PM.png)

### File select boxes in HTML Forms :

File select boxes are used to allow the user to select a local file and send it as an attachment to the web server.It is similar to a text box with a button which allows the user to browse for a file.Instead of browsing for the file, the path and the name of the file can also be written. File select boxes are created using the “input” element with a type attribute having value as “file”.

```html
<!DOCTYPE html>
<html>
<h3>Example of a File Select Box</3>
    <body>
    <form>
        <label for="fileselect">Upload:</label>
        <input type="file" name="upload" id="fileselect">
    </form>
</body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-14-at-2.40.47-AM.png)

### Text area in an HTML Form :

Text Area is a multiple line text input control which allows user to provide a description or text in multiple lines. A Text Area input control is created using the “textarea” element.

```html
<!DOCTYPE html>
<html>
  <h3>Example of a Text Area Box</h3>
  <body>
    <form>
      <label for="Description">Description:</label>
      <textarea
        rows="5"
        cols="50"
        name="Description"
        id="Description"
      ></textarea>
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-14-at-2.52.37-AM.png)

### Select Boxes in HTML Forms :

Select boxes are used to allow users to select one or more than one option from a pull-down list of options. Select boxes are created using two elements which are “select” and “option”.List items are defined within the select element.

```html
<!DOCTYPE html>
<html>
  <h3>Example of a Select Box</h3>
  <body>
    <form>
      <label for="country">Country:</label>
      <select name="country" id="country">
        <option value="India">India</option>
        <option value="Sri Lanka">Sri Lanka</option>
        <option value="Australia">Australia</option>
      </select>
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-14-at-2.58.28-AM.png)

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-14-at-2.58.38-AM.png)

### Reset And Submit Buttons :

The Submit Button allows the user to send the form data to the web server. The Reset Button is used to reset the form data and use the default values.

```html
<!DOCTYPE html>
<html>
  <h3>Example of a Submit And Reset Button</h3>
  <body>
    <form action="test.php" method="post" id="users">
      <label for="username">Username:</label>
      <input type="text" name="username" id="Username" />
      <input type="submit" value="Submit" />
      <input type="reset" value="Reset" />
    </form>
  </body>
</html>
```

![image](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-12-14-at-3.05.00-AM.png)

The Action Attribute :
The action to be performed after the submission of the form is decided by the action attribute. Generally, the form data is sent to a webpage on the web server after the user clicks on the submit button.

```html
<!DOCTYPE html>
<html>
  <h3>Example of a Submit And Reset Button</h3>
  <body>
    <form action="test.php" method="post" id="users">
      <label for="username">Username:</label>
      <input type="text" name="username" id="Username" />
      <input type="submit" value="Submit" />
      <input type="reset" value="Reset" />
    </form>
  </body>
</html>
```

## List CSS

### Different List Item Markers

The list-style-type property specifies the type of list item marker.

The following example shows some of the available list item markers:

```css
ul.a {
  list-style-type: circle;
}

ul.b {
  list-style-type: square;
}

ol.c {
  list-style-type: upper-roman;
}

ol.d {
  list-style-type: lower-alpha;
}
```

![image](assets/image19)

### An Image as The List Item Marker

The list-style-image property specifies an image as the list item marker:

```css
ul {
  list-style-image: url('sqpurple.gif');
}
```
![image](assets/image20)


### Position The List Item Markers
The list-style-position property specifies the position of the list-item markers (bullet points).

"list-style-position: outside;" means that the bullet points will be outside the list item. The start of each line of a list item will be aligned vertically. This is default:

![image](assets/image21)

"list-style-position: inside;" means that the bullet points will be inside the list item. As it is part of the list item, it will be part of the text and push the text at the start:

![image](assets/image22)

### Table CSS


**width** 
to set the width of the table

**padding** 
to set the space between the border of each table cell and its content

**text-transform** 
to convert the content of the table headers to uppercase

**letter-spacing**, **font-size**
to add additional styling to the content of the table headers

**border-top**, **border-bottom**
to set borders above and below the table headers

**text-align** 
to align the writing to the left of some table cells and to the right of the others

**background-color** 
to change the background color of the alternating table rows

**:hover** 
to highlight a table row when a user's mouse goes over it

## Forms css

### Setting box-sizing
I usually set * {box-sizing:border-box;} not only for forms, but also webpages. When you set it, the width of all the elements will contain the padding.

For example, set the width and padding as follows.

```css
.some-class {
  width:200px;
  padding:20px;
}
```

### Padding
Adding some inner space to the input field can help improve clarity. You can accomplish this with the padding property.

```css
input[type=text] {
  padding: 10px;
}
```

![image](https://i0.wp.com/blog.logrocket.com/wp-content/uploads/2020/03/input-field-padding.png?resize=200%2C53&ssl=1)

### Margin
If there are other elements near your input field, you may want to add a margin around it to prevent clustering.

```css
input[type=text] {
  padding:10px;
  margin:10px 0; // add top and bottom margin
}
```

![image](https://i0.wp.com/blog.logrocket.com/wp-content/uploads/2020/03/input-field-margin.jpeg?w=700&ssl=1)


### Border
In most browsers, text input fields have borders, which you can customize.

```css
.border-customized-input {
   border: 2px solid #eee;
}
```
You can also remove a border altogether.

```css
.border-removed-input {
  border: 0;
}
```

### Box shadow

You can use the CSS box-shadow property to add a drop shadow. You can achieve a range of effects by playing around with the property’s five values.

```css
input[type=text] {
  padding:10px;
  border:0;
  box-shadow:0 0 15px 4px rgba(0,0,0,0.06);
}
```

![img](https://i2.wp.com/blog.logrocket.com/wp-content/uploads/2020/03/input-field-box-shadow.png?resize=251%2C142&ssl=1)

### Border radius

The border-radius property can have a massive impact on the feel of your forms. By curving the edges of the boxes, you can significantly alter the appearance of your input fields.

```css
.rounded-input {
  padding:10px;
  border-radius:10px;
}
```

![img](https://i0.wp.com/blog.logrocket.com/wp-content/uploads/2020/03/input-field-border-radius.png?w=356&ssl=1)
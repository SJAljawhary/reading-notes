## Why forms 
### Form controls
There are several types of form controls that we can use to collect information from visitors to our site.

1. Adding text :
- Text input (single-line).
- Password input.
- Text area (multi-line).

2. Making choices :
- Radio buttons.
- Checkboxes.
- Drop-down boxes.

3. Submitting forms :
- Submit buttons.
- Image buttons
- File upload

4. Uploading files .

### How forms work
1. A user fills in a form and then presses a button
to submit the information to the server.
2. The name of each form control is sent to the server along with the value the user enters or selects.
3. The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database.
4. The server creates a new page to send back to the browser based on the information received.

![form](https://fenorri.com/features/forms/form.png)

### Form structure
`<form>`
Form controls live inside a `form` element. This element should always carry the action attribute and will usually have a method and id attribute too.
1. action :Every `<form>` element requires an action attribute.
2. method :Forms can be sent using one of two methods: **get or post**:
The get method is ideal for:
* short forms (such as search boxes).
* when we are just retrieving data from the web server (not sending information that should be added to or deleted from a database).

We should use the post method if your form:
* allows users to upload a file.
* is very long.
* contains sensitive data (e.g. passwords).
* adds information to, or deletes information.

### Text input 
The input element is used to create several different form
controls. The value of the type attribute determines what kind
of input they will be creating :

* `type="text"`
When the type attribute has a value of text, it creates a singleline text input.

* `name`
The value of this attribute identifies the form control and is sent along with the information they enter to the server.

* `max length`
You can use the maxlength attribute to limit the number of characters a user may enter into the text field. Its value is the number of characters they may enter.


### Password input
`type="password"`
When the type attribute has a value of password it creates a text box that acts just like a single-line text input, except the characters are blocked out.

* `name`
The name attribute indicates the name of the password input which is sent to the server with the password the user enters.

* `size,maxlength`
It can also carry the size and maxlength attributes like the
the single-line text input.

### Text area
`<textarea>`
The `<textarea>` element is used to create a mutli-line text input. Unlike other input elements this is not an empty element. It should therefore have an opening and a closing tag.
Any text that appears between the opening `<textarea>` and
closing `</textarea>` tags will appear in the text box when the
page loads.

![text area](https://i.stack.imgur.com/9LsrC.png)

### Radio button
`type="radio"`
Radio buttons allow users to pick just one of a number of options.

* `name`
The name attribute is sent to the server with the value of the
option the user selects.

* `value`
The value attribute indicates the value that is sent to the
server for the selected option.

* `checked`
The checked attribute can be used to indicate which value (if
any) should be selected when the page loads. The value of this
attribute is checked.

### Checkbox
`type="checkbox"`
Checkboxes allow users to select (and unselect) one or more options in answer to a question.

* `name`
The name attribute is sent to the server with the value of the
option(s) the user selects.

* `value`
The value attribute indicates the value sent to the server if this checkbox is checked.

* `checked`
The checked attribute indicates that this box should be checked
when the page loads. If used, its value should be checked.

![checkbox](https://docs.devexpress.com/OfficeFileAPI/images/xtrarichedit_checkboxes133120.png)

### Drop Down List Box
A drop down list box (also known as a select box) allows users to select one option from a drop down list.

![drop down list box](https://developer.gnome.org/hig-book/unstable/images/controls-combo.png.en)

* `<select>`
The `<select>` element is used to create a drop down list box. It contains two or more `<option>` elements.

* `name`
The name attribute indicates the name of the form control being
sent to the server, along with the value the user selected.

* `<option>`
The `<option>` element is used to specify the options that the user can select from. The words between the opening `<option>`
and closing `</option>` tags will be shown to the user in the drop down box.

* `value`
The `<option>` element uses the value attribute to indicate the
value that is sent to the server along with the name of the control if this option is selected.

* `selected`
The selected attribute can be used to indicate the option that
should be selected when the page loads. The value of this attribute should be selected.

### Multiple Select Box
`<select>`

* `size`
We can turn a drop down select box into a box that shows more
than one option by adding the size attribute. Its value should
be the number of options we want to show at once.

* `multiple`
We can allow users to select multiple options from this list by
adding the multiple attribute with a value of multiple.

![Multiple select box](https://assets.hongkiat.com/uploads/multijs-select-menu-plugin/01-multijs-select-menu.jpg)

### File Input Box
`input`
`type="file"`
This type of input creates a box that looks like a text input
followed by a browse button.
When the user clicks on the browse button, a window opens up that allows them to select a file from their computer to be uploaded to the website.

![file input box](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT_VrR1U-OJ7BhbrnvPxuYHLp75KX64HFhGCYHuoftWHtZEvWtuUy9E1Tc9C2UrKoqcs28&usqp=CAU)

### Submit Button
`type="submit"`
The submit button is used to send a form to the server.

* `name`
It can use a name attribute but it does not need to have one.

* `value`
The value attribute is used to control the text that appears
on a button.

![submit button](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSH5WYKdZAHXaLYNmUDnneVbG93infqxjj4KA&usqp=CAU)

### Image Button
`type="image"`
If you want to use an image for the submit button, you can give
the type attribute a value of image.

![image button](https://puserbumi.radarcirebon.com/wp-content/uploads/sites/17/2021/01/cara-mendapatkan-subscribe.jpg)

### Button & hidden Controls
`<button>`
The `<button>` element was introduced to allow users more control over how their buttons appear, and to allow other
elements to appear inside the button.

* `type="hidden"`
They allow web page authors to add values to forms that users cannot see.

### Labelling Form Controls
`<label>`
When introducing form controls,the code was kept simple by
indicating the purpose of each one in text next to it.

![labelling form controls](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT0e4JP0M8ZSVCx5w-753LJvBM1KAGyi6uWA0asY_q8ftDVgNz0URGYd9Wwz07X8Ipp8iQ&usqp=CAU)

* `for`
The for attribute states which form control the label belongs to.
Note how the radio buttons use the id attribute. The value of the id attribute uniquely identifies an element from all other elements on a page.

### Grouping Form Elements
* `<fieldset>`
You can group related form controls together inside the
`<fieldset>` element. This is particularly helpful for longer
forms.

* `<legend>`
The `<legend>` element can come directly after the opening
`<fieldset>` tag and contains a caption which helps identify the purpose of that group of form controls.

### Form Validation
You have probably seen forms on the web that give users messages if the form control has not been filled in correctly.

![form validation](https://www.jeasyui.com/tutorial/form/images/form3.png)

### Date Input
`type="date"`
If we are asking the user for a date, we can use an `<input>`
element and give the type attribute a value of date.
This will create a date input in browsers that support the new
HMTL5 input types.

![data input](https://media.geeksforgeeks.org/wp-content/uploads/20200505122351/date12.png)

### Email & URL Input
`<input>`
HTML5 has also introduced inputs that allow visitors to enter email addresses and URLs. Browsers that do not support these input types will just treat them as text boxes.
`type="email"`
If we ask a user for an email address, we can use the email
input.
`type="url"`
A URL input can be used when we are asking a user for a web
page address.

### Search Input
`<input>`
`type="search"`
If we want to create a single line text box for search queries,
HTML5 provides a special search input.

![search](https://miro.medium.com/max/3200/0*zWsQzRdcIz9o_lTY)

`placeholder`
On any text input, we can also use an attribute called
placeholder whose value is text that will be shown in the text box until the user clicks in that area.


![placeholder](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZ3wXuxSSMrnsl9nYGRBaIU3qQon6qQENiUg&usqp=CAU)

## Bullet Point Styles
`list-style-type`
The list-style-type property allows us to control the shape
or style of a bullet point (also known as a **marker**).
It can be used on rules that apply to the `<ol>`, `<ul>`, and `<li>` elements.

![bullet](https://www.w3.org/wiki/images/5/5e/Referenc.gif)

## Images for Bullets
`list-style-image`
We can specify an image to act as a bullet point using the list-style-image property.

![images for bullets](https://www.all-ppt-templates.com/images/powerpoint-bullets-menu.jpg)

## Positioning the Marker
`list-style-position`
Lists are indented into the page by default and the list-styleposition property indicates whether the marker should
appear on the **inside** or the **outside** of the box containing the
main points.

## List Shorthand
`list-style`
It allows us to express the markers' style, image and position properties in any order.

## Table Properties
* `width` : to set the width of the table.
* `padding` to set the space between the border of each table
cell and its content.
* `text-transform` : to convert the content of the table headers to uppercase.
* `letter-spacing, font-size` : to add additional styling to the content of the table headers.
* `border-top, border-bottom` :  to set borders above and below
the table headers.
* `text-align` : to align the writing to the left of some table cells and to the right of the others.
* `background-color` : to change the background color of the
alternating table rows.
* `:hover` to highlight a table row when a user's mouse goes over it


## Border on Empty Cells
If we have empty cells in our table, then you can use the empty-cells property to specify whether or not their borders should be shown.

- It can take one of three values:
* `show` : This shows the borders of any empty cells.
* `hide` : This hides the borders of any empty cells.
* `inherit` :  If we have one table nested inside another, the inherit value instructs the table cells to obey the rules of the containing table.

![border on empty cells](https://media.geeksforgeeks.org/wp-content/uploads/emptycells3.png)

## Gaps Between Cells
`border-spacing, border-collapse`
Allows us to control the distance between adjacent cells.
It is possible to collapse adjacent borders to prevent this using the
border-collapse property.
- Possible values are:
* `collapse` :  Borders are collapsed into a single border where possible.
(border-spacing will be ignored and cells pushed together, and empty-cells
properties will be ignored.)

* `separate` :  Borders are detached from each other. (border-spacing and
empty-cells will be obeyed.)

![collasping](https://media.geeksforgeeks.org/wp-content/uploads/cell-spacing.png)

## Styling Forms
**CSS** is commonly used to control the appearance of form elements. This is both to make them *more attractive* and to make them *more consistent*
across different browsers.

* It is most common to style:
●● Text inputs and text areas.
●● Submit buttons.
●● Labels on forms, to get the form controls to align nicely.

## Styling Text Inputs
1. font-size .
2. color .
3. background color of the input.
4. border .
5. :focus pseudo-class .
6. :hover psuedo-class .
7. background-image .

## Styling submit buttons
* `color`: is used to change the color of the text on the button.
* `text-shadow`: can give a 3D look to the text in browsers that
support this property.
* `border-bottom`: has been used to make the bottom border of
the button slightly thicker,which gives it a more 3D feel.

* `background color`
* `:hover`

![submit](https://www.crushpixel.com/big-static15/preview4/hand-mouse-cursor-clicks-submit-2054328.jpg)

## Cursor styles
The cursor property allows us to control the type of mouse cursor that should be displayed to users.

Here are the most commonly used values for this property:
* auto
* crosshair
* default
* pointer
* move
* text
* wait
* help
* url("cursor.gif");

![cursor styles](https://i.stack.imgur.com/E76ws.png)

## Events
#### Different event types
Here is a selection of the events that occur in the browser while we are browsing the web.Any of these events can be used to trigger a function in our JavaScript code.

* `UI EVENTS`
Occur when a user interacts with the browser's user interface (UI) rather than the web page.
![ui events](https://slideplayer.com/slide/16279781/95/images/3/%28Some%29+Event+Types+UI+events+%E2%80%93+occur+when+a+user+interacts+with+the+browser%E2%80%99s+user+interface+%28UI%29+%E2%80%93+work+with+window+object..jpg)

* `KEYBOARD ENENTS`
Occur when a user interacts with the keyboard .
1. `keydown` : User first presses a key (repeats while key is depressed)
2. `keyup User`:User  releases a key
3. `keypress` : Character is being inserted (repeats while key is depressed)

* `MOUSE EVENTS`
Occur when a user interacts with a mouse. trackpad, or touchscreen.
![MOUSE EVENTS](http://3.bp.blogspot.com/-3WEzC9KCfVc/VMAUIdd_7TI/AAAAAAAAYgw/fS1CJ7894vg/s1600/javascript%2Bmouse%2Bevents%2Blist.png)

* `FOCUS EVENTA`
1. `focus / focusin`:Element gains focus
2. `blur / focusout`:Element loses focus

* `FORM EVENTS`
Occur when a user interacts with a form element.
1. `submit`: When a form is submitted, the submit event fires on the node representing the `<form>` element.
2. `change`: Fires when the status of several form elements change. For example, when:
• a selection is made from a drop-down select box.
• a radio button is selected.
• a checkbox is selected or deselected.
3. `input`: The input event is commonly used with `<input>` and `<textarea>` elements.

![form events](https://miro.medium.com/max/2648/1*q_PmjV-CMktSFK_f5JsNRw.png)

* `MUTATION EVENTS`
Occur when the DOM structure has been changed by a script.
1. `DOMSubtreeModified`Change has been made to document.
2. `DOMNodelnserted`:Node has been inserted as a direct child of another node.
3. `DOMNodeRemoved`:Node has been removed from another node.
4. `OOMNodelnsertedlntoDocument`:Node has been inserted as a descendant of another node.
5. `DOMNodeRemovedFromOocument`:Node has been removed as a descendant of another node.

#### How events trigger jAVASCRIPT code

When the user interacts with the HTML on a web page, there are three
steps involved in getting it to trigger some JavaScript code.
Together these steps are known as event handling.
1. Select the element node(s) we want the script to respond to.
2. Indicate which event on the selected node(s) will trigger the response.
3. State the code you want to run when the event occurs.

How event handling can be used to provide feedback to users filling in a registration form ??
1. Select element.
2. Specify event.
3. Call code.

#### Three ways to bind an eveny to an element
1. `HTML event handlers` : This method of event handling is no longer used because it is better to separate the JavaScript from the HTML.

     `element.onevent = functionName;`

2. `Traditional DOM event handlers` : They are considered better than
HTML event handlers because they let you separate the JavaScript from the HTML.
3. `DOM level 2 event listeners` : They are now the favored way of handling events.

     ` element .addEventlistener('event', functionName [, Boolean]) ;`

## Event Flow
HTML elements nest inside other elements.
When we hover a link , we will be also hovering on it's parent elements.
The event flow in two directions :
1. event bubbling
2. event capturing

![event flow](https://i.stack.imgur.com/1r40v.png)

### The event object
When an event occurs, the event object tells us information about the event, and the element it happened upon.

The event object also had different names for the properties and methods:
**Properties**
1. `target`:The target of the event (most specific element interacted with).
2. `type`:Type of event that was fired.
3. `cancelable`:Whether we can cancel the default behavior of an element.

**Methods**
1. `preventOefault()` : Cancel default behavior of the event (if it can be canceled).
2. `stopPropagation()`: Stops the event from bubbling or capturing any further.

### Event Delegation
Benifits of event delegation :
1. Works with new elements.
2. Solves limitations with this keyword.
3. Simplifies our code.

### Changing default behaviour
The event object has methods that change the default behavior of an element and how the element's ancestors respond to the event :
1. `preventDefau1t ()`
2. `stopPropagation()`

### The this keyword
The this keyword refers to the owner of a function. this refers to the element that the event is on.
This works when no parameters are being passed to the function
(and therefore it is not called from an anonymous function).





     

    







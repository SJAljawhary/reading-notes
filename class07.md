# HTML Tables 
#### What's a table ?

It's an arrangement of data in rows and columns, or possibly in a more complex structure. Tables are widely used in communication, research, and data analysis. Tables appear in print media, handwritten notes, computer software, architectural ornamentation, traffic signs, and many other place


* Each block in the grid is referred to as a table cell.
* In HTML a table is written out row by row.

![tables](https://emedia.rmit.edu.au/learninglab/sites/default/files/reports_tables2.png)

#### Basic table structure

1. `table` : this element is used to create a table. The contents of the table are written out **row
by row**.
2. `tr` : this element stands for table row, and It is followed by one or more `td` elements (one for each cell
in that row).
3. `td` : Each cell of a table is represented using a `td`
element, It stands for table data.

![table structure](https://www.oreilly.com/library/view/web-design-in/1565925157/tagoreillycom20070306oreillyimages157933.png)

#### Table headings
`th` : this element is used just like the `td` element but its purpose is to represent the heading for either a column or a row.

#### Spanning columns
Sometimes we may need the entries in a table to stretch across more than one column.
The **colspan attribute** can be used on a <th> or <td> element
and indicates how many columns that cell should run across.
#### Spanning rows
We may also need entries in a table to stretch down across
more than one row.
The **rowspan attribute** can be used on a <th> or <td> element to indicate how many rows a cell should span down the table.

![spanning columns](https://flylib.com/books/2/631/1/html/2/images/08fig19.jpg)

#### Long tables
These three elements help distinguish between the main content of the table and the first and last rows .
1. `thead` : The headings of the table should sit inside it.
2. `tbody` : The body should sit inside it.
3. `tfoot` : The footer belongs inside it.

![long table](https://www.positronx.io/wp-content/uploads/2020/04/vue-table-9530-04.png)

#### Old Code:
##### Width & Spacing
* The **width attribute** is used on the opening `table` tag to
indicate how wide that table should be.
* And on some opening `th` and `td` tags to specify the width of individual cells.
* The opening `table` tag could also use the **cellpadding attribute** to add space inside each cell of the table, and the
**cellspacing attribute** to create space between each cell of
the table.

##### Border & Background
* The **border attribute** was used on both the `table` and `td`
elements to indicate the width of the border in pixels.
* The **background-color** attribute was used to indicate background colors of either the entire table or individual table cells.

# JS Constructor Functions
### Creating an object 
#### Constructor Notation
The object constructor and the new keyword create a blank object,which then we can add properties and methods to it.

##### First step
Using the **new** word and the **()** constructor function combination to create a new object.

##### Second step
Using the **dot notation** to add properties and methods to this object .

```

let store = new object ();
    locName: 'Seattle',
    minCustperHr: 23,
    maxCustperHr: 65,
    avgCookies: 6.3,

```

#### Updating an object'
To update the value of the properties :
1. using the dot notation:`store.name = 'Seattle';`
2. using the square brackets:`store['store'] = 'Seattle';`
3. we can delete a property using delete keyword:`delete store.name;`

### Creating many objects
#### Constructor Notation
Sometimes we want several objects to represent similar things.
Object constructors can use a function as a template for creating objects.
##### First step
Create the template with the object's properties and methods.
 
```

function store(locName,minCustperHr,maxCustperHr){
    this.locName = 'Seattle',
    this.minCustperHr = 23,
    this.maxCustperHr = 65,
}

```

* The **this keyword** is used instead of the object name to indicate that the property or method belongs to the object that this function creates.
* The **name of a constructor function** usually begins with a **capital letter**.
* Each statement that creates a new property or method for this object **ends in a semicolon**.


#### Creating objects using constructor syntax

When an object is created using theconstructor function ,properties and methods are then assigned to the object.
To access a property of this object, we can use dot notation,
just as we can with any object.

#### A function in global scope

When a function is created **at the top level of a script**
(which is, not inside another object or function), then it
is in the **global scope** or global context.

#### A Method of an object

When a function is defined inside an object, it
becomes a method. In a method, this refers to the
containing object.

#### Function expression as method

If a named function has been defined in global scope, and it is then used as a method of an object, this refers to the object it is contained within.

### Storing data

In JavaScript, data is represented using name/value pairs:
1. Variables :
* A variable has just one key (the variable name
and one value).
* Variable names are separated from their value by an
equals sign :
`var locName = 'Seattle' ;`

2. Arrays : 
* Arrays can store multiple pieces of information.
* Each piece of information is separated by a comma.
* The order of the values is important because items in an array are assigned a number (called an index) :
`var locName = ['Seattle','35','50']`
* Arrays are an objects.

### Individual objects
Objects store sets of name/value pairs. They can be properties (variables) or methods (functions).

```

var store = {
name: ' Tokyo',
capacity: 40
};

``` 

### Multiple objects
When we need to create multiple objects within the same page, we should use an object constructor to provide a template for the objects.

```

function Hotel (name, capacity)
this .name = name;
this.capacity = capacity;

``` 

* Advanteges of literal function :
- When we are storing / transmitting data between applications.
- For global or configuration objects that set up information for the page.

* Advanteges of constructor function :
-  We have lots of objects used with similar functionality within a page.
- A complex object might not be used in code.

### What are built-in objects ?
Browsers come with a set of built-in objects that represent things like the browser window and the web page shown in that window. These built-in objects act like a toolkit for creating interactive web pages.

![built-in objects](https://wethegeek.com/wp-content/uploads/2019/07/firefox-1024x507.jpg)

#### The toolkit has three compartments: 
1. Browser object model.
2. Document object model.
3. Global javascript objects.

#### What is an object model ?
We have seen that an object can be used to create a
model of something from the real world using data.
An object model is a group of objects, each of which represent related things from the real world.
Together they form a model of something larger.








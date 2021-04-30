# Text

## Headings
HTML has six "levels" of headings:
`h1` is used for main headings.
`h2` is used for subheadings.
If there are further sections under the subheadings then the
`h3` element is used, and so on...

![headings](https://www.tutorialrepublic.com/lib/images/html/html-headings.png)

## Paragraphs
To create a paragraph, surround the words that make up the paragraph with an opening `p`
tag and closing `/p` tag.

### Bold and Italic
By enclosing words in the tags `b` and `/b` we can make characters appear **bold**.

By enclosing words in the tags `i` and `/i` we can make characters appear *italic*.

## Superscript and Subscript
1. superscript :The `sup` element is used
to contain characters that should be superscript like raising a number to a power 5^2.
2. subscript :The `sub` element is used to contain characters that should be subscript. It is commonly used with chemical formulas such as H20.

## Line breaks and horizantal rules
If we wanted to add a line break inside the
middle of a paragraph you can use the line break tag `br /`.
![line break](https://static.javatpoint.com/htmlpages/images/html-br-tag2.png)

To create a break between themes we can add a
horizontal rule between sections using the `hr /` tag.

![horizantal rules](https://www.w3docs.com/uploads/media/default/0001/01/0c46c334f0f566736856790f751c5a29799a6734.png)

## Visual editors & their code views
HTML editors such as *Dreamweaver* usually have two views of the page we are creating: a **visual editor** and a **code view**.

![visual editor](https://make.wordpress.org/support/files/2009/08/WordPress-TinyMCE-overview.gif)


## Strong and Emphasis 
* The use of the `strong` element indicates that its content has strong importance, and it will be shown in **bold**.

* The `em` element indicates emphasis that subtly changes the meaning of a sentence, and it will be shown in *Italic*. 

## Quotations
To marking up quotations , There are two elements:
1. `blockquote` : used for longer quotes.

2. `q` : used for shorter qoutes.

## Abbreviations & Acronyms
`abbr` is used when we use abbreviation or
an acronym, A title attribute on the opening tag is used to specify the full term:
* Example :
`<abbr title="Professor">Prof</abbr>`

## Citations & Definitions
#### Cite
When we are referencing a piece of work such as a book or research paper, the `cite` element can be used to indicate where the citation is
from.

#### Dfn
The `dfn` element is used to indicate the defining instance of a new term.

## Author Details
The `address` element is used to contain contact details for the author of the page.
* Example :

```
<address>
<p><a href="mailto:homer@example.org">
homer@example.org</a></p>
<p>742 Evergreen Terrace, Springfield.</p>
</address>
```

## Changes to Content
1. #### `del` and `ins`

The `ins` element can be used to show content that has been inserted into a document, while
the `del` element can show text that has been deleted from it.
* Example :

```
<p>It was the <del>worst</del> <ins>best</ins> idea she had ever had.</p>
```

2. #### `s`
The `s` element indicates something that is no longer accurate or relevant (but that
should not be deleted).

## Block & inline elements
Block elements look like they start on a new line "shown in black in the bellow image", but Inline elements flow within the text and do not start on a new line"shown in red in the image" :

![block and inline elements](https://i.stack.imgur.com/dVPHz.png)
## CSS
CSS allows us to create rules that control the
way that each individual box (and the contents
of that box) is presented.

Using the css we can style our page elements like:
1. *Boxes* :
* Width and height
* Borders (color, width, and style)
* Background color and images
* Position in the browser window.
2. *Text* :
* Typeface
* Size
* Color
* Italics, bold, uppercase,
* lowercase, small-caps

### CSS Associates Style rules with HTML elements
A CSS rule contains two parts: a **selector** and a **declaration**.
See this example where `p` is the selector which indicate which element the rule applies to, and `font-family:Arial` is the declaration which indicate how the elements referred to in the selector should be styled:


```
p {
font-family: Arial;}
``` 


The declaration is consists of two parts :
1. *property*
2. *value*


``` h1, h2, h3 {
font-family: Arial;
color: yellow;} 
```


### Using External CSS
The `link` element can be used in an HTML document to tell the browser where to find the CSS
file used to style the page, this link uses three attributes :
1. href :specifies the path to the CSS file (which is often placed in a folder called css or styles).
2. type :specifies the type of document being linked to. The value should be text/css.
3. rel :specifies the relationship between the HTML page and the file it is linked to.

When building a site with more than one page, we should use an external CSS style sheet.

### Using Internal CSS
The CSS rules can be included within HTML page by placing them inside a `style` element, which usually sits inside the `head` element of the page.


```
<style type="text/css">
body {
font-family: arial;
background-color: rgb(185,179,175);}
h1 {
color: rgb(255,255,255);}
</style>
```


![css selectors](https://image.slidesharecdn.com/mark-csssyntaxselector-140213211343-phpapp01/95/mark-css-syntax-selector-3-638.jpg?cb=1392326713)

Different types of selectors allow us to target our rules at different elements.

## Statements

A script is a series of instructions that a computer can follow one-by-one.
Each individual instruction or step is known as a statement it should end with a semicolon and take place between the curly braces.

### JAVASCRIPT IS CASE SENSITIVE
JavaScript is case sensitive so **hourNow** means
something different to **HourNow** or **HOURNOW**.

## Comments
We write comments to explain what our code does.
They help make it easier to read and understand.

* `//` is used for a single line.
* `/*  */` is used for multi lines.

## What is a variable ?
Variables is used to save the bits of information it needs to do its job inside them.
Why it's called  variables ?
Because the data stored in a variable can change (or vary) each time a script runs.

* Declaring the variables and give them values :

 ``` var age = 3 ; ```

## Data Types
There are three data types in javascript :
1. ***Numbers*** :integers , negative and decimal numbers can be contained :`0.56` , `-456` , `50`
2. ***String*** :consists of letters and other characters: ` 'Welcome here !'`
3. ***Boolean*** :can have one of two values: `true` or `false`.

So we use the variables to store these data types inside it.

When declaring a variable in JavaScript,we do not need to specify what type of data it will hold.

### Shorthand for creating variables
1. Variables are declared and values assigned in the same statement:


```
var price = 5;
var quantity = 14;
var total = price * quantity;
```


2. Three variables are declared on the same line, then values assigned to each :


```
var price, quantity, total ;
price = 5;
quanti ty = 14;
total = price * quantity;
```


3. Two variables are declared and assigned values on the same line. Then one is declared and assigned a value on the next line :


```
var price
var total
5, quantity = 14;
price * quantity;
```


### Rules for naming variables
1. The name *must begin* with a **letter**, **dollar sign ($)**,or an **underscore (_)**, It must not start with a number.
2. The name can contain letters, numbers, dollar sign ($), or anunderscore (_). Note that we **must not use** a **dash(-)** or a **period (.)** in a variable name.
3. We cannot use keywords or reserved words like **var** for example.
4. All variables are case sensitive, so **score** and **Score** would be different variable names.
5. Use a name that describes the kind of information that the variable stores.
6. If the variable name is made up of more than one word, use a capital letter for the first letter of every word after the first word,
* For example: `firstName` .

### Arrays
It's a special type of variable,It doesn't
just store one value; it stores a list of values.

We create an array and give it a name just like we would any other variable (using the var
keyword followed by the name of the array).

The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. 

The values in the array do not need to be the same data type, so we can store a string, a number and a Boolean all in the same array.

![arrays](https://htpwj-zone1-rrzzqutxbqkmxn.netdna-ssl.com/wp-content/uploads/2015/07/arrays_in_javascript.gif)


#### Values in arrays
The list inside an array starts at zero (not one),which called **index**,which can be used to access specific items in the array.


``` 
var col ors;
colors= ['white ' ,
'black ' ,
' custom'];
``` 

here each index and it's value is shown like :
|Index|value|
|-----|-----|
|  0  |white|
|  1  |black|
|  2  |custom|

To access the third item for example :


```
var thirdItem ;
thirdItem = colors[2];
``` 

The number of items inside the array indicates it's length :


``` var numColors ;
numColors =colors. length;
```


### Expressions
There are two types of expressions:
1. Expression that just assign a value to a variable:
`var color = 'beige';`
2. Expressions that use two or more variables to return a single value:
`var area = 3 * 2;`

## Operators
They allow programmers to create a single value from one or more values.
 ![operators](https://i0.wp.com/makemeanalyst.com/wp-content/uploads/2017/06/Relational-Operators-in-Python.png?resize=508%2C305)

 #### Aithmetic operators
 
 ![arithmatic operators](https://2.bp.blogspot.com/-Aa3I3yOraos/W8LSLWl3Q5I/AAAAAAAAESw/RJugarKq2mQn0zb8BXB6cYHtKOjYXoAEgCLcBGAs/w1200-h630-p-k-no-nu/arithmatic-operators.PNG)

#### String operators
Joining together two or more strings to create one
new string **concatenation** :


```
var firstName = 'Alma ' ;
var lastName = ' John' ;
var full Name = firstName + lastName;
```


#### Mixing strings and numbers together
* Example(1) :


```
var cost l = '5';
var cost2 = '6 ' ;
var total = costl + cost2 ;
The result here is : '56'
```


* Example(2) :


```
var number = 15;
var street= 'John Road';
var add = number + street;
The result here is : '15John'
```


* Example(3):


```
var score= ' seven ';
var score2 = ' nine';
var total = score * score2;
The result here is **NAN**
```


## Decisions and loops
![decision](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2011/09/Basic-Flowchart-Template-with-one-decision-.png)

The decision have two components :
1. the evaluated expression which return a value.
2. a conditional statement says what to do in a given situation.

![condition](https://cdn.programiz.com/sites/tutorial2program/files/cpp-if-else-working.png)

#### Comparison operators 
Use them to evaluate the condition :
* == or !=: comparing the value
* === or !== : comparing both the value and the type.
* < or >
* <= or >=

` score >= pass ` for example .
#### Logical operators

![logical operators](http://4.bp.blogspot.com/-1QctoBEAAPA/UflqwEoXNLI/AAAAAAAAEFs/2-GkdOprLLI/s1600/Logical+Operators+in+Java.jpg)

## IF statement
To check a condition , if it's true , the statement in the code block will executed.


```
if (score >= 50){
    congratulate();
}
``` 


## If..else statement
To check a condition , if it's true the first code block is executed, and if it's false the code in the second block is executed.


```
if (score >= 50){
    congratulate();
}else{
    encourage();
}
```



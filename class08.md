# Layout

### Key Concepts in Positioning Elements

1. Building Blocks : Each HTML element is consireded as if it's in its own box. This box will either be :
* a block-level box :start on a new line, Examples :`h1` `p` `ul` `li` .

* an inline box : flow in between,surrounding text Examples : `img` `b` `i` .

2. Containing Elements : When one block-level element sitsinside another block-level element then the outer box isknown as the **containing or parent element**.

![block & inline](http://www.gsis.kumamoto-u.ac.jp/opencourses_en/ipf/10/images/box-08_English.png)

### Controlling the Position of Elements

CSS has these following positioning schemes that allow you to control the layout of a page: 
* normal flow : Every block-level element
appears on a new line, which causes each item to appear lower down the page than the previous one.

* relative positioning : This moves an element from the position it would be in normal flow, shifting it to the top, right,bottom, or left of where it would have been placed.

* absolute positioning : This positions the element
in relation to it's containing element.

To indicate where a box should be positioned, we also need to use **box offset** properties to tell the browser how far from the top or bottom and left or right it should be placed.

#### Fixed Positioning :
This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element.
#### Floating Elements
Floating an element allows us to take that element out of normal flow and position it to the far left or right of a containing box.

## Normal flow
##### position:static
In normal flow, each block-level element sits on top of the next one.
## Relative Positioning
##### position:relative
Relative positioning moves an element in relation to where it would have been in normal flow.

##### Absolute Positioning
When the position property is given a value of absolute,the box is taken out of normal flow and no longer affects the position of other elements on
the page.

## Fixed Positioning
##### position:fixed
Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed.

## Floating Elements
##### float
The float property allows us to take an element in normal flow and place it as far to the left or right of the containing element as possible.
We use this property to place elements **side-by-side**.

## Clearing Floats
##### clear
The clear property allows us to say that no element (within the same containing element) should touch the left or righthand sides of a box. It can take the following values:
1. left.
2. right.
3. both.
4. none.

#### Creating Multi-Column
##### Layouts with Floats
This is achieved by using a `div` element to represent each column,these three CSS properties are used to position the columns next to each other:
1. width.
2. float.
3. margin.

## Screen Sizes
Different visitors to our site will have different sized screens that show different amounts of information, so our design needs to be able to
work on a range of different sized screens.

![screen sizes](http://www.zazzlemedia.co.uk/wp-content/uploads/2015/10/device-sizes.png)

## Screen Resolution
Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.

## Page Sizes
Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide.

## Fixed Width Layouts
Fixed width layout designs do not change size as the
user increases or decreases the size of their browser window.

## Liquid Layouts
Designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.

 
## Layout grids
The grid structure is used to help the designers to position items on a page :

![layout grids](https://visme.co/blog/wp-content/uploads/2018/03/How-Grids-Can-Help-You-Create-Professional-Looking-Designs-Symmetrical-Modular-Grid.png)

* Creates a continuity between different pages which may use different designs.
* Helps users predict where to find information on various pages.

* Makes it easier to add new
content to the site in a
consistent way.

* Helps people collaborate
on the design of a site in a
consistent way.

### Possible Layouts:
960 Pixel wide
12 Column Grid

![960 pixel wide](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTxhp53CqyONIh1bSExGaCHYhjbCSjEmOnWJg&usqp=CAU)

Here each column has a margin set to 10 px, which creates a gap of 20 px between each column and 10 px to the left and right sides of the page.

## CSS fameworks

CSS framworks is very useful in providing the code for common tasks, such as creating layout grids, styling forms, and so on.


* Advantges :
1. Avoid the repeatedly writing code for the same tasks.
2. Avoid browser bugs.

* Disadvantges :
1. The claa names in our HTML code is required  so that it's only control the presentation of the page not describe it's content.
2. They often contain more code than we need for our particular web page .

![css framework](https://groundworkcss.github.io/groundwork/images/layout-a.png)

After the layout and the columns and spaces between them is ready now the only rules
we needed to add are shown on
this page.

 The rules:
* Control the font and the position of the text in the boxes.
* Set the background colors for the boxes.
* Set the height of the feature and article boxes.
* Add a margin to the top and bottom of each box.


## Multiple style sheets
To include multiple CSS files in one page using :
1. import :  HTML page can link to one style sheet and that stylesheet can use the **@import**
rule to import other style sheets.


2. link : In HTML we can use a separate **link** between the head element for each style sheet.







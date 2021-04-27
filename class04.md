# Links
links created bu using `a`element which contains the **href** attribute to specify the page we want to link it with our main page.

## Directory structure
We can organize the **structure** of our code files using a folder for each different section. The family tree describes the **relationship** between these files and folders. 
The **homepage** is written in HTML and called **index.html**.

![family tree](https://stuyhsdesign.files.wordpress.com/2015/09/directory-structure1.png?w=656)

## Relative URLS
If all of the files in our site are in one folder, we use the file name for that page to give the relative URL for it.

## Email links

We use `mailto` to create a link that contains the user's email program and addresses an email to a specified email address, we use the `a`
element:

`<a href="mailto:sondos@example.org">Email sondos</a>`

### Opening links in a new window
We use `target` to open the link in a new window:

`<a href="http://www.google.com" target="_blank">
Google</a> (opens in new window)` :

Google(opens in new window)

## A liquid layout
To specify the width of each box so that the design will stretch to fit the size of the
screen.
 
## Layout grids
The grid structure is used to help the designers to position items on a page :

![layout grids](https://visme.co/blog/wp-content/uploads/2018/03/How-Grids-Can-Help-You-Create-Professional-Looking-Designs-Symmetrical-Modular-Grid.png)

* Creates a continuity between different pages which may use different designs.
* Helps users predict where to find information on various pages.

## Multiple style sheets
To include multiple CSS files in one page using :
1. import .
2. link.

# Functions,methods and objects

### what is a function ?
If we want to group a series of statements together to do a specific task we can use functions :

![function](https://i.stack.imgur.com/5XzX8.png)

#### Declaring the function
We can declare it by write it's name and then write the statment which we want to specify a task between the curly bruckets :

`function sum(){document.write(num1+num2)};`

#### Calling the function
the function name  will call the function:
`sum();`

To get a single value like when we do a summation operation , we can return the value in a declared variable :
`var sum = num1 + num2`
`return sum;`
Also we can return more than one value using an array:
`var sum= num1 + num2`
`var multiply= num1 * num2`
`var results = [sum , multiply];`
`return results;`

#### Variable scope
The location where we declare the variable will affect where it can be used within our code.
When we create the variable in a spasific function we can use it only inside this function which this called **local variables** .
To use this variable in other place not just in this function we should declare it outsite the finction , and here it's called **global variable**.

**Global variables** use more memory because the browser has to remember them for as long as the web page using them is loaded. **Local variables** are only remembered during the period of time that a function is being executed.

## Why pair program ?

![pair programming](https://martinfowler.com/articles/on-pair-programming/driver_navigator.png) 

1. Greater efficiency.
2. Engaged collaboration.
3. Learning from fellow students
4. Social skills.
5. Job interview readiness
6.  Work environment readiness.




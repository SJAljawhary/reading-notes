# What is an object ?
![objects](https://pbs.twimg.com/media/EUxbHTtWoAAXPp9.jpg)

Group together a set of variables and functions to create a model of a something we would recognize from the real world. In an object, variables and functions take on new names.
* The variables in an object called **"properties"**, properties give us more information about this object like it's name and how many specific things it has for example.

* The functions in an object called **"Methods"**, methods represent tasks that are associated with the object .

![object](https://raw.githubusercontent.com/ATL-WDI-Curriculum/js-objects-and-json/master/images/object-property-method.jpg)

Programmers use a lot of name/value pairs:
• HTML : uses attribute names and values.

• CSS : uses property names and values.

• JS :
* variables have a name and you can assign them a value of a string, number, or Boolean.
* Arrays have a name and a group of values. (Each item in an array is a name/value pair).
* Named functions have a name and value that is a set of statements to run if the function is called.

## Creating an object
### (Literal Notation)


```
var hotel ={
    name : 'December',
    rooms : 50,
    booked : 34,
    checkAvailabitiy : function(){
        return this.rooms - this.booked;
    }
};
```

#### Accessing an object 
The dot notation is used to access the properties or methods of an object,square brackets are used also to access properties.

` var carModel = car.model ;`
or ` var carModel = car['model'];`

If we have two objects on the same page, we would create each one using the same notation but store them in variables with different names.

## Document Object Model (DOM)
It's a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document.

It covers two primary areas :
1. Making a model of the HTML page.
2. Accessing and changing the HTML PAGE.

The DOM is called an object model because the model **(the DOM tree)** is made of objects.

![DOM tree](https://www.researchgate.net/profile/Jian-Chang-8/publication/254002847/figure/fig1/AS:298235726974978@1448116346303/Example-of-DOM-Node-Tree.png)

DOM also defines methods and properties to access and update each object in this model, which in turn updates what the user sees in the browser.

**APIs** let programs (and scripts) talk to each other. 

**DOM tree** cosists of four main types of nodes, and every element, attribute, and piece of text in the HTML is represented by its own *DOM node* :

1. The document node: at the top of the tree a document node is added,it represents the entire page.

2. Element nodes: describe the structure of an HTML page. (The `<h1> - <h6>` elements describe whatm parts are headings.

3. Attribute nodes: The opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree.

4. Text nodes: When we access an element node, we
can then reach the text within that element. This is stored in it's own text node.

#### Working with the DOM tree
* ***Step(1)*** :access the elements
- select an individual element node using these three ways :
1. getElementById() : 
Selects an individual element given the value of it's id attribute.
The HTML must have an id attribute in order for it to be selectable. 

2. querySelector() : 
Uses CSS selector syntax that would select one or more elements.

3. move from one element node to a related element node:
  - parentNode
  - previousSibling / nextSibling
  - firstChild / lastChild

- select multiple elements using these three ways: 
1. getElementsByClassName() : 
Selects one or more elements given the value of their class attribute.
The HTML must have a class attribute for it to be selectable.

2. getElementsByTagName() :
Selects all elements on the page with the specified tag name.

3. querySelectorAll() :
Uses CSS selector syntax to select one or more elements and returns all of those that match.

* ***Step(2)*** :work with those elements
1. access/update text nodes.
2. work with HTML content.
3. access or update attribute values

### Caching DOM queries
To find elements in the DOM tree we use methods called DOM queries:
* When an element is selected to access or update , the interpreter should find this element in the DOM tree.
* when the node which represents this element is found , we can work with it , it's parent or any child.
* If our script needs to use the same element more than once, we can store the location of the elements in a variable ,so this saves the browser from looking through the DOM tree again to find the element which this is called **"caching the selection"**.

### Accessing elements
Sometimes we want to access an individual element and other times we want to access a group of elements.



## Nodelists :
When a DOM method can return more than one element, it returns a **Nodelist** which is a collection of element nodes,eaach node is given an index number.

Nodelists look like arrays and are numbered like
arrays, but they are not actually arrays; they are a type of object called a *collection*.

* In a **live Nodelist**, when our script updates the page, the Nodelist is updated at the same time.
* In a **static Nodelist** when our script updates the page, the NodeList is not updated to reflect the changes made by the script.

#### selecting an element from a nodelist
1. The item() method.
2. Array syntaxm, which is faster than the first method.


#### Looping through a nodelist
If we want to apply the same code to numerous elements, looping through a Nodelist is a powerful technique.

## Traversing the DOM
When we have an element node, we can select another element in relation to it using these five
properties:
1. parentNode
2. previousSibling
3. nextSibling
4. firstChild
5. lastChild

### jQuery
Most browsers,treat whitespace between elements, and we should strip all the whitespace out of a page before serving it to the browser,one of the most popular ways to address this kind of problem is to use a JavaScript library such
as jQuery,


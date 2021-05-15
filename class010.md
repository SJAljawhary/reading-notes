## Error handling and debugging

We will learn how to find the errors in our code ,it will also teach us how
to write scripts that deal with potential errors gracefully.

### Order of Execution
To find the source of an error, it helps to know how scripts are processed.
The order in which statements are executed can be complex.

### Execution Contexts
Every statement in a script lives in one of three execution contexts:
1. `Global Context` : Code that is in the script, but not in a function.
There is only one global context in any page.

2. `Function Context` : Code that is being run within a function.
Each function has its own function context.

3. `Eval Context (not shown)` : Text is executed like code in an internal function
called eval().

### Variable Scope
* Global Scope : If a variable is declared outside a function, it can
be used anywhere because it has global scope.
If we do not use the var keyword when creating a variable, it is placed in global scope.

* Function-level Scope : When a variable is declared within a function, it can only be used within that function. This is because it has function-level scope.

### The Stack
The javascript interpreter processes one line of codeat a time,when a statement nedds data from another function,it stacks the new function on top of the current task.

### Execution Context $ Hoisting
Each time a script enters a new execution context, there are two phases of activity:
1. `Prepare` : 
• The new scope is created.
• Variables, functions, and arguments are created.
• The value of the this keyword is determined.

2. `Execute` :
• Now it can assign values to variables.
• Reference functions and run their code.
• Execute statements.

### Understanding Scope
In the interpreter, each execution context has its own variables object.
It holds the variables, functions, and parameters available within it.
Each execution context can also access its parent's variables object.

Functions in JavaScript are said to have lexical scope.
They are linked to the object they were defined within.
So, for each execution context, the scope is the
current execution context's variables object, plus the
variables object for each parent execution context.

### Understanding Errors
If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handling code.

If we are anticipating that something in our code may cause an error, you can use a set of statements to handle the error .
This is important because if the error is not handled, the script will just stop processing and the user will not know why. So exception-handling code should
inform users when there is a problem.

### Error Objects
Error objects can help us find where your mistakes are and browsers have tools to help us read them.

When an Error object is created, it will contain the following properties:
1. `name` : Type of execution
2. `message` : Description
3. `fileNumber` : Name of the JavaScript file
4. `lineNumber` : Line number of error

There are seven types of built-in error objects in JavaScript :
1. `Error`.

2. `SyntaxError`: SYNTAX IS NOT CORRECT
This is caused by incorrect use of the rules of the language. It is often the result of a simple typo :
**MISMATCHING OR UNCLOSED QUOTES**
document .write ("Howdyl );
SyntaxError: Unexp ec t ed EOF
**MISSING CLOSING BRACKET**
document .getElementByid('page' I
SyntaxErr or : Expected token ' ) '
**MISSING COMMA IN ARRAY**
Would be same for missing] at the end
var l ist = ['Item 1', 'Item 2 ' l 'rtem 3'];
SyntaxError: Expected token ']'

3. `ReferenceError`:VARIABLE DOES NOT EXIST
This is caused by a variable that is not declared or is out of scope:
**VARIABLE IS UNDECLARED**
var wi dth = 12 ;
var area = width * height ;
ReferenceError: Can't find variable:
height
**NAMED FUNCTION IS UNDEFINED**
document.write ( randomFunction() ) ;
ReferenceError: Can't find variable :
randomFunction

4. `TypeError`.
5. `RangeError`.
6. `URI Error`: INCORRECT USE OF URI FUNCTIONS
If these characters are not escaped in URls, they will cause an error: / ? & I : ;
**CHARACTERS ARE NOT ESCAPED**
decodeURI('http: //bbc . com/ news . phplla=l') ;
URlError: URI error

7. `EvalError`.

### How To Deal With Errors
Now that we know what an error is and how the browser treats them, there are two things we can do with the errors.
1. Debug the script to fix errors.
2. Handle errors gracefully.

### A debugging Workflow
Debugging is about deduction: eliminating potential causes of an error.

Where is the problem ?
First, should try to can narrow down the area where
the problem seems to be. In a long script, this is
especially important.
1. Look at the error message, it tells you:
• The relevant script that caused the problem.
• The line number where it became a problem for
the interpreter. (As you will see, the cause of
the error may be earlier in a script; but this is the
point at which the script could not continue.)
• The type of error (although the underlying cause
of the error may be different).
2. Check how far the script is running.
Use tools to write messages to the console to tell
how far your script has executed.
3. Use breakpoints where things are going wrong.
They let you pause execution and inspect the va lues
that are stored in variables.

### Browser DEV Tools & Javascript Console

The JavaScript console will tell us when there is a problem with a script,where to look for the problem, and what kind of issue it seems to be.
The JavaScript console is just one of severa l developer tools that are found in all modern browsers.

When we are debugging errors, it can help if we look at the error in more than one browser as they can show us different error messages.
If we open the errors . html file from t he sample code in our browser, and then open the console, we will see an error is displayed.

The console is exsist in many browsers such us **Chrome** , **Firefox** , **Internet Explorer**, we will talk about how to use it to look at errors inside them.

##### How to look at errors in chrome
The console will show us when there is an error in our JavaScript. It also displays the line where it became a problem for the interpreter.
##### Typing in the console in chrome
We can also just type code into the console and it will show us a result.

### Writing from script to the console
Browsers that have a console have a **console object**, which has several methods that our script can use to display data in the console.
The object is documented in the **Console API**.

### Logging data to the console
There are several uses of the console . log () method:
1. to indicate the script is running.
2. When input loses focus, write value to console.
- When the user submits the form, four values are displayed:
3. That the user clicked submit.

                ```
                $(' #calculator').on('submit', function(e)
                e.preventDefault();
                console.log('Clicked submit . . . ') ;
                ```


4. The value in the width input.

                ```
                width = $('#width').val();
                console.log('Width ' +width} ;
                ```


5. The value in the height input.

                 ```
                 height= $('#height').val();
                 console.log( 'Height ', height);

                 ```

6. The value of the area variable.

                 ```
                area = width * height;
                console. log(area);
                
                ```

### More console methods 
![console methods](https://blog.kentonvizdos.com/content/images/2020/06/carbon-2.png)

To differentiate between the types of messages we write to the console, we can use three different methods. They use variou colors and icons to distinguish them:
![three methods](https://media.geeksforgeeks.org/wp-content/uploads/20200614095921/console-sidebar.png)

##### Grouping messages
If we want to write a set of related data to the console, we can use the **console. group () method** to group the messages together.We can then expand and contract the results.

When we have finished writing out the results for the group, to indicate the end of the group **the console .groupEnd () method** is used.

##### Writing tabular data
In browsers that support it, the **console. table () method** lets
us output a table showing:
- objects.
- arrays that contain other objects or arrays.

##### Writing on a condition
Using the **console. assert() method**,we can test if a condition is met, and write to the console only if the expression
evaluates to false.

### Breakpoints
We can pause the execution of a script on any line using breakpoints. Then we can check the values stored in variables at that point in time.

![breakpoints](https://d3of8ou1mslcoj.cloudfront.net/content/uploads/2012/05/javascript_breakpoints1.png)

###### Stepping through code 
If we set multiple breakpoints, we can step through them one-by-one to see where values change and a problem might occur.

###### Conditional breakpoints
We can indicate that a breakpoint should be triggered only if a condition that we specify is met. The condition can use existing variables.

![conditional breakpoint](https://i2.wp.com/dailydotnettips.com/wp-content/uploads/2010/12/image_thumb12.png?w=578&ssl=1)

###### Debugger keyword
We can create a breakpoint in our code using just the debugger keyword. When the developer tools are open, this will automatically create a breakpoint.

### Handling Exceptions
If we know our code might fail, use **try**, **catch**, and **finally**.
Each one is given its own code block :
- *try* : Try to execute this code .
- *catch* (exception) : If there is an exception, run this code .
- *finally* : This always gets executed .

### Throw error for NaN
If we try to use a string in a mathematical operation (other than in addition), we do not get an error, we get a special value called **NaN (not a number)**.

### Debugging Tips
Here are a selection of practical tips that we can try to use when debugging our scripts:
1. *ANOTHER BROWSER* : Some problems are browser specific.
Try the code in another browser to see which ones are causing a problem.
2. *ADD NUMBERS* : Write numbers to the console so we can see which the items get logged. It shows how far our  code runs before errors stop it.
3. *STRIP IT BACK* : Remove parts of code, and strip it down to the minimum we need.
4. *EXPLAINING THE CODE* : Programmers often report finding a solution to a problem while explaining the code to someone else.
5. *SEARCH* : Stack Overflow is a Q+A site for programmers.
Or use a traditional search engine such as Google, Bing, or DuckDuckGo.
6. *CODE PLAYGROUNDS*.
7. *VALIDATION TOOLS* : There are a number of on line validation tools that can help us try to find errors in our code:
- **JAVASCRIPT** :
`http://www.jslint.com`
`http://www.jshint .com`
- **JSON** :
`http:// www.jsonlint.com`
- **JQUERY** :
There is a jQuery debugger plugin available for Chrome which can be found in the Chrome web store.


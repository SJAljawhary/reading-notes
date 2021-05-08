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



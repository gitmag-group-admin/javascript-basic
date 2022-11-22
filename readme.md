
#  What is JavaScript

JavaScript is a programming language initially designed to interact with elements of web pages.
JavaScript allows you to add interactivity to a web page. Typically, you use JavaScript with HTML and CSS to enhance a web page’s functionality, such as [validating forms](https://www.javascripttutorial.net/javascript-dom/javascript-form-validation/), creating interactive maps, and displaying animated charts.

When a web page is loaded, i.e., after HTML and CSS have been downloaded, the JavaScript engine in the web browser executes the JavaScript code. The JavaScript code then modifies the HTML and CSS to update the user interface dynamically.

The **JavaScript engine** is a program that executes JavaScript code. In the beginning, JavaScript engines were implemented as interpreters.

However, modern JavaScript engines are typically implemented as just-in-time compilers that compile JavaScript code to bytecode for improved performance.

  

##  Client-side vs. Server-side JavaScript

When JavaScript is used on a web page, it is executed in web browsers. In this case, JavaScript works as a client-side language.

JavaScript can run on both web browsers and servers. A popular JavaScript server-side environment is [Node.js](https://www.javascripttutorial.net/nodejs-tutorial/). Unlike client-side JavaScript, server-side JavaScript executes on the server that allows you to access databases, file systems, etc.

## JavaScript History

In 1995, JavaScript was created by a Netscape developer named [Brendan Eich](https://en.wikipedia.org/wiki/Brendan_Eich). First, its name was Mocha. And then, its name was changed to LiveScript.

Netscape released JavaScript 1.1 in Netscape Navigator 3. In the meantime, Microsoft introduced a web browser product called the [Internet Explorer](https://en.wikipedia.org/wiki/Internet_Explorer) 3 (IE 3), which competed with Netscape. However, IE came with its own JavaScript implementation called [JScript](https://en.wikipedia.org/wiki/JScript). Microsoft used the name JScript to avoid possible license issues with Netscape.

Hence, two different JavaScript versions were in the market:

-   JavaScript in Netscape Navigator
-   JScript in Internet Explorer.

JavaScript had no standards that governed its syntax and features. And the community decided that it was time to standardize the language.

In 1997, JavaScript 1.1 was submitted to the [European Computer Manufacturers Association](https://www.ecma-international.org/) (ECMA) as a proposal. [Technical Committee #39](https://www.ecma-international.org/memento/tc39-m.htm) (TC39) was assigned to standardize the language to make it a general-purpose, cross-platform, and vendor-neutral scripting language.
TC39 came up with ECMA-262, a standard for defining a new scripting language named ECMAScript (often pronounced Ek-ma-script).

After that, the International Organization for Standardization and International Electrotechnical Commissions (ISO/IEC) adopted ECMAScript (ISO/IEC-16262).


# JavaScript Code Editors


### Popular JavaScript Code Editors
To edit JavaScript source code, you need a plain text editor such as Notepad on Windows. However, to simplify and speed up typing of JavaScript code, you need a JavaScript code editor.

Besides basic editing features, a JavaScript code editor provides you with syntax highlighting, indentation, autocomplete, and brace matching functionality. Some editors also allow you to debug JavaScript.

The following are some popular JavaScript code editors:
-   [Visual Studio Code](https://code.visualstudio.com/)
-   [Atom](https://atom.io/)
-   [Notepad++](https://notepad-plus-plus.org/)
-   [Vim](https://www.vim.org/)

Note that all these JavaScript editors are free. As a matter of choice, we will use the Visual Studio Code.

### Visual Studio Code

Visual Studio Code is a free and open-source code editor developed by Microsoft. Visual Studio Code is often called VS Code.

![enter image description here](https://www.javascripttutorial.net/wp-content/uploads/2019/12/JavaScript-Code-Editor-VS-Code.png)
VS Code works across platforms including Windows, Linux, and macOS.

VS Code is highly customizable. It allows you to change the theme, keyboard shortcuts, preferences. It has lots of useful extensions that add extra functionality to the editor.

VS Code includes built-in support for JavaScript, which includes IntelliSense, debugging, formatting, code navigation, refactoring, and many other advanced language features.

To learn all the features supported by VS code, you check it out the [JavaScript in Visual Studio Code](https://code.visualstudio.com/docs/languages/javascript).

### Download Visual Studio Code
To download the Visual Studio Code, you go to the following download link:

[Download Visual Studio Code](https://code.visualstudio.com/download)

### Installing Visual Studio Code

Setting up the Visual Studio Code is easy and quick. It is a small download so that you can install it in a few minutes.

### A) Windows

To install the VS Code on Windows, you follow these steps:

-   First, execute the installer from the downloaded file.
-   Then, open the Visual Studio code.

Note that the installer will add the Visual Studio Code to your `%PATH%`. It will allow you to type the command `code .` to launch the VS Code on that folder.

### B) macOS

You follow these steps to install the VS Code on macOS:

-   First, double-click on the downloaded archive to expands the contents.
-   Then, drag Visual Studio Code.app to the Applications to make it available in the launchpad.

### Installing the Live Server extension

The live server extension allows you to launch a development local server with the hot reload feature for static pages. Once you change the JavaScript code, you don’t need to refresh the page to see the changes.

To install the Live Server extension, you follow these steps:

-   First, click the Extensions.
-   Second, search for the Live Server and select the Live Server extension on the list.
-   Finally, click the Install button.

![enter image description here](https://www.javascripttutorial.net/wp-content/uploads/2020/04/Live-Server.png)

# JavaScript Hello World Example

To insert JavaScript into an HTML page, you use the `<script>` element. There are two ways to use the <script> element in an HTML page:

-   Embed JavaScript code directly into the HTML page.
-   Reference an external JavaScript code file..

### Embed JavaScript code in an HTML page
Placing JavaScript code inside the `<script>` element directly is not recommended and should be used only for proof of concept or testing purposes.

The JavaScript code in the `<script>` element is interpreted from top to bottom. For example:

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>JavaScript Hello World Example</title>
        <script>
            alert('Hello, World!');
        </script>
    </head>
    <body>
    </body>
    </html>


In the `<script>` element, we use the **`alert()`** function to display the `Hello, World!` message.

### Include an external JavaScript file
To include a JavaScript from an external file:

-   First, create a file whose extension is `.js` e.g., `app.js` and place it in the `js` subfolder. Note that placing the JavaScript file in the `js` folder is not required however it is a good practice.
-   Then, use the URL to the JavasScript source code file in the `src` attribute of the `<script>` element.

The following shows the contents of the app.js file:

    alert('Hello, World!');

And the following shows the `helloworld.html` file:

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>JavaScript Hello World Example</title>
        <script src="js/app.js"></script>
    </head>
    <body>
    
    </body>
    </html>

If you launch the `helloworld.html` file in the web browser, you will see an alert that displays the `Hello, World!` message.

Note that you can load a JavaScript file from a remote server. This allows you to serve up JavaScript from various domains e.g., content delivery network (CDN) to speed up the page.

When you have multiple JavaScript files on a page, the JavaScript engine interprets the files in the order that they appear. For example:

    <script src="js/service.js"></script>
    <script src="js/app.js"></script>

In this example, JavaScript engine will interpret the `service.js` and the `app.js` files in sequence. It completes interpreting the `service.js` file first before interpreting the `app.js` file.

For the page that includes many external JavaScript files, the blank page is shown during the page rendering phase.

To avoid this, you include the JavaScript file just before the `</body>` tag as shown in this example:

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>JavaScript Hello World Example</title>
    </head>
    <body>
     
       <!-- end of page content here-->
       <script src="js/service.js"></script>
       <script src="js/app.js"></script>
    </body>
    </html>

### The async and defer attributes
To change how the browser load and execute JavaScript files, you use one of two attributes of the `<script>` element `async` and `defer`.

These attributes take effect only on the external script files. The `async` attribute instructs the web browser to execute the JavaScript file asynchronously. The `async` attribute does not guarantee the script files to execute in the order that they appear. For example:

    <script async src="service.js"></script>
    <script async src="app.js"></script>

The `app.js` file might execute before the `service.js` file. Therefore, you must ensure that there is no dependency between them.
The `defer` attribute requests the web browser to execute the script file after the HTML document has been parsed.

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>JavaScript defer demonstration</title>
        <script defer src="defer-script.js"></script>
    </head>
    <body>
    </body>
    </html>

Even though we place the `<script>` element in the `<head>` section, the script will wait for the browser to receive the closing tag `<html>` to start executing.

### Summary

-   Use `<script>` element to include a JavaScript file in a HTML page.
-   The `async` attribute of the `<script>` element instructs the web browser to fetch the JavaScript file in parallel and then parse and execute as soon as the JavaScript file is available.
-   The `defer` attribute of the `<script>` element allows the web browser to execute the JavaScript file after the document has been parsed.

# JavaScript Syntax


### Statements

A statement is a code that declares a variable or instructs the JavaScript engine to do a task. A simple statement is terminated by a semicolon (`;`).

Although the semicolon (`;`) is optional; you should always use it to terminate a statement. For example, the following [declares a variable](https://www.javascripttutorial.net/javascript-variables/) and shows it to the console:

    let message = "Welcome to JavaScript";
    console.log(message);
    
### Blocks

A block is a sequence of zero or more simple statements. A block is delimited by a pair of curly brackets `{}`. For example:

    if (window.localStorage) {
      console.log('The local storage is supported');
    }

### Comments

Comments allow you to add notes or hints to JavaScript code. When executing the code, the JavaScript engine ignores the comments.

JavaScript supports single-line and block comments.

### Single-line comments

A single-line comment starts with two forward-slashes characters (`//`). A single-line comment makes all the text following the `//` on the same line into a comment. For example:

    // this is a single-line comment

### Block comments

A delimited comment begins with a forward slash and asterisk `/*` and ends with the opposite `*/` as in the following example:

    /* This is a block comment
    that can span multiple lines */

### Keywords & Reserved words
JavaScript defines a list of reserved keywords that have specific uses. Therefore, you cannot use the reserved keywords as identifiers or property names by rules.

The following table shows the JavaScript reserved words defined in ECMA-262:

![enter image description here](https://github.com/gitmag-group-admin/javascript-basic/blob/main/1.PNG?raw=truec)
### Declare a variable
To declare a variable, you use the `var` keyword followed by the variable name as follows:

    var message;

A variable name can be any valid identifier. By default, the `message` variable has a special value [`undefined`](https://www.javascripttutorial.net/javascript-data-types/#undefined) if you have not assigned a value to it.

Variable names follow these rules:
-   Variable names are case-sensitive. This means that the `message` and `Message` are different variables.
-   Variable names can only contain letters, numbers, underscores, or dollar signs and cannot contain spaces. Also, variable names must begin with a letter, an underscore (`_`) or a dollar sign (`$)`.
-   Variable names cannot use the reserved words.

By convention, variable names use camelcase like `message`, `yourAge`, and `myName`.

JavaScript is a dynamically typed language. This means that you don’t need to specify the variable’s [type](https://www.javascripttutorial.net/javascript-data-types/) in the declaration like other static typed languages such as Java or [C#](https://www.csharptutorial.net/csharp-tutorial/csharp-variables/).

Starting in ES6, you can use the `let` keyword to declare a variable like this:

    let message;
It’s a good practice to use the `let` keyword to declare a variable. Later, you’ll learn the differences [between `var` and `let` keywords](https://www.javascripttutorial.net/es6/difference-between-var-and-let/). And you should not worry about it for now.

### Initialize a variable
Once you have declared a variable, you can initialize it with a value. To initialize a variable, you specify the variable name, followed by an equals sign (`=`) and a value.

For example, The following declares the `message` variable and initializes it with a literal string `"Hello"`:

    let message;
    message = "Hello";
To declare and initialize a variable at the same time, you use the following syntax:

    let variableName = value;
For example, the following statement declares the `message` variable and initializes it with the literal string `"Hello"`:

    let message = "Hello";

### Change a variable

Once you initialize a variable, you can change its value by assigning a different value. For example:

    let message = "Hello";
    message = 'Bye';

### Constants
A constant holds a value that doesn’t change. To declare a constant, you use the const keyword. When defining a constant, you need to initialize it with a value. For example:

    const workday = 5;
Once defining a constant, you cannot change its value.

The following example attempts to change the value of the workday constant to 4 and causes an error:

    workday = 2;
Error:

    Uncaught TypeError: Assignment to constant variable.


# JavaScript Data Types

JavaScript has the primitive data types:
-   [`null`](https://www.javascripttutorial.net/javascript-data-types/#null)
-   [`undefined`](https://www.javascripttutorial.net/javascript-data-types/#undefined)
-   [`boolean`](https://www.javascripttutorial.net/javascript-data-types/#boolean)
-   [`number`](https://www.javascripttutorial.net/javascript-data-types/#number)
-   [`string`](https://www.javascripttutorial.net/javascript-data-types/#string)
- and a complex data type [`object`](https://www.javascripttutorial.net/javascript-data-types/#object).

JavaScript is a dynamically typed language. It means that a [variable](https://www.javascripttutorial.net/javascript-variables/) doesn’t associate with a type. In other words, a variable can hold a value of different types. For example:

    let counter = 120; // counter is a number
    counter = false;   // counter is now a boolean
    counter = "foo";   // counter is now a string
To get the current type of the value that the variable stores, you use the `[typeof](https://www.javascripttutorial.net/javascript-typeof/)` operator:

    let counter = 120;
    console.log(typeof(counter)); // "number"
    
    counter = false; 
    console.log(typeof(counter)); // "boolean"
    
    counter = "Hi";
    console.log(typeof(counter)); // "string"

Output:

    "number"
    "boolean"
    "string"

### The undefined type

The `undefined` type is a primitive type that has only one value `undefined`. By default, when a variable is declared but not initialized, it is assigned the value of `undefined`.

Consider the following example:

    let counter;
    console.log(counter);        // undefined
    console.log(typeof counter); // undefined

In this example, the `counter` is a variable. Since `counter` hasn’t been initialized, it is assigned the value `undefined`. The type of `counter` is also `undefined`.

It’s important to note that the `typeof` operator also returns `undefined` when you call it on a variable that hasn’t been declared:

    console.log(typeof undeclaredVar); // undefined

### The null type
The `null` type is the second primitive data type that also has only one value `null`. For example:

    let obj = null;
    console.log(typeof obj); // object
JavaScript defines that `null` is equal to `undefined` as follows:

    console.log(null == undefined); // true
### The number type
JavaScript uses the `number` type to represent both integer and floating-point numbers.

The following statement declares a variable and initializes its value with an integer:

    let num = 100;
To represent a floating-point number, you include a decimal point followed by at least one number. For example:

    let price= 12.5; 
    let discount = 0.05;
Note that JavaScript automatically converts a floating-point number into an integer number if the number appears to be a whole number.

The reason is that Javascript always wants to use less memory since a floating-point value uses twice as much memory as an integer value. For example:

    let price = 200.00; // interpreted as an integer 200
To get the range of the number type, you use `Number.MIN_VALUE` and `Number.MAX_VALUE`. For example:

    console.log(Number.MAX_VALUE); // 1.7976931348623157e+308
    console.log(Number.MIN_VALUE); // 5e-324

Also, you can use `Infinity` and `-Infinity` to represent the infinite number. For example:

    console.log(Number.MAX_VALUE + Number.MAX_VALUE); // Infinity
    console.log(-Number.MAX_VALUE - Number.MAX_VALUE); // -Infinity

### NaN

`NaN` stands for Not a Number. It is a special numeric value that indicates an invalid number. For example, the division of a string by a number returns `NaN`:.

    console.log('a'/2); // NaN;

The `NaN` has two special characteristics:

-   Any operation with `NaN` returns `NaN`.
-   The `NaN` does not equal any value, including itself.

Here are some examples:

    console.log(NaN/2); // NaN
    console.log(NaN == NaN); // false

### The string type

In JavaScript, a string is a sequence of zero or more characters. A string literal begins and ends with either a single quote(`'`) or a double quote (`"`).

A string that begins with a double quote must end with a double quote. Likewise, a string that begins with a single quote must also end with a single quote:

    let greeting = 'Hi';
    let message  = "Bye";
If you want to single quote or double quotes in a literal string, you need to use the backslash to escape it. For example:

    let message = 'I\'m also a valid string'; // use \ to escape the single quote (')
JavaScript strings are immutable. This means that it cannot be modified once created. However, you can create a new string from an existing string. For example:

    let str = 'JavaScript';
    str = str + ' String';
In this example:

-   First, declare the `str` variable and initialize it to a string of `'JavaScript'`.
-   Second, use the `+` operator to combine `'JavaScript'` with `' String'` to make its value as `'Javascript String'`.

Behind the scene, the JavaScript engine creates a new string that holds the new string `'JavaScript String'` and destroys the original strings `'JavaScript'` and `' String'`.

The following example attempts to change the first character of the string JavaScript:

    let s = 'JavaScript';
    s[0] = 'j';
    console.log(s)
The output is:

    'JavaScript'
But not:

    `'javaScript'`
### The boolean type
The `boolean` type has two literal values: `true` and `false` in lowercase. The following example declares two variables that hold the boolean values.

    let inProgress = true;
    let completed = false;
    
    console.log(typeof completed); // boolean

JavaScript allows values of other types to be converted into boolean values of `true` or `false`.

To convert a value of another data type into a boolean value, you use the [`Boolean()`](https://www.javascripttutorial.net/javascript-boolean/) function. 
For example:

    console.log(Boolean('Hi'));// true
    console.log(Boolean(''));  // false
    
    console.log(Boolean(20));  // true
    console.log(Boolean(Infinity));  // true
    console.log(Boolean(0));  // false
    
    console.log(Boolean({foo: 100}));  // true on non-empty object
    console.log(Boolean(null));// false

### The object type
In JavaScript, an [object](https://www.javascripttutorial.net/home/javascript-objects/) is a collection of [properties](https://www.javascripttutorial.net/home/javascript-object-properties/), where each property is defined as a key-value pair.

The following example defines an empty object using the object literal syntax:

    let emptyObject = {};
The following example defines the `person` object with two properties: `firstName` and `lastName`.

    let person = {
        firstName: 'John',
        lastName: 'Doe'
    };
A property name of an object can be any string. You can use quotes around the property name if it is not a valid identifier.

For example, if the person object has a property `first-name`, you must place it in the quotes such as `"first-name"`.

A property of an object can hold an object. For example:

    let contact = {
        firstName: 'John',
        lastName: 'Doe',
        email: 'john.doe@example.com',
        phone: '(408)-555-9999',
        address: {
            building: '4000',
            street: 'North 1st street',
            city: 'San Jose',
            state: 'CA',
            country: 'USA'
        }
    }
The `contact` object has the `firstName`, `lastName`, `email`, `phone`, and `address` properties.

The `address` property itself holds an object that has `building`, `street`, `city`, `state`, and `country` properties.

To access a object’s property, you can use

-   The dot notation (`.`)
-   The array-like notation (`[]`).

The following example uses the dot notation (`.`) to access the `firstName` and `lastName` properties of the `contact` object.

    console.log(contact.firstName);
    console.log(contact.lastName);
If you reference a property that does not exist, you’ll get an `undefined` value. For example:

    console.log(contact.age); // undefined
The following example uses the array-like notation to access the `email` and `phone` properties of the `contact` object.

    console.log(contact['phone']); // '(408)-555-9999'
    console.log(contact['email']); // 'john.doe@example.com'

# JavaScript Arrays
### Introduction to JavaScript arrays

In JavaScript, an array is an ordered list of values. Each value is called an element specified by an index.

![enter image description here](https://www.javascripttutorial.net/wp-content/uploads/2020/09/JavaScript-Array.png)
An JavaScript array has the following characteristics:

1.  First, an array can hold values of mixed types. For example, you can have an array that stores elements with the types number, string, and boolean.
2.  Second, the size of an array is dynamic and auto-growing. In other words, you don’t need to specify the array size upfront.

### Creating JavaScript arrays

JavaScript provides you with two ways to create an array. The first one is to use the `Array` constructor as follows:

    let scores = new Array();
The `scores` array is empty, which does hold any elements.

If you know the number of elements that the array will hold, you can create an array with an initial size as shown in the following example:

    let scores = Array(10);
To create an array and initialize it with some elements, you pass the elements as a comma-separated list into the `Array()` constructor.

For example, the following creates the `scores` array that has five elements (or numbers):

    let scores = new Array(9,10,8,7,6);
However, when you pass a value of another type like `string` into the `Array()` constructor, you create an array with an element of that value. For example:

    let athletes = new Array(3); // creates an array with initial size 3
    let scores = new Array(1, 2, 3); // create an array with three numbers 1,2 3
    let signs = new Array('Red'); // creates an array with one element 'Red'
JavaScript allows you to omit the `new` operator when you use the Array() constructor. For example, the following statement creates the `artists` array.

    let artists = Array();
In practice, you’ll rarely use the `Array()` constructor to create an array.

The more preferred way to create an array is to use the array literal notation:

    let arrayName = [element1, element2, element3, ...];
The array literal form uses the square brackets `[]` to wrap a comma-separated list of elements.

The following example creates the `colors` array that holds string elements:

    let colors = ['red', 'green', 'blue'];
To create an empty array, you use square brackets without specifying any element like this:

    let emptyArray = [];
### Accessing JavaScript array elements

JavaScript arrays are zero-based indexed. In other words, the first element of an array starts at index 0, the second element starts at index 1, and so on.

To access an element in an array, you specify an index in the square brackets `[]`:

    arrayName[index]
The following shows how to access the elements of the `mountains` array:

    let mountains = ['Everest', 'Fuji', 'Nanga Parbat'];
    
    console.log(mountains[0]); // 'Everest'
    console.log(mountains[1]); // 'Fuji'
    console.log(mountains[2]); // 'Nanga Parbat'
Output:

    [ 'Everest', 'Fuji', 'K2' ]

### Getting the array size

Typically, the `[length](https://www.javascripttutorial.net/javascript-array-length/)` property of an array returns the number of elements. The following example shows how to use the `length` property:

    let mountains = ['Everest', 'Fuji', 'Nanga Parbat'];
    console.log(mountains.length); // 3

### Basic operations on arrays

The following explains some basic operations on arrays. And you’ll learn advanced operations such as `[map()](https://www.javascripttutorial.net/javascript-array-map/)`, `[filter()](https://www.javascripttutorial.net/javascript-array-filter/)`, and `[reduce()](https://www.javascripttutorial.net/javascript-array-reduce/)` in the next tutorials.

### 1) Adding an element to the end of an array

To add an element to the end of an array, you use the `push()` method:

    let seas = ['Black Sea', 'Caribbean Sea', 'North Sea', 'Baltic Sea'];
    seas.push('Red Sea');
    
    console.log(seas); 
Output:

    [ 'Black Sea', 'Caribbean Sea', 'North Sea', 'Baltic Sea', 'Red Sea' ]

### 2) Adding an element to the beginning of an array

To add an element to the beginning of an array, you use the `unshift()` method:

    let seas = ['Black Sea', 'Caribbean Sea', 'North Sea', 'Baltic Sea'];
    seas.unshift('Red Sea');
    
    console.log(seas);

Output:

    [ 'Red Sea', 'Black Sea', 'Caribbean Sea', 'North Sea', 'Baltic Sea' ]
### 3) Removing an element from the end of an array
To remove an element from the end of an array, you use the `pop()` method:

    let seas = ['Black Sea', 'Caribbean Sea', 'North Sea', 'Baltic Sea'];
    const lastElement = seas.pop();
    console.log(lastElement); 

Output:

    Baltic Sea
### 4) Removing an element from the beginning of an array
To remove an element from the beginning of an array, you use the `shift()` method:

    let seas = ['Black Sea', 'Caribbean Sea', 'North Sea', 'Baltic Sea'];
    const firstElement = seas.shift();
    
    console.log(firstElement);
Output:

    Black Sea
### 5) Finding an index of an element in the array
To find the index of an element, you use the `indexOf()` method:

    let seas = ['Black Sea', 'Caribbean Sea', 'North Sea', 'Baltic Sea'];
    let index = seas.indexOf('North Sea');
    
    console.log(index); // 2
### 6) Check if an value is an array
To check if a value is an array, you use `Array.isArray()` method:

    console.log(Array.isArray(seas)); // true

# JavaScript Operators (1)



### Introduction to the JavaScript Arithmetic Operators

An arithmetic operator accepts numerical values as operands and returns a single numerical value. The numerical values can be literals or variables.

### Addition operator (+)

The addition operator returns the sum of two values. For example, the following uses the addition operator to calculate the sum of two numbers:

    let sum = 10 + 20;
    console.log(sum); // 30
Also, you can use the addition operator with two [variables](https://www.javascripttutorial.net/javascript-variables/). For example:

    let netPrice    = 9.99,
        shippingFee = 1.99;
    let grossPrice  = netPrice + shippingFee;
    
    console.log(grossPrice);
Output:

    11.98

If either value is a [string](https://www.javascripttutorial.net/string/), the addition operator uses the following rules:

-   If both values are strings, it concatenates the second string to the first one.
-   If one value is a string, it implicitly converts the numeric value into a string and conatenate two strings.

For example, the following uses the addition operator to add concatenate two strings:

    let x = '10',
        y = '20';
    let result = x + y;
    
    console.log(result);
Output:

    1020
The following example shows how to use the addition operator to calculate the sum of a number and a string:

    let result = 10 + '20';
    
    console.log(result);    
Output:

    `1020`
In this example, JavaScript converts the number `10` into a string `'10'` and concatenates the second string `'20'` to it.

### Subtraction operator (-)
The subtraction operator (`-`) subtracts one number from another. For example:

    let result = 30 - 10;
    console.log(result); // 20
If a value is a string, a boolean, null, or undefined, the JavaScript engine will:

-   First, convert the into a number using the Number() function.
-   Second, perform the subtraction.
- 
### Multiplication operator (*)
JavaScript uses the asterisk (*) to represent the multiplication operator. The multiplication operator multiplies two numbers and returns a single value. For example:

    let result = 2 * 3;
    console.log(result);
Output:

    6
If either value is not a number, the JavaScript engine implicitly converts it into a number using the `Number()` function and performs the multiplication. For example:

    let result = '5' * 2;
    
    console.log(result);
Output:

    10
### Divide operator (/)
Javascript uses the slash (`/`) character to represent the divide operator. The divide operator divides the first value by the second one. For example:

    let result = 20 / 10;
    
    console.log(result); // 2
If either value is not a number, the JavaScript engine converts it into a number for division. For example:

    let result = '20' / 2;
    console.log(result); // 10;

### JavaScript remainder operator
JavaScript uses the `%` to represent the remainder operator. The remainder operator returns the remainder left over when one value is divided by another value.

### JavaScript remainder operator examples
Let’s take some examples of using the JavaScript remainder operator.

#### 1) Using the remainder operator with positive dividend example

The following example shows how to use the remainder operator with a positive dividend:

    let remainder = 5 % -2;
    console.log(remainder); // 1
    
    remainder = 5 % 2;
    console.log(remainder); // 1

#### 2) Using the remainder operator with negative dividend example

The following example uses the remainder operator with a negative dividend:

    let remainder = -5 % 3;
    console.log(remainder); // -2
    
    remainder = -5 % -3;
    console.log(remainder); // -2

#### 3) Using the remainder operator special values
If a dividend is an `Infinity` and a divisor is a finite number, the remainder is `NaN`. For example:

    let remainder = Infinity % 2;
    console.log(remainder); // NaN

If a dividend is a finite number and a divisor is zero, the remainder is `NaN`:

    let remainder = 10 % 0;
    console.log(remainder); // NaN


### Using the remainder operator to check if a number is an odd number
To check if a number is an odd number, you use the remainder operator (`%`) like the following example:

    let num = 13;
    let isOdd = num % 2;
In this example, if the `num` is an odd number, the remainder is one. But if the `num` is an even number, the remainder is zero.

### JavaScript assignment operators
An assignment operator (`=`) assigns a value to a variable. The syntax of the assignment operator is as follows:

    let a = b;
In this syntax, JavaScript evaluates the expression `b` first and assigns the result to the variable `a`.

The following example declares the `counter` variable and initializes its value to zero:

    let counter = 0;
The following example increases the `counter` variable by one and assigns the result to the `counter` variable:

    let counter = 0;
    counter = counter + 1;

When evaluating the second statement, JavaScript evaluates the expression on the right hand first (`counter + 1`) and assigns the result to the `counter` variable. After the second assignment, the `counter` variable is `1`.

To make the code more concise, you can use the `+=` operator like this:

    let counter = 0;
    counter += 1;
In this syntax, you don’t have to repeat the `counter` variable twice in the assignment.

The following table illustrates assignment operators that are shorthand for another operator and the assignment:
![enter image description here](https://github.com/gitmag-group-admin/javascript-basic/blob/main/2.PNG?raw=true)
### Chaining JavaScript assignment operators
If you want to assign a single value to multiple variables, you can chain the assignment operators. For example:

    let a = 10, b = 20, c = 30;
    a = b = c; // all variables are 30

In this example, JavaScript evaluates from right to left. Therefore, it does the following:

    let a = 10, b = 20, c = 30;
    
    b = c; // b is 30
    a = b; // a is also 30 

### JavaScript unary operators
Unary operators work on one value. The following table shows the unary operators and their meanings:
![enter image description here](https://github.com/gitmag-group-admin/javascript-basic/blob/main/3.PNG?raw=true)
### Unary plus (+)
The unary plus operator is a simple plus sign (`+`). If you place the unary plus before a numeric value, it does nothing. For example

    let x = 10;
    let y = +x;
    
    console.log(y); // 10
the following uses the unary plus operator to convert the string `'10'` to the number `10`:

    let s = '10';
    console.log(+s); // 10
The following example uses the unary plus operator (`+`) converts a boolean value into a number, `false` to `0` and `true` to `1`.

    let f = false,
        t = true;
    
    console.log(+f); // 0
    console.log(+t); // 1

### Unary minus (-)
The unary minus operator is a single minus sign (`-`). If you apply the unary minus operator to a number, it negates the number. For example:

    let x = 10;
    let y = -x;
    
    console.log(y); // -10
If you apply the unary minus operator to a non-numeric value, it converts the value into a number using the same rules as the unary plus operator and then negates the value.

### Increment / Decrement operators
The increment operator has two plus signs (`++`) while the decrement operator has two minus signs (`--`).

Both increment and decrement operators have two versions: prefix and postfix. And you place the prefix and postfix versions of the increment or decrement operators before and after the variable to which they apply.

The following example uses the prefix increment operator to add one to a variable:

    let age = 25;
    ++age;
    
    console.log(age); // 26
It’s equivalent to the following:

    let age = 25;
    age = age + 1;
    console.log(age); // 26
The following example uses the prefix decrement operator to subtract one from a variable:

    let weight = 90;
    --weight;
    
    console.log(weight); // 89
It is equivalent to the following:

    let weight = 90;
    weight = weight - 1;
    
    console.log(weight); // 89
When you apply the prefix increment or decrement, JavaScript changes the variable before evaluating the statement. For example:

    let weight = 90;
    weight = ++weight + 5;
    
    console.log(weight); // 96

In this example:

-   First, increase the weight on the right-hand side so ++weight is 91
-   Second, add five to the ++weight that returns 96
-   Third, assign the result to the weight on the left-hand side.

Likewise, the following example uses a prefix decrement operator:

    let weight = 90;
    weight = --weight + 5;
    
    console.log(weight); // 94
In this example:

-   First, subtract one from the weight, –weight returns 89
-   Second, add five to the –weight that returns 94
-   Third, assign the result to the weight on the left-hand side.

The postfix increment or decrement operator changes the value after the statement is evaluated. For example:

    let weight = 90;
    let newWeight = weight++ + 5;
    
    console.log(newWeight); // 95
    console.log(weight); // 91
How it works.

-   First, add five to weight (90) and assign the result to the new weight (95)
-   Second, add one to the weight variable after the second statement completes, the weight becomes 91.
-   Third, output both newWeight and weight to the console.

When applying the increment/decrement operator to a non-numeric value, it performs the following steps :

-   First, convert the value into a number using the same rules as the unary plus (+) operator.
-   Then, add one to or subtract one from the value.


# JavaScript Operators (2)

### JavaScript Comparison Operators
To compare two values, you use a comparison operator. The following table shows the comparison operators in JavaScript:
  
![enter image description here](https://github.com/gitmag-group-admin/javascript-basic/blob/main/4.PNG?raw=true)

  A comparison operator returns a [Boolean](https://www.javascripttutorial.net/javascript-boolean/) value indicating that the comparison is true or not. See the following example:

    let r1 = 20 > 10; // true
    let r2 = 20 < 10; // false
    let r3 = 10 == 10; // true
A comparison operator takes two values. If the types of the values are not comparable, the comparison operator converts them into values of comparable types according to specific rules.

### Compare numbers

If values are numbers, the comparison operators perform a numeric comparison. For example:

    let a = 10, 
        b = 20; 
    
    console.log(a >= b);  // false
    console.log(a == 10); // true

This example is straightforward. The variable `a` is `10`, `b` is `20`. The expression `a >= b` expression returns `false` and the expression `a == 10` expression returns `true`.

### Compare strings

If the operands are strings, JavaScript compares the character codes numerically one by one in the string.

    let name1 = 'alice',
        name2 = 'bob';    
    
    let result = name1 < name2;
    console.log(result); // true
    console.log(name1 == 'alice'); // true
Because JavaScript compares the character codes in the strings numerically, you may receive an unexpected result, for example:

    let f1 = 'apple',
        f2 = 'Banana';
    let result = f2 < f1;
    console.log(result); // true
In this example, `f2` is less than `f1` because the letter `B` has the character code `66` while the letter `a` has the character code `97`.

To fix this, you need to:

-   First, convert the strings into a common format, either lowercase or uppercase
-   Second, compare the converted values

For example:

    let f1 = 'apple',
        f2 = 'Banana';
    
    let result = f2.toLowerCase() < f1.toLowerCase();
    console.log(result); // false
Note that the `toLowerCase()` is a method of the String object that converts the string to lowercase.

### Compare a number with a value of another type

If a value is a number and the other is not, the comparison operator will convert the non-numeric value into a number and compare them numerically. For example:

    console.log(10 < '20'); // true
In this example, the comparison operator converts the string `'20'` into the number `20` and compares with the number 10. Here is an example:

    console.log(10 == '10'); // true
In this example, the comparison operator converts the string `'10'` into the number `10` and compares them numerically.

### Compare a Boolean with another value
If a value is a Boolean value, JavaScript converts it to a number and compares the converted value with the other value; `true` is converted to `1` and `false` is converted to `0`. For example:

    console.log(true > 0); // true
    console.log(false < 1); // true
    console.log(true > false); // true
    console.log(false > true); // false
    console.log(true >= true); // true
    console.log(true <= true); // true
    console.log(false <= false); // true
    console.log(false >= false); // true

In addition to the above rules, the equal (`==`) and not-equal(`!=`) operators also have the following rules.

### Strict equal (`===`) and not strict equal (`!==`)
Besides the comparison operators above, JavaScript provides the strict equal ( `===`) and not strict equal ( `!==`) operators.

![enter image description here](https://github.com/gitmag-group-admin/javascript-basic/blob/main/5.PNG?raw=true)

  The strict equal and not strict equal operators behave like the equal and not equal operators except that they don’t convert the operand before comparison. See the following example:

    console.log("10" == 10); // true
    console.log("10" === 10); // false

In the first comparison, since we use the equality operator, JavaScript converts the string into the number and performs the comparison.

However, in the second comparison, we use the strict equal operator ( `===`), JavaScript doesn’t convert the string before comparison, therefore the result is `false`.

### JavaScript Logical Operators
The logical operators are important in JavaScript because they allow you to compare variables and do something based on the result of that comparison.
For example, if the result of the comparison is `true`, you can run a block of code; if it’s `false`, you can execute another code block.

JavaScript provides three logical operators:

-   ! (Logical NOT)
-   || (Logical OR)
-   && (Logical AND)

#### 1) The Logical NOT operator (!)
JavaScript uses an exclamation point `!` to represent the logical NOT operator. The `!` operator can be applied to a single value of any type, not just a Boolean value.

When you apply the `!` operator to a boolean value, the `!` returns `true` if the value is `false` and `false` if the value if `true`. For example:

    let eligible = false,
        required = true;
    
    console.log(!eligible);
    console.log(!required);
Output:

    true
    false

In this example, the `eligible` is `true` so `!eligible` returns `false`. And since the `required` is `true`, the `!required` returns `false`.

When you apply the `!` operator to a non-Boolean value. The `!` operator first converts the value to a [boolean](https://www.javascripttutorial.net/javascript-data-types/#boolean) value and then negates it.


The following demonstrates the results of the logical `!` operator when applying to a non-boolean value:

    console.log(!undefined); // true
    console.log(!null); // true
    console.log(!20); //false
    console.log(!0); //true
    console.log(!NaN); //true
    console.log(!{}); // false
    console.log(!''); //true
    console.log(!'OK'); //false
    console.log(!false); //true
    console.log(!true); //false

#### 2) The Logical AND operator (`&&`)
JavaScript uses the double ampersand (`&&`) to represent the logical AND operator. The following expression uses the `&&` operator:

    let result = a && b;
If `a` can be converted to `true`, the `&&` operator returns the `b`; otherwise, it returns the `a`. In fact, this rule is applied to all boolean values.

The following truth table illustrates the result of the `&&` operator when it is applied to two Boolean values:
![enter image description here](https://github.com/gitmag-group-admin/javascript-basic/blob/main/6.PNG?raw=true)
The result of the `&&` operator is true only if both values are `true`, otherwise, it is `false`. For example:

    let eligible = false,
        required = true;
    
    console.log(eligible && required); // false

In this example, the `eligible` is `false`, therefore, the value of the expression `eligible && required` is `false`.

See the following example:

    let eligible = true,
        required = true;
    
    console.log(eligible && required); // true

In this example, both `eligible` and `required` are `true`, therefore, the value of the expression `eligible && required` is `true`.

### The chain of `&&` operators
The following expression uses multiple `&&` operators:

    let result = value1 && value2 && value3;
The `&&` operator carries the following:

-   Evaluates values from left to right.
-   For each value, converts it to a boolean. If the result is `false`, stops and returns the original value.
-   If all values are truthy values, returns the last value.

In other words, The `&&` operator returns the first falsy value or the last value if none were found.

#### 3) The Logical OR operator (`||`)

JavaScript uses the double pipe `||` to represent the logical OR operator. You can apply the `||` operator to two values of any type:

    let result = a || b;
If `a` can be converted to `true`, returns `a`; else, returns `b`. This rule is also applied to boolean values.

The following truth table illustrates the result of the `||` operator based on the value of the operands:
![enter image description here](https://github.com/gitmag-group-admin/javascript-basic/blob/main/7.PNG?raw=true)
The `||` operator returns `false` if both values evaluate to `false`. In case either value is `true`, the `||` operator returns `true`. For example:

    let eligible = true,
        required = false;
    
    console.log(eligible || required); // true

The following expression applies the `||` operator to the two non-boolean values:

In this example, the eligible || required returns true because one of the values (`required`) is true. See another example:

    let eligible = false,
        required = false;
    
    console.log(eligible || required); // false

In this example, the expression `eligible || required` returns `false` because both values are `false`.

### The `||` operator is also short-circuited
Similar to the `&&` operator, the `||` operator is short-circuited. It means that if the first value evaluates to `true`, the `&&` operator doesn’t evaluate the second one.

### The chain of `||` operators

The following example shows how to use multiple || operators in an expression:

    let result = value1 || value2 || value3;
The `||` operator does the following:

-   Evaluates values from left to right.
-   For each value, converts it to a boolean value. If the result of the conversion is `true`, stops and returns the value.
-   If all values have been evaluated to `false`, returns the last value.

In other words, the chain of the `||` operators returns the first truthy value or the last one if no truthy value was found.

# JavaScript if
### Introduction to the JavaScript if statement
The `if` statement executes block if a condition is `true`. The following shows the syntax of the `if` statement:

    if( condition )
       statement;
The `condition` can be a value or an expression. Typically, the condition evaluates to a [Boolean](https://www.javascripttutorial.net/javascript-data-types/#boolean) value, which is `true` or `false`.

If the `condition` evaluates to `true`, the `if` statement executes the `statement`. Otherwise, the `if` statement passes the control to the next statement after it.

If the `condition` evaluates to a non-Boolean value, JavaScript implicitly converts its result to a Boolean value by calling the [`Boolean()`](https://www.javascripttutorial.net/javascript-boolean/) function.

If you have more than one statement to execute, you need to use wrap them in a block using a pair of curly braces as follows:

    if (condition) {
      // statements to execute
    }
However, it’s a good practice to always use curly braces with the `if` statement. By doing this, you make your code easier to maintain and avoid possible mistakes.

### JavaScript if statement examples
The following example uses the `if` statement to check if the age is equal to or greater than `18`:

    let age = 18;
    if (age >= 18) {
      console.log('You can sign up');
    }
Output:

    `You can sign up`

How it works.

First, declare and initialize the [variable](https://www.javascripttutorial.net/javascript-variables/) `age` to `18`:

    let age = 18;

Second, check if the age is greater or equal to `18` using the `if` statement. Because the expression `age >= 18` is `true`, the code inside the `if` statement executes that outputs a message to the console:

    if (age >= 18) {
      console.log('You can sign up');
    }
The following example also uses the `if` statement. However, the `age` is `16` which causes the condition to evaluate to `false`. Therefore, you won’t see any message in the output:

    let age = 16;
    if (age >= 18) {
      console.log('You can sign up');
    }

### Nested if statement
It’s possible to use an `if` statement inside another `if` statement. For example:

    let age = 16;
    let state = 'CA';
    
    if (state == 'CA') {
      if (age >= 16) {
        console.log('You can drive.');
      }
    }
Output:

    You can drive.

### Introduction to the JavaScript if…else statement
The `[if]` statement executes a block if a condition is `true`. When the condition is `false`, it does nothing. But if you want to execute a statement if the condition is `false`, you can use an `if...else` statement.

The following shows the syntax of the `if...else` statement:

    if( condition ) {
      // ...
    } else { 
      // ...
    }
In this syntax, the `condition` is a value or an expression that evaluates to `true` or `false`. If the condition is `true`, the `if...else` statement executes the block that follows the `if` branch.

If the condition is `false`, the `if...else` statement executes the block that follows the `else` branch.

Typically, the `condition` evaluates to a boolean value, which is `true` or `false`. However, if it evaluates to a non-boolean value, the `if...else` statement will convert it to the boolean value.

### JavaScript if…else statement examples
The following example uses the `if...else` statement to check if the age is greater than or equal to 18:

    let age = 18;
    
    if (age >= 18) {
      console.log('You can sign up.');
    } else {
      console.log('You must be at least 18 to sign up.');
    }
In this example, the `age` is `18`. Therefore, the expression `age >= 18` is `true`. Hence, you’ll see the following message in the console:

    You can sign up.
The following example is the same as above except that the `age` is `18` instead of `16`:

    let age = 16;
    
    if (age >= 18) {
      console.log('You can sign up.');
    } else {
      console.log('You must be at least 18 to sign up.');
    }
Output:

    `You must be at least 18 to sign up.`
In this example, the `age` is `16`. Therefore, the expression `age >= 18` evaluates to `false`. Hence, the statement in the `else` branch executes that output the message to the console.

The following example uses a logical operator AND (&&) as the condition in the if block:

    let age = 16;
    let country = 'USA';
    
    if (age >= 16 && country === 'USA') {
      console.log('You can get a driving license.');
    } else {
      console.log('You are not eligible to get a driving license.');
    }
Because the age is 16 and the country is the USA, the following expression returns true.

    age >= 16 && country === 'USA'
And you see the following output:

    You can get a driving license.

### Introduction to the JavaScript if else if statement
The `[if]` an [if…else](https://www.javascripttutorial.net/javascript-if-else/) statements accept a single condition and execute the `if` or `else` block accordingly based on the condition.

To check multiple conditions and execute the corresponding block if a condition is `true`, you use the `if...else...if` statement like this:

    if (condition1) {
      // ...
    } else if (condition2) {
      // ...
    } else if (condition3) {
      //...
    } else {
      //...
    }

In this syntax, the `if...else...if` statement has three conditions. In theory, you can have as many conditions as you want to, where each `else...if` branch has a condition.

The `if...else...if` statement checks the conditions from top to bottom and executes the corresponding block if the condition is `true`.

The `if...else...if` statement stops evaluating the remaining conditions as soon as a condition is `true`. For example, if the `condition2` is `true`, the `if...else...if` statement won’t evaluate the `condition3`.

If all the conditions are `false`, the `if...else...if` statement executes the block in the `else` branch.

### JavaScript if else if examples
Let’s take some examples of using the `if...else...if` statement.

#### 1) A simple JavaScript if…else…if statement example

The following example uses the `if...else...if` statement to get the month name from a month number:

    let month = 6;
    let monthName;
    
    if (month == 1) {
      monthName = 'Jan';
    } else if (month == 2) {
      monthName = 'Feb';
    } else if (month == 3) {
      monthName = 'Mar';
    } else if (month == 4) {
      monthName = 'Apr';
    } else if (month == 5) {
      monthName = 'May';
    } else if (month == 6) {
      monthName = 'Jun';
    } else if (month == 7) {
      monthName = 'Jul';
    } else if (month == 8) {
      monthName = 'Aug';
    } else if (month == 9) {
      monthName = 'Sep';
    } else if (month == 10) {
      monthName = 'Oct';
    } else if (month == 11) {
      monthName = 'Nov';
    } else if (month == 12) {
      monthName = 'Dec';
    } else {
      monthName = 'Invalid month';
    }
    console.log(monthName);
Output:

```
Jun
```

In this example, we compare the month with 12 numbers from 1 to 12 and assign the corresponding month name to the `monthName` variable.

Since the month is `6`, the expression `month==6` evaluates to `true`. Therefore, the `if...else...if` statement assigns the literal string `'Jun'` to the `monthName` variable. Therefore, you see `Jun` in the console.

If you change the month to a number that is not between 1 and 12, you’ll see the `Invalid Month` in the console because the `else` clause will execute.

#### 2) Using JavaScript if…else…if statement to calculate the body mass index
The following example calculates a body mass index (BMI) of a person. It uses the `if...else...if` statement to determine the weight status based on the BMI:

    let weight = 70; // kg
    let height = 1.72; // meter
    
    // calculate the body mass index (BMI)
    let bmi = weight / (height * height);
    
    let weightStatus;
    
    if (bmi < 18.5) {
      weightStatus = 'Underweight';
    } else if (bmi >= 18.5 && bmi <= 24.9) {
      weightStatus = 'Healthy Weight';
    } else if (bmi >= 25 && bmi <= 29.9) {
      weightStatus = 'Overweight';
    } else {
      weightStatus = 'Obesity';
    }
    
    console.log(weightStatus);

Output:

    `Healthy Weight`
How it works.

-   First, declare two variables that hold the weight in kilogram and height in meter. In a realworld application, you’ll get these values from a web form.
-   Second, calculate the body mass index by dividing the weight by the square of the height.
-   Third, determine the weight status based on the BMI using the `if...else..if` statement.
-   Finally, output the weight status to the console.

### Introduction to JavaScript ternary

When you want to execute a block if a condition evaluates to `true`, you often use an [if…else](https://www.javascripttutorial.net/javascript-if-else/) statement. For example:

    let age = 18;
    let message;
    
    if (age >= 16) {
      message = 'You can drive.';
    } else {
      message = 'You cannot drive.';
    }
    
    console.log(message);

In this example, we show a message that a person can drive if the age is greater than or equal to 16. Alternatively, you can use a ternary operator instead of the [if-else](https://www.javascripttutorial.net/javascript-if-else/) statement like this:

    let age = 18;
    let message;
    
    age >= 16 ? (message = 'You can drive.') : (message = 'You cannot drive.');
    
    console.log(message);

Or you can use the ternary operator in an expression as follows:

    let age = 18;
    let message;
    
    message = age >= 16 ? 'You can drive.' : 'You cannot drive.';
    
    console.log(message);

Here’s the syntax of the ternary operator:

    `condition ? expressionIfTrue : expressionIfFalse;`
In this syntax, the `condition` is an expression that evaluates to a Boolean value, either `true` or `false`.

If the condition is `true`, the first expression (`expresionIfTrue`) executes. If it is false, the second expression (`expressionIfFalse`) executes.

The following shows the syntax of the ternary operator used in an expression:

    `let variableName = condition ? expressionIfTrue : expressionIfFalse;`
In this syntax, if the `condition` is `true`, the `variableName` will take the result of the first expression (`expressionIfTrue`) or `expressionIfFalse` otherwise.

### JavaScript ternary operator examples

Let’s take some examples of using the ternary operator.

#### 1) Using the JavaScript ternary operator to perform multiple statements

The following example uses the ternary operator to perform multiple operations, where each operation is separated by a comma. For example:

    let authenticated = true;
    let nextURL = authenticated
      ? (alert('You will redirect to admin area'), '/admin')
      : (alert('Access denied'), '/403');
    
    // redirect to nextURL here
    console.log(nextURL); // '/admin'

In this example, the returned value of the ternary operator is the last value in the comma-separated list.
#### 2) Simplifying ternary operator example
See the following example:

    let locked = 1;
    let canChange = locked != 1 ? true : false;

If the `locked` is 1, then the `canChange` variable is set to `false`, otherwise, it is set to `true`. In this case, you can simplify it by using a Boolean expression as follows:

    let locked = 1;
    let canChange = locked != 1;

#### 3) Using multiple JavaScript ternary operators example
The following example shows how to use two ternary operators in the same expression:

    let speed = 90;
    let message = speed >= 120 ? 'Too Fast' : speed >= 80 ? 'Fast' : 'OK';
    
    console.log(message);
Output:
```javascript
Fast
```

It’s a good practice to use the ternary operator when it makes the code easier to read. If the logic contains many `if...else` statements, you should avoid using the ternary operators.

# JavaScript switch case
### Introduction to the JavaScript switch case statement
The `switch` statement evaluates an `expression`, compares its result with `case` values, and executes the statement associated with the matching `case` value.

The following illustrates the syntax of the `switch` statement:

    switch (expression) {
        case value1:
            statement1;
            break;
        case value2:
            statement2;
            break;
        case value3:
            statement3;
            break;
        default:
            statement;
    }

How it works.

-   First, evaluate the `expression` inside the parentheses after the `switch` keyword.
-   Second, compare the result of the expression with the `value1`, `value2`, … in the `case` branches from top to bottom. The `switch` statement uses the strict comparison (`===`).
-   Third, execute the statement in the `case` branch where the result of the `expression` equals the value that follows the `case` keyword. The [`break`](https://www.javascripttutorial.net/javascript-break/) statement exits the `switch` statement. If you skip the `break` statement, the code execution falls through the original `case` branch into the next one. If the result of the `expression` does not strictly equal to any value, the `switch` statement will execute the `statement` in the `default` branch.

That the `switch` statement will stop comparing the `expression`‘s result with the remaining case values as long as it finds a match.

The `switch` statement is like the [if…else…if](https://www.javascripttutorial.net/javascript-if-else-if/) statement. But it has more readable syntax.

In practice, you often use a `switch` statement to replace a complex `if...else...if` statement to make the code more readable.

Technically, the `switch` statement is equivalent to the following `if...else...if` statement:

    if (expression === value1) {
      statement1;
    } else if (expression === value2) {
      statement2;
    } else if (expression === value3) {
      statement3;
    } else {
      statement;
    }

### JavaScript switch case examples
Let’s take some examples of using the JavaScript `switch` statement.

#### 1) Using JavaScript switch statement to get the day of the week
The following example uses the `switch` statement to get the day of the week based on a day number:

    let day = 3;
    let dayName;
    
    switch (day) {
      case 1:
        dayName = 'Sunday';
        break;
      case 2:
        dayName = 'Monday';
        break;
      case 3:
        dayName = 'Tuesday';
        break;
      case 4:
        dayName = 'Wednesday';
        break;
      case 5:
        dayName = 'Thursday';
        break;
      case 6:
        dayName = 'Friday';
        break;
      case 7:
        dayName = 'Saturday';
        break;
      default:
        dayName = 'Invalid day';
    }
    
    console.log(dayName); // Tuesday

Output:

    Tuesday
    
How it works.

First, declare the day variable that holds the day number and the day name variable (dayName).

Second, get the day of the week based on the day number using the `switch` statement. If the day is `1`, the day of the week is `Sunday`. If the day is `2`, the day of the week is `Monday`, and so on.

Third, output the day of the week to the console.

#### 2) Using the JavaScript switch statement to get the day count based of a month

The following example uses the `switch` statement to get the day count of a month:

    let year = 2016;
    let month = 2;
    let dayCount;
    
    switch (month) {
      case 1:
      case 3:
      case 5:
      case 7:
      case 8:
      case 10:
      case 12:
        dayCount = 31;
        break;
      case 4:
      case 6:
      case 9:
      case 11:
        dayCount = 30;
        break;
      case 2:
        // leap year
        if ((year % 4 == 0 && !(year % 100 == 0)) || year % 400 == 0) {
          dayCount = 29;
        } else {
          dayCount = 28;
        }
        break;
      default:
        dayCount = -1; // invalid month
    }
    
    console.log(dayCount); // 29

In this example, we have four cases:

-   If the month is 1, 3,5, 7, 8, 10, or 12, the number of days in a month is 31.
-   If the month is 4, 6, 9, or 11, the number of days in that month is 30.
-   If the month is 2, and the year is not the leap year, the number of days is 28. If the year is the leap year, the number of days is 29.
-   If the month is not in the valid range (1-12), the `default` branch executes and sets the `dayCount` variable to -1, which indicates the invalid month.

# JavaScript while Loop and  do…while Loop

### Introduction to the JavaScript while loop statement
The JavaScript `while` statement creates a loop that executes a block as long as a condition evaluates to `true`.

The following illustrates the syntax of the `while` statement:

    while (expression) {
        // statement
    }

The `while` statement evaluates the `expression` before each iteration of the loop.

If the `expression` evaluates to `true`, the `while` statement executes the `statement`. Otherwise, the `while` loop exits.

Because the `while` loop evaluates the `expression` before each iteration, it is known as a pretest loop.

If the `expression` evaluates to `false` before the loop enters, the `while` loop will never execute.

### JavaScript while loop example
The following example uses the `while` statement to output the odd numbers between 1 and 10 to the console:

    let count = 1;
    while (count < 10) {
        console.log(count);
        count +=2;
    }

Output:

    1
    3
    5
    7
    9

How the script works

-   First, declare and initialize the `count` variable to `1`.
-   Second, execute the statement inside the loop if the `count` variable is less than `10`. In each iteration, ouput the count to the console and increase the count by `2`.
-   Third, after `5` iterations, the `count` is `11`. Therefore, the condition `count < 10` is `false`, the loop exits.

### Introduction to the JavaScript do…while statement

The `do...while` loop statement creates a loop that executes a block until a condition evaluates to `false`.

The following statement illustrates the syntax of the `do...while` loop:

    do {
      statement;
    } while(expression);

Unlike the [`while`](https://www.javascripttutorial.net/javascript-while-loop/) loop, the `do-while` loop always executes the `statement` at least once before evaluating the `expression`.

Because the `do...while` loop evaluates expression after each iteration, it’s often referred to as a post-test loop.

Inside the loop body, you need to make changes to some [variables](https://www.javascripttutorial.net/javascript-variables/) to ensure that the `expression` is `false` after some iterations. Otherwise, you’ll have an indefinite loop.

Note that starting with ES6+, the trailing semicolon (`;`) after the `while(expression)` is optional. So you can use the following syntax:

    do {
      statement;
    } while(expression)

In practice, you often use the `do...while` statement when you want to execute the loop body at least once before checking the condition.

### JavaScript do while statement examples

Let’s take some examples of using the do…while statement.

#### 1) Simple JavaScript do while statement example

The following example uses the `do...while` statement to output five numbers from 0 to 4 to the console:

    let count = 0;
    do {
      console.log(count);
      count++;
    } while (count < 5)

Output:

    0
    1
    2
    3
    4

In this example:

-   First, declare and initialize the `count` variable to zero.
-   Second, show the `count` and increase its value by one in each iteration until its value is greater or equal 5.

#### 2) Using the JavaScript do while statement to make a simple number guessing game

The following example uses the `do...while` statement to generate a number guessing game.

The script generates a random integer between 1 and 10. And you have to make a number of guesses until your number matches the random number.

    // generate a secret number between 1 and 10
    const MIN = 1;
    const MAX = 10;
    
    let secretNumber = Math.floor(Math.random() * (MAX - MIN + 1)) + MIN;
    
    let guesses = 0; // for storing the number of guesses
    let hint = ''; // for storing hint
    let number = 0;
    do {
      // get input from user
      let input = prompt(`Please enter a number between ${MIN} and ${MAX}` + hint);
    
      // get the integer
      number = parseInt(input);
    
      // increase the number of guesses
      guesses++;
    
      // check input number with the secret number
      //  provide hint if needed
      if (number > secretNumber) {
        hint = ', and less than ' + number;
      } else if (number < secretNumber) {
        hint = ', and greater than ' + number;
      } else if (number == secretNumber) {
        alert(`Bravo! you're correct after ${guesses} guess(es).`);
      }
    } while (number != secretNumber);

How it works.

-   First, generate a random number between 1 and 10.
-   Second, [prompt](https://www.javascripttutorial.net/javascript-bom/javascript-prompt/) for input an integer and compare it with the secret number. If they are not equal, show a hint. Otherwise, display the congratulation message.

# JavaScript for Loop

### Introduction to the JavaScript for loop statement

The `for` loop statement creates a loop with three optional expressions. The following illustrates the syntax of the `for` loop statement:

    for (initializer; condition; iterator) {
        // statements
    }

#### 1) iterator
The `for` statement executes the `initializer` only once the loop starts. Typically, you declare and initialize a local loop variable in the initializer.

#### 2) condition
The `condition` is a boolean expression that determines whether the `for` should execute the next iteration.

The `for` statement evaluates the `condition` before each iteration. If the condition is `true` (or is not present), it executes the next iteration. Otherwise, it’ll end the loop.

#### 3) iterator
The `for` statement executes the `iterator` after each iteration.

In the `for` loop, the three expressions are optional. The following shows the `for` loop without any 

    expressions:
    for ( ; ; ) {
       // statements
    }

### JavaScript for loop examples
Let’s take some examples of using the `for` loop statement.

#### 1) A simple JavaScript for loop example

The following example uses the `for` loop statement to show numbers from 1 to 4 to console:

    for (let i = 1; i < 5; i++) {
      console.log(i);
    }

Output:

    1
    2
    3
    4

How it works.

-   First, declare a variable `counter` and initialize it to 1.
-   Second, display the value of `counter` in the console if `counter` is less than 5.
-   Third, increase the value of `counter` by one in each iteration of the loop.

#### 2) Using the JavaScript for loop without the initializer example
The following example uses a `for` loop that has no initializer expression:

    let j = 1;
    for (; j < 10; j += 2) {
      console.log(j);
    }

Output:

    1
    3
    5
    7
    9

#### 3) Using the JavaScript for loop without the condition example
Similar to the `initializer` expression, the `condition` expression is optional. If you omit the `condition` expression, you need to use a `[break]` statement to terminate the loop.

    for (let j = 1; ; j += 2) {
      console.log(j);
      if (j > 10) {
        break;
      }
    }

Output:

    1
    3
    5
    7
    9
    11

#### 3) Using the JavaScript for loop statement without any expression example
All three expressions of the `for` loop statements are optional. Therefore, you can omit all of them. For example:

    let j = 1;
    for (;;) {
      if (j > 10) {
        break;
      }
      console.log(j);
      j += 2;
    }

Output:

    1
    3
    5
    7
    9

#### 4) Using the JavaScript for loop without the loop body example
JavaScript allows the `for` statement to have an empty statement. In this case, you place a semicolon (`;`) immediately after the `for` statement.

For example, the following uses a for loop to calculate the sum of 10 numbers from 1 to 10:

    let sum = 0;
    for (let i = 0; i <= 9; i++, sum += i);
    console.log(sum);

Output:
```
55
```

# JavaScript break, continue, Comma Operator

### The label statement
In JavaScript, you can label a statement for later use. Here’s the syntax of the `label` statement:

    label: statement;

In this syntax, the label can be any valid identifier. For example, the following shows how to label a `for` loop using the `outer` label:

    outer: for (let i = 0; i < 5; i++) {
        console.log(i);
    }

Once defining a label, you can reference it in the `break` or `continue` statement.

### Introduction to JavaScript break statement

The `break` statement prematurely terminates a loop such as `for`, `do...while`, and `while` loop, a `switch`, or a `label` statement. Here’s the syntax of the `break` statement:

    break [label];
In this syntax, the `label` is optional if you use the `break` statement in a loop or `switch`. However, if you use the `break` statement with a label statement, you need to specify it.

This tutorial focuses on how to use the `break` statement to terminate the loop prematurely.

### Using JavaScript break statement in a for loop
The following `for` loop statement outputs five numbers from `0` to `4`:
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
Output:
```
0
1
2
3
4
```

To terminate the `for` loop prematurely, you can use a `break` statement. For example, the following illustrates how to use a `break` statement inside a `for` loop:
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
  if (i == 2) {
    break;
  }
}
```

Output:
```
0
1
2
```
In this example, we use an `if` statement inside the loop. If the current value of `i` is `2`, the `if` statement executes the `break` statement that terminates the loop.

### Using the break statement to terminate a nested loop
A nested loop has one loop inside another. For example, the following uses a nested `for` loop to output a pair of numbers from `1` to `3`:

```javascript
for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    console.log(i, j);
  }
}
```

Output:

```
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```
If you use a `break` statement inside an inner loop, it only terminates the enclosing loop. For example:
```javascript
for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    if (i + j == 4) {
      break;
    }
    console.log(i, j);
  }
}
```
Output:
```
1 1
1 2
2 1
```
In this example, if the sum of `i` and `j` is `4`, the `break` statement terminates the inner loop. To terminate the nested loop, you use a label statement. For example:
```javascript
outer: for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    if (i + j == 4) {
      break outer;
    }
    console.log(i, j);
  }
}
```
Output:
```
1 1
1 2
```
In this example, we label the outer loop with the label `outer`. Inside the inner loop, we specify the `outer` label in the `break` statement. The `break` statement to terminate the nested loop if the sum of `i` and `j` is `4`.

### Using JavaScript break statement in a while loop

The following output five numbers from 1 to 5 to the console using a `while` loop:
```javascript
let i = 0;

while (i < 5) {
  i++;
  console.log(i);
}
```
Output:

```
1
2
3
4
5
```
Like a `for` loop, the `break` statement terminates a `while` loop prematurely. For example:
```javascript
let i = 0;

while (i < 5) {
  i++;
  console.log(i);
  if (i == 3) {
    break;
  }
}
```
Output:
```
1
2
3
```
In this example, when the current value of `i` is `3`, the `break` statement terminates the loop. Therefore, you see only three numbers in the output.

### Introduction to the JavaScript continue statement
The `continue` statement terminates the execution of the statement in the current iteration of a loop and immediately continues to the next iteration.

Here’s the syntax of the continue statement:

```javascript
continue [label];
```
In this syntax, the label is optional. It is a valid identifier associated with the label of a statement. For more, check out the `break` statement tutorial for more information on the label statement.

Typically, you use the `continue` with an `if` statement like this:

```javascript
// inside a loop
if(condition){
  continue;
}
```

In this syntax, the `if` statement specifies a condition to execute the `continue` statement inside a loop.
### Using the continue statement in a for loop

When using the `continue` statement in a `for` loop, it doesn’t terminate the loop entirely. Instead, it jumps to the `iterator` expression.

The following example uses a `continue` in a `for` loop to display the odd number in the console:
```javascript
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    continue;
  }
  console.log(i);
}
```
Output:
```
1
3
5
7
9
```
In this example, the `for` loop iterates over the numbers from `0` to `9`.

The `i%2` returns the remainder of the division of the current value of `i` by `2`.

If the remainder is zero, the `if` statement executes the `continue` statement that skips the current iteration of the loop and jumps to the iterator expression `i++`. Otherwise, it outputs the value of `i` to the console.

### Using the continue statement in a while loop

When using the continue statement in a while loop, it doesn’t terminate the execution of the loop entirely. Instead, it jumps back to the condition.

The following example uses a continue statement in a while loop to display the odd numbers from 1 to 10:
```javascript
let i = 0;
while (i < 10) {
  i++;
  if (i % 2 === 0) {
    continue;
  }
  console.log(i);
}
```
Output:

```
1
3
5
7
9
```
### Using the continue statement with a label example
The `continue` statement can include an optional label like this:
```javascript
continue label;
```
The following nested loop displays pairs of numbers from 1 to 2:
```javascript
for (let i = 1; i < 4; i++) {
  for (let j = 1; j < 4; j++) {
    console.log(i, j);
  }
}
```
Output:
```
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```
The following shows how to use the continue statement with a label:
```javascript
outer: for (let i = 1; i < 4; i++) {
  for (let j = 1; j < 4; j++) {
    if (i + j == 3) continue outer;
    console.log(i, j);
  }
}
```
Output:
```
1 1
3 1
3 2
3 3
```

### Introduction to the JavaScript comma operator
JavaScript uses a comma (`,`) to represent the comma operator. A comma operator takes two expressions, evaluates them from left to right, and returns the value of the right expression.

Here’s the syntax of the comma operator:
```
leftExpression, rightExpression
```
For example:
```javascript
let result = (10, 10 + 20);
console.log(result);
```
Output:
```
30
```
In this example, the 10, 10+20 returns the value of the right expression, which is 10+20. Therefore, the result value is 30.

See the following example:
```javascript
let x = 10;
let y = (x++, x + 1);

console.log(x, y);
```

Output:
`11 12`

In this example, we increase the value of `x` by one (`x++`), add one to `x` (`x+1`) and assign `x` to `y`. Therefore, `x` is `11`, and `y` is `12` after the statement.

However, to make the code more explicit, you can use two statements rather than one statement with a comma operator like this:

```javascript
let x = 10;
x++;
let y = x + 1;

console.log(x, y);
```
This code is more explicit.

In practice, you might want to use the comma operator inside a `for` loop to update multiple variables each time through the loop.

The following example uses the comma operator in a for loop to display an array of nine elements as a matrix of 3 rows and three columns:
```javascript
let board = [1, 2, 3, 4, 5, 6, 7, 8, 9];

let s = '';
for (let i = 0, j = 1; i < board.length; i++, j++) {
  s += board[i] + ' ';
  if (j % 3 == 0) {
    console.log(s);
    s = '';
  }
}
```
Output:

```
1 2 3
4 5 6
7 8 9
```

# JavaScript Functions
### Introduction to JavaScript functions
When developing an application, you often need to perform the same action in many places. For example, you may want to show a message whenever an error occurs.

To avoid repeating the same code all over places, you can use a function to wrap that code and reuse it.
### Declare a function
To declare a function, you use the `function` keyword, followed by the function name, a list of parameters, and the function body as follows:
```javascript
function functionName(parameters) {
    // function body
    // ...
}
```
The function name must be a valid JavaScript identifier. By convention, the function names are in camelCase and start with verbs like `getData()`, `fetchContents()`, and `isValid()`.

A function can accept zero, one, or multiple parameters. In the case of multiple parameters, you need to use a comma to separate two parameters.

The following declares a function `say()` that accepts no parameter:
```javascript
function say() {
}
```
The following declares a function named `square()` that accepts one parameter:
```javascript
function square(a) {
}
```
And the following declares a function named `add()` that accepts two parameters:
```javascript
function add(a, b) {
}
```
Inside the function body, you can write the code to implement an action. For example, the following `say()` function simply shows a message to the console:
```javascript
function say(message) {
    console.log(message);
}
```
In the body of the `say()` function, we call the `console.log()` function to output a message to the console.

### Calling a function

To use a function, you need to call it. Calling a function is also known as invoking a function. To call a function, you use its name followed by arguments enclosing in parentheses like this:
```javascript
functionName(arguments);
```
When calling a function, JavaScript executes the code inside the function body. For example, the following shows how to call the `say()` function:
```javascript
say('Hello');
```
In this example, we call the `say()` function and pass a literal string `'Hello'` into it.

### Parameters vs. Arguments
The terms parameters and arguments are often used interchangeably. However, they are essentially different.

When declaring a function, you specify the parameters. However, when calling a function, you pass the arguments that are corresponding to the parameters.

For example, in the `say()` function, the `message` is the parameter and the `'Hello'` string is an argument that corresponds to the `message` parameter.
### Returning a value
Every function in JavaScript implicitly returns `undefined` unless you explicitly specify a return value. For example:
```javascript
function say(message) {
    console.log(message);
}

let result = say('Hello');
console.log('Result:', result);
```
Output:
```javascript
Hello
Result: undefined
```
To specify a return value for a function, you use the `return` statement followed by an expression or a value, like this:
```javascript
return expression;
```
For example, the following `add()` function returns the sum of the two arguments:
```javascript
function add(a, b) {
    return a + b;
}
```
The following shows how to call the `add()` function:
```javascript
let sum = add(10, 20);
console.log('Sum:', sum);
```
Output:
```http
Sum: 30
```
The following example uses multiple `return` statements in a function to return different values based on conditions:
```javascript
function compare(a, b) {
    if (a > b) {
        return -1;
    } else if (a < b) {
        return 1;
    }
    return 0;
}
```
The `compare()` function compares two values. It returns:

-   -1 if the first argument is greater than the second one.
-   1 if the first argument is less than the second one.
-   0 if the first argument equals the second one.

The function immediately stops executing immediately when it reaches the `return` statement. Therefore, you can use the `return` statement without a value to exit the function prematurely, like this:
```javascript
function say(message) {
    // show nothing if the message is empty
    if (! message ) {
        return;
    }
    console.log(message);
}
```
In this example, if the `message` is blank (or `undefined`), the `say()` function will show nothing.

The function can return a single value. If you want to [return multiple values from a function](https://www.javascripttutorial.net/javascript-return-multiple-values/), you need to pack these values in an array or an object.

### Function hoisting

In JavaScript, you can use a function before declaring it. For example:
```javascript
showMe(); // a hoisting example

function showMe(){
    console.log('an hoisting example');
}
```
This feature is called [hoisting](https://www.javascripttutorial.net/javascript-hoisting/).

Function hoisting is a mechanism that the JavaScript engine physically moves function declarations to the top of the code before executing them.

The following shows the version of the code before the JavaScript engine executes it:

    `function showMe(){
        console.log('a hoisting example');
    }
    
    showMe(); // a hoisting example`

### Storing functions in variables
[Functions](https://www.javascripttutorial.net/javascript-function/) are first-class citizens in JavaScript. In other words, you can treat functions like values of other types.

The following defines the `add()` function and assigns the function name to the variable `sum`:
```javascript
function add(a, b) {
    return a + b;
}

let sum = add;
```

In the assignment statement, we don’t include the opening and closing parentheses at the end of the `add` identifier. We also don’t execute the function but reference the function.

By doing this, we can have two ways to execute the same function. For example, we can call it normally as follows:

```javascript
let result = add(10, 20);
```
Alternatively, we can all the `add()` function via the `sum` variable like this:

```javascript
let result = sum(10,20);
```


### Introduction to JavaScript anonymous functions
An anonymous function is a [function](https://www.javascripttutorial.net/javascript-function/) without a name. The following shows how to define an anonymous function:
```javascript
(function () {
   //...
});
```
Note that if you don’t place the anonymous function inside the `()`, you’ll get a syntax error. The `()` makes the anonymous function an expression that returns a function object.

An anonymous function is not accessible after its initial creation. Therefore, you often need to assign it to a variable.

For example, the following shows an anonymous function that displays a message
```javascript
let show = function() {
    console.log('Anonymous function');
};

show();
```
In this example, the anonymous function has no name between the `function` keyword and parentheses `()`. Because we need to call the anonymous function later, we assign the anonymous function to the `show` variable.

### Using anonymous functions as arguments
In practice, you often pass anonymous functions as arguments to other functions. For example:
```javascript
setTimeout(function() {
    console.log('Execute later after 1 second')
}, 1000);
```
In this example, we pass an anonymous function into the `setTimeout()` function. The `setTimeout()` function executes this anonymous function one second later.


### Arrow functions
ES6 introduced [arrow function](https://www.javascripttutorial.net/es6/javascript-arrow-function/) expression that provides a shorthand for declaring anonymous functions:

For example, this function:
```javascript
let show = function () {
    console.log('Anonymous function');
};
```
… can be shortened using the following arrow function:
```javascript
let show = () => console.log('Anonymous function');
```
Similarly, the following anonymous function:
```javascript
let add = function (a, b) {
    return a + b;
};
```
… is functionally equivalent to the following arrow function:
```javascript
let add = (a, b) => a + b;
```
# JavaScript Recursive Function
## Introduction to the JavaScript recursive functions
A recursive function is a [function](https://www.javascripttutorial.net/javascript-function/) that calls itself until it doesn’t. And this technique is called recursion.

Suppose that you have a function called `recurse()`. The `recurse()` is a recursive function if it calls itself inside its body, like this:
```javascript
function recurse() {
    // ...
    recurse();
    // ...
}
```
A recursive function always has a condition to stop calling itself. Otherwise, it will call itself indefinitely. So a recursive function typically looks like the following:
```javascript
function recurse() {
    if(condition) {
        // stop calling itself
        //...
    } else {
        recurse();
    }
}
```
Generally, you use recursive functions to break down a big problem into smaller ones. Typically, you will find the recursive functions in data structures like binary trees and graphs and algorithms such as binary search and quicksort.

### JavaScript recursive function examples
Let’s take some examples of using recursive functions.

#### 1) A simple JavaScript recursive function example

Suppose that you need to develop a function that counts down from a specified number to 1. For example, to count down from 3 to 1:
```
3
2
1
```
The following shows the `countDown()` function:
```javascript
function countDown(fromNumber) {
    console.log(fromNumber);
}

countDown(3);
```
This `countDown(3)` shows only the number 3.

To count down from the number 3 to 1, you can:

1.  show the number 3.
2.  and call the `countDown(2)` that shows the number 2.
3.  and call the `countDown(1)` that shows the number 1.

The following changes the `countDown()` to a recursive function:
```javascript
function countDown(fromNumber) {
    console.log(fromNumber);
    countDown(fromNumber-1);
}

countDown(3);
```
This `countDown(3)` will run until the call stack size is exceeded, like this:
```javascript
Uncaught RangeError: Maximum call stack size exceeded.
```
… because it doesn’t have the condition to stop calling itself.

The count down will stop when the next number is zero. Therefore, you add an [if condition](https://www.javascripttutorial.net/javascript-if/) as follows:
```javascript
function countDown(fromNumber) {
    console.log(fromNumber);

    let nextNumber = fromNumber - 1;

    if (nextNumber > 0) {
        countDown(nextNumber);
    }
}
countDown(3);
```
Output:
```
3
2
1
```
The `countDown()` seems to work as expected.

However, as mentioned in the [Function type tutorial](https://www.javascripttutorial.net/javascript-function-type/), the function’s name is a reference to the actual function object.

If the function name is set to `null` somewhere in the code, the recursive function will stop working.

For example, the following code will result in an error:
```javascript
let newYearCountDown = countDown;
// somewhere in the code
countDown = null;
// the following function call will cause an error
newYearCountDown(10);
```
Error:
`Uncaught TypeError: countDown is not a function`
How the script works:

-   First, assign the `countDown` function name to the variable `newYearCountDown`.
-   Second, set the `countDown` function reference to `null`.
-   Third, call the `newYearCountDown` function.

The code causes an error because the body of the `countDown()` function references the `countDown` function name, which was set to `null` at the time of calling the function.

To fix it, you can use a named function expression as follows:
```javascript
let countDown = function f(fromNumber) {
    console.log(fromNumber);

    let nextNumber = fromNumber - 1;

    if (nextNumber > 0) {
        f(nextNumber);
    }
}

let newYearCountDown = countDown;
countDown = null;
newYearCountDown(10);
```
#### 2) Calculate the sum of n natural numbers example

Suppose you need to calculate the sum of natural numbers from 1 to n using the recursion technique. To do that, you need to define the `sum()` recursively as follows:
```
sum(n) = n + sum(n-1)
sum(n-1) = n - 1 + sum(n-2)
...
sum(1) = 1
```
The following illustrates the `sum()` recursive function:
```javascript
function sum(n) {
  if (n <= 1) {
    return n;
  }
  return n + sum(n - 1);
}
```
# JavaScript Default Parameters
In JavaScript, default function parameters allow you to initialize named parameters with default values if no values or `undefined` are passed into the function.

    `function say(message='Hi') {
        console.log(message);
    }
    
    say(); // 'Hi'
    say('Hello') // 'Hello'`

The default value of the `message` paramater in the `say()` function is `'Hi'`.

### Arguments vs. Parameters
Sometimes, you can use the terms argument and parameter interchangeably. However, by definition, parameters are what you specify in the [function declaration](https://www.javascripttutorial.net/javascript-function/) whereas the arguments are what you pass into the function.

Consider the following `add()` function:
```javascript
function add(x, y) {
   return x + y;
}

add(100,200);
```
In this example, the `x` and `y` are the parameters of the `add()` function, and the values passed to the `add()` function `100` and `200` are the arguments.

### Setting JavaScript default parameters for a function

In JavaScript, a parameter has a default value of [undefined](https://www.javascripttutorial.net/javascript-data-types/#undefined). It means that if you don’t pass the arguments into the [function](https://www.javascripttutorial.net/javascript-function/), its parameters will have the default values of `undefined`.

See the following example:

    function say(message) {
        console.log(message);
    }
    
    say(); // undefined`

The `say()` function takes the `message` parameter. Because we didn’t pass any argument into the `say()` function, the value of the `message` parameter is `undefined`.

Suppose that you want to give the `message` parameter a default value 10.

A typical way for achieving this is to test parameter value and assign a default value if it is `undefined` using a [ternary operator](https://www.javascripttutorial.net/javascript-ternary-operator/):

    function say(message) {
        message = typeof message !== 'undefined' ? message : 'Hi';
        console.log(message);
    }
    say(); // 'Hi'

In this example, we didn’t pass any value into the `say()` function. Therefore, the default value of the message argument is `undefined`. Inside the function, we reassigned the `message` variable the `Hi` string.

ES6 provides you with an easier way to set the default values for the function parameters like this:
```javascript
function fn(param1=default1, param2=default2,..) {
}
```
In the syntax above, you use the [assignment operator](https://www.javascripttutorial.net/javascript-assignment-operators/) (`=`) and the default value after the parameter name to set a default value for that parameter. For example:

    function say(message='Hi') {
        console.log(message);
    }
    
    say(); // 'Hi'
    say(undefined); // 'Hi'
    say('Hello'); // 'Hello'

How it works.

-   In the first function call, we didn’t pass any argument into the `say()` function, therefore `message` parameter took the default value `'Hi'`.
-   In the second function call, we passed the `undefined` into the `say()` function, hence the `message` parameter also took the default value `'Hi'`.
-   In the third function call, we passed the `'Hello'` string into the `say()` function, therefore `message` parameter took the string `'Hello'` as the default value.

### More JavaScript default parameter examples

Let’s look at some more examples to learn some available options for setting default values of the function parameters.

#### 1) Passing undefined arguments

The following `createDiv()` function creates a new `<div>` element in the document with a specific height, width, and border-style:

    function createDiv(height = '100px', width = '100px', border = 'solid 1px red') {
        let div = document.createElement('div');
        div.style.height = height;
        div.style.width = width;
        div.style.border = border;
        document.body.appendChild(div);
        return div;
    }

The following doesn’t pass any arguments to the function so the `createDiv()` function uses the default values for the parameters.

```
createDiv();
```
Suppose you want to use the default values for the height and width parameters and specific border style. In this case, you need to pass `undefined` values to the first two parameters as follows:

```javascript
createDiv(undefined,undefined,'solid 5px blue');
```
#### 2) Evaluating default parameters

JavaScript engine evaluates the default arguments at the time you call the function. See the following example:

    function put(toy, toyBox = []) {
        toyBox.push(toy);
        return toyBox;
    }
    
    console.log(put('Toy Car'));
    // -> ['Toy Car']
    console.log(put('Teddy Bear'));
    // -> ['Teddy Bear'], not ['Toy Car','Teddy Bear']

The parameter can take a default value which is a result of a function.

Consider the following example:

    function date(d = today()) {
        console.log(d);
    }
    function today() {
        return (new Date()).toLocaleDateString("en-US");
    }
    date();

The `date()` function takes one parameter whose default value is the returned value of the `today()` function. The `today()` function returns today’s date in a specified string format.

When we declared the `date()` function, the `today()` function has not yet evaluated until we called the `date()` function.

We can use this feature to make arguments mandatory. If the caller doesn’t pass any argument, we throw an error as follows:

    function requiredArg() {
       throw new Error('The argument is required');
    }
    function add(x = requiredArg(), y = requiredArg()){
       return x + y;
    }
    
    add(10); // error
    add(10,20); // OK

#### 3) Using other parameters in default values
You can assign a parameter a default value that references other default parameters as shown in the following example:

    function add(x = 1, y = x, z = x + y) {
        return x + y + z;
    }
    
    console.log(add()); // 4

In the `add()` function:

-   The default value of the `y` is set to `x` parameter.
-   The default value of the `z` is the sum of `x` and `y`
-   The `add()` function returns the sum of `x`, `y`, and `z`.

The parameter list seems to have its own [scope](https://www.javascripttutorial.net/javascript-variable-scope/). If you reference the parameter that has not been initialized yet, you will get an error. For example:

    function subtract( x = y, y = 1 ) {
        return x - y;
    }
    subtract(10);

Error message:

    Uncaught ReferenceError: Cannot access 'y' before initialization

### Using functions

You can use a return value of a function as a default value for a parameter. For example:

    let taxRate = () => 0.1;
    let getPrice = function( price, tax = price * taxRate() ) {
        return price + tax;
    }
    
    let fullPrice = getPrice(100);
    console.log(fullPrice); // 110

In the `getPrice()` function, we called the `taxRate()` function to get the tax rate and use this tax rate to calculate the tax amount from the price.

### The arguments object

The value of the `arguments` object inside the function is the number of actual arguments that you pass to the function. For example:

    function add(x, y = 1, z = 2) {
        console.log( arguments.length );
        return x + y + z;
    }
    
    add(10); // 1
    add(10, 20); // 2
    add(10, 20, 30); // 3

Now, you should understand the JavaScript default function parameters and how to use them effectively.

# Javascript Object Methods
### Introduction to the JavaScript object methods

An object is a collection of key/value pairs or [properties](https://www.javascripttutorial.net/javascript-object-properties/). When the value is a function, the property becomes a method. Typically, you use methods to describe the object behaviors.

For example, the following adds the `greet` method to the `person` object:
```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};

person.greet = function () {
    console.log('Hello!');
}

person.greet();
```
Output:

    Hello!

In this example:

-   First, use a function expression to define a function and assign it to the `greet` property of the `person` object.
-   Then, call the method `greet()` method.

Besides using a function expression, you can define a function and assign it to an object like this:
```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};

function greet() {
    console.log('Hello, World!');
}

person.greet = greet;

person.greet();
```

In this example:

-   First, define the `greet()` function as a regular function.
-   Second, assign the function name to the the `greet` property of the `person` object.
-   Third, call the `greet()` method.

### Object method shorthand

JavaScript allows you to define methods of an object using the object literal syntax as shown in the following example:

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe',
    greet: function () {
        console.log('Hello, World!');
    }
};
```
ES6 provides you with the [concise method syntax](https://www.javascripttutorial.net/es6/object-literal-extensions/) that allows you to define a method for an object:
```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe',
    greet() {
        console.log('Hello, World!');
    }
};

person.greet();
```
This syntax looks much cleaner and less verbose.

### The this value

Typically, methods need to access other properties of the object.

For example, you may want to define a method that returns the full name of the person object by concatenating the first name and last name.

Inside a method, the `this` value references the object that invokes the method. Therefore, you can access a property using the `this` value as follows:

```javascript
this.propertyName
```
The following example uses the `this` value in the `getFullName()` method:
```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe',
    greet: function () {
        console.log('Hello, World!');
    },
    getFullName: function () {
        return this.firstName + ' ' + this.lastName;
    }
};


console.log(person.getFullName());
```
Output

    'John Doe'

# JavaScript Constructor Function

### Introduction to JavaScript constructor functions
In the [JavaScript objects tutorial](https://www.javascripttutorial.net/javascript-objects/), you learned how to use the object literal syntax to create a new object.

For example, the following creates a new person object with two properties `firstName` and `lastName`:
```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};
```
In practice, you often need to create many similar objects like the `person` object.

To do that, you can use a constructor function to define a custom type and the `new` operator to create multiple objects from this type.

Technically speaking, a constructor function is a regular [function](https://www.javascripttutorial.net/javascript-function/) with the following convention:

-   The name of a constructor function starts with a capital letter like `Person`, `Document`, etc.
-   A constructor function should be called only with the `new` operator.

The following example defines a constructor function called `Person`:
```javascript
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}
```
In this example, the `Person` is the same as a regular function except that its name starts with the capital letter `P`.

To create a new instance of the `Person`, you use the `new` operator:
```javascript
let person = new Person('John','Doe');
```
Basically, the `new` operator does the following:

-   Create a new empty object and assign it to the `this` variable.
-   Assign the arguments `'John'` and `'Doe'` to the `firstName` and `lastName` properties of the object.
-   Return the `this` value.

It’s functionally equivalent to the following:
```javascript
function Person(firstName, lastName) {
    // this = {};

    // add properties to this
    this.firstName = firstName;
    this.lastName = lastName;

    // return this;
}
```
Therefore, the following statement:

```javascript
let person = new Person('John','Doe');
```
… returns the same result as the following statement:
```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};
```
However, the constructor function `Person` allows you to create multiple similar objects. For example:
```javascript
let person1 = new Person('Jane','Doe')
let person2 = new Person('James','Smith')
```
### Adding methods to JavaScript constructor functions
An object may have methods that manipulate its data. To add a method to an object created via the constructor function, you can use the `this` keyword. For example:
```javascript
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;

    this.getFullName = function () {
        return this.firstName + " " + this.lastName;
    };
}
```
Now, you can create a new `Person` object and invoke the `getFullName()` method:
```javascript
let person = new Person("John", "Doe");
console.log(person.getFullName());
```
Output:
```
John Doe
```
The problem with the constructor function is that when you create multiple instances of the `Person`, the `this.getFullName()` is duplicated in every instance, which is not memory efficient.

To resolve this, you can use the [prototype](https://www.javascripttutorial.net/javascript-prototype/) so that all instances of a custom type can share the same methods.
### Returning from constructor functions

Typically, a constructor function implicitly returns `this` that set to the newly created object. But if it has a `return` statement, then here’s are the rules:

-   If `return` is called with an object, the constructor function returns that object instead of `this`.
-   If `return` is called with a value other than an object, it is ignored.

### Calling a constructor function without the `new` keyword

Technically, you can call a constructor function like a regular function without using the `new` keyword like this:
```javascript
let person = Person('John','Doe');
```
In this case, the `Person` just executes like a regular function. Therefore, the `this` inside the `Person` function doesn’t bind to the `person` variable but the [global object](https://www.javascripttutorial.net/es-next/javascript-globalthis/).

If you attempt to access the `firstName` or `lastName` property, you’ll get an error:
```css
console.log(person.firstName);
```
Error:

    TypeError: Cannot read property 'firstName' of undefined
Similarly, you cannot access the `getFullName()` method since it’s bound to the global object.
```css
person.getFullName();
```
Error:

    TypeError: Cannot read property 'getFullName' of undefined

To prevent a constructor function to be invoked without the `new` keyword, ES6 introduced the `[new.target](https://www.javascripttutorial.net/es6/javascript-new-target/)` property.

If a constructor function is called with the `new` keyword, the `new.target` returns a reference of the function. Otherwise, it returns `undefined`.

The following adds a statement inside the `Person` function to show the `new.target` to the console:

```javascript
function Person(firstName, lastName) {
    console.log(new.target);

    this.firstName = firstName;
    this.lastName  = lastName;

    this.getFullName = function () {
        return this.firstName + " " + this.lastName;
    };
}
```
The following returns `undefined` because the `Person` constructor function is called like a regular function:
```javascript
let person = Person("John", "Doe");
```
Output:
```javascript
undefined
```
However, the following returns a reference to the `Person` function because it’s called with the `new` keyword:
```javascript
let person = new Person("John", "Doe");
```
Output:
```json
[Function: Person]
```
By using the `new.target`, you can force the callers of the constructor function to use the `new` keyword. Otherwise, you can throw an error like this:
```javascript
function Person(firstName, lastName) {
    if (!new.target) {
        throw Error("Cannot be called without the new keyword");
    }

    this.firstName = firstName;
    this.lastName = lastName;
}
```
Alternatively, you can make the syntax more flexible by creating a new `Person` object if the users of the constructor function don’t use the `new` keyword:
```javascript
function Person(firstName, lastName) {
    if (!new.target) {
        return new Person(firstName, lastName);
    }

    this.firstName = firstName;
    this.lastName = lastName;
}

let person = Person("John", "Doe");

console.log(person.firstName);
```
This pattern is often used in JavaScript libraries and frameworks to make the syntax more flexible.


# Demystifying the JavaScript this Keyword
If you have been working with other programming languages such as Java, [C#](https://www.csharptutorial.net/csharp-tutorial/csharp-this/), or [PHP](https://www.phptutorial.net/php-oop/php-this/), you’re already familiar with the `this` keyword.

In these languages, the `this` keyword represents the current instance of the class. And it is only relevant within the class.

JavaScript also has `this` keyword. However, the `this` keyword in JavaScript behaves differently from other programming languages.

In JavaScript, you can use the `this` keyword in the [global and function contexts](https://www.javascripttutorial.net/javascript-execution-context/). Moreover, the behavior of the `this` keyword changes between strict and non-strict modes.

### What is this keyword
In general, the `this` references the object of which the function is a property. In other words, the `this` references the object that is currently calling the function.

Suppose you have an object called `counter` that has a method `next()`. When you call the `next()` method, you can access the `this` object.
```javascript
let counter = {
  count: 0,
  next: function () {
    return ++this.count;
  },
};

counter.next();
```
Inside the `next()` function, the `this` references the `counter` object. See the following method call:
```css
counter.next();
```
The `next()` is a function that is the property of the `counter` object. Therefore, inside the `next()` function, the `this` references the `counter` object.

### Global context
In the global context, the `this` references the [global object](https://www.javascripttutorial.net/es-next/javascript-globalthis/), which is the `window` object on the web browser or `global` object on Node.js.

This behavior is consistent in both strict and non-strict modes. Here’s the output on the web browser:

    console.log(this === window); // true

If you assign a property to `this` object in the global context, JavaScript will add the property to the global object as shown in the following example:

    this.color= 'Red';
    console.log(window.color); // 'Red'

### Function context

In JavaScript, you can call a [function](https://www.javascripttutorial.net/javascript-function/) in the following ways:

-   Function invocation
-   Method invocation
-   Constructor invocation
-   Indirect invocation

Each function invocation defines its own context. Therefore, the `this` behaves differently.

#### 1) Simple function invocation

In the non-strict mode, the `this` references the global object when the function is called as follows:
```javascript
function show() {
   console.log(this === window); // true
}

show();
```
When you call the `show()` function, the `this` references the [global object](https://www.javascripttutorial.net/es-next/javascript-globalthis/), which is the `window` on the web browser and `global` on Node.js.

Calling the `show()` function is the same as:
```javascript
window.show();
```
In the strict mode, JavaScript sets the `this` inside a function to `undefined`. For example:
```javascript
"use strict";

function show() {
    console.log(this === undefined);
}

show();
```
To enable the strict mode, you use the directive `"use strict"` at the beginning of the JavaScript file. If you want to apply the strict mode to a specific function only, you place it at the top of the function body.

Note that the strict mode has been available since ECMAScript 5.1. The `strict` mode applies to both function and nested functions. For example:
```javascript
function show() {
    "use strict";
    console.log(this === undefined); // true

    function display() {
        console.log(this === undefined); // true
    }
    display();
}

show();
```
Output:

    true
    true

In the `display()` inner function, the `this` also set to `undefined` as shown in the console.

### 2) Method invocation

When you call a method of an object, JavaScript sets `this` to the object that owns the method. See the following `car` object

    let car = {
        brand: 'Honda',
        getBrand: function () {
            return this.brand;
        }
    }
    
    console.log(car.getBrand()); // Honda

In this example, the `this` object in the `getBrand()` method references the `car` object.

Since a method is a property of an object which is a value, you can store it in a variable.
```javascript
let brand = car.getBrand;
```
And then call the method via the variable

    console.log(brand()); // undefined

You get `undefined` instead of `"Honda"` because when you call a method without specifying its object, JavaScript sets `this` to the global object in non-strict mode and `undefined` in the strict mode.

To fix this issue, you use the `[bind()](https://www.javascripttutorial.net/javascript-bind/)` method of the `Function.prototype` object. The `bind()` method creates a new function whose the `this` keyword is set to a specified value.
```javascript
let brand = car.getBrand.bind(car);
console.log(brand()); // Honda
```
In this example, when you call the `brand()` method, the `this` keyword is bound to the `car` object. For example:
```javascript
let car = {
    brand: 'Honda',
    getBrand: function () {
        return this.brand;
    }
}

let bike = {
    brand: 'Harley Davidson'
}

let brand = car.getBrand.bind(bike);
console.log(brand());
```
Output:

    Harley Davidson

In this example, the `bind()` method sets the `this` to the `bike` object, therefore, you see the value of the `brand` property of the `bike` object on the console.

### 3) Constructor invocation

When you use the `new` keyword to create an instance of a function object, you use the function as a constructor.

The following example declares a `Car` function, then invokes it as a constructor:

```javascript
function Car(brand) {
    this.brand = brand;
}

Car.prototype.getBrand = function () {
    return this.brand;
}

let car = new Car('Honda');
console.log(car.getBrand());
```
The expression `new Car('Honda')` is a constructor invocation of the `Car` function.

JavaScript creates a new object and sets `this` to the newly created object. This pattern works great with only one potential problem.

Now, you can invoke the `Car()` as a function or as a constructor. If you omit the `new` keyword as follows:

    var bmw = Car('BMW');
    console.log(bmw.brand);
    // => TypeError: Cannot read property 'brand' of undefined

Since the `this` value in the `Car()` sets to the global object, the `bmw.brand` returns `undefined`.

To make sure that the `Car()` function is always invoked using constructor invocation, you add a check at the beginning of the `Car()` function as follows:
```javascript
function Car(brand) {
    if (!(this instanceof Car)) {
        throw Error('Must use the new operator to call the function');
    }
    this.brand = brand;
}
```
ES6 introduced a meta-property named [`new.target`](https://www.javascripttutorial.net/es6/javascript-new-target/) that allows you to detect whether a function is invoked as a simple invocation or as a constructor.

You can modify the `Car()` function that uses the `new.target` metaproperty as follows:
```javascript
function Car(brand) {
    if (!new.target) {
        throw Error('Must use the new operator to call the function');
    }
    this.brand = brand;
}
```
### 4) Indirect Invocation
In JavaScript, [functions are first-class citizens](https://www.javascripttutorial.net/javascript-functions-are-first-class-citizens/). In other words, functions are objects, which are instances of the [Function type](https://www.javascripttutorial.net/javascript-function-type/).

The `Function` type has two methods: `call()` and `apply()` . These methods allow you to set the `this` value when calling a function. For example:

```javascript
function getBrand(prefix) {
    console.log(prefix + this.brand);
}

let honda = {
    brand: 'Honda'
};
let audi = {
    brand: 'Audi'
};

getBrand.call(honda, "It's a ");
getBrand.call(audi, "It's an ");
```
Output:
```php
It's a Honda
It's an Audi
```
In this example, we called the `getBrand()` function indirectly using the `call()` method of the `getBrand` function. We passed `honda` and `audi` object as the first argument of the `call()` method, therefore, we got the corresponding brand in each call.

The `apply()` method is similar to the `call()` method except that its second argument is an array of arguments.
```javascript
getBrand.apply(honda, ["It's a "]); // "It's a Honda"
getBrand.apply(audi, ["It's an "]); // "It's a Audi"
```
### Arrow functions

[ES6](https://www.javascripttutorial.net/es6/) introduced a new concept called [arrow function](https://www.javascripttutorial.net/es6/javascript-arrow-function/). In arrow functions, JavaScript sets the `this` lexically.

It means the arrow function does not create its own [execution context](https://www.javascripttutorial.net/javascript-execution-context/) but inherits the `this` from the outer function where the arrow function is defined. See the following example:

    let getThis = () => this;
    console.log(getThis() === window); // true
In this example, the `this` value is set to the global object i.e., `window` in the web browser.

Since an arrow function does not create its own execution context, defining a method using an arrow function will cause an issue. For example:
```javascript
function Car() {
  this.speed = 120;
}

Car.prototype.getSpeed = () => {
  return this.speed;
};

var car = new Car();
console.log(car.getSpeed());
```
Inside the `getSpeed()` method, the `this` value reference the global object, not the `Car` object but the global object doesn’t have a property called speed. Therefore, the `this.speed` in the `getSpeed()` method returns `undefined`.

# JavaScript Object Properties
### Object Property types

JavaScript specifies the characteristics of properties of [objects](https://www.javascripttutorial.net/javascript-objects/) via internal attributes surrounded by the two pairs of square brackets, e.g., `[[Enumerable]]`.

Objects have two types of properties: data and accessor properties.
#### 1) Data properties

A data property contains a single location for a data value. A data property has four attributes:

-   `[[Configurarable]]` – determines whether a property can be redefined or removed via `delete` operator.
-   `[[Enumerable]]` – indicates if a property can be returned in the `[for...in](https://www.javascripttutorial.net/javascript-for-in/)` loop.
-   `[[Writable]]` – specifies that the value of a property can be changed.
-   `[[Value]]` – contains the actual value of a property.

By default, the `[[Configurable]]` , `[[Enumerable]]`And `[[Writable]]` attributes set to `true` for all properties defined directly on an object. The default value of the`[[Value]]` attribute is `undefined`.

The following example creates a `person` object with two properties `firstName` and `lastName` with the configurable, enumerable, and writable attributes set to `true`. And their values are set to `'John'` and `'Doe'` respectively:
```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};
```
To change any attribute of a property, you use the `Object.defineProperty()` method.

The `Object.defineProperty()` method accepts three arguments:

-   An object.
-   A property name of the object.
-   A property descriptor object that has four properties: `configurable`, `enumerable`, `writable`, and `value`.

If you use the `Object.defineProperty()` method to define a property of the object, the default values of `[[Configurable]]`, `[[Enumerable]]`, and `[[Writable]]` are set to `false` unless otherwise specified.

The following example creates a `person` object with the `age` property:
```javascript
let person = {};
person.age = 25;
```
Since the default value of the `[[Configurable]]` attribute is set to `true`, you can remove it via the `delete` operator:
```javascript
delete person.age;
console.log(person.age);
```
Output:
```javascript
undefined
```
The following example creates a `person` object and adds the `ssn` property to it using the `Object.defineProperty()` method:
```javascript
'use strict';

let person = {};

Object.defineProperty(person, 'ssn', {
    configurable: false,
    value: '012-38-9119'
});

delete person.ssn;
```
Output:
```php
TypeError: Cannot delete property 'ssn' of #<Object>
```
In this example, the `configurable` attribute is set to `false`. herefore, deleting the `ssn` property causes an error.

Also, once you define a property as non-configurable, you cannot change it to configurable.

If you use the `Object.defineProperty()` method to change any attribute other than the writable, you’ll get an error. or example:
```javascript
'use strict';

let person = {};

Object.defineProperty(person, 'ssn', {
    configurable: false,
    value: '012-38-9119'
});


Object.defineProperty(person, 'ssn', {
    configurable: true
});
```
Output:
```javascript
TypeError: Cannot redefine property: ssn
```
By default, the `enumerable` attribute of all the properties defined on an object is `true`. t means that you can iterate over all object properties using the [`for...in`](https://www.javascripttutorial.net/javascript-for-in/) loop like this:
```javascript
let person = {};
person.age = 25;
person.ssn = '012-38-9119';

for (let property in person) {
    console.log(property);
}
```
Output:
```
age
ssn
```
The following makes the `ssn` property non-enumerable by setting the `enumerable` attribute to `false`.
```javascript
let person = {};
person.age = 25;
person.ssn = '012-38-9119';

Object.defineProperty(person, 'ssn', {
    enumerable: false
});

for (let prop in person) {
    console.log(prop);
}
```
Output
```
age
```
#### 2) Accessor properties

Similar to data properties, accessor properties also have `[[Configurable]]` and `[[Enumerable]]` attributes.

But the accessor properties have the `[[Get]]` and `[[Set]]` attributes instead of `[[Value]]` and `[[Writable]]`.

When you read data from an accessor property, the `[[Get]]` function is called automatically to return a value. The default return value of the `[[Get]]` function is `undefined`.

If you assign a value to an accessor property, the `[[Set]]` function is called automatically.

To define an accessor property, you must use the `Object.defineProperty()` method. or example:

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
}

Object.defineProperty(person, 'fullName', {
    get: function () {
        return this.firstName + ' ' + this.lastName;
    },
    set: function (value) {
        let parts = value.split(' ');
        if (parts.length == 2) {
            this.firstName = parts[0];
            this.lastName = parts[1];
        } else {
            throw 'Invalid name format';
        }
    }
});

console.log(person.fullName);
```
Output:

    'John Doe'

In this example:

-   First, define the `person` object that contains two properties: `firstName` and `lastName`.
-   Then, add the `fullName` property to the `person` object as an accessor property.

In the `fullname` accessor property:

-   The `[[Get]]` returns the full name that is the result of [concatenating](https://www.javascripttutorial.net/javascript-string-concat/) of `firstName`, `space`, and `lastName`.
-   The `[[Set]]` method [splits](https://www.javascripttutorial.net/javascript-string-split/) the argument by the space and assigns the `firstName` and `lastName` properties the corresponding parts of the name.
-   If the full name is not in the correct format i.e., first name, space, and last name, it will [throw an error](https://www.javascripttutorial.net/es6/promise-error-handling/).


### Define multiple properties: `Object.defineProperties()`

In ES5, you can define multiple properties in a single statement using the `Object.defineProperties()` method. or example:

```javascript
var product = {};

Object.defineProperties(product, {
    name: {
        value: 'Smartphone'
    },
    price: {
        value: 799
    },
    tax: {
        value: 0.1
    },
    netPrice: {
        get: function () {
            return this.price * (1 + this.tax);
        }
    }
});

console.log('The net price of a ' + product.name + ' is ' + product.netPrice.toFixed(2) + ' USD');
```
Output:

    The net price of a Smartphone is 878.90 USD

In this example, we defined three data properties: `name`, `price`, and `tax`, and one accessor property `netPrice` for the `product` object.

### JavaScript object property descriptor

The `Object.getOwnPropertyDescriptor()` method allows you to get the descriptor object of a property. The `Object.getOwnPropertyDescriptor()` method takes two arguments:

1.  An object
2.  A property of the object

It returns a descriptor object that describes a property. The descriptor object has four properties: configurable, enumerable, writable, and value.

The following example gets the descriptor object of the `name` property of the `product` object in the prior example.

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};


let descriptor = Object.getOwnPropertyDescriptor(person, 'firstName');

console.log(descriptor);
```
Output:

```javascript
{ value: 'John',
  writable: true,
  enumerable: true,
  configurable: true }
```

# JavaScript for…in Loop, Object.values(), Object.entries()
### Introduction to JavaScript `for...in` loop

The `for...in` loop over the [enumerable properties](https://www.javascripttutorial.net/javascript-enumerable-properties/) that are keyed by strings of an [object](https://www.javascripttutorial.net/javascript-objects/). Note that a property can be keyed by a string or a [symbol](https://www.javascripttutorial.net/es6/symbol/).

A property is enumerable when its internal `enumerable` flag is set to `true`.

The `enumerable` flag defaults to `true` when a property is created via a simple assignment or via a property initializer:
```
object.propertyName = value;
```
or
```javascript
let obj = {
    propertyName: value,
    ...
};
```
The following shows the syntax of the `for...in` loop:
```javascript
for(const propertyName in object) {
    // ...
}
```
The `for...in` allows you to access each property and value of an object without knowing the specific name of the property. For example:

```javascript
var person = {
    firstName: 'John',
    lastName: 'Doe',
    ssn: '299-24-2351'
};

for(var prop in person) {
    console.log(prop + ':' + person[prop]);
}
```
Output:
```javascript
firstName:John
lastName:Doe
ssn:299-24-2351
```
In this example, we used the `for...in` loop to iterate over the properties of the person object. We accessed the value of each property using the following syntax:
```javascript
object[property];
```
### The `for...in` loop & Inheritance

When you loop over the properties of an object that [inherits](https://www.javascripttutorial.net/javascript-prototypal-inheritance/) from another object, the `for...in` statement goes up in the [prototype](https://www.javascripttutorial.net/javascript-prototype/) chain and enumerates over inherited properties. Consider the following example:
```javascript
var decoration = {
    color: 'red'
};

var circle = Object.create(decoration);
circle.radius = 10;


for(const prop in circle) {
    console.log(prop);
}
```
Output:

    radius
    color

The `circle` object has its own prototype that references the `decoration` object. Therefore, the `for...in` loop displays the properties of the `circle` object and its prototype.

If you want to enumerate only the [own properties](https://www.javascripttutorial.net/javascript-own-properties/) of an object, you use the `hasOwnProperty()` method:
```javascript
for(const prop in circle) {
    if(circle.hasOwnProperty(prop)) {
        console.log(prop);
    }
}
```
Output:

    radius

### The `for...in` loop and Array

It’s good practice to not use the `for...in` to iterate over an [array](https://www.javascripttutorial.net/javascript-array/), especially when the order of the array elements is important.

The following example works flawlessly:
```javascript
const items = [10 , 20, 30];
let total = 0;

for(const item in items) {
    total += items[item];
}
console.log(total); 
```
However, someone may set a property of the built-in [`Array`](https://www.javascripttutorial.net/javascript-array/) type in their libraries as follows:
```javascript
Array.prototype.foo = 100;
```
Hence, the `for...in` will not work correctly. For example:
```javascript
// somewhere else
Array.prototype.foo = 100;

const items = [10, 20, 30];
let total = 0;

for (var prop in items) {
  console.log({ prop, value: items[prop] });
  total += items[prop];
}
console.log(total);
```
Output:
```javascript
{ prop: '0', value: 10 }
{ prop: '1', value: 20 }
{ prop: '2', value: 30 }
{ prop: 'foo', value: 100 }
160
```
Or another example:
```javascript
var arr = [];
// set the third element to 3, other elements are `undefined`
arr[2] = 3; 

for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);    
}
```
The output shows three elements of the array, which is correct:

    undefined
    undefined
    3

However, the `for...in` loop ignores the first two elements:
```javascript
for (const key in arr) {
    console.log(arr[key]);
}
```
Output:

    3

The output shows only the third element, not the first two elements.

### JavaScript Object.values()
Prior to ES2017, you use a `for...in` loop and `Object.hasOwnProperty()` method to access values of [own](https://www.javascripttutorial.net/javascript-own-properties/) [enumerable properties](https://www.javascripttutorial.net/javascript-enumerable-properties/) of an [object](https://www.javascripttutorial.net/javascript-objects/). For example:

```javascript
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 25
};

for (const key in person) {
    if (person.hasOwnProperty(key)) {
        const value = person[key];
        console.log(value);

    }
}
```
Output:
```
John
Doe
25
```
ES2017 introduces a new method called `Object.values()` that allows you to return an [array](https://www.javascripttutorial.net/javascript-array/) of own enumerable property’s values of an object.

The following shows the syntax of the `Object.values()`:
```javascript
Object.values(obj)
```
The `Object.values()` accepts an object and returns its own enumerable property’s values as an array. See the following example:
```javascript
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 25
};

const profile = Object.values(person);

console.log(profile);
```
Output:
```json
[ 'John', 'Doe', 25 ]
```
## `Object.values()` vs. `for...in`

The `Object.values()` returns own enumerable properties while the `for...in` loop iterates properties in the prototype chain.

Technically, if you use the `for...in` loop with the `Object.hasOwnProperty()` method, you will get the same set of values as the `Object.values()`.

### Introduction to JavaScript `Object.entries()` method

ES2017 introduces the `Object.entries()` method that accepts an object and returns its own enumerable string-keyed property `[key, value]` pairs of the object.

Here is the syntax of the `Object.entries()` method:
```javascript
Object.entries()
```
See the following example:
```javascript
const ssn = Symbol('ssn');
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 25,
    [ssn]: '123-345-789'
};

const kv = Object.entries(person);

console.log(kv);
```
Output:
```json
[
    ['firstName', 'John'],
    ['lastName', 'Doe'],
    ['age', 25]
]
```
In this example:

-   The firstName, lastName, and age are own enumerable string-keyed property of the person object, therefore, they are included in the result.
-   The `ssn` is not a string-key property of the person object, so it is not included in the result.

## `Object.entries()` vs. `for...in`

The main difference between the `Object.entries()` and the `for...in` loop is that the `for...in` loop also enumerates object [properties](https://www.javascripttutorial.net/javascript-object-properties/) in the [prototype chain](https://www.javascripttutorial.net/javascript-prototype/).


# JavaScript Factory Functions
### Introduction to the factory functions in JavaScript

A factory function is a [function](https://www.javascripttutorial.net/javascript-function/) that returns a new [object](https://www.javascripttutorial.net/javascript-objects/). The following creates a person object named `person1`:

```javascript
let person1 = {
  firstName: 'John',
  lastName: 'Doe',
  getFullName() {
    return this.firstName + ' ' + this.lastName;
  },
};

console.log(person1.getFullName());
```
Output:

    John Doe

The `person1` object has two properties: `firstName` and `lastName`, and one method `getFullName()` that returns the full name.

Suppose that you need to create another similar object called `person2`, you can duplicate the code as follows:
```javascript
let person2 = {
  firstName: 'Jane',
  lastName: 'Doe',
  getFullName() {
    return this.firstName + ' ' + this.lastName;
  },
};

console.log(person2.getFullName());
```
Output:

    Jane Doe

In this example, the `person1` and `person2` objects have the same properties and methods.

The problem is that the more objects you want to create, the more duplicate code you have.

To avoid copying the same code all over again, you can define a function that creates the `person` object:
```javascript
function createPerson(firstName, lastName) {
  return {
    firstName: firstName,
    lastName: lastName,
    getFullName() {
      return firstName + ' ' + lastName;
    },
  };
}
```
When a function creates and returns a new object, it is called a factory function. The `createPerson()` is a factory function because it returns a new `person` object.

The following show how to use the `createPerson()` factory function to create two objects `person1` and `person2`:
```javascript
function createPerson(firstName, lastName) {
  return {
    firstName: firstName,
    lastName: lastName,
    getFullName() {
      return firstName + ' ' + lastName;
    },
  };
}

let person1 = createPerson('John', 'Doe');
let person2 = createPerson('Jane', 'Doe');

console.log(person1.getFullName());
console.log(person2.getFullName());
```
By using the factory function, you create any number of the `person` objects without duplicating code.

When you create an object, the JavaScript engine allocates memory to it. If you create many `person` objects, the JavaScript engine needs lots of memory spaces to store these objects.

However, each `person` object has a copy of the same `getFullName()` method. It’s not efficient memory management.

To avoid duplicating the same `getFullName()` function in every object, you can remove the `getFullName()` method from the `person` object:
```javascript
function createPerson(firstName, lastName) {
    return {
        firstName: firstName,
        lastName: lastName
    }
}
```
And move this method to another object:
```javascript
var personActions = {
  getFullName() {
    return this.firstName + ' ' + this.lastName;
  },
};
```
And before calling the `getFullName()` method on the `person` object, you can assign the method of the `personActions` object to the `person` object as follows:
```javascript
let person1 = createPerson('John', 'Doe');
let person2 = createPerson('Jane', 'Doe');

person1.getFullName = personActions.getFullName;
person2.getFullName = personActions.getFullName;

console.log(person1.getFullName());
console.log(person2.getFullName());
```
This approach is not scalable if the object has many methods because you have to manually assign them individually. This is why the `Object.create()` method comes into play.

### The Object.create() method

The `Object.create()` method creates a new object using an existing object as the [prototype](https://www.javascripttutorial.net/javascript-prototype/) of the new object:
```javascript
Object.create(proto, [propertiesObject])
```
So you can use the `Object.create()` as follows:
```javascript
var personActions = {
  getFullName() {
    return this.firstName + ' ' + this.lastName;
  },
};

function createPerson(firstName, lastName) {
  let person = Object.create(personActions);
  person.firstName = firstName;
  person.lastName = lastName;
  return person;
}
```
Now, you can create `person` objects and call the methods of the `personActions` object:
```javascript
let person1 = createPerson('John', 'Doe');
let person2 = createPerson('Jane', 'Doe');

console.log(person1.getFullName());
console.log(person2.getFullName());
```
The code works perfectly fine. However, in practice, you will rarely use the factory functions. Instead, you use [classes](https://www.javascripttutorial.net/es6/javascript-class/) or [constructor/prototype](https://www.javascripttutorial.net/javascript-constructor-prototype/) patterns.


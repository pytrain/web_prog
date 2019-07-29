<center>
  <h1>Introduction to PHP</h1>
</center>

## Useful Pointers
- [Learn PHP - Free Interactive PHP Tutorial](https://www.learn-php.org)
- [PHP Tutorial](https://www.tutorialrepublic.com/php-tutorial/) (by Tutorial Republic) 
- [PHP 101: PHP For the Absolute Beginner](https://devzone.zend.com/6/php-101-php-for-the-absolute-beginner/)


**We will cover the following:**
- [What is PHP?](#what-is-php?)
- [Advantages of PHP](#advantages-of-php)
- [My First PHP Script](#my-first-php-script)
- [Variables](#variables)
- [Data Types](#data-types)

## What is PHP?
---

- The Hypertext Preprocessor (PHP) is a very popular and widely-used open source server-side scripting language to write dynamically generated web pages.
- PHP scripts are executed on the server and the result is sent to the web browser as plain HTML.
- PHP can be integrated with databases such as MySQL, PostgreSQL, Oracle, Microsoft SQL Server, Sybase, etc. 
- With PHP you can (among other things): 
  - Generate pages and files dynamically.
  - Create, open, read, write and close files on the server.
  - Collect data from a web form such as user information, email, phone no, etc.
  - Send emails to the users of your website.
  - Send and receive cookies to track the visitor of your website.
  - Store, delete, and modify information in your database.
  - Restrict unauthorized access to your website.
  - Encrypt data for safe transmission over internet.
  
## Advantages of PHP
---

- **Easy to learn**
- **Open source**
- **Portability**: PHP runs on various platforms such as Microsoft Windows, Linux, Mac OS, etc. and it is compatible with almost all servers used today such Apache, IIS, etc.
- **Fast Performance**: Scripts written in PHP usually execute or runs faster than those written in other scripting languages like ASP, Ruby, Python, Java, etc.
- **Vast Community**

## My First PHP Script
---

- A PHP script starts with the **`<?php`** and ends with the **`?>`** tag.
- Every PHP statement end with a semicolon (**`;`**)

```php
<?php
// Display greeting message
echo "Hello, world!";
?>
```

- PHP files are plain text files with .php extension.
- PHP can be embedded within a normal HTML web page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>A Simple PHP File</title>
</head>
<body>
   <?php echo "Hello, world!"; ?>
</body>
</html>
```

### Comments
- PHP supports single-line as well as multi-line comments. 
- To write a single-line comment either start the line with either two slashes (**`//`**) or a hash symbol (**`#`**).
- To write multi-line comments, start the comment with a slash followed by an asterisk (**`/*`**) and end the comment with an asterisk followed by a slash (**`*/`**)

```php
<?php
// This is a single line comment
# This is also a single line comment
echo "Hello, world!";
?>

<?php
/*
This is a multiple line comment block
that spans across more than
one line
*/
echo "Hello, world!";
?>
```

### Case Sensitivity in PHP
- Variable names in PHP are case-sensitive.
- Keywords, function and classes names are case-insensitive.

```php
<?php
// Assign value to variable
$color = "blue";
 
// Try to print variable value
echo "The color of the sky is " . $color . "<br>";
echo "The color of the sky is " . $Color . "<br>"; // undefined
echo "The color of the sky is " . $COLOR . "<br>"; // undefined
?>
```

```php
<?php
// Assign value to variable
$color = "blue";
 
// Get the type of a variable
echo gettype($color) . "<br>";
echo GETTYPE($color) . "<br>";  // as above
?>
```

### Echo and Print Statements
- You can use the **echo** and **print** statements to display output to the browser. 
- Both statements are a language construct not a real function. They work exactly the same way.
- The **print** statement can only output one string, and always returns 1.
- The **echo** statement considered marginally faster than the **print** statement since it doesn't return any value.

```php
<?php

print "Hello World!";

// Displaying HTML code
print "<h4>This is a simple heading.</h4>";
print "<h4 style='color: red;'>This is heading with style.</h4>";

// Defining variables
$txt = "Hello World!";
$num = 123456789;
$colors = array("Red", "Green", "Blue");

// Displaying variables with echo
echo $txt;
echo "<br>";
echo $num;
echo "<br>";
echo $colors[0];

// Displaying variables with print
print $txt;
print "<br>";
print $num;
print "<br>";
print $colors[0];
?>
```

## Variables
---

- A variable does not need to be declared before adding a value to it.
- All variables in PHP start with a **`$`** sign, followed by the name of the variable.
A variable name must start with a letter or the underscore character **`_`**.
- A variable name cannot start with a number.
A variable name in PHP can only contain alpha-numeric characters and underscores (**`A-z`**, **`0-9`**, and **`_`**).

```php
<?php
// Declaring variables
$txt = "Hello World!";
$number = 10;
 
// Displaying variables value
echo $txt;  // Output: Hello World!
echo $number; // Output: 10
?>
```

### Constants
- Are like variables, except that once they are defined, they cannot be undefined or changed.
- Are defined using PHP's **define()** function.
- A valid constant name must starts with a letter or underscore, followed by any number of letters, numbers or underscores with one exception: the **`$`** prefix is not required for constant names.

```php
<?php
// Defining constant
define("SITE_URL", "https://github.com/pytrain/web_prog");
 
// Using constant
echo 'Thank you for visiting - ' . SITE_URL;
?>
```

## Data Types
---

- PHP supports total eight primitive data types: 
  1. Integer
  2. Floating point number or Float
  3. String
  4. Booleans
  5. Array
  6. Object
  7. resource
  8. NULL.
  
### Integer
- Can be specified in decimal (base 10), hexadecimal (base 16 - prefixed with **0x**) or octal (base 8 - prefixed with **0**) notation.

```php
<?php
$a = 123; // decimal number
var_dump($a);
echo "<br>";
 
$b = -123; // a negative number
var_dump($b);
echo "<br>";
 
$c = 0x1A; // hexadecimal number
var_dump($c);
echo "<br>";
 
$d = 0123; // octal number
var_dump($d);
?>
```

### Floating Point Numbers or Doubles
```php
<?php
$a = 1.234;
var_dump($a);
echo "<br>";
 
$b = 10.2e3;
var_dump($b);
echo "<br>";
 
$c = 4E-10;
var_dump($c);
?>
```

### <>---<> Operations on Integers and Doubles

```php
<?php
$x = 10;
$y = 4;
echo($x + $y); // 0utputs: 14
echo($x - $y); // 0utputs: 6
echo($x * $y); // 0utputs: 40
echo($x / $y); // 0utputs: 2.5
echo($x % $y); // 0utputs: 2
?>
```

```php
<?php
// Round fractions up
echo ceil(4.2);    // 0utputs: 5
echo ceil(9.99);   // 0utputs: 10
echo ceil(-5.18);  // 0utputs: -5
 
// Round fractions down
echo floor(4.2);    // 0utputs: 4
echo floor(9.99);   // 0utputs: 9
echo floor(-5.18);  // 0utputs: -6
?>
```

```php
<?php
$x = 10;
echo $x; // Outputs: 10
 
$x = 20;
$x += 30;
echo $x; // Outputs: 50
 
$x = 50;
$x -= 20;
?>
```

```php
<?php
$x = 10;
echo ++$x; // Outputs: 11
echo $x;   // Outputs: 11
 
$x = 10;
echo $x++; // Outputs: 10
echo $x;   // Outputs: 11
 
$x = 10;
echo --$x; // Outputs: 9
echo $x;   // Outputs: 9
 
$x = 10;
echo $x--; // Outputs: 10
echo $x;   // Outputs: 9
?>
```

### Strings
- You can use either single quote (**`'`**) or double quotes (**`"`**) to define a string.
- Strings enclosed in single-quotes are treated almost literally.
- Strings delimited by the double quotes replaces variables with the string representations of their values as well as specially interpreting certain escape sequences.
- A string can hold letters, numbers, and special characters and it can be as large as up to 2GB 

```php
<?php
$a = 'Hello world!';
echo $a;
echo "<br>";
 
$b = "Hello world!";
echo $b;
echo "<br>";
 
$c = 'Stay here, I\'ll be back.';
echo $c;
?>
```

The escape-sequence replacements are:

- **`\n`** is replaced by the newline character
- **`\r`** is replaced by the carriage-return character
- **`\t`** is replaced by the tab character
- **`\\\\$`** is replaced by the dollar sign itself (**`$`**)
- **`\\"`** is replaced by a single double-quote (**`"`**)
- **`\\\\`** is replaced by a single backslash (**`\\`**)

```php
<?php
$my_str = 'World';
echo "Hello, $my_str!<br>";      // Displays: Hello World!
echo 'Hello, $my_str!<br>';      // Displays: Hello, $my_str!
 
echo '<pre>Hello\tWorld!</pre>'; // Displays: Hello\tWorld!
echo "<pre>Hello\tWorld!</pre>"; // Displays: Hello   World!
echo 'I\'ll be back';            // Displays: I'll be back
?>
```

### <>---<> String Manipulations
```php
<?php
$my_str = 'Welcome to the Introductory Web Programming course';

// Count the number of charcaters
echo strlen($my_str);

// Count the number of words
echo str_word_count($my_str);

// Display replaced string
echo str_replace("course", "Course", $my_str);

// Display reversed string
echo strrev($my_str);
?>
```

### <>---<> String Operators

| Operator | Description | Example | Result |
| --- | --- | --- | --- |
**.**	| Concatenation	| $\$$str1 . $\$$str2 | Concatenation of $\$$str1 and $\$$str2 |
**.=**	| Concatenation assignment | $\$$str1 .= $\$$str2	| Appends the $\$$str2 to the $\$$str1 |

```php
<?php
$x = "Hello";
$y = " World!";
echo $x . $y; // Outputs: Hello World!
 
$x .= $y;
echo $x; // Outputs: Hello World!
?>
```

### Booleans
- Can take two possible values either 1 (true) or 0 (false).

```php
<?php
// Assign the value TRUE to a variable
$show_error = true;
var_dump($show_error);
?>
```

### <>---<> Comparison Operators

```php
<?php
$x = 25;
$y = 35;
$z = "25";
var_dump($x == $z);  // Outputs: boolean true
var_dump($x === $z); // Outputs: boolean false
var_dump($x != $y);  // Outputs: boolean true
var_dump($x !== $z); // Outputs: boolean true
var_dump($x < $y);   // Outputs: boolean true
var_dump($x > $y);   // Outputs: boolean false
var_dump($x <= $y);  // Outputs: boolean true
var_dump($x >= $y);  // Outputs: boolean false
?>
```

### Arrays
- An array is formally defined as an indexed collection of data values. 
- Each index (also known as the key) of an array is unique and references a corresponding value.
- There are three types of arrays that you can create. These are:
  1. **Indexed array** — An array with a numeric key.
  2. **Associative array** — An array where each key has its own specific value.
  3. **Multidimensional array** — An array containing one or more arrays within itself.
  
### <>---<> Indexed Array
- An indexed or numeric array stores each array element with a numeric index

```php
<?php
$colors = array("Red", "Green", "Blue");
var_dump($colors);
echo "<br>";
?>
```

```php
<?php
$colors[0] = "Red"; 
$colors[1] = "Green"; 
$colors[2] = "Blue"; 
?>
```

### <>---<> Associative Arrays
- In an associative array, the keys assigned to values can be arbitrary and user defined strings.

```php
<?php
$color_codes = array(
    "Red" => "#ff0000",
    "Green" => "#00ff00",
    "Blue" => "#0000ff"
);
var_dump($color_codes);
?>
```

```php
<?php
$color_codes["Red"] = "#ff0000"; 
$color_codes["Green"] = "#00ff00"; 
$color_codes["Blue"] = "#0000ff"; 
?>
```

### <>---<> Multidimensional Arrays
- The multidimensional array is an array in which each element can also be an array and each element in the sub-array can be an array or further contain array within itself and so on

```php
<?php
// Define a multidimensional array
$contacts = array(
    array(
        "name" => "Peter Parker",
        "email" => "peterparker@mail.com",
    ),
    array(
        "name" => "Clark Kent",
        "email" => "clarkkent@mail.com",
    ),
    array(
        "name" => "Harry Potter",
        "email" => "harrypotter@mail.com",
    )
);
// Access nested value
echo "Peter Parker's Email-id is: " . $contacts[0]["email"];
?>
```

### <>---<> Viewing Array Structure and Values
- **var_dump()** or **print_r()**

```php
<?php
// Define array
$cities = array("London", "Paris", "New York");
 
// Display the cities array
print_r($cities);

var_dump($cities);
?>
```

### <>---<> Sorting Arrays
- **sort()** and **rsort()** — For sorting indexed arrays in ascending and descending orders respectively.
- **asort()** and **arsort()** — For sorting associative arrays by value in ascending and descending orders respectively.
- **ksort()** and **krsort()** — For sorting associative arrays by key in ascending and descending orders respectively.

```php
<?php
// Define array
$colors = array("Red", "Green", "Blue", "Yellow");
 
// Sorting and printing array
sort($colors);
print_r($colors);

rsort($colors);
print_r($colors);
?>
```

```php
<?php
// Define array
$age = array("Peter"=>20, "Harry"=>14, "John"=>45, "Clark"=>35);
 
// Sorting array by value and print
asort($age);
print_r($age);
?>
```

```php
<?php
// Define array
$age = array("Peter"=>20, "Harry"=>14, "John"=>45, "Clark"=>35);
 
// Sorting array by key and print
krsort($age);
print_r($age);
?>
```

### <>---<> Array Operators

| Operator | Description | Example | Result |
| --- | --- | --- | --- |
| +	| Union	| $\$$x + $\$$y |	Union of $\$$x and $\$$y |
| ==	| Equality |	$\$$x == $\$$y |	True if $\$$x and $\$$y have the same  key/value pairs |
| ===	| Identity	| $\$$x === $\$$y	| True if $\$$x and $\$$y have the same  key/value pairs |
| $ $| $ $ | $ $ | in the same order and of the same types |
| !=	| Inequality |	$\$$x != $\$$y |	True if $\$$x is not equal to $\$$y |
| <>	| Inequality |	$\$$x <> $\$$y |	True if $\$$x is not equal to $\$$y |
| !==	| Non-identity |	$\$$x !== $\$$y |	True if $\$$x is not identical to $\$$y |

```php
<?php
$x = array("a" => "Red", "b" => "Green", "c" => "Blue");
$y = array("u" => "Yellow", "v" => "Orange", "w" => "Pink");
$z = $x + $y; // Union of $x and $y
var_dump($z);
var_dump($x == $y);   // Outputs: boolean false
var_dump($x === $y);  // Outputs: boolean false
var_dump($x != $y);   // Outputs: boolean true
var_dump($x <> $y);   // Outputs: boolean true
var_dump($x !== $y);  // Outputs: boolean true
?>
```

### Objects
- An object is a data type that not only allows storing data but also information on, how to process that data. 
- An object is a specific instance of a class which serve as templates for objects. 
- Every object has properties and methods corresponding to those of its parent class. 
- Every object instance is completely independent, with its own properties and methods, and can thus be manipulated independently of other objects of the same class.

```php
// Class definition
class greeting{
    // properties
    public $str = "Hello World!";
    
    // methods
    function show_greeting(){
        return $this->str;
    }
}
 
// Create object from class
$message = new greeting;
var_dump($message);
?>
```

### Resources
- A resource is a special variable, holding a reference to an external resource.
- Resource variables typically hold special handlers to opened files and database connections.

```php
<?php
// Open a file for reading
$handle = fopen("note.txt", "r");
var_dump($handle);
echo "<br>";
 
// Connect to MySQL database server with default setting
$link = mysql_connect("localhost", "root", "");
var_dump($link);
?>
```

### NULL
- The special NULL value is used to represent empty variables in PHP. 
- A variable of type NULL is a variable without any data. 
- NULL is the only possible value of type null.
- When a variable is created without a value in PHP like **`$var;`**, it is automatically assigned a value of null.

```php
<?php
$a = NULL;
var_dump($a);
echo "<br>";
 
$b = "Hello World!";
$b = NULL;
var_dump($b);
?>
```

```php
$var1 = NULL;

// is not the same as
$var2 = ""

// $var1 has null value while $var2 indicates no value assigned to it.
```

## Conditional Statements
---

### if Statements

```php
// Syntax

if(condition){
    // Code to be executed
}

if(condition){
    // Code to be executed if condition is true
} else{
    // Code to be executed if condition is false
}

if(condition1){
    // Code to be executed if condition1 is true
} elseif(condition2){
    // Code to be executed if the condition1 is false and condition2 is true
} else{
    // Code to be executed if both condition1 and condition2 are false
}
```

```php
<?php
$d = date("D");
if($d == "Fri"){
    echo "Have a nice weekend!";
} elseif($d == "Sun"){
    echo "Have a nice Sunday!";
} else{
    echo "Have a nice day!";
}
?>
```

### The Ternary Operator
- Provides a shorthand way of writing the **if...else** statements.
- It is represented by the question mark (**?**) symbol and it takes three operands: a condition to check, a result for **true**, and a result for **false**.

condition ? value1 : value2;

```php
<?php
if($age < 18){
    echo 'Child'; // Display Child if age is less than 18
} else{
    echo 'Adult'; // Display Adult if age is greater than or equal to 18
}
?>

\\ Using the ternary operator
<?php echo ($age < 18) ? 'Child' : 'Adult'; ?>
```

### Switch…Case Statements
- The switch-case statement tests a variable against a series of values until it finds a match, and then executes the block of code corresponding to that match.
- How it works:
  - The **switch** statement executes line by line and once PHP finds a **case** statement that evaluates to true, it's not only executes the code corresponding to that case statement, but also executes all the subsequent **case** statements till the end of the **switch** block automatically.
  - To prevent this add a **break** statement to the end of each case block. 
  
```php
\\ Syntax
switch(n){
    case label1:
        // Code to be executed if n=label1
        break;
    case label2:
        // Code to be executed if n=label2
        break;
    ...
    default:
        // Code to be executed if n is different from all labels
}
```

```php
<?php
$today = date("D");
switch($today){
    case "Mon":
        echo "Today is Monday. Clean your house.";
        break;
    case "Tue":
        echo "Today is Tuesday. Buy some food.";
        break;
    case "Wed":
        echo "Today is Wednesday. Visit a doctor.";
        break;
    case "Thu":
        echo "Today is Thursday. Repair your car.";
        break;
    case "Fri":
        echo "Today is Friday. Party tonight.";
        break;
    case "Sat":
        echo "Today is Saturday. Its movie time.";
        break;
    case "Sun":
        echo "Today is Sunday. Do some rest.";
        break;
    default:
        echo "No information available for that day.";
        break;
}
?>
```

## Loops
---

PHP supports four different types of loops.

- **while** — loops through a block of code until the condition is evaluate to true.
- **do…while** — the block of code executed once and then condition is evaluated. If the condition is true the statement is repeated as long as the specified condition is true.
- **for** — loops through a block of code until the counter reaches a specified number.
- **foreach** — loops through a block of code for each element in an array.

### The "while” Loop

```php
// Syntax
while(condition){
    // Code to be executed
}
```

```php
// An example
<?php
$i = 1;
while($i <= 3){
    $i++;
    echo "The number is " . $i . "<br>";
}
?>
```

### The “do-while” Loop
- With a **do-while** loop the block of code executed once, and then the condition is evaluated, if the condition is true, the statement is repeated as long as the specified condition evaluated to is true.

```php
// Syntax
do{
    // Code to be executed
}
while(condition);
```

```php
<?php
$i = 1;
do{
    $i++;
    echo "The number is " . $i . "<br>";
}
while($i <= 3);
?>
```

### The ""for" Loop

```php
// Syntax
for(initialization; condition; increment){
    // Code to be executed
}
```

```php
// An example
<?php
for($i=1; $i<=3; $i++){
    echo "The number is " . $i . "<br>";
}
?>
```

### "foreach" Loop

```php
// Syntax
foreach($array as $value){
    // Code to be executed
}

foreach($array as $key => $value){
    // Code to be executed
}
```

```php
// Example
<?php
$colors = array("Red", "Green", "Blue");
 
// Loop through colors array
foreach($colors as $value){
    echo $value . "<br>";
}
?>
```

```php
// Another example
<?php
$superhero = array(
    "name" => "Peter Parker",
    "email" => "peterparker@mail.com",
    "age" => 18
);
 
// Loop through superhero array
foreach($superhero as $key => $value){
    echo $key . " : " . $value . "<br>";
}
?>
```

## Functions
- By default, function arguments are passed by value.
- Passing an argument by reference is done by prepending an ampersand (**&**) to the argument name in the function definition.
- Variables declared within a function are local and they cannot be viewed or manipulated from outside of that function.

```php
// Basic syntax

function functionName(){
    // Code to be executed
}

function myFunc($oneParameter, $anotherParameter){
    // Code to be executed
}
```

```php
// An example
<?php
// Defining function
function whatIsToday(){
    echo "Today is " . date('l', mktime());
}
// Calling function
whatIsToday();
?>
```

```php
// Another example
<?php
// Defining function
function getSum($num1, $num2){
  $sum = $num1 + $num2;
  echo "Sum of the two numbers $num1 and $num2 is : $sum";
}
 
// Calling function
getSum(10, 20);
?>
```

### Functions with Optional Parameters and Default Values
- You can create functions with optional parameters by inserting the parameter name, followed by an equals (**=**) sign.

```php
<?php
// Defining function
function customFont($font, $size=1.5){
    echo "<p style=\"font-family: $font; font-size: {$size}em;\">Hello, world!</p>";
}
 
// Calling function
customFont("Arial", 2);
customFont("Times", 3);
customFont("Courier");
?>
```

### Returning Values from a Function
- A function can not return multiple values. 
- You can obtain similar results by returning an array.

```php
<?php
// Defining function
function getSum($num1, $num2){
    $total = $num1 + $num2;
    return $total;
}
 
// Printing returned value
echo getSum(5, 10); // Outputs: 15
?>
```

```php
<?php
// Defining function
function divideNumbers($dividend, $divisor){
    $quotient = $dividend / $divisor;
    $array = array($dividend, $divisor, $quotient);
    return $array;
}
 
// Assign variables as if they were an array
list($dividend, $divisor, $quotient) = divideNumbers(10, 2);
echo $dividend;  // Outputs: 10
echo $divisor;   // Outputs: 2
echo $quotient;  // Outputs: 5
?>
```

```php
<?php
/* Defining a function that multiply a number
by itself and return the new value */
function selfMultiply(&$number){
    $number *= $number;
    return $number;
}
 
$mynum = 5;
echo $mynum; // Outputs: 5
 
selfMultiply($mynum);
echo $mynum; // Outputs: 25
?>
```

### The global Keyword
- You can use the **global** keyword before the variables inside a function. This keyword turns the variable into a global variable, making it visible or accessible both inside and outside the function.

```php
<?php
$greet = "Hello World!";
 
// Defining function
function test(){
    global $greet;
    echo $greet;
}
 
test(); // Outpus: Hello World!
echo $greet; // Outpus: Hello World!
 
// Assign a new value to variable
$greet = "Goodbye";
 
test(); // Outputs: Goodbye
echo $greet; // Outputs: Goodbye
?>
```

## GET and POST
---

- A web browser communicates with the server typically using one of the two HTTP (Hypertext Transfer Protocol) methods — GET and POST. 
- Both methods pass the information differently and have different advantages and disadvantages.

### The GET Method
- In GET method the data is sent as URL parameters that are usually strings of name and value pairs separated by ampersands (&).

In general, a URL with GET data will look like this:

http://www.example.com/action.php?**name**=*john*&**age**=24

- The bold parts in the URL are the GET parameters and the italic parts are the value of those parameters. 
- More than one **parameter=value** can be embedded in the URL by concatenating with ampersands (**&**).
- You can only send simple text data via GET method.

### The POST Method
- In POST method the data is sent to the server as a package in a separate communication with the processing script. 
- Data sent through POST method will not visible in the URL.

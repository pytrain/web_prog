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

## What is PHP?
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
- **Easy to learn**
- **Open source**
- **Portability**: PHP runs on various platforms such as Microsoft Windows, Linux, Mac OS, etc. and it is compatible with almost all servers used today such Apache, IIS, etc.
- **Fast Performance**: Scripts written in PHP usually execute or runs faster than those written in other scripting languages like ASP, Ruby, Python, Java, etc.
- **Vast Community**

## My First PHP Script
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
- PHP support single-line as well as multi-line comments. 
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

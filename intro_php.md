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

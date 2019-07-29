<center>
  <h1>PHP Setup and Introduction</h1>
</center>

**We will cover the following:**
- [PHP Setup](#php-setup)
- [Test for PHP](#test-for-php)

## PHP Setup
---

We want to manually install PHP so that we can have more control over it's configuration and the resources that come with the downloaded version.

### Installation Guides

- **Mac/Unix/Linux:** You "should" have PHP already available to you as it now comes bundled with your operating system installation. We, however, need to [verify](#test-for-php) that the version number is sufficient.
- **Windows:** Below is the best estimate of the steps necessary for installing and configuring your PHP installation. Note: we did not have a Windows device to test these steps.
  1. Download the Zip file under "Windows downloads" [here](https://www.php.net/downloads.php). If you are questioning whether or not to use Thread Safe or Non-Thread Safe, choose Thread Safe.
  2. Unzip this file and put the contents such that the PHP folder has a path that mimics `C:\php` if there is not already a folder there. Your downloaded zip folder will have the version number and such in the folder name; rename this to just "php".  
    **Note:** There is a `php.exe` file in this folder. That essentially is the PHP executable that you will be using via the command prompt. We just need to make some configuration changes and PATH changes so you don't have to type `C:\php\php.exe` every time you want to run PHP.
  3. Copy or rename `C:\php\php.ini-development` to become `C:\php\php.ini`. This allows us to have a pre-made INI file (configuration file) for the PHP executable, but we still have more edits to it before we can use it.
  4. Approximately line 751: change `;extension_dir = "./"` to be `extension_dir = "C:\php\ext"`. Note that I removed the semicolon to uncomment this line in the INI file as well. [(More Information)](https://www.php.net/manual/en/ini.core.php#ini.extension-dir)
  5. Uncomment the following extensions:
     1. Line 906: `curl`
     2. Line 908: `gd2`
     3. Line 915: `mbstring`
     4. Line 917: `mysqli`
     5. Line 922: `pdo_mysql`
     6. Line 939: `xmlrpc`
  6. We could change the INI file to allow us to use the PHP `mail()` function so we can send mail, but at this time, we do not want to try finding our ISP information and such to put there.
  7. Adding PHP to your environment PATH:
     1. System Properties > "Advanced" Tab > Environment Variables
     2. Scroll to find "PATH" and then click on it and edit it.
     3. Add the following exactly at the end of this variables value line: `;C:\php`
     4. Accept the changes and you might have to restart in order for this change to take effect.

## Test for PHP
---

Most tutorails instruct you to write a PHP script, put a single line of PHP code in there, and then load it into your browser. There is a different way to do this and these 3 steps are not all that it takes to get a PHP script running.

1. Test without writing a script: Open up your terminal/command prompt and try typing in `php -v` and press enter. You should see the following as a result if successful:
  ```
PHP 7.1.23 (cli) (built: Feb 22 2019 22:19:32) ( NTS )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.1.0, Copyright (c) 1998-2018 Zend Technologies
```
2. Using a file:
   1. Create a text/ASCII file named index.php
   2. Put the following code in this file: `<?php phpinfo(); ?>`
   3. `cd` in your temrinal/comand prompt to the file's directory location.
   4. Run from the command line or terminal: `php -S localhost:8000` This starts a local PHP server on your local webpage.
   5. Open a browser and navigate to: http://localhost:8000/ (note: you might need https)
   6. You should be seeing a page that displays your PHP server information.

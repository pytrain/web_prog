<center>
  <h1>PHP Setup and Introduction</h1>
</center>

**We will cover the following:**
- [PHP Setup]()
- [Testing PHP]()
- [PHP Intro]()

## PHP Setup
---

You can obtain the necessary files to install PHP on your local machine [here](https://www.php.net/downloads.php). For Mac/Unix/Linux users, you "should" have it already installed for you since it comes with the operating system installation.

Windows users, there are some steps in the [official documentation](https://www.php.net/manual/en/install.windows.php) that might be of some aid to you. If you do not have PHP installed, please let us know.

## Testing PHP
---

In order to test that PHP is installed on your machine, let's check the version of your installation from the command line/terminal:

```
php -v
```

If you do not see the following type of text, let us know:

```
PHP 7.1.23 (cli) (built: Feb 22 2019 22:19:32) ( NTS )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.1.0, Copyright (c) 1998-2018 Zend Technologies
```

## PHP Intro
---

If we have the installation working, let's start by running a sample PHP code.

1. Create a text/ASCII file named index.php
2. Put the following code in this file: `<?php phpinfo(); ?>`
3. `cd` in your temrinal/comand prompt to the file.
4. Run from the command line or terminal: `php -S localhost:8000` This starts a local PHP server on your local webpage.
5. Open a browser and navigate to: http://localhost:8000/ (note: you might need https)

You should be seeing a page that displays your PHP server information.

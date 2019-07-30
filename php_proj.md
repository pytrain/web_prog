<center>
  <h1>PHP: Sample Application/Project</h1>
</center>

This lecture period will be used to apply our new knowledge of PHP while building upon that of HTML, CSS Javascript, and jQuery.

## A Sample Website
---

We will start by building a sample website and guide you through step-by-step to integrate PHP functionality. This assumes you are able to run PHP locally, but if not, please try to use an online editor that allows you to write PHP code, test it, and have multiple files/folders for this project.

1. Obtaining the HTML Template:
   1. Open a browser window/tab and navigate to this [url](https://getbootstrap.com/docs/4.3/getting-started/introduction/#starter-template).  
      This page is showing a starter Bootstrap template where Bootstrap is a useful library for both CSS and Javascript. It allows you to simplify creating websites by using their pre-defined CSS and Javascript classes and functionality.]
   2. Copy and paste this code into a text/ASCII editor and save it as `index.php` in a folder called `my_site`.
2. Viewing your current PHP website.
   1. At this point, we have just HTML, CSS, and Javascript/jQuery code in a single page. We do not have PHP code yet, but we will add code later in this project.
   2. Open your `index.php` in your web browser. You should see only the source code and not the rendered h1 tag of "Hello, world!". Let's fix that.
   3. Open a terminal/command prompt and change directories (`cd`) to be within the `my_site` folder.
   4. Run the following command to start the PHP interpreter: `php -S localhost:8000`
   5. Now, in your browser, change the url of that page that we were at to the following: [http://localhost:8000/](http://localhost:8000/).
   6. You should now see the h1 tag of "Hello, world!" rendered HTML code.
3. Adding more elements to the page.
   1. Let's add a navigation bar at the top of the page.
   2. Replace our h1 tag with the following code:
      ```html
      <nav class="navbar navbar-expand-md navbar-dark bg-dark fixed-top">
        <a class="navbar-brand" href="#">Navbar</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExampleDefault" aria-controls="navbarsExampleDefault" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
      </nav>

      <main role="main" class="container">

        <div class="starter-template">
          <h1>Bootstrap starter template</h1>
          <p class="lead">Use this document as a way to quickly start any new project.<br> All you get is this text and a mostly barebones HTML document.</p>
        </div>

      </main>
      ```
   3. You should see something similar to this page: https://getbootstrap.com/docs/4.3/examples/starter-template/
   4. There is something very different other than the navigation and search bar differences. The text in the middle of the page is not correctly styled.
   5. Add the following style to the header section of your website.
       ```css
       body {
           padding-top: 5rem;
       }
       .starter-template {
           padding: 3rem 1.5rem;
           text-align: center;
       }
       ```

At this point in the project, you should be able to pause and look at the source code of the HTML and CSS that is being used. Notice the classes being used are Bootstrap-defined classes and that they are descriptive names. Notice how the CSS only aligns text and adds space. This should be a good start for our PHP project now.

Let's create a simple login form (username only for now) on this single page.

1. Remove the paragraph text in the middle of the page and let's add a simple input form and button.
   1. Let's use the code for the sample email form here: https://getbootstrap.com/docs/4.3/components/forms/#overview
   2. Copy this code into your `index.php` page where the paragraph text was.
   3. Verify by reloading your page in the browser to see the changes.
   4. Let's change this form to be only a username (not email) and just a button.  
      ![now](https://raw.githubusercontent.com/pytrain/web_prog/master/images/one.png)
2. Let's add a little PHP functionality.
   1. Replace the form with the following code:
       ```php
       <?php
         if ($_SERVER['REQUEST_METHOD'] != 'POST'){
             echo '<h1>Bootstrap starter template</h1>
                   <form action="index.php" method="post">
                     <div class="form-group">
                       <input type="text" class="form-control" name="userName" placeholder="Enter username">
                     </div>
                     <button type="submit" class="btn btn-primary">Submit</button>
                   </form>';
         }
         else {
             echo "<h1>Welcome " . $_POST['userName'] . "</h1>";
             echo "<p>Your username is: " . $_POST['userName'] . "</p>";
         }
       ?>
       ```
    2. Test out the functionality and see that your username is returned when the form is submitted.
    
At this point, we have a basic PHP application that only returns values submitted by users. What other functionality would you want to add to this form? Perhaps instead of a welcome message, we want to change the navigation to show the username and have a settings panel for customization? Or, perhaps we want to have when the user submits the form to be rejected depending upon the username?

Ultimately, there are many options here, but we are going to do something different. We're going to log the username in a file and then return a chart with the user logins as a timeseries.

Adding usernames to a file:
1. The only modification we need is that when the user sees the welcome message, we need to add the username to a file as well.
   1. Add the following code within the `else` portion of the conditional:
      ```php
      $file = 'people.txt';
      $now = date("Y-m-d H:i:s");
      // Open the file to get existing content
      if (file_exists($file)){
          $current = file_get_contents($file);
          // Append a new person to the file
          $current .= "\n" . $_POST['userName'] . ", " . $now;
          // Write the contents back to the file
          file_put_contents($file, $current);
      }
      else{
          // Start a new person entry
          $current = $_POST['userName'] . ", " . $now;
          // Write the contents back to the file
          file_put_contents($file, $current);
      }
      ```
   2. Verify that this file is written to by using the form.
   3. We have now a file-based database of users and entry times.
2. Now, we need to visualize this data either when the user enters or as a continuous plot that updates as the file changes. There are many, many ways to solve this and I will leave this as an exercise for you to complete. For the time being, we can instead take and list continually the last 10 visitors and times to our website.
   1. We need a separate portion of code in our page that tests to see if the file exists, open and read it contents, and then display the last 10 entries.
   2. Add the following code to your page below the login stuff:
       ```php
       <?php
           $file = 'people.txt';
           if (file_exists($file)){
               echo "<br><br>";
               echo '<div class="alert alert-secondary">
                       <h3 class="alert-heading">Latest 10 Vists</h3>
                       <hr>';
               $current = file($file);
               for ($i = max(0, count($current)-10); $i < count($current); $i++){
                   echo "<p>" . $current[$i] . "</p>";
               }
               echo "</div>";
           }
       ?>
       ```
    3. Verify that this now works and updates as you enter users.

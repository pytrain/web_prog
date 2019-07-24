<center>
  <h1>Introduction to HTML</h1>
</center>

## Useful Pointers
- [Intro to HTML/CSS: Making Webpages](https://www.khanacademy.org/computing/computer-programming/html-css) (from Khan Academy)
- [Introduction to HTML for Beginners](https://www.afterhoursprogramming.com/tutorial/html/introduction-html/) (from After Hours Programming)
- [HTML Tutorial](https://www.quackit.com/html/tutorial/) (from Quackit)

**We will cover the following:**
- [Basic components of a web page](one)
- Formatting
- Attributes
- Links
- Images
- Tables

[one]: ## Basic Components of a Web Page
---

- An HTML document is a text file made up of HTML elements. 
- An HTML element is an individual component of an HTML document. 
- HTML tags tell your browser which elements to present and how to present them. 
- Where the element appears is determined by the order in which the tags appear.

```html
<!DOCTYPE html>
<html>

  <head>
    <title>HTML Programming Example</title>
  </head>
  
  <body>
    <h1>Create My First Website</h1>
    <p>Here are the basic components of an HTML document!</p>
  </body>
  
</html>
```

- The **`<!DOCTYPE...>`**  declaration tells the browser which version of HTML the document is using.
- The **`<html>`** element is the document's root element - it can be thought of as a container that all other tags sit inside (except for the `!DOCTYPE` declaration).
- The **`<head>`** tag contains information that is not normally viewable within your browser (such as meta tags, JavaScript and CSS), although the **`<title>`** tag is an exception to this. The content of the **`<title>`** tag is displayed in the browser's title bar.
- The **`<body>`** tag is the main area for your content. This is where most of your code (and viewable elements) will go.
- The **`<h1>`** tag defines a level 1 heading.
- The **`<p>`** tag defines a paragraph. This contains the body text.
  
## Formatting
---

### Headings
```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Bold Characters
```html
<strong>Bold Characters:</strong> Regular Character.
```

### Italic Characters
```html
This HTML course is <em>GREAT</em>!
```

### Line Break
```html
Here is a <br>line break.
```

### Thematic Break
```html
We will cover HTML, and
  <hr>
CSS and Javascript.
```

### Unordered (un-numbered) List
```html
    <ul>
      <li>Unordered Item 1</li>
      <li>Unordered Item 2</li>
      <li>Unordered Item 3</li>
    </ul>
```

### Ordered (numbered) List
```html
    <ol>
      <li>Ordered Item 1</li>
      <li>Ordered Item 2</li>
      <li>Ordered Item 3</li>
    </ol>
```

## Attributes
---

- Can be added to HTML elements to provide further information about that element.
- HTML tags can contain one or more attributes. 
- Attributes are added to a tag to provide the browser with more information about how the tag should appear or behave. 
- Attributes consist of a name and a value separated by an equals (=) sign.

```html
<abbr title="Hypertext Markup Language">HTML</abbr>
```
You can add more than one attribute to a given element.
```html
<a href="https://www.github.com/pytrain" title="Great introduction to web programming!">HTML Tutorial</a>
```
List of attributes:  
**title:*** Used to display a "tooltip" for your elements.  
**href:** Specifies the location of the web page that we're linking to  
**class:** Used with Cascading Style Sheets (CSS) to apply the styles from a given class.  
**style:** Used with CSS to apply styles directly to the element (i.e. inline styles).

## Links
---

- Links (or hyperlinks), are defined using the **`<a>`** tag (or the anchor element).
- To create a hyperlink, you use the **`<a>`** tag in conjunction with the href attribute. 
- The value of the href attribute is the URL, or, location of where the link is pointing to.

### Links Example
```html
Here is an example of link:  <a href="https://www.github.com/pytrain" target="_blank"> HTML Tutorial </a>.  You can try out!
```
#### Absolute URLS
This refers to a URL where the full path is provided
```html
<a href="https://www.github.com/pytrain/web_prog"> Absolute URLS.</a>
```
#### Relative URLS
This refers to a URL where the path, **relative to the current location**, is provided.
```html
<a href="web_prog/">Relative URLS.</a>
```
#### Root Relative URLS
This refers to a URL where the path, **relative to the domain's root**, is provided.
```html
<a href="/pytrain/web_prog/">Root Relative URLS.</a>
```
### Link Targets
Use to nominate whether to open the URL in a new window or the current window.

| Target Type | Description |
| --- | --- |
| **_blank**	| Opens the URL in a new browser window. |
| **_self**	| Loads the URL in the current browser window. |
| **_parent**	| Loads the URL into the parent frame (still within the current browser window). This is only applicable when using frames. |
| **_top**	| Loads the URL in the current browser window, but cancelling out any frames. Therefore, if frames were being used, they aren't any longer. |

```html
Here is an example of link:  <a href="https://www.github.com/pytrain" target="_blank"> HTML Tutorial </a>.  You can try out!
```

### Jump Links
- Make your links "jump" to other sections within the same page (or another page). 
- The process involved two steps.

```html
<h4 id="jump_link">Sample Jump Link</h4>

<a href="#jump_link">Jump to Sample Jump Link</a>
```

### Email Link

- Allows you to create a hyperlink to an email address. 
- Use the **mailto** attribute in your anchor tag.

```html
<a href="mailto:Jules_Kouatchou@example.com">Email Jules Kouatchou</a>
```
```html
<a href="mailto:Jules_Kouatchou@example.com?subject=Question&body=Hey there">Email Jules Kouatchou</a>
```

## Images
---

- To embed an image into a web page, the image first needs to exist in either **.jpg**, **.gif**, or **.png** format. 
- Use the **`<img>`** tag, specifying the actual location of the image
```html
<img src="/pix/samples/18m.jpg" width="166" height="101" alt="Photo of three cats">
```

| Attributes | Description |
| --- | --- | 
| **src** |	Required attribute. This is the path (absolute or relative) to the image.  |
| **width** | Optional attribute that specifies the width to display the image. |
| **height** |	Optional attribute that specifies the height to display the image. |
| **alt** |	Alternate text that specifies text to be used in case the browser/user agent can't render the image. |

## Comments
---

You write comments like this:
```html
<!-- Write your comment here -->
```

## Tables
---

- Allow you to present tabular data in a nice, structured way.
- Present data within a grid — with rows and columns.

The basic table elements are:

- **`<table>`** Tag to reate a table.
- **`<tr>`** Tag to define a row.
- **`<th>`** Tag for table data cell.
- **`<td>`** Tag for table headers.

```html
<table>
    <tr>
        <th>Table Header 01</th>
        <th>Table Header 02</th>
        <th>Table Header 03</th>
    </tr>
    <tr>
        <td>Cell 11</td>
        <td>Cell 12</td>
        <td>Cell 13</td>
    </tr>
    <tr>
        <td>Cell 21</td>
        <td>Cell 22</td>
        <td>Cell 23</td>
    </tr>
</table>
```

## Meta Tags
---

- Allow you to provide metadata about your HTML pages
- Useful for search engines, browsers, and other applications trying to understand more about your page

You can add metadata to your web pages by placing **`<meta>`** tags between the **`<head> </head>`** tags. 


| Attribute	| Description |
| --- | --- |
**name** |	Metadata name. The name specifies what aspect of metadata is being set. |
**content** |	Specifies the property's value. |
**charset** |	Specifies a character encoding declaration. |
**http-equiv** |	Used for http response message headers. For example http-equiv can be used to refresh the page or to set a cookie. Values include content-type, expires, refresh and set-cookie. |

```html
<!-- Keyword: -->
<meta name="keywords" content="HTML, meta tags, metadata">

<!-- Description: -->
<meta name="description" content="Contains info about meta tags">

<!-- Author: -->
<meta name="author" content="Jules Kouatchou">

<!-- Refresh the page every 15 seconds: -->
<meta http-equiv="refresh" content="15">
```

## Forms
---

- Allow you to build more dynamic websites.
- Made up of any number of form elements.
- The elements enable the user to do things such as enter information or make a selection from a preset options.

A form is defined using the **`<form>  </form>`** tags

```html
<form>
...
(form elements go here)
...
</form>
```

### The `<input>` Tag
    
- Allows you to specify various types of user input fields such as text, radio buttons, checkboxes etc.

### Text
- Used when you want the user to type short amounts of text into the form.

```html
<form>
    First name: <input type="text" name="firstname">
    Last name: <input type="text" name="lastname">
</form>
```

### Radio Buttons
- Used when you want the user to select only one option from a pre-determined set of options.
- User can select one option only.

```html
<form>
    <input type="radio" name="course" value="html"> HTML
    <input type="radio" name="course" value="python"> Python
</form>
```

### Checkboxes
- Enable the user to make multiple selections.
- Used when you want to allow the users to make more than one selection.
```html
<form>
  I am familiar with:
    <input type="checkbox" name="technology" value="HTML"> HTML
    <input type="checkbox" name="technology" value="CSS"> CSS
    <input type="checkbox" name="technology" value="Javascript"> Javascript
    <input type="checkbox" name="technology" value="PHP"> PHP
</form>
```
### Submit
- The submit button allows the user to actually submit the form.

```html
<form action="/html/tags/html_form_tag_action.cfm">
  I am familiar with:
    <input type="checkbox" name="technology" value="HTML"> HTML
    <input type="checkbox" name="technology" value="CSS"> CSS
    <input type="checkbox" name="technology" value="Javascript"> Javascript
    <input type="checkbox" name="technology" value="PHP"> PHP
    <input type="submit">
</form>
```
### Select List
- A dropdown list with options.
- Allows the user to select one option from a list of pre-defined options.
- Created using the **`<select>`** element in conjunction with the **`<option>`** element.

```html
<form>
    <select>
        <option value="hampton">Hampton</option>
        <option value="lanham">Lanham</option>
        <option value="greenbelt">Greenbelt</option>
        <option value="richmond">Richmond</option>
    </select>
</form>
```

### Textarea
- Use to enable users to enter larger blocks of text than with the **`<input>`** tag.
- It is recommended to use the **maxlength** attribute to restrict the user's input to a certain number of characters. 
- Can also use the **cols** and **rows** attributes to adjust the width and height.

```html
<form>
    <textarea maxlength="100" rows="5" cols="30">Enter comments here.</textarea>
</form>
```

### Form Action
- Need the system to do something with the data when user submits a form.
- The action page is the page that the form is submitted to.
- This page could contain advanced scripts or programming that inserts the form data into a database or emails an administrator etc.

```html
<form action="/html/tags/html_form_tag_action.cfm" method="get">
    First name: <input type="text" name="first_name" value="" maxlength="100">
    Last name: <input type="text" name="last_name" value="" maxlength="100">
    <input type="submit" value="Submit">
</form>
```

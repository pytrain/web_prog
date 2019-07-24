<center><img src="http://www.nasa.gov/sites/all/themes/custom/nasatwo/images/nasa-logo.svg"></center>

# Introduction to HTML

## Useful Pointers
- [Intro to HTML/CSS: Making Webpages](https://www.khanacademy.org/computing/computer-programming/html-css) (from Khan Academy)
- [Introduction to HTML for Beginners](https://www.afterhoursprogramming.com/tutorial/html/introduction-html/) (from After Hours Programming)
- [HTML Tutorial](https://www.quackit.com/html/tutorial/) (from Quackit)

**We will cover the following:**
- Basic components of a web page
- Formatting
- Attributes
- Links
- Images
- Tables

## Basic Components of a Web Page
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

- The **<span><</span>!DOCTYPE...<span>></span>**  declaration tells the browser which version of HTML the document is using.
- The **<span><</span>html<span>></span>** element is the document's root element - it can be thought of as a container that all other tags sit inside (except for the !DOCTYPE declaration).
- The **<span><</span>head<span>></span>** tag contains information that is not normally viewable within your browser (such as meta tags, JavaScript and CSS), although the **<span><</span>title<span>></span>** tag is an exception to this. The content of the **<span><</span>title<span>></span>** tag is displayed in the browser's title bar.
- The **<span><</span>body<span>></span>** tag is the main area for your content. This is where most of your code (and viewable elements) will go.
- The **<span><</span>h1<span>></span>** tag defines a level 1 heading.
- The **<span><</span>p<span>></span>** tag defines a paragraph. This contains the body text.
  
## Formatting

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

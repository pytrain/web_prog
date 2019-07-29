<center>
  <h1>Introduction to jQuery</h1>
</center>

**We will cover the following:**
- [Obtaining jQuery](#obtaining-jquery)
- [jQuery Intro](#jquery-intro)
- [Selectors](#selectors)
- [Manipulation](#manipulation)
- [Events](#events)
- [Effects](#effects)
- [Resources](#resources)

## Obtaining jQuery
---

First, and foremost, jQuery is just a **Javascript library**. So, in order to _use_ this library, we must obtain it via one of the methods below:

1. CDN (Content Delivery Network) - hosted online [link](https://jquery.com/download/#using-jquery-with-a-cdn)
  a. [code.jquery.com](https://code.jquery.com/)
  a. [Google](https://developers.google.com/speed/libraries/#jquery)
  b. [Microsoft](https://docs.microsoft.com/en-us/aspnet/ajax/cdn/overview#jQuery_Releases_on_the_CDN_0)
  c. [cdnjs](https://cdnjs.com/libraries/jquery/)
  d. [jsdelivr](https://www.jsdelivr.com/package/npm/jquery)
2. Download and use locally: [link](https://jquery.com/download/)

Let's create a sample page and test the CDN from jquery.com:

```html
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <title>Demo</title>
</head>
<body>
    <a href="https://jquery.com/">jQuery</a>
    <script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
    <script>
      $( document ).ready(function() {
        $( "a" ).click(function( event ) {
          alert( "Thanks for visiting!" );
          event.preventDefault();
        });
      });
    </script>
</body>
</html>
```

Save this HTML file and then open it within the browser to obtain an alert that is coded for the link.

## jQuery Intro
---

Now that we have a local page with jQuery running from a CDN, let's look at the code that was used to create the behavior we experienced.

If we look at the example above, the `$()` is eseentially it's own object (also known as `jQuery`) which is used for selecting elements and allowing one to perform actions upon it. Notice how we have this separate from the jQuery loading line and we didn't edit the JS file.

```jquery
$();
jQuery();
```

If we look back at Javascript alone, many programmers wrap their code with an `onload function` to ensure that their code runs after the browser loads the document:

```javascript
window.onload = function() {
    alert( "welcome" );
};
```

Which will wait to run untail all images (including ads) are finished downloading. jQuery has the ability to run code when the document is ready instead

```jquery
$( document ).ready(function() {
    alert( "welcome" );
});
```

Here, we use the `ready` event to ensure that the document element, once ready, executes the function to alert the user.

**Note:** There is also subject matter related to traversing elements and chaining together operations using the `(.)` notation. We will not be covering this.

## Selectors
---

We can select elements of the page via
1. ID: `$( "#myId" );`
2. Class: `$( ".feature" );`
3. Attribute: `$( 'a[target="_blank"]' );`
4. Compound CSS: `$( "li strong" );`
5. Comma-separated: `$( "em, i" );`
6. Psuedo-Selectors: `$( "p:nth-child(2)" );`

We want to ensure that selections contain elements, so instead of testing if the selection returns true in a conditional statement, we check the length of elements selected:

```jquery
if ( $( "div.foo" ).length ){
  ...
}
```

which we can also save the selections into a variable:

```jquery
var divs = $( "div" ); // selects all div elements
```

There is a selection keyword that is available to be used within a jQuery function:

```jquery
$('div').click(function(event){ 
  $(this); // refers to div elements
});
```

## Manipulation
---

We use jQuery to select elements and then we can modify them directly.

```jquery
// Gets the value of the alt attribute
$('img').attr('alt');

// Sets the value of the alt attribute
$('img').attr('alt', 'Wild kangaroo');
```
The manipulation spans attributes, styles, and DOM changes. Some examples of styles and DOM changes are below:

CSS Style manipulation:

```jquery
$('h1 span').css('font-size', 'normal');
$('div').css({
  fontSize: '13px', 
  background: '#f60'
});
$('header').height(200);
```

DOM manipulation:

```jquery
$('section').prepend('<h3>Featured</h3>');
$('h1').text('Hello World');
```

### Exercise

Let's change the height of the link text on the sample page to be 40em.

[Here's](https://api.jquery.com/category/manipulation/) a list of the manipulation methods.

## Events
---

We can add event handlers to elements when an event occurs easily with jQuery. Below is an example where for all list items, if a user clicks on one of them, it adds a method `addClass` to the entire list of elements.

```jquery
$('li').click(function(event){
  $(this).addClass('saved-item');
});
```

Here's a fun [JS Fiddle example](https://jsfiddle.net/boilerplate/jquery) that changes the color of the box when a button is clicked.

### Exercise

Change the color of odd list items when a button below the list is hovered upon.

_Note:_ There is a shorthand for event methods `.on('click, function...)`.

## Effects
---

Instead of user interaction, [effects](https://api.jquery.com/category/effects/) can show/hide elements or move them too. Let's see a demo of this:

```html
<div class="notice-warning">
  <div class="notice-close">&#215;</div>
  <strong>Warning!</strong> I&#8217;m about to lose my cool.
</div>
```

```jquery
$('.notice-close').on('click', function(event){
  $('.notice-warning').fadeOut('slow', function(event){
    $(this).remove();
  });
});
```

## Resources
---

- [jQuery Official Tutorial](https://learn.jquery.com/)
- [jQuery Tutorial](https://learn.shayhowe.com/advanced-html-css/jquery/)

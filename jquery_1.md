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

1. CND - direct link to one online
2. Download and use locally

## jQuery Intro
---

We are going to start with a sample project within JS Fiddle that already loads jQuery for you with a page code as below:

```html
<html>
  <head>
    <title>jQuery addClass example</title>
    <script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.js"></script>
    <link rel="stylesheet" type="text/css" href="/css/result-light.css">
    <script type="text/javascript">
      window.onload=function(){
        // find elements
        var banner = $("#banner-message")
        var button = $("button")

        // handle click and add class
        button.on("click", function(){
          banner.addClass("alt")
        })
      }
    </script>
  </head>
  <body>
    <div id="banner-message">
      <p>Hello World</p>
      <button>Change color</button>
    </div>
  </body>
</html>
```

**Note:** There is also subject matter related to traversing elements and chaining together operations using the `(.)` notation. We will not be covering this.

## Selectors
---

## Manipulation
---

## Events
---

## Effects
---

## Resources
---

- [jQuery Official Tutorial](https://learn.jquery.com/)
- [jQuery Tutorial](https://learn.shayhowe.com/advanced-html-css/jquery/)

<center>
  <h1>Introduction to CSS (Cascading Style Sheets)</h1>
</center>

https://developer.mozilla.org/en-US/docs/Web
https://learn.shayhowe.com/
https://www.smashingmagazine.com/2019/01/how-to-learn-css/
https://learnxinyminutes.com/docs/css/

**We will cover the following:**
- [Basics of CSS](#basics-of-css)
- CSS Selectors
- [Resources](#resources)

CSS: animations, grids, backgrounds, box model, flexbox, transitions, positioning, typography

## Basics of CSS
--

- The purpose of CSS is used to manipulate how your HTML webpage is visually presented or "styled".
- The "Cascading" in CSS is that there is an inherent hierarchy of the styling rules upon an element. So, multiple style sources can apply to a single webpage (HTML) element.
- CSS can be inline in an HTML document, in the header of a HTML document, or as an external file that is referenced/loaded into the header of a HTML document.

```html
<!DOCTYPE html>
<html>

  <head>
    <title>HTML Programming Example</title>
    
    <style>
      h1 {
          font-size: 20px;
      }
    </style>
    
    <link href="style.css" type="text/css" rel="stylesheet">
  </head>
  
  <body>
    <h1 style="color: red">Create My First Website</h1>
    <p>Here are the basic components of an HTML document!</p>
    
    <h1 style="font-size: 30px">Another H1 Header</h1>
  </body>
  
</html>
```

Above, we can set the color of the first `h1` HTML tag contents to be colored red. If we wanted to do that for all of our h1 headings, we would include it in the header or in `style.css` as a reference to h1 as above where we have set all of the h1 font sizes to be 20px. Regarding hierarchy, the font-size style in the `<style>` tag changes all of the font-sizes of h1 texts to be 20px. Then, if there is a reference to h1 in the `style.css` file, that would override the prior application of the 20px font size. Next, if we look at the second h1 tag within the body of the HTML document, we see that for that particular text, we will have the font size as 30px instead of 20px. This last inline style overrides any styles on a more general scope.

As a general introduction as to the purpose of CSS, let's walk through a 4-minute tutorial on web design found [here](https://jgthms.com/web-design-in-4-minutes/).

https://www.freecodecamp.org/news/get-started-with-css-in-5-minutes-e0804813fc3e/

## CSS Selectors
---

1. Global (*)
2. Element (h1)
3. Class (.classname)
3. ID (#idname) - can only be assigned to one element (https://css-tricks.com/the-difference-between-id-and-class/)

## Fonts and Colors

## CSS Layouts

Exercises:
- Their own personal website or blog (sketch a draft, then create it)
- CSS Zen Garden
- Position planet - https://www.khanacademy.org/computing/computer-programming/html-css/css-layout-properties/pc/challenge-position-planet
- A photo gallery?

## Resources
---

- [cssreference.io](https://cssreference.io/): A good page reference of different types of css attributes
- [css weekly](https://css-weekly.com/): A css-centric email newsletter
- [Code Academy](https://www.codecademy.com/learn/learn-css)
- [BEM (Box Element Modifier)](http://getbem.com/introduction/#_=_)
- [CSS Layout Tutorial](http://learnlayout.com/index.html)
- [Web Design in 4 minutes](https://jgthms.com/web-design-in-4-minutes/#_=_)
- [Code Guide by @mdo](https://codeguide.co/#_=_)
- [Web Technologies - Mozilla](https://developer.mozilla.org/en-US/docs/Web)
- [CSS Diner](https://flukeout.github.io/): Fun website that gives you practice on selectors
- [CSS Selectors](https://www.sitepoint.com/css-selectors/)
- [Can I Use](https://caniuse.com/#home): Helpful website on browser compatibility
- [CSS Learning](https://github.com/micromata/awesome-css-learning)
- [CSS Huge Learning Resource](https://zendev.com/ultimate-guide-to-learning-css.html)
- [CSS on Solo Learn](https://www.sololearn.com/Course/CSS/)
- [CSS Documentation Reference](https://devdocs.io/css/)
- [Bootstrap CSS](https://getbootstrap.com/docs/3.3/css/): A good packaged CSS style made for you to use.
- [CSS Zen Garden](http://www.csszengarden.com/): A website that is fun to manipulate with very many examples from others.

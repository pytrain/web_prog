<center>
  <h1>Javascript: Part II (Application/Project)</h1>
</center>

This lecture period will be used to apply our new knowledge of combining HTML, CSS, and Javascript.

**We will cover the following:**
- [A Planetary Website](#a-planetary-website)
- [HTML](#html)
- [CSS](#css)
- [Javascript](#javascript)

## A Planetary Website
---

Single-page websites are beginning to become desired among the community of web developers. So, today, we are going to make a website/blog about the planets of our solar system (_Note:_ For those Pluto lovers out there, you are allowed to include it as well.)

Let's start with a sample HTML page that already has an associated CSS style with it so we can add more to it as well as apply our new knowledge of Javascript to this page.

### Exercise: Obtain Sample Code
1. Head on over to [CSS Zen Garden](http://www.csszengarden.com/) and download the example HTML file (index.html) and CSS file (style.css).
2. Put them in a folder labeled "planets" so that we can refer back to this project easily.
3. Open the "index.html" in your web browser to view what we are starting with.

## HTML
---

In this portion of the exercise, we will test your knowledge of HTML to aid in making our planetary website even better!

1. Change the title and subtitle of the page to your plantary website title.
2. Comment out the line that loads the CSS file. We will put it back, but only after we have modified it.
3. Remove the sidebar ("aside") portion of the website.
4. Put a line under our site's title.
5. Let's create some navigation by putting an unordered list underneath this horizontal line with the names of the planets.
6. Next, remove the rest of the content so that we can put some of our own there.
7. Add headings for each of the planets and link to them on the page from the unordered list (i.e., the list of planets will become our navigation; anchor links).
8. Under each planet, let's add one line of text in a paragraph to describe this planet. If you want to get fancy, add a table with facts about the planet.
9. Add an image of each planet either before the descriptive text or after.
10. Uncomment the style sheet in the header of the webpage.

## CSS
---

In this portion of the exercise, we will now modify the CSS style to add some flare to our website.

1. Open style.css in your text editor and familiarize yourself with the contents.
2. If you look at your website, you will notice the the "Zen Garden" logo and title are still showing up. Let's remove all background images.
3. Why can't we see our website's title? Fix this issue by only modifying the style.css file.
4. The alignment of our title and subtitle aren't looking so great. Let's align this in the center of the page. (this might take some time to do)
5. Since we have a navigation, let's work on the style of this:
  1. Remove the dots or bullet points from the unordered list.
  2. Change the font size to be 30px.
  3. Align this text to be on the same line next to each other.
  4. Change the color of these to be some type of green.
6. Lastly, let's put back the logo of the page and modify it to be the NASA logo.

## Javascript
---

In this last portion of the exercise, we add functionality to the page by creating events and interactions.

1. For the first planet, change the background color of the web page to symbolize that particular planet when a user hovers over the section title.
2. In the header of the page, let's put a number of planets by counting how many sections or navigation links there are in the HTML code.
3. Alert the user a fact about the last planet when they click on either the last section heading or navigation.
4. Add Pluto the navigation and a section title by prompting them at page loading whether or not they support Pluto.
5. Put this code about Pluto in a function so that it is separate from other Javascript code and ensure it still works.

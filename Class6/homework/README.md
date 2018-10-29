# HOMEWORK

## FEWD Week #3: Advanced Topics in CSS

<br>

### Description

This week we learned about pseudo classes, pseudo elements, positioning and responsive design.  Let's update our blog with what we've learned.


### BONUS

Want to have a little fun?  After next week, we'll be focusing on the Javascript portion of our curriculum, let's get a headstart and make our menu slide into place or out of view when we click the menu toggle.

To do this we need to add two new elements to our html page.  Both elements are `<script>` tags.  The first script tag is a link to the jQuery CDN.  You may remember when we talked about using Google Fonts that we discussed how CDNs (or Content Delivery Networks) were a network of super fast servers that deliver content to our users.

Similar to how we need to first load Google Fonts on our page in order to use them in our CSS, we need to load jQuery first before we can use it in our Javascript.  While the `link` tag is used to load external CSS files, the `script` tag is used to load external Javascript files.

The `script` tag does double duty in that it can be used to both load an external Javascript file **or** wrap Javascript code on our html page (sort of like how we can write CSS directly in our HTML file if we wrap it in `style` tags).  The second `script` tag wraps our code that makes our toggle work.

Here's the code you need to add to your page.  Make sure to **add it _after_ your closing `</footer>` tag** and **_before_ your closing `</body>` tag.**

```html
<!-- The closing footer tag should be above this comment -->

  <script src="https://code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8=" crossorigin="anonymous"></script>

  <script>
    $('.menu-toggle').click(function(){

      $('header nav').slideToggle();

    });
  </script>

<!-- The closing body tag should be below this comment -->
```

Does it work?  Let's unpack what's happening here:

1. We load jQuery from the CDN source in the first script tag.  Once it's loaded, we can use it in our scripts on the page, which is what we do in the second `script` tag.

2. Inside the second `script` tag, we wrote a little script that uses jQuery to *listen* for clicks on the the element with the class of `menu-toggle`.  Whenever a click happens on the menu toggle, it runs the code inside the function.

3. The line inside the function goes into our page DOM and finds the element that matches our selector of `header nav` and then uses the jQuery method called `slideToggle()` to cause the header nav to slide up and out of view if it is currently displayed, or slide down and into view if it is currently hidden.

If you watch the header nav element in the dev tools while clicking on the menu-toggle, you'll see that jQuery is just applying some inline styles to our header nav.  It uses those styles to animate our element and when it's done it makes sure that the element stays hidden by applying the style `display: none`.  You might notice that this can cause a problem if you collapse the menu and then make the window wider.  The menu disappears entirely!  That's because the style `display: none` is still applied to the element inline.  We can fix this though by just adding `!important` to the display rule in our CSS media query.  You might remember that this special keyword is the only way to override inline styles, which would normally have the highest specificity. Make sure you **only** add this rule to your media query so that you're overriding the display property exclusively on larger devices.

```css

 \* Add the !important keyword to your header nav display property in the media query *\

   header nav {
    position: static;
    width: 50%;
    display: flex !important; /* <-- Add it here */
    justify-content: space-between;
    float: right;
    margin: 1.5rem 2rem;
  }

```

Congratulations!  You just wrote some Javascript.  :tada:




### Resources

[Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)

[Responsive Web Design](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)



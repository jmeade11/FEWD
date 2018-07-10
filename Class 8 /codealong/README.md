# CODEALONG

## jQuery Syntax

In this class, we'll be learning the basics of loading jQuery and using it to do some things like adding, removing and toggling classes.

Don't forget, you must load jQuery into your webpage where you want to use it first!

To get some practice with that, copy and paste the web page below into a new file and save it locally.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Loading jQuery</title>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.1.0/css/all.css" integrity="sha384-lKuwvrZot6UHsBSfcMvOkWwlCMgc0TaWr+30HWe3a4ltaBwTZhyTEggF5tJv8tbt" crossorigin="anonymous">
  <style>
    * {
      box-sizing: border-box;
    }
    html, body {
      margin: 0;
      background-color: deepskyblue;
      color: rgba(255,255,255,.9);
      min-height: 100vh;
      font-family: sans-serif;
      font-size: 120%;
    }
    header {
      position: relative;
      padding: 2rem;
      background-color: darkorange;
      min-height: 7rem;
    }
    nav {
      position: absolute;
      bottom: 0;
      right: 0;
    }
    nav a {
      color: white;
      padding: 2rem;
      text-decoration: none;
    }
    main {
      display: flex;
      flex-wrap: wrap;
    }
    main div {
      width: 50%;
      height: 35vh;
      padding: 2rem;
      text-align: center;
      color: darkblue;
    }
    i {
      font-size: 5rem;
    }
  </style>
</head>
<body>
  <header>
    <i class="fas fa-history"></i>
    <nav class="menu">
      <a href="#home">Home</a>
      <a href="#products">Products</a>
      <a href="#testimonials">Testimonials</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>
  <main>
    <div id="electrify" class="bolt">
      <h2>Electrifying</h2>
      <i class="fas fa-bolt"></i>
    </div>
    <div id="timesaver">
      <h2>Timesaver</h2>
      <i class="fas fa-stopwatch"></i>
    </div>
  </main>



<!-- Load your scripts here -->

</body>
</html>


```

The steps to load jQuery are as follows:

<ol>
  <li>Go to: <strong style="color: var(--ga-red)">https://code.jquery.com</strong></li>
  <li>Choose the latest version of jQuery (currently 3.3.1) and click the link for the <strong><em>minified</em></strong> package (not slim minified)</li>
  <li>Copy the script tag in the modal window</li>
  <li>Paste it in your web page <strong><em>before the closing body tag</em></strong></li>
</ol>

### CodePen CodeAlongs


#### [Menu Toggle](https://codepen.io/jme11/pen/dKLLxr)

jQuery has already been added to this Codepen for you. Click the **Fork** button to create a copy for yourself.

##### Using the addClass() Method

We’re going to add a class to the body tag when the page loads.  To do this we use the basic jQuery syntax of:

```js
$('selector’).action();
```

The selector we’ll be using is the ```body``` and the action (technically called a method) is ```addClass()```, but the addClass method needs to be told which class to add.  We do that by passing the class name to the method in the parentheses.

Type: ```$('body').addClass('let-there-be-light’);``` in the JS window.  When you do and the page is refreshed, it will add the let-there-be-light class to the body and the animation will play.  Notice that the class is added to the body but has two effects:

The background color of the body is changed from black to green.  The transition property in the body declaration ensures that the color is transitioned smoothly.  This is done with these two declarations in our CSS:

```css
body {
  background-color: black;
  transition: background-color 3s 2s;
  backface-visibility: hidden;
}

.let-there-be-light {
  background-color: green;
}
```

The logo animates into place.  This is done by taking advantage of the general descendant combinator!  Notice the CSS declaration:

```css
.let-there-be-light header img {
  animation: grow-in 3s both 1s ease-in-out;
}
```

The declaration above applies the animation to any ```img``` element in the ```header``` but **only** if one of its ancestors has the .let-there-be-light class!

##### Adding An Event Listener and Handler

Now we want to wire up our menu.  If you click on the menu toggle in the upper right corner, nothing happens.  We need to fix that.

The CSS is already set up to make the menu appear when a class of ```open``` is added to a parent of the toggle.  Let's make sure it works by doing that manually.

In the HTML, add the ```open``` class to the header element.  Notice what's happened.  The menu is now displayed.  That's because in the CSS we have the following declarations:

```css

#menu {

 /* Removed styles for brevity */

  position: fixed;
  top: 0;
  right: -75%;
  bottom: 0;
  z-index: 5;
  transition: .5s right ease-out;

}


.open #menu {
  right: 0;
}

```

So, what's happening here is that the menu by default is placed using fixed positioning with it's right property set to -75%.  This has the effect of moving the menu offscreen to the right so it isn't visible.  When the open class is added to any ancestor though, it causes the right property of the menu to be overridden with the value of 0.  That means that the menu will be positioned on the right edge of the viewport.  The transition property makes it slide in nice and smoothly.

Okay, remove the open class now from the HTML.

We need to set up an **event listener** to *listen* for clicks on the the menu-toggle and then respond to them by adding the open class to the header element.  Let's start with setting up the event listener.  Event listeners follow a similar pattern:

```js
$('selector').event_to_listen_for(function(){ /* Here's where we respond */ });
```

So, we start with the selector the same as we did before, and the event we're going to listen for is the click event. Add the event handler after the first line of code you added in the steps above to the JS window in CodePen.

```js

$('#menu-toggle').click(function(){


});
```

After typing the function part out on one line, we add some returns between the curly braces to make room for our handler code.

To create the handler (what we want to happen when a click is observed), you can follow the pattern above to use the ```addClass()``` method to add the open class to the header using jQuery. Your code should look like this:

```js

$('#menu-toggle').click(function(){

  $('header').addClass('open');

});

```

Does it work?  Sort of.  The class is added and the menu opens, but it never closes.  We can use a different method to get the behavior we want.  That method is ```toggleClass()```.  The toggleClass method will add the class(es) you pass to it inside the parantheses if they don't exist *or* remove them if they do exist.  Change the addClass() method to toggleClass() and test it again.


#### [Traffic Light](https://codepen.io/jme11/pen/KeLOgP)

jQuery has already been added to this Codepen for you. Click the **Fork** button to create a copy for yourself.

##### Creating Click Handlers

Follow the pattern to add classes to turn on the lamps with the corresponding button.

Using the addClass() method to illuminate the lamps works great, but it doesn't really behave like a proper traffic light.  We need to cause all of the other lights to turn off when one lamp is illuminated.

To do this, you'll use ```removeClass()``` to remove the classes for both other lamps in each click handler.  The removeClass method works just like the addClass and toggleClass methods.

If you got the removeClass method to work, congrats!  However, we can still do a bit better.  Clean up your code by consolidating the removeClass methods into one statement by using the comma combinator in the selector.  Remember, the comma combinator means that each selector is separately targeted.  The classes will need to be combined as well.  Because ```removeClass()``` will only remove the class if it exists, you can safely pass it both class names.  Be sure to just use a space to separate the class names (just like you would in html).


#### [Bouncing Ball](https://codepen.io/jme11/pen/xzeqjz?editors=0110)

jQuery has already been added to this Codepen for you. Click the **Fork** button to create a copy for yourself.

##### Creating Click Handlers for the Red and Blue Buttons

Now you're on your own.  Use your new skills to add click handlers for the red and blue buttons.  Remember to make your selector target **only** the buttons with the red or blue class in the event listener.  (If you just use the blue or red class as the selector, the ball will have a click handler added as well).

When you click on the button it should remove the current color class on the ball then add the corresponding new class.  For example, when you click on the blue button, it should add the blue class to the ball, but also remove the red class.

Did you get the ball to change between red and blue?  Awesome!  Once again, we can make our code cleaner and more efficient by using what's known as **method chaining**.  Method chaining allows us to chain the add and remove class methods in one statement.  This is more efficient, because the Javascript engine only has to find the element with the id of ball once!  Method chaining looks like this:

```js
$('selector').action().action();
```
##### Creating a Click Handler for the Bounce Button

The bounce button has several additional challenges in that there’s no unique class or id on the bounce button.  See if you can create a selector using a pseudo class that will target only the 3 third button in the group, or the last button in the group.

The bounce button also needs to *toggle* the bounce on and off, since there’s no corresponding waiting button.

Finally, in your css, move the waiting class to the end of the CSS file.  (Just select the class and its declaration, cut it and then paste it after all of the other declarations in the css area).  Click on the bounce button.  If you simply used toggleClass on the bounce class, notice how the button no longer works!  Why?  You can right-click on the ball and inspect it to see that the bounce class is being added, but the waiting class is still there.  That was fine when the waiting class was before the bounce class in the css, but when you move it, it no longer can be overridden because of the cascade order of the css.  To make our Javascript more ‘resilient’ (less likely to break from a change that we make to a different part of our program), you’ll need to also toggle the waiting class off and on.  Chain your methods to toggle between the bounce and waiting classes.


## Additional Methods to Practice Using

We also looked at the following methods in class:

```fadeIn()```: fades in a hidden element that has display none applied to it.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```fadeOut()```: fades out a visible element.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```fadeToggle()```: toggles between fading in a hidden element or fading out a visible element.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```slideDown()```: slides a hidden element that has display none applied to it down to cause it to display.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```slideUp()```: slides a visible element up to cause it to be hidden.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```slideToggle()```: toggles between sliding down a hidden element or sliding up a visible element.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```css({'property': 'value'})```:  You can add any inline styles to elements with the css() method.  The styles are passed as an object (we'll learn more about this later).  The object syntax is as follows:

```js

{'property': 'value', 'property': 'value', 'property': 'value'}

```

Notice that we add quotes to the properties and values and separate them with a comma.  If you forget the quotes on the properties, that's okay, but if the property name has a hyphen in it (like background-color), it will cause an error.  You **may not** use any other punctuation to separate the property: value pairs other than a comma, and you will get an error if you have a trailing comma (i.e., a comma at the end of the list).

```hide()```: hides an element by adding display: none to it.

```show()```: shows an element by adding display: block to it.

```toggle()```: toggles between the show and hide states.








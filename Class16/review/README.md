# REVIEW

#### [Style Changer](https://codepen.io/jme11/pen/XBJBWp?editors=0110)

jQuery has already been added to this Codepen for you. Click the **Fork** button to create a copy for yourself.

##### Review: Creating Event Listeners and Event Handlers

You can see a demo of the page we'll be building [here](https://codepen.io/jme11/live/WzJrad).  Click on the vertical dots to display the menu and test its features.

We've covered a ton of jQuery in the last few weeks, so let's be sure we have the basics down pat.

1. Create an event listener for the menu-toggle and use the slideToggle method on the menu in its handler.  Remember that slideToggle is one of the built in effects that jQuery does out of the box, so there's no CSS we need to add to animate the menu.

2. Add an event listener for the font-family switcher.  In the event handler, toggle the sans-serif class.

3. Create an event listener for **each** of the light and dark themes. Use the toggleClass methods to add/remove the corresponding `.light` and `.dark` classes to the body element.

##### Working with Variables

To make the text larger or smaller, we're going to take advantage of the fact that font-size is inherited from its parent by default in CSS.  Notice that I've used rem or em for all of the font sizes within the CSS for the page.

The plan is to:

1. Get the current computed base font-size for the page and store it in a variable temporarily.
2. Next, we'll multiply the current font-size by 1.1 to make it larger or .9 to make it smaller.  In order to perform math operations, we need to make sure we're working with numbers!
3. Use the ```.css()``` method to set the base font size on the body.  To do this, we'll have to make sure our value has 'px' appended to it.

###### Getting the Computed Font Size

Many of the methods in jQuery are known as both *getters* and *setters*.  That means that we can use them without a value to retrieve the current value (i.e., as a getter), or pass a new value to set it.

We'll use the ```.css()``` method to retrieve the value of the font-size of the body as follows:

```js
const currentSize = $('body').css('font-size');
```
We're using ```const``` here to declare our variable because it is a *constant* value that we won't be reassigning.

###### Converting the Value to a Number

Remember that Javascript does this thing where it tries to *coerce* values into the datatype that it thinks you want.  If a string contains only numeric digits, Javascript will just do the job of converting the string to a number when we try and carry out a mathematic operation.

Let's check what the value of currentSize is by logging it to the console.  After the variable declaration, add the following line and then check the console:

```js
console.log(currentSize);

```

Unfortunately, the output we get is ```14.4px```.  That means that we have to do the conversion ourselves.  Fortunately, there's an easy way to do that in this case.  Because the number portion of the string that we want is the first part of the string, we can use either the Javascript ```parseFloat()``` or ```parseInt()``` methods.  The parseFloat method is better for us here because it returns the number with all of its decimals.  If we just wanted the integer (i.e., the part before the decimal), we would use parseInt() instead.

Let's create a second variable to store the result of parsing the value and multiplying it by the corresponding larger or smaller factors.

```js
/* To enlarge the text, we use 1.1 */
const newSize = parseFloat(currentSize) * 1.1;

/* To reduce the text size, we use .9 */
const newSize = parseFloat(currentSize) * .9;

```

###### Setting the New Font Size

The last part is simple.  We're going to just use the css() method again to set the new font size, but we need to concatenate the 'px' to the end of the value stored in the variable.

```js

$('body').css({'font-size': newSize+'px'});

```

###### Putting it All Together

Use the above techniques to create two new event listeners and handlers for the ```#smaller``` and ```#larger``` elements.


##### Resetting Everything

Now that all of our style changers are linked up, we can handle the reset.  Start by creating an event listener for the ```#reset``` element.  For the event handler inside it, we need to do the following:

1. Remove all of the styles from the body.
2. Remove any of the dark, light, or serif classes that may have been added to the body.
3. Reset the text in the ```#font-family span``` to read: 'Serif Font'.

###### Remove All of the Styles from the Body

To remove all of the styles, there are three options:

1. Use the `attr()` method and pass it ```'style', ''``` in its parathenses.  The empty string that you give it will replace the styles and effectively remove all of them.
2. You can also do this with the similar method ```prop()```.
3. Finally, you can use the ```removeAttr()``` method.

Let's use the last one because it's the one that makes it clearest what we're doing here.

```js
$('body').removeAttr('style');
```

###### Remove the Class that were Added to the Body

To remove dark, light and serif classes, remember that you can pass them all to the removeClass() method in one go separating them with spaces only.  This is safe and reliable because jQuery automatically only removes the classes that it finds.

Also, since we're working with the body again, let's chain those methods:

```js

/* Writing each operation on its own line makes it easier to read */

$('body')
    .removeAttr('style')
    .removeClass('dark light serif');
```

###### Changing the Text in the Font-Family List Item

This part is easy.  We'll just use the text() method:

```js
$('#font-family span').text('Serif Font');
```



##### BONUS

Can you swap the text of the font-family switcher when you click on the link?  There are several ways to do this but one way is:

1. Use the body selector and the getter for the css() method to determine what the current font is and store it in a variable called currentFont. Make sure to grab the value before you change it by toggling the class (in other words, you'll want this code statement to be the first thing in your event handler).

2. Use the text method to update the value of the text inside the span tag with the value of the currentFont variable.

3. To captialize the text, you can add a CSS rule for the span tag and use the ```text-transform``` property.

4. To make it really professional, you can use those string literals to concatenate the currentFont variable with the word 'Font', so it reads "Sans-Serif Font" or "Serif Font".



## Additional Methods to Practice Using

In today's class we looked at one of the DOM manipulation methods for changing text, add this to your list:

```text()```: Replaces everything inside the selected elements with the plaintext that you supply within the parantheses.  Don't forget that text is always a string so you must enclose it in quotes unless you're passing it via a variable.

```fadeIn()```: fades in a hidden element that has display none applied to it.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```fadeOut()```: fades out a visible element.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```fadeToggle()```: toggles between fading in a hidden element or fading out a visible element.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

```slideDown()```: slides a hidden element (one that has display none applied to it) down to cause it to display.  You can pass it values like 'slow' or a number (remember no quotes around numbers), which represents the time in milliseconds.  1000 milliseconds = 1 second.

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








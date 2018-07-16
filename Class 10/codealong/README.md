# CODEALONG

## Loading jQuery Review

The steps to load jQuery are as follows:

<ol>
  <li>Go to: https://code.jquery.com</li>
  <li>Choose the latest version of jQuery (currently 3.3.1) and click the link for the <strong><em>minified</em></strong> package (not slim minified)</li>
  <li>Copy the script tag in the modal window</li>
  <li>Paste it in your web page <strong><em>before the closing body tag</em></strong></li>
</ol>

### CodePen CodeAlongs

#### [Day, Evening or Night?](https://codepen.io/jme11/pen/jpqwvR?editors=0010)

jQuery has already been added to this Codepen for you. Click the **Fork** button to create a copy for yourself.

You can see a demo of the page we'll be building [here](https://codepen.io/jme11/live/OwNgMO).  When the page loads, it will display a message indicating the time of day it is.

1. The getHours() of the Javascript date object returns just the hours portion of the time as 0-23 hours.  There are already three variables created.  Use console.log() with each of the variables to see what they return.

```js
/* for example... */
console.log(time);
```
2. You will need to write 3 separate if statements.  Each one needs to evaluate to true or false.  Each condition will have two parts: the starting time and then the ending time.

```js
/* for example... */
if(hours >= 6 && hours < 12) {
  /* if the hours are greater than or equal to 5 AND
     less than 12 do something */
}
```

The times you'll want to check for are:

- If the hours are 5:00AM - 4:59PM: It's daytime
- If the hours are 5:00PM - 9:59PM: It's evening
- If the hours are 10:00PM - 4:59AM: It's nighttime

3. Inside of each of the if statements, add the corresponding text to the h1 element (i.e., It's daytime, etc.) and add the corresponding class to the body (i.e., day, evening, night)

#### [Show Password](https://codepen.io/jme11/pen/XBXvqe?editors=0010)

jQuery has already been added to this Codepen for you. Click the **Fork** button to create a copy for yourself.

You can see a demo of the page we'll be building [here](https://codepen.io/jme11/live/QBNyMb).  Type a value in the password field and toggle the checkbox to show and hide the value.

Take a moment to familiarize yourself with the form portion of the pen:

```html
<form>
  <h2>Login To Your Account</h2>
  <input placeholder="Username" type="text"></input>
  <input placeholder="Password" type="password" id="password"></input>
  <input id="show-password" type="checkbox">
  <label for="show-password">show password</label>
  <button>Login</button>
</form>
```

We haven't worked with forms or form inputs yet (but we will in detail in a future class).  Notice that there are are three types of inputs in this form.  One input has a type of **text**.  Another input has a type of **password**. Finally, there is an input with a type of **checkbox**.

The ```type``` attribute (also called a property in HTML parlance :smile:) controls how the browser treats its contents.  Inputs with the password type are automatically obfuscated so that you can't read what's entered in them, whereas inputs with the checkbox type render as checkboxes and have a checked or unchecked state.  Inputs with the type of text are general purpose inputs that accept any alphanumeric value.  You'll learn about many more input types before you've completed this course.

##### Control Flow in Practice

Today's class is all about control flow.  We'll be learning several ways to make our programs do things based on a condition that evaluates as true.  The most common way we do this is with an *if statement*.

In this codepen, we're going to use an if statement to check if the "show password" checkbox is marked.  If it is, we'll change the password input type so that the password is displayed in plain text.  If it isn't checked, we'll set the password input type to password.

So the steps are:

1. Create an event listener that listens for clicks on the show password checkbox.

2. Write an if-else statement that checks if the checkbox is checked.

3. If the checkbox **is** checked, set the type property on the password input to **text**.

4. If the checkbox **is not** checked, set the type property on the password input to **password**.


###### Checking for the Checked State of a Checkbox

Every if or else if, statement checks for a boolean value of true.  If the condition inside the parantheses of the if statement is **true**, the code inside the curly braces that follows it will be run.  If it is **not true** the code in the curly braces immediately after the parantheses is ignored.

The basic syntax for an if statement is:

```js
if (condition) {

  /* if the condition above is true
     any code here will be run */

}
```

The jQuery ```.is()``` method returns true or false, which makes it perfect for the condition part of the if statement.  For the .is() method, we need to tell jQuery which element(s) to check, and the *state* to check.  So, in this case, we'll pass the value ```':checked'``` to it.

```js
$('#show-password').is(':checked');

/* This will return true or false for the checkbox with the id of show-password  */

```
###### Swapping the Input Type

We seen the ```.prop()``` and ```.attr()``` methods in jQuery before when we wanted to remove all of the styles from an element.  In that case, we passed an empty string to the style property.  This time we want to pass an actual value to the type property on the input field to change it.  The basic syntax is as follows:


```js

$('selector').prop('property', 'value-to-set');

/* The attr method works here too */

$('selector').attr('property', 'value-to-set');

```

Since we know that inputs with the type of "text" display the input contents in plain text and the "password" type obfuscates the contents, all you have to do is write an if-else statement that will set the property type to text when the checkbox is checked and then if it is not true, use the else to make sure the property is set to password.

##### BONUS

To make our code a bit more efficient, we can use the $(this) selector in our if statement.  Can you make it work? :smile:



## Additional Methods to Practice Using

In today's class we looked at one of the DOM manipulation methods for changing text, add this to your list:

```html()```: Replaces everything inside the selected elements with the html that you supply within the parantheses.  Don't forget that html is always a string so you must enclose it in quotes unless you're passing it via a variable.  **Very similar to the text method.**

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








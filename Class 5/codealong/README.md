# CODEALONG

## CSS Positioning

In this class, we'll learn how to precisely position elements on the page using the CSS **position** property.  You should understand how each of the following affects the elements it's used with and the elements around it.

1. Relative position
2. Fixed position
3. Absolute position

## CSS Transforms

The CSS **transform** property applies a 2D or 3D transformation to an element. This property allows you to rotate, scale, move, skew, and add perspective to elements.

We'll only be covering this topic briefly, but we'll revisit it when we cover Animations next week.

## CSS Pseudo Classes

Pseudo classes are used to select elements when they are in a special *state*. For example, when an element is being hover over, or when it is the last or first child of its parent element.  These can be sometimes less than intuitive, but they are incredibly useful both in your CSS and in Javascript.  Pseudo classes are preceded in your CSS with a ```:```.

## CSS Pseudo Elements

Pseudo elements are very different from pseudo classes.  Pseudo elements are parts of elements that can be styled through CSS.  You use ```::``` followed by the pseudo element name to use it in your CSS.  And, fyi, you can't use these as selectors in Javascript.

You may have already learned how to use one pseudo element when you did the Relaxr blog.  If you created a drop cap, you may have done so with the ```::first-letter``` pseudo element!

The two most useful pseudo elements are the ```::before``` and ```::after``` elements.  These create actual elements that are **injected into the DOM through our CSS**!



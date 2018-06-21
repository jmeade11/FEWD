# FEWD Week #2: CSS Selectors & Layouts

<br>

---

### Description

Now that you know how to use multiple techniques to layout your page, which one will you use?  Refer to the codealong exercises from Class 4.  They should help you to make your layout work no matter what technique you choose.

If you nailed the homework, CONGRATS!  Ready to do some more?  Check out the [Flexbox Froggy](http://flexboxfroggy.com/) or [Grid Garden](http://cssgridgarden.com/) games to practice your skills and learn about some of the properties we didn't cover in class.

<br>

---

### Helpful Hints

#### Floats? Flexbox? Grid?

If you're undecided on which technique to use, try Float or Grid.  Flexbox isn't really a great choice for laying out a whole page, because it only allows us to control the layout in one direction.  Flexbox is a great choice for individual elements on the page though, so if you want to get some practice with it, try using it to layout your top navigation.

Using a combination of techniques to achieve the best outcome — mixing flexbox or floats at the element level with grid to layout your overall page for example — is not only perfectly acceptable, it's actually the best way to go.

##### When to use Float

- Floats are great if you want to have **text flow around an image** or a pull quote.  This is precisely what they were designed to do.
- Float is also helpful for page layout, if you know you really must **support very old browsers** like Internet Explorer.  If your webpage design must be reproduced faithfully for every site visitor, using float will give you the best coverage today.
- There is a technique that allows you to conditionally load styles for Internet Explorer 10 and 11.  This would be an option for allowing you to use modern tools like Flexbox and Grid, but provide at least a comparable experience for those who are still using older versions of Internet Explorer.  Read more about this technique [here](https://paper-leaf.com/blog/2014/09/targeting-ie-10-11-browsers-css/).

##### When to use Flexbox

- Flexbox is a great option for laying out **parts** of your page.  For example, if you have a group of elements that you want to all align in a column or row and you want to be able to have fine grain control over the placement of the items, flexbox is the ideal option.
- Flexbox is also the way to go if you want to **vertically align** elements in their container.  No other CSS properties allow us to do this so easily and without hacks.
- Flexbox is also a great choice if you have lots of similar elements that you want to layout as a collection.  For example, if you have a card design, where each card links to an article or blog post, or for a **gallery** of thumbnail images.  The flex-wrap property makes this easy and reliable.

##### When to use CSS Grid

- Grid is the ultimate choice for **laying out entire pages** of content.  The intuitive and declarative properties for grid areas and the breadth of properties for adding gaps; dealing with flexible sizing and wrapping; handling overlap; etc., make this the hands down winner.  The only drawback is that because it is the newest standard of the three, it has the poorest support of them all.  Still, support is available in all major browsers today since late last year, so this is something you should invest in learning.
- Grid can also be a great option for **laying out components**.  Components are groups of elements that together form a distinct and reuseable building block in your page.  For example, if you have a [card design](https://econsultancy.com/blog/64646-15-delicious-examples-of-card-based-web-design) where you'll have lots of similar cards displayed on the page, grid is a great option to layout the card itself.

#### How to Add Google Fonts

Google fonts are a great for achieving a more polished design on the web.

##### Why do We Need Google Fonts?

So far, we've been using either the default font declaration or specifying 'sans-serif' as our alternative font-family.  This is fine, but it's pretty boring.  On the web, if we want to jazz things up with better looking fonts, we have to use a font service.  Why?  Because we simply don't know which fonts will be installed on a user's device.

Font files that we specify when we use Google Fonts have to be sent to the user's browser... and they can be big files, which can slow things down.  That's not good for UX.  Google Fonts serves the fonts we choose from a super fast network of servers designed and optimized to deliver web content called a CDN (Content Delivery Network).  Also, since Google Fonts are so popular among web professionals, our site visitors may actually have already downloaded the same font we've specified when they visited another website.  That means that the font may already be cached on their machine.  CDN's make sure that if we have already downloaded the content being served (the font file in this case), it doesn't resend the file unless it's been changed and we need a newer version!

##### Using Google Fonts

1. To use Google Fonts, go to https://fonts.google.com/.
2. Click on the ⨁ symbol next to the font name for the font you wish to use.
3. A pop up titlebar will apear at the bottom of the screen the total number of font families you have selected.
4. Click the titlebar to display the details for that font.
5. There are two links in red that read **Embed** and **Customize**.
6. Click the **Customize** link and choose the font weights and styles you want to include in your page.  **REMEMBER**: font files are big, so make sure to only select the font weights and styles you really need or your site visitors will have to download files unnecessarily.
7. Click back on the **Embed** link and copy the link code.  It will look something like this, depending on the font, font weights and font styles you choose:
```html
<link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">
```
8. Add this link to your page ```<head>``` tags and **make sure to put it *before* your page stylesheet**.  The Google Fonts stylesheet acts like any other stylesheet and is subject to cascading rules.  If you don't add it first, the fonts may not display as expected.
9. Back on the Google Fonts page in the pop up modal, there will be the CSS rule that you'll use for you fonts in your stylesheet.  So copy the code under the title **Specify in CSS** and add it to the rule set for your selector.  For example, if you want to use the Roboto Google Font everywhere in your page, you would add it to your html selector rules:
```css
html {
  font-family: 'Roboto', sans-serif;
}

/* You can also specify, different fonts for unique elements on the page */
h1, h2 {
  font-family: 'Lobster', cursive; /* Now, only h1 and h2 elements will have this font */
}
```
Note that there are *fallback* fonts specified in the CSS declarations.  The Roboto font, for example, will fallback to sans-serif if the Roboto font doesn't load for any reason.  In this case the default sans-serif font for the device is used instead.
10. To specify a different font-weight, use the numbers that correspond to the weights that you've added to your initial font selection.  For example, the Roboto font has 12 different styles ranging from *thin* to *black*.  To use the thin version, you would add the font-weight to your CSS declaration like this:
```css
h1 {
  font-weight: 100;
  /* All your other styles for h1 can go here too */
}

##### Other Options

Google fonts also has some additional styles that you can use to make your fonts stand out.  Check them out in the [Guide to Google Fonts](https://developers.google.com/fonts/docs/getting_started).

<br>

---

### Resources

[Google's Guide to Google Fonts](https://developers.google.com/fonts/docs/getting_started)

[CSS Tricks Complete Guide to Using Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

[CSS Tricks Complete Guide to Using Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)



# HOMEWORK

## FEWD Week #2: CSS Selectors & Layouts

<br>

### Description

Now that you know how to use multiple techniques to layout your page, which one will you use?  Refer to the codealong exercises from Class 4.  They should help you to make your layout work no matter what technique you choose.

If you nailed the homework, CONGRATS!  Ready to do some more?  Check out the [Flexbox Froggy](http://flexboxfroggy.com/) or [Grid Garden](http://cssgridgarden.com/) games to practice your skills and learn about some of the properties we didn't cover in class.

<br>

---

### Design File Details

#### Colors

background color: #f0efef<br>
yellow: #f9e42e<br>
dark blue: #033048<br>
light grey: #606161<br>
almost black: #121212<br>

#### Fonts

Font: [Open Sans](https://fonts.google.com/?query=open+sans)
Weight: 300 Light, 600 Semibold, 800 Extrabold

#### Layout

Main column width: 65% <br>
Sidebar width: 35% <br>
Gutter: 1em <br>

#### Images

[Relaxr Logo White](relaxr-images/relaxr-logo-white.svg)

[Relaxr Logo Yellow](relaxr-images/relaxr-logo-yellow.svg)

[Blog Photo 1](https://raw.githubusercontent.com/jmeade11/FEWD/master/Class4/homework/relaxr-images/blog_photo1.jpg)

[Blog Photo 2](https://raw.githubusercontent.com/jmeade11/FEWD/master/Class4/homework/relaxr-images/blog_photo2.jpg)

[Facebook Icon](relaxr-images/facebook.svg)

[Twitter Icon](relaxr-images/twitter.svg)


#### Styles

##### Header

Nav: Semibold, 1em;

##### Main

Post Titles - 2em, semibold

"How I implemented Relaxr in 2 weeks and changed my life"

"I traveled across the globe thanks to Relaxr’s Excel automation"

Blog Text - Light 1.1em

Here's some lorem ipsum you can use **or** if you have installed Emmet, you can simply type lorem and press the tab key:<br>
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rerum veritatis voluptas quibusdam eum, non quos itaque iure pariatur laboriosam excepturi vero.

Remember to wrap each post including it's heading, image and text in `<article>` tags!

To make your drop caps look up `::first-letter` on Google.  You'll need to use float here, so see if you can make it work!

Read More - 1.1em semibold

##### Sidebar

Sidebar headers - 1em, extra bold

Categories list - 1em, light

Success Stories <br>
Stats <br>
How Tos <br>
Best of Business Tips

About text - 1em light

Proin sed justo vel sapien varius auctor. Proin scelerisque massa at luctus tincidunt. Fusce porttitor, sapien sed tincidunt fringilla.

Learn More - Semibold, 1.25em

![Screenshot of Week 2 Homework](../../embedded-images/relaxr_blog.jpg)

### Helpful Hints

#### Floats? Flexbox? Grid?

If you're undecided on which technique to use, try Float or Grid.  Flexbox isn't really the best choice for laying out a whole page because it only allows us to control the layout in one direction.  Flexbox is a great choice for individual elements on the page though, so if you want to get some practice with it, try using it to layout your top navigation.

Using a combination of techniques to achieve the best outcome — mixing flexbox or floats at the element level with grid to layout your overall page for example — is not only perfectly acceptable, it's actually the best way to go.

##### When to use Float

- Floats are great if you want to have **text flow around an image** or a pull quote.  This is precisely what they were designed to do.
- Float is also helpful for page layout if you know you really must **support very old browsers** like Internet Explorer.  If your webpage design must be reproduced faithfully for every site visitor, using float will give you the best coverage today.
- There is a technique that allows you to conditionally load styles for Internet Explorer 10 and 11.  This would be an option for allowing you to use modern tools like Flexbox and Grid, but provide at least a comparable experience for those who are still using older versions of Internet Explorer.  Read more about this technique [here](https://paper-leaf.com/blog/2014/09/targeting-ie-10-11-browsers-css/).

##### When to use Flexbox

- Flexbox is a great option for laying out **parts** of your page.  For example, if you have a group of elements that you want to all align in a column or row and you want to be able to have fine-grain control over the placement of the items, flexbox is the ideal option.
- Flexbox is also the way to go if you want to **vertically align** elements in their container.  No other CSS properties allow us to do this so easily and without hacks.
- Flexbox is also a great choice if you have lots of similar elements that you want to layout as a collection.  For example, if you have a card design, where each card links to an article or blog post, or for a **gallery** of thumbnail images.  The flex-wrap property makes this easy and reliable.

##### When to use CSS Grid

- Grid is the ultimate choice for **laying out entire pages** of content.  The intuitive and declarative properties for grid areas and the breadth of properties for adding gaps; dealing with flexible sizing and wrapping; handling overlap; etc., make this the hands down winner.  The only drawback is that because it is the newest standard of the three, it has the poorest support of them all.  Still, support is available in all major browsers today since late last year, so this is something you should invest in learning.
- Grid can also be a great option for **laying out components**.  Components are groups of elements that together form a distinct and reuseable building block in your page.  For example, if you have a [card design](https://econsultancy.com/blog/64646-15-delicious-examples-of-card-based-web-design) where you'll have lots of similar cards displayed on the page, grid is a great option to layout the card itself.

### Resources

[Google's Guide to Google Fonts](https://developers.google.com/fonts/docs/getting_started)

[CSS Tricks Complete Guide to Using Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

[CSS Tricks Complete Guide to Using Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)



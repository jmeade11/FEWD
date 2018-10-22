# HOMEWORK

## Revisiting Relaxr

Last week the homework was very hard and you had to try and make sense of a lot with very help.  Spend some time before next class and get your Relaxr project completed and uploaded.
<br>

---

### Steps to follow

#### Setting Up Your Project

By now you've had lots of practice creating a website project with folders for your css and images, as well as creating your html boilerplate. 

1. Set up your folders and download the images.

##### Images

To download the images, follow the link for each image and then right-click on the image and choose **Save Images As...** from the context menu.  Make sure to save the files in the images folder of your project.

[Relaxr Logo White](relaxr-images/relaxr-logo-white.svg)<br>
[Relaxr Logo Yellow](relaxr-images/relaxr-logo-yellow.svg)<br>
[Blog Photo 1](https://raw.githubusercontent.com/jmeade11/FEWD/master/Class4/homework/relaxr-images/blog_photo1.jpg)<br>
[Blog Photo 2](https://raw.githubusercontent.com/jmeade11/FEWD/master/Class4/homework/relaxr-images/blog_photo2.jpg)<br>
[Facebook Icon](relaxr-images/facebook.svg)<br>
[Twitter Icon](relaxr-images/twitter.svg)<br>

2. Drag your project folder on to Atom to open it in the projects pane. 

3. Right-click on the project folder and choose **New File** and name the file index.html.

4. Right-click on the **css** folder and choose **New File** and name the file styles.css.

5. Go [Google Fonts](https://fonts.google.com/?query=open+sans) and search for the Open Sans font.  Click the plus symbol to select the font.  In the dialog box, click the **Customize** tab and choose the following font weights: 300 Light, 600 Semibold, 800 Extrabold.  Click on the **Embed** tab and copy the link tag.

6. Paste the link tag from Google Fonts into your html page below the title tags in the page head.

7. Create a link tag for your stylesheet in the html page **below** the Google fonts link tag in the page head.

8. Open your styles.css file and add your reset.

<details>
  <summary><strong>GET A HINT</strong></summary>
  
```css
* {
    margin: 0;
    box-sizing: border-box;
}
```
</details><br>

9. Add your base font-family (you can copy this from the Google Fonts embed tab) and set the font weight to 300. Set the page background color to #f0efef and the font color to #606161.

<details>
  <summary><strong>GET A HINT</strong></summary>
  
```css
html {
  font-family: 'Open Sans', sans-serif;
  background-color: #f0efef;
  color: #606161;
  font-weight: 300;
}
```
</details><br>

10. Back on your html page, add html tags for the `header`, `main`, `aside`, `section` and `footer`. 

<details>
  <summary><strong>GET A HINT</strong></summary>
  
```html
<body>
  <header></header>
  <main></main>
  <aside></aside>
  <section></section>
  <footer></footer>
</body>

```
</details><br>

11. In the `header`, add your image for the white logo and a `nav` tag for your main navigation.  Inside the `nav` tag, add anchors for each of the pages: About, FAQ, Team, Contact Us, Blog.

<details>
  <summary><strong>GET A HINT</strong></summary>
  
```html
<header>
  <img src="images/relaxr-logo-white.svg" alt="Relaxr Logo">
  <nav>
      <a href="#">About</a>
      <a href="#">FAQ</a>
      <a href="#">Team</a>
      <a href="#">Contact Us</a>
      <a href="#">Blog</a>
  </nav>
</header>

```
</details><br>

12. Inside the `main` section, add your `article` tag for the first blog post.  Inside the `article` add your heading for the post title: "How I implemented Relaxr in 2 weeks and changed my life", followed by the `blog_photo1.jpg` image and some lorem text (type lorem and press the <kbd>tab</kbd> key if you're using Emmet). Lastly, add an anchor tag for Read More.  

<details>
  <summary><strong>GET A HINT</strong></summary>

```html
<main>
  <article>
    <h2>How I implemented Relaxr in 2 weeks and changed my life</h2>
    <img src="images/blog_photo1.jpg" alt="Relaxr Blog Photo">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi, explicabo, voluptatibus. Hic sed esse, laboriosam numquam amet eos nemo. Minus mollitia provident, illum perferendis assumenda excepturi ipsum animi, ratione aspernatur.</p>
    <a href="#">Read More ></a>
  </article>
</main>

```
</details><br>

13.  Duplicate what you've done for the first blog post by creating a new article tag after the first and following the same pattern for the second post entitled: "I traveled across the globe thanks to Relaxr’s Excel automation"

14. In the `aside` tag, add your heading tags (`h3` makes sense) for each of the Categories, About Relaxr, and Learn More headings.  Categories should be followed by a `nav` that contains anchor tags for each of the: Success stories, Stats, How tos, and Best of Business tips links.   About Relaxr should be followed by a paragraph with just some placeholder text: "Proin sed justo vel sapien varius auctor. Proin scelerisque massa at luctus tincidunt. Fusce porttitor, sapien sed tincidunt fringilla."  Finally, after the Learn More add a div with the text Ad Unit inside of it.

<details>
  <summary><strong>GET A HINT</strong></summary>

```html
<aside>
  <h3>Categories</h3>
  <nav>
    <a href="#">Success stories</a>
    <a href="#">Stats</a>
    <a href="#">How tos</a>
    <a href="#">Best of Business tips</a>
  </nav>
  <h3>About Relaxr</h3>
  <p>Proin sed justo vel sapien varius auctor. Proin scelerisque massa at luctus tincidunt. Fusce porttitor, sapien sed tincidunt fringilla.</p>
  <h3>Learn More</h3>
  <div>
    Ad Unit
  </div>
</aside>

```
</details><br>

15. Our section is simple.  We're just going to add a link or a button.  I'm going to use a button here for variety and so you can see how to style the button.  Add a `button` tag with the text "Sign Up Now!", to the `section` tag.

<details>
  <summary><strong>GET A HINT</strong></summary>

```html
<section>
  <button>
    Sign Up Now!
  </button>
</section>

```
</details><br>

16. Finally, in our `footer` tag we'll add the Relaxr logo followed by a `nav`.  Inside the `nav` add the the two social images wrapped in anchor tags.


<details>
  <summary><strong>GET A HINT</strong></summary>

```html
<footer>
  <img src="images/relaxr-logo-yellow.svg" alt="Relaxr Logo">
  <nav>
    <a href="#"><img src="images/twitter.svg" alt="Twitter logo"></a>
    <a href="#"><img src="images/facebook.svg" alt="Facebook.svg"></a>
  </nav>
</footer>

```
</details><br>

17. Now that the html is done, we can move on to finishing our css.  In the css file, let's start by making some general rules that will apply universally.  We can override these later as needed.  First, we want to remove the underline from all of the anchor tag links on the page.

<details>
  <summary><strong>GET A HINT</strong></summary>

```css
a {
  text-decoration: none;
}

```
</details><br>

18. We also want to deal with the image sizes.  Add some classes to the images in your html so we can target them.  For each of the relaxr logos on the page, give them a class of `logo`.   Then we can target the social icons inside the nav by giving the class of `social` to the `nav` in the footer that wraps them.  Finally, give each of the two blog posts images a class of `post-image`.   Now, make the images inside of the social `nav` and the images with a class of `logo` **2rem** in height.  Remember that you can use a comma to separate multiple selectors when you want the same rules to apply to all the elements that match any of the selectors (comma between selectors acts like **OR**).  The blog post images should have a width of 100%.

<details>
  <summary><strong>GET A HINT</strong></summary>

```css
.logo,
.social > img {
  height: 2rem;
}

```
</details><br>

19.  Next lets tackle the `header`.  It should have a background color of #033048 and padding of 2rem.  We could use float on our `nav` element inside the header to float it to the right, but I'm going to use flexbox here for practice.  Set the display on the `header` to flex and use `align-items` set to center so the logo and the anchor tags will be horizontally centered.  Do you remember which value you can give `justify-content` to make it so that the left over *space* is added *between* the logo and the nav? 

<details>
  <summary><strong>GET A HINT</strong></summary>

```css

header {
  background-color: #033048;
  padding: 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}


```
</details><br>

20. To finish up the header areas, we'll style the nav.
- Make the nav 50% in width and set it to display as flex, as well.  Use justify-content set to space-between to evenly space out the anchor tags inside it.  
- Next, make the anchor tags inside the **header nav only** have a color of #f9e42e and a weight of semibold (i.e., 600).

<details>
  <summary><strong>GET A HINT</strong></summary>

```css
header nav {
  width: 50%;
  display: flex;
  justify-content: space-between;
}

header a {
  color: #f9e42e;
  font-weight: 600;
}

```
</details><br>

21. Next we can tackle our `article` elements.  
 - We need to style the post headings with a color of #033048, a font size of 2em and a font weight of semibold (600).  
 - The paragraphs inside the articles just need the font size set to 1.1em.  
 - In our html, lets give the anchor tags inside the the article a class of `read-more` so we can more easily target them.  Then, in our css we need to make a anchors behave like a *block* element.  Do you remember which display property to use? Once they are acting like block elements we can set the text alignment on them to right, change the color to #033048, give them some top and bottom padding of 1rem and set the border-bottom to 1px wide and solid.  Also, change the font-size to 1.1em and the weight to 600.
 - Lastly, we need to style the drop cap for the paragraph. Although both of our posts only show one `p` tag, we should be safe and use the first-child pseudo class followed by the first-letter pseudo element.  Remember that we're targeting all of this on the `p` element in the article so no spaces between the p, first-child or first-letter in our selector (a space would mean target a descendant). Give it a font-size of 2em, font weight of 800, float it to the left and give it a little margin on the right (.25em looks good).

<details>
  <summary><strong>GET A HINT</strong></summary>

```css
article h2 {
  color: #033048;
  font-size: 2em;
  font-weight: 600;
}

article p {
  font-size: 1.1em;
}

article p:first-child::first-letter {
  font-size: 2em;
  float: left;
  font-weight: 800;
  margin-right: .25em;
}

.read-more {
  display: block;
  font-size: 1.1em;
  font-weight: 600;
  text-align: right;
  color: #033048;
  padding: 1rem 0;
  border-bottom: 1px solid;
}

```
</details><br>

22. Next area to style is the `aside`.
- Everything in the sidebar is the same color.  We can set the color once for the sidebar, but you may have noticed that anchor tags never inherit their color so we'll need to address them separately.  Use a comma here and apply the color #033048 to `aside` and `aside a`.
- We also want the aside `nav`, `p` and `h3` elements to all get a margin-bottom of 1em.
- The `aside a` need to behave like block elements.
- Finally, let's style the ad unit with a background-color of white, padding of 1em, text aligned to the center, a font-size of 2em, weight of semibold and a min-height of 30rem.

<details>
  <summary><strong>GET A HINT</strong></summary>

```css

aside,
aside a {
  color: #033048;
}

aside nav,
aside p,
aside h3 {
  margin-bottom: 1em;
}

aside nav a {
  display: block;
}

aside div {
  background-color: white;
  padding: 1em;
  text-align: center;
  font-size: 2em;
  font-weight: 800;
  min-height: 30rem;
}

```
</details><br>

23. The `section` is the next bit that needs styling. 
- Set its background to #f9e42e, give it 2rem of padding and make everything inside of it centered (text-align).
- The button needs to get a background color of #033048, color of white, font-size of 1rem and font-weight of 600.  To give it a little more presence, add padding of 1em to the top and bottom and 1.5 to the left and right.  Finally, buttons have a border by default, we we're going to get rid of it with `border: none`.  Even though we don't have a border, we can still use `border-radius` to knock off the hard corners of the button by setting it to 8px.  

<details>
  <summary><strong>GET A HINT</strong></summary>

```css

section {
  background-color: #f9e42e;
  padding: 2rem;
  text-align: center;
}

button {
  background-color: #033048;
  border: none;
  border-radius: 8px;
  padding: 1em 1.5em;
  color: white;
  font-size: 1rem;
  font-weight: 600;
}

```
</details><br>

24. The footer is pretty straightforward
- Set the background to #033048, give it padding of 2rem and align its contents to the center.
- Give the nav in the footer padding of 1rem.
- Give each of the anchor tags inside the nave a margin of 1rem.

<details>
  <summary><strong>GET A HINT</strong></summary>

```css
footer {
  background-color: #033048;
  padding: 2rem;
  text-align: center;
}

footer nav {
  padding: 1rem;
}

footer nav a {
  margin: 1rem;
}
```
</details><br>

25.  Now all that is left is to deal with getting the main and aside into place next to one another.

- OPTION 1: GRID 
  - The simplest way to handle the layout would be grid.  Just set the display: grid on the body and use the `grid-template-areas` for header, main, aside, cta and footer.  Use the `grid-template-columns` property set to `65% 25%`. Then, add the `grid-area` on the `header` set to header; the `grid-area` on the `main` set to main; the `grid-area` on the `aside` set to aside; the `grid-area` on the `section` set to cta; and the `grid-area` on the `footer` set to footer. 

<details>
  <summary><strong>GET A HINT</strong></summary>

```css
body {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 65% 25%;
  grid-template-rows: auto;
  grid-gap: 0 1rem;
  grid-template-areas:
    "header header"
    "main aside"
    "cta cta"
    "footer footer";
}

/* Set grid area for each area */

header {
  grid-area: header;
}
main {
  grid-area: main;
}
aside {
  grid-area: aside;
}
section {
  grid-area: cta;
}
footer {
  grid-area: footer;
}

```
</details><br>




- OPTION 2: FLOAT 
  - Float will be the most support option.  Set both the `main` and the `aside` to float left.  Give the `main` a margin of 2rem on the left and the aside a margin of 2rem. Set the width of the `main` to calc(65% - 2em) (to account for the margin).  Set the width of the `aside` to calc(35% - 4rem) to account for its margin.  Remember to clear the float in the section!

<details>
  <summary><strong>GET A HINT</strong></summary>

```css

main {
  padding: 2rem 0;
  float: left;
  width: calc(65% - 2rem);
  margin-left: 2rem;
}

aside {
  padding: 2rem 0;
  float: left;
  width: calc(35% - 4rem);
  margin: 0 2rem;
}

section {
  clear: both;
}
```
</details><br>

![Screenshot of Week 2 Homework](../../embedded-images/relaxr_blog.jpg)<br>
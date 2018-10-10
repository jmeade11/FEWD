### CLASS 2 HOMEWORK

## YOUR PERSONAL WEBSITE
#### Due: Monday, October 15

This week, you'll be building a personal website to share with your classmates like the one shown below.  You should have already prepared for this assignment by:

1. Creating a folder for the website you'll be building.
2. Adding folders for your images and styles.
3. Adding a basic index.html file with boilerplate.
4. Adding at least 5 pictures to your images folder.

So far, your project should resemble the following:

![Your file structure so far](../../embedded-images/cls1-hmwk-files.png)

## DEVELOPING YOUR CONTENT

5. For this assignment, you'll be writing about yourself, so there's no starter text.  Don't worry, you only need to create the following:
- A headline for your webpage.
- A brief introduction of 2 - 3 sentences about yourself.
- A short description of what you do at work.  Again, 2 - 3 sentences is fine.
- A short introduction and list of your favorite pastimes.

## STRUCTURING YOUR WEBSITE CONTENT

### Semantic Page Structure

6. Once you have your content prepared, you'll need to add it to your html page.  Start by sectioning off the page with the `header`, `main` and `footer` sections in the page body.
<details>
  <summary><strong>GET A HINT</strong></summary>
  
```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
</head>
<body>
  <header></header>
  <main></main>
  <footer></footer>
</body>
</html>
```

</details>

### Header Section

7. Add your headline to the `header` section and wrap it in an appropriate tag (you'll want this to be the largest one on the page).
8. Add your introductory paragraph to the `header` (it's a paragraph, so use the appropriate tag). 
9. Add your `nav` tags next also in the header.
10. Inside the `nav`, add an anchor tag for each of our main sections: work, hobbies, gallery.  We'll be using ids with the same names, so go ahead and add the href attributes for them (remember that the name of the id is preceeded by a `#`).  

<details>
  <summary><strong>GET A HINT</strong></summary>
  
```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
</head>
<body>
  <header>
    <h1>Your Headline Here</h1>
    <p>Your introductory paragraph should go here</p>
    <nav>
      <a href="#work">work</a>
      <a href="#hobbies">hobbies</a>
      <a href="#gallery">gallery</a>
    </nav>
  </header>
  <main></main>
  <footer></footer>
</body>
</html>
```

</details>

### Main Section

11. Our main content needs to be broken down into 3 sections, each with an corresponding to the links above.  Use an appropriate tag for each *section* :wink:.
12. Inside the work section, add your *heading* (this should be smaller than the one used previously for your headline), followed by the *paragraph* you wrote about what you do for work.
13. You'll want to wrap the heading and the paragraph in the section with a `div` so that you can set it in columns later.
14. Add an image that represents you at work.  This could be a logo from your company website.  Do you remember how to get an image from a website with the right-click?
15. Do the same for the hobbies section, adding a heading, intro paragraph and a list of your hobbies.  Remember to wrap them all in a `div.
16. Finally, use what you learned today about adding content images with the `img` tag and insert all of your pictures into the gallery section.

<details>
  <summary><strong>GET A HINT</strong></summary>
  
```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
</head>
<body>
  <header>
    <h1>Your Headline Here</h1>
    <p>Your introductory paragraph should go here</p>
    <nav>
      <a href="#work">work</a>
      <a href="#hobbies">hobbies</a>
      <a href="#gallery">gallery</a>
    </nav>
  </header>
  <main>
    <section id="work">
      <div>
        <h2>Your Work Heading</h2>
        <p>A paragraph about what you do.</p>
      </div>
    </section>
    <section id="hobbies">
      <div>
        <h2>Your Hobbies Heading</h2>
        <p>A paragraph introducing your hobbies.</p>
        <ul>
          <li>Hobby</li>
          <li>Hobby</li>
        </ul>
      </div>
    </section>
    <section id="gallery">
      <img src="images/image1.jpg">
      <img src="images/image2.jpg">
      <img src="images/image3.jpg">
      <img src="images/image4.jpg">
      <img src="images/image5.jpg">
    </section>
  </main>
  <footer></footer>
</body>
</html>
```

</details>

### Footer Section

17. The footer section is simple.  Just add a paragraph that reads: Get in touch! and follow it with a `nav`.
18. Inside the `nav`, create an anchor tag for an email address (you can make a fake one if you're concerned about privacy) and one other for your linkedin page.

<details>
  <summary><strong>GET A HINT</strong></summary>
  
```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
</head>
<body>
  <header>
    <h1>Your Headline Here</h1>
    <p>Your introductory paragraph should go here</p>
    <nav>
      <a href="#work">work</a>
      <a href="#hobbies">hobbies</a>
      <a href="#gallery">gallery</a>
    </nav>
  </header>
  <main>
    <section id="work">
      <div>
        <h2>Your Work Heading</h2>
        <p>A paragraph about what you do.</p>
      </div>
    </section>
    <section id="hobbies">
      <div>
        <h2>Your Hobbies Heading</h2>
        <p>A paragraph introducing your hobbies.</p>
        <ul>
          <li>Hobby</li>
          <li>Hobby</li>
        </ul>
      </div>
    </section>
    <section id="gallery">
      <img src="images/image1.jpg">
      <img src="images/image2.jpg">
      <img src="images/image3.jpg">
      <img src="images/image4.jpg">
      <img src="images/image5.jpg">
    </section>
  </main>
  <footer>
    <p>Get in touch!</p>
    <nav>
      <a href="https://www.linkedin.com/in/jenniferannmeade/">Linkedin</a>
      <a href="mailto:fake-email@gmail.com">Email</a>
    </nav>
  </footer>
</body>
</html>
```

</details>

## STYLING YOUR WEBSITE

19. Create your `styles.css` file in your `css` folder and link it to your `index.html`.
21. Go to [fonts.google.com](https://fonts.google.com/), search for and add the Raleway font in the weights of 200, 500, and 900.

<details>
  <summary>GET A HINT</summary>
  
  > Either choose, File > New file then File > Save As and make sure you save the file in the css folder or right-click on the css folder and choose New file.  In VS Code, you can just click the file with a plus icon next to the file name in the project area.
  
  > Go to [fonts.google.com](https://fonts.google.com/), choose the Raleway font.  Click the plus sign, then in the pop-up click on the tab for **CUSTOMIZE** and select the font weights: 200, 500, and 900.  Click back to the **EMBED** tag and copy the link tag and paste it *before* your styles.css file.
  
  ```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
  <link href="https://fonts.googleapis.com/css?family=Raleway:200,500,900" rel="stylesheet">
  <link rel="stylesheet" href="css/styles.css">
</head>
  ```
</details>

22. Inside your `styles.css` file, add the universal 

<details>
  <summary>GET A HINT</summary>
  
  > Either choose, File > New file then File > Save As and make sure you save the file in the css folder or right-click on the css folder and choose New file.  In VS Code, you can just click the file with a plus icon next to the file name in the project area.
  
  ```html
<!DOCTYPE html>
<html>
<head>
  <title>About Me</title>
  <link rel="stylesheet" href="css/styles.css">
</head>
  ```
</details>


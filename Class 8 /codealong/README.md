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







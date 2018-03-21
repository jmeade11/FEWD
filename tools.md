
# Tools of the trade
This is a running list of some tools that will help you be more productive, efficient and/or accurate.

- Emmet: Emmet is a set of plug-ins for text editors (like Sublime Text, VS Code or Atom) that allow for high-speed coding and editing in HTML, XML, XSL, and other structured code formats via content assist.

## Emmet

### Installing Emmet
To add Emmet support to Sublime Text, first you'll need to install [Package Control](https://packagecontrol.io).  Package Control makes it possible to easily find and install hundreds of plugins for Sublime Text.  

1. Follow the instructions [here](https://packagecontrol.io/installation) to install Package Control.
2. Once Package Control is installed (exit and restart Sublime Text after installation), launch the Package Control by choosing **Sublime Text > Preferences > Package Control** or with the keyboard shortcut <kbd>⌘</kbd> (command) + <kbd>⇧</kbd> (shift) + P.
3. When the dialog launches, begin typing `install` to jump to the **Package Control: Install Package** option.  
4. Select the install package option to launch the dialog list of available packages.  Start typing `emmet` to jump to the Emmet package.
5. Select Emmet and follow any onscreen instructions to install it.

You may have to restart Sublime Text to begin using Emmet.  

### Using Emmet 
#### Basic Usage
Emmet is activated with the <kbd>Tab ↹</kbd> key by default.  Open and **save a new file with the html extension** (Emmet needs to know what kind of a file it is so it can make the correct insertions and suggestions).  Type `div` and then press the <kbd>Tab ↹</kbd> key.  Emmet will replace div with `<div></div>` and insert the cursor automatically between the start and end tags.

#### Nested Tags with >
You can also create multiple lines of nested tags with the `>`.  If you wanted to create an div tag that contains a paragraph tag, you would type: `div>p` with no spaces, then press the <kbd>Tab ↹</kbd> key. In this case, Emmet would replace the text with:

    <div>
        <p></p>
    </div>

#### Sibling Tags with +
To create multiple sibling tags, you use the `+`.  For example, if you wanted to create a basic structure for your page body, you might type: `header+main+footer`.  When you press the <kbd>Tab ↹</kbd> key, the follow code would be produced.

    <header></header>
    <main></main>
    <footer></footer>
    
#### Multiple Tags (of the same kind) with *
To create multiple tags, you use the `*`.  This is great for creating lists, for example.  If you want to create an unordered list with 5 list items, just type: `ul>li*5` and press the <kbd>Tab ↹</kbd> key.  Emmet will produce the list and place the cursor in between the first list item tags.  Type your list content and press the <kbd>Tab ↹</kbd> key to automatically jump the cursor between the next list item tags.

#### Going Up a Level with ^
Using the > allows you to nest tags, but if you want to go up a level, you use the `^` (caret, not the control key).  For example, to produce something like this:

    <ul>
       <li></li>
       <li></li>
       <li></li>
    </ul>
    <p></p>

You would type: `ul>li*3^+p` and then press the the <kbd>Tab ↹</kbd> key.

#### Boilerplate HTML page with !
One of my favorite shortcuts is that you can produce boilerplate for an entire html page with one single character: `!`.  Typing `!` and press the <kbd>Tab ↹</kbd> key produces: 

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
    </head>
    <body>
      
    </body>
    </html>
    
#### Tags with Attributes with []
Emmet will automatically insert basic attributes for tags like `a` and `img`.  Additionally, it will place the cursor inside the attribute and allow you to use the <kbd>Tab ↹</kbd> key to jump to the next attribute or the inside of the tags.  For example, by default, if you type `img` and just press the <kbd>Tab ↹</kbd> key, Emmet will insert: `<img src="" alt="">`, with the cursor between the quotes of the source attribute.  After typing the source, press the <kbd>Tab ↹</kbd> key to jump to the alt attribute.  

You can specifically add your own attributes or override the default ones by placing the attribute in brackets like so: `div[role="button"]`, which would produce `<div role="button"></div>`.  If you don't want to specify a value just type the attribute name in the brackets, such as: `section[title]`.  This will produce: `<section title=""></section>`.

#### Some Helpful Shortcuts
Emmet includes **a lot** of shortcuts and features.  Here are some of my favorites:

##### Toggle Comments with <kbd>⌘</kbd> + <kbd>⌥</kbd> + /
Very often you'll need to comment some code out when you're trying to isolate a problem when you're debugging issues.  Emmet makes this super easy.  Just select the code that you want to comment out and type: <kbd>⌘</kbd> (command) + <kbd>⌥</kbd> (alt/option) + /.

##### Wrap with Abbreviations with <kbd>^</kbd> + <kbd>⌥</kbd> + <kbd>ENTER</kbd> or <kbd>^</kbd> + W
You've seen me use this in class a lot.  It's extremely helpful for wrapping lists of text.  For example, if you have a list of text that you want to wrap in a nav with an unordered list and anchor tags, such as:

    Facebook
    Twitter
    Instagram

Select the text and press <kbd>^</kbd> + <kbd>⌥</kbd> + <kbd>ENTER</kbd> or <kbd>^</kbd> + W.  At the bottom of the screen, you'll see it reads "Enter Wrap Abbreviation" with a field to the right.  Just type the tags you want to wrap the list in, for example: `nav>ul>li*>a` would produce:

    <nav>
      <ul>
        <li><a href="">Facebook</a></li>
        <li><a href="">Twitter</a></li>
        <li><a href="">Instagram</a></li>
      </ul>
    </nav>
    
The `*` following the `li` tells Emmet to wrap the lines individually from that point forward. 

##### Creating a Stylesheet Link with link:css
This is a quick way to create a link to an external stylesheet.  Just type `link:css` and press the <kbd>Tab ↹</kbd> key.  Be weary of getting to lazy and forgetting how this basic tag is structured. :wink:

##### Rename a Tag
Swapping out one tag for another can be a pain, but with Emmet, you just put your cursor inside of the tag you want to change.  Next, press <kbd>⇧</kbd> + <kbd>⌘</kbd> + K and type the new tag name.  As you type Emmet will update the start and end tags simultaneously.

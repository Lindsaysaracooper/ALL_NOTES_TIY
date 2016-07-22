# Day 01 - Course Introductions, Command Line, HTML, CSS

## Challenge
5 mins to write as many HTML tags as you can think of

## Notes
### Command Line
- pwd - print working directory
- ls - list files in current directory
- cd - change directory
- .. - up one level in the directory trees
- mkdir - make directory
- touch - make files
- rm - remove a file
- clear - clears the bash output
- mv - moves a file, also used for renaming
- cp - copies a file
- . - current directory
- tree - print a tree from current directory down
- rmdir - remove directory (or you can rm -r, recursively remove)

### HTML
- Your browser will read anything you give it and interpret it as text content.
- anything inside of `<>` will be interpreted as a tag
- use semantic tags for yourself, other developers, your browser, and accessibility tools

#### anatomy of an html tag:
```html
<tagname attributeName="value"></closingtag>
<selfClosingTag />
<!-- comment Write a bunch of stuff here-->
```

#### required html structure:
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>The title of your page</title>
  </head>
  <body>

  </body>
</html>
```

### CSS
- Cascading Style Sheets
- rules "cascade" down the html tree
- the style of your html page
- link into html with a link tag:
```html
<link rel="stylesheet" href="main.css" media="screen"/>
```

#### anatomy of a css ruleset:
```css
selector {
  property: value
}
```

#### css selectors
- tagname
- classes (.className)
- id (#idName)
- ` ` space character selects any descendent
- `>` right angle bracket selects only direct descendants
- `tagName.className` selects elements with BOTH tag and class match

#### css specificity
- rules are applied in order (top to bottom)
- competing rules follow specificity rules to decide who wins
- from least to most specific: tagname, classname, id
- the more selectors the more specific. A rule with two classnames trumps a rule with one. BUT a two tagnames rule is still less specific than one classname.

### Surge
- we use surge to host our websites easily. You have already installed the tool and can use it from your terminal
- use surge from a directory containing an index.html file. this file will be the entry point for your website.
- the command is `surge`. that's all! you can optionally type a path if you ran the command in a different location from where your index.html file lives
- you can optionally change the path you wish to host and also the sub-domain of the surge site you are creating. press enter until you've made it through all these prompts.
- You should submit your surge site's link for your homework assignments - TEST THEM TO MAKE SURE THEY WORK **before** you submit them to me!

## Resources
- [HTML elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [CSS resources](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

# Day 02 - Git Basics, CSS layout

## Review
- css colors
  - prefer hex values over names (`#fff` or `#ffffff`)
- screen sizing
  - while writing css, modifiy the size of your browser window to ensure that your styles work across different windows. Use % instead of px whenever possible to make layouts more fluid.
- linking within a document
  - use the `id` attribute to create linkable anchors on a page.
  - use the `a` tag and set the `href` attribute to the id to force the browser to scroll to the id'd element.
- adding multiple classes to an element, multiple attributes to one element
  - any element can have multiple attributes, but should only have ONE of any particular type of attribute
  - attributes should be in the opening tag of an element
  - multiple classes for a given element should be space delminted. the following div has 2 classes: `<div class="hero company-splash">`
- Paths
  - absolute: includes protocol, such as http:// or file://
  - root relative: denoted with a preceeding slash, always adds path to the root of the current domain, either the root of your computer, OR the web domain such as `http://google.com`
  - relative: takes into account the exact current location (not just the root of the current location) and will tack your path onto current location.

## Challenge
### QUIZ (ACK!)
1. What is the most specific selector?
  1. p > div
  2. div.container
  3. .container .child
  4. section#popup
1. What html tag is used for including links to a page?
1. What command in the terminal will create a new file?
1. What color will the paragraphs with the "feature" class be?
```css
    p {
      color: pink;
    }
    p.feature {
      color: blue;
    }
    .feature p {
      color: green;
    }
    p > .feature {
      color: red;
    }
```


## Notes
### Git
- version control software
- creating a new repository, which represents the code and code history of an entire project
  - `git init` creates a new empty repository in the current directory ON YOUR LOCAL MACHINE
  - create a matching repository in Github using their GUI.
  - follow the instructions on the new repo, or use these commands to link your local version to the github remote version:
    - `git remote add origin <https path to your remote repo>`
    - `git push origin master -u`
- basic flow:
  - make changes, create files, write code, etc
  - `git status` prints out changes that are or are not being tracked by git. use this to confirm you did what you think you did.
  - `git add .` add all files in the current directory to git for tracking
  - `git commit -m <your message here>` commit all the changes to memory in git.
  - `git push origin master`

### Block vs Inline elements
  - css display property: block, inline, inline-block
  - block
    - proud parents
    - contain children
    - swell to the size of their container
    - have no height by default
    - don't like to be next to anyone
    - respect your height, width, margin properties
  - inline
    - bratty teenagers
    - don't respect height, width, margin top or bottom
    - like being close to others
    - default only as wide as their Contents
    - have no height by default

### Box model
  - content - modified by height and width properties, the inner most box of the box model
  - padding - the space between border and content, has the background color of the element itself
  - border - the border of an element, short hand property with style, size, color. you can also alter border-radius.
  - margin - the space outside an elements border that other elements may not touch. pushes an element away from siblings or parents.
  - box-sizing: property that determines what height and width properties are modifying. defaults to content-box, but is usually preferable to reassign to border-box

### Css centering
  - block
    - set an explicit width less than 100%
    - add `margin: 0 auto;`
    - profit
    - element will be centered within the parent
  - inline
    - apply to the parent elements
    - `text-align: center;`
    - element will be centered WITHIN the parent

### Css layout
  - `display: inline-block;`
    - use when you don't care about a little white space between elements
    - gives the best of both worlds!
  - `float: <left or right>`
    - moves the applied element OUT OF FLOW OF page
    - element now allows other elements to touch it
    - will move itself up and to the `<left or right>` as far as possible while still respecting other elements KNOWN widths and heights
    - parents of floated children DON'T KNOW where their children are!
      - to fix this use the clearfix hack:
      ```css
      main::after {
        display: block;
        content: 'hi';
        clear: both;
      }
      ```

## Resources
- [Collapsing Margins](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing)
# Day 03 - CSS pseudo selectors, CSS positioning, Pixel Perfect, Keyboard Shortcuts

## Review
- Git
- Length units
  - px
  - em - standard unit based on text size
  - rem - like ems but based on the html font size instead of the current element
  - vh vw - like percent of height and width but based on viewport rather than element
  - % - percent of an element
- Pseudo elements
  - child html elements created using only css
  - ::before ::after
  - require a `content` property, even if it is only set to `''`
  - we used for the clearfix hack (to help parents find their floated children)
  - mostly used for adding style element to a page such as a triangle pointing at some content
- Triangles

## Challenge
Get in pairs and work together to build an HTML tree for the AirBnB website. Be prepared to justify why you structured your HTML as you did.
![](examples/airbnb.jpg)

## Notes
### css positioning
- default is `position: static`
- other values are absolute, relative, fixed, ~sticky

#### fixed
  - fixed to the viewport of the page
  - removed an element from the flow of the page
  - top, right, bottom, left move the elements corresponding edge from the viewports corresponding edge
  - element will be sized based on its content unless height and width are specified OR if both top and bottom (or left and right) are specified

#### relative
  - stays in the flow of the page, taking up space where it would normally live
  - top right bottom left move the element's corresponding edge away from its original position's corresponding edge
  - if both left and right are specified, left will win. top wins the top bottom battle

#### fixed
  - removed from the flow of the page
  - element will be sized based on its content unless height and width are specified OR if both top and bottom (or left and right) are specified
  - top right bottom left move the element's corresponding edge from its **nearest non-statically positioned parent's** (or the viewport) corresponding edge

### pseudo selectors
  - subset of another css selector - like adding a caveat to an existing selector
    - hover state (only applies when mouse hovers over the selected element)
    - first-child (only applies to selected elements that are also first children of their parents)
  - all denoted with a single `:` that follows the actual selector
    - `button.submit:hover` (applies to a button element with the submit class that is being hovered)
  - first-child: the selected element should be the first child of a parent
  - first-of-type: the selected element should be the first matching element in its parent (not necessarily the first child)
  - nth-of-type/child(an+b) : a is a multiplier, b is a starting number. nth-of-type(3n+2) would select every third element that matches starting with the second element. (the multiplier is optional) (odd, or even are valid as the arguments)

### pixel perfect
- install the tool found [here](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)
- turn on file access at `chrome://extensions` - make sure to the allow access to files is checked

### css reset/normalize
- sets default styles that are consistent among all browsers
- use the cdn version of normalize
  - cdn stands for content delivery network
  - allows your browser to cache results and make fewer network calls
  - is a network of distributed servers that host assets like js files and css files
- link to it just like any other css stylesheet

### keyboard shortcuts
- ctrl d - forward delete
- ctrl a - jump to the beginning of a line
- ctrl e - jump to the end of a line
- ctrl k - delete an entire line
- ctrl p - move cursor up
- ctrl n - move cursor down
- ctrl f - move cursor forward
- ctrl b - move cursor back
- cmd shift d - duplicates a line (text editor)
- ctrl shift m - markdown preview (text editor)
- cmd w - close a tab
- cmd shift w - closes a window
- cmd shift [ or ] - move between tabs

## Resources
Look up html and css to see how well supported across browsers it is [http://caniuse.com/](http://caniuse.com/)
# Day 04 - Form Accessibility, Icon fonts, RWD, media queries

## Review
- which tags are self closing?
  - img, input, link, meta, br, hr
  - can't put content inside a self closing tag
  - use atom beautify to align tags if you have messy code
- vocab
  - anatomy of html
    ```html
    <div class="cool-div">What am I?</div>
    ```
  - anatomy of css
    ```css
    div.cool-div {
      background: url('http://www.fillmurray.com/300/300');
    }
    ```
- centering
  - inline centering use `text-align: center;` to the parent
  - block centering set explicit width less than 100%, `margin: 0 auto;`. OR no width set but `margin: 0 someValue;`
- container fit only it's children (not swell to 100%)
  - take it out of flow
    - position: absolute;
      - z-index (works for siblings that are not statically positioned) moves elements in 3d space forward and back
    - float
  - inline-block
- difference between inline/block
- difference between float or inline-block
  - inline-block doesn't take it out of the flow
  - inline-block leaves a small white space between elements
- inheritance
  - almost all properties inherit
  - if you're not sure, look it up on mdn docs
- clearfix
  - overflow hidden vs ::after element
  - prefer ::after element for semantics and device compatibility

## Challenge
Recreate the following using only html and css (the action occurs on click):
![](/Users/tiy/Documents/button.gif)

## Notes
### icon fonts
  - allow us to treat icon images like text (we can apply color, font-size, etc)
  - setup
    - download the zip from fontawesome
    - add the css file to your project folder
    - add the font folder to your project
    - link in the css file in your html
    - profit
  - insert into the page with an `<i>` tag and the appropriate classes.

### form elements and labels
  - the `for` attribute of a label should match the `id` attribute of its corresponding input element
  - all inputs should have a `name` attribute for accessibility purposes
  - labels can be the parent of their inputs, OR can be siblings. Both are used in the real world.

### responsive design
  - style widths with %s
  - apply max-width to prevent ugly large screen layouts
  - allow height to be dictated by content!!!
  - top and bottom (margin, padding) should be defined in ems or rems
  - add this to the head of your html `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
  - when your page just starts looking awful and no responsive design will fix it, resort to media queries

### media queries
  ```css
  @media media-type and (parameters) {
    selector {
      property: value;
    }
  }
  ```
  - media-type example is 'screen' or 'print' or 'handheld'
  - parameter examples are 'orientation: landscape' or 'max-width: 400px'
  - they should be at the bottom of your css so they overwrite previous rules

## Resources
- [Font Awesome](http://fontawesome.io/)
- [Fontello](http://fontello.com/)
- [Scaling background images](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Background_and_Borders/Scaling_background_images)
- [Responsive Web Design Checklist](http://rwdchecklist.com/)
# Day 06 - Sass

## Review

## Challenge
Use HTML and CSS (only) to create a dropdown menu that opens on hover. Use the following markup:

```HTML
<ul>
  <li><a href="#">Menu Title</a></li>
  <li><a href="#">Item 1</a></li>
  <li><a href="#">Item 2</a></li>
  <li><a href="#">Item 3</a></li>
  <li><a href="#">Item 4</a></li>
  <li><a href="#">Item 5</a></li>
</ul>
```

If you finish, try to make sub-levels!

## Notes
### Sass
#### setup
  - "watch" a folder of scss files for changes. Anytime you save changes, the scss will be compiled into a css file.
  - `sass --watch path/to/folder/where/scss/files/are:path/where/css/file/should/live --style compressed`

#### partials
  - link separate `.scss` files in with an `@import` statement
  - "partial" `.scss` files should be named with a preceeding `_` (eg. `styles/_drop-down.scss`)

#### nesting
  - the descendent selector (a ` ` space character) can be replaced with nested rules. example:

  ```sass
    .dropdown-menu {
      a {
        text-decoration: none;
      }
    }
  ```

  the above selects an `a` that is a descendent of the class `dropdown-menu`
  - nesting makes code more legible and helps keep related code together
  - nesting rules compile into plain css, making more specific rules
  - aim to nest no more than 4 levels deep, ever!
  - use the `&` for parent selector (used for pseudo selectors etc)

  ```sass
  .dropdown-menu {
    a {
      text-decoration: none;
      &:hover {
        text-decoration: underline;
      }
    }
  }
  ```

#### variables
  - denoted with a `$` eg: `$color-background: #fff;`
  - used to store repeated **values**
  - must be defined before it is used
  - we can now change a value in just ONE place, and those changes will cascade through to any place they are referenced!

#### mixins
  - used to store repeated **rule sets**
  - defined like so:

  ```sass
  @mixin nameOfMixin {
    property: value;
    other-property: otherValue;
  }
  ```

  - used like so:

  ```sass
  body {
    @include nameOfMixin;
  }
  ```

  - mixins can have arguments
    - defined like so:

    ```sass
    @mixin nameOfMixin($someSpecifiedValue) {
      property: value;
      other-property: $someSpecifiedValue;
    }
    ```

    - used like so:

    ```sass
    body {
      @include nameOfMixin(50px);
    }
    ```

## Resources
- [The Sass Way - Choosing great variable names](http://thesassway.com/beginner/variable-naming)
- [The Sass Way - Nested selectors: the inception rule](http://thesassway.com/beginner/the-inception-rule)
- [The Sass Way - Referencing parent selectors using the ampersand character](http://thesassway.com/intermediate/referencing-parent-selectors-using-ampersand)
- [The Sass Way - Modular CSS naming conventions](http://thesassway.com/advanced/modular-css-naming-conventions)
- [CSS Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)


# Day 07 - Grid systems, Sass libraries, Git Partner Flow

## Review
- sass map
  - links your html to the scss file so that you can find errors more easily
- .gitignore file, .surgeignore file
  - gitignore.io
  - ignore files in git repo or surge project
  - those files are not included when syncing with remote versions
- mixins
  - createing a mixin
```scss
@mixin mixinName($localVariableName) {
  color: $localVariableName;
  border-radius: anotherValue;
}
```
  - using a mixin
```scss
@include mixinName(value);
```
- nesting
  - keep nesting less than 4 levels deep
  - the 4th level is usually reserved for state such as `&:hover` or the like

## Challenge

## Notes
### DRY (use classes to not repeat code)
  - don't repeat yo'self
  - use classes for repeat styles
  - sass variables for repeating values
  - mixins for repeating rulesets
  - after you've written the same code 3 times, it's time to **abstract** that code into a variable, mixin, etc

### CSS transitions
  - transitions make changes to elements style over time
  - any property that has gradient values can be transitioned
  - use shorthand `transition` property:
    - `transition: background 2s, color .5s;`
  - include `transition` property to ruleset of element that should transition.
    - often used with states like hover. the target style should reside in the hover ruleset
  - css animations are a thing, feel free to look them up with all your extra time

### mixin libraries / grid frameworks
  - bourbon
    - installation
      - one time only : `sudo gem install bourbon`
      - `bourbon install` in the project's sass directory
    - use
      - `@import 'path/to/bourbon/partial';`
      - sass watch the sass directory
      - profit
    - pixel to rem/ems
    - border color
    - ellipsis
  - neat
    - grid framework - a layout tool that defines our website in terms of vertical columns and how many columns an element takes up
    - installation
      - one time only : `sudo gem install neat`
      - `neat install` in the project's sass directory
    - use
      - `@import 'path/to/neat/partial';` **after** bourbon import (neat depends on bourbon)
      - include neat mixins in your sass files
        - `@include outer-container(1000px)` sets up an area of the page to be a grid and sets the max width of that grid
        - `@include span-columns(4)` sets an element to be 4 (or other number) of columns wide
        - `@include omega()` removes margin right from the last element in a grid layout so it fits in the row

### github branches
![](../images/git-branching.jpg)
  - branches represent a series of commits, a particular path through history
  - `git checkout -b <branch name>` (-b makes NEW branch)
  - `git checkout <branch name>` (existing move to an existing branch)
  - merge commits are special commits that marry two branches together. The branches can diverge again in the future.


### github group project flow
![](../images/git-flow.jpg)
  - one person in the group makes the repo and puts it on github
  - give your partners collaborator status on github
  - partners should clone the remote into a new project folder to start the project `git clone <remote git address> <path/to/the/project/folder>.`
  - for each feature: work locally **on a feature branch**, commit after successful changes
  - push local branch to the remote branch `git push origin <branch name>`
  - make a pull request to merge the remote branch into the remote master on github
  - get your teammates to approve the code
  - after the pull request is merged, everyone pulls origin master
    - the writer of the newly merged code runs `git checkout master` and then `git pull origin master`, fix any merge conflicts, and add and commit the result.
    - the other team members stay on their feature branches and run `git pull origin `, fix any merge conflicts, and add and commit the result.


## Resources
- [Bourbon Docs](http://bourbon.io/docs/)
- [Neat Docs](http://neat.bourbon.io/examples/)
# Day 08 - JS Intro

## Review
- git clone - a way of making local copy a remote repository on your machine
  - `git clone <remote repo path> <local folder path>`

## Challenge
Recreate this using only one block level element:

![talking bubble](../images/talking-bubble.png)

## Notes
- linking in a js file
  - use the `<script>` tag.
  - include as the last element in your `<body>` tag
  - `<script src="path/to/js/file.js" type="text/javascript"></script>`
- js types
  - string
    - any text value, could be whole paragraphs or just a single letter, or numbers as strings
    - denoted with quotation marks
    - prefer single quotation marks
    - `'this is a string!'`
  - numbers
    - any number value, could be with or without decimal points
    - also NaN (not a number), Infinity
    - `5` `NaN`
  - booleans
    - the values `true` or `false`
  - undefined
    - the default nothing value of variable and some code expressions when they evaluate
  - null
    - the expressly empty value of nothing. usually set by the developer
- evaluation
  - every JS expression evaluates to a value
  - primitive types evaluate to their primitive value
- variables
  - containers to store values
  - declaration `var variableName;`
    - evaluates to undefined;
  - assignment `variableName = 5;`
    - evaluates to the evaluation of the right side of the expression
  - usually do both at once `var variableName = 5;`
- js operators
  - used in JS expressions; the expression will evaluate out and the operator will be forgotten
  - math operators
    - `+ - / * %`
  - assignment operator
    - `=`
  - string operators
    - `+` "concatenation operator"
  - equality operators
    - `< > <= >= === == !==`
      - double equal coerces values
      - triple equal ("strict equality") does not coerce
- coercion
  - we can turn any value (ANY VALUE) in javascript into one of the 3 primitive types via coercion
  - to coerce to a string: `String(value)`
  - to coerce to a number: `Number(value)`
  - to coerce to a boolean: `Boolean(value)`
- object and array syntax and accessors
  - objects and arrays are MADE UP OF other types - they are not primitives
  - array: indexed list of items
    - the items in an array don't have labels or names
    - `[1, 4, 65, 23, 132]`
      - square brackets `[]` denote an array
      - values are separated by commas
      - values can be anything
      - zero indexed - the first item is the zeroth item
      - accessing items in an array
        - square brackets ALSO access values in an array
        - `arrayName[indexValue]` evaluates to the indexValueth item in arrayName
  - object: key and value pairs, where values can be ANY TYPE or value
    - items in objects don't have any inherent order
    - they are indicated by their property name (aka key, aka label)
    - we use `{}` to denote an object
      ```
      {
        name: 'Jess',
        favoriteThings: ['unicorns', 'cats', 'swing music'],
        age: 32
      }
      ```
      - key value pairs are separated by commas
      - key and its value are separated by a colon
      - keys can have any valid variable name
      - keys are also called properties
    - accessing items in an object
      - the `.` is a property accessor. anytime you see a `.` that means the thing on the left is an object, and the thing on the right is a property name
      - `jessObject.favoriteThings` evaluates to the favoriteThings property's value on the jessObject object.
- functions
  - declaration:
  ```
  function functionName() {
    // reusable code block
  }
  ```
  - functions are blocks of code that do something.
  - we can give them names in order to use and reuse them
- document
  - the document object is the JS representation of our HTML document
  - we can access the document with the `document` variable.
  - we can access any elements in the document with the `querySelector` property like this:
  ```js
  document.querySelector('anyCssSelector')
  ```
  - if we want to see an html element in its JS representation in our console, use this:
  ```js
  console.dir(document.querySelector('div'));
  ```

  # Day 09 - JS Introduction, Conditional logic, Event Listeners

  ## Review
  see review example

  ## Challenge
  See TIYO for var and assignment worksheet

  ## Notes
  - Break down your problems into smaller steps!
    - Think about "ingredients" - what stuff do you need to make your code work? Create variables for all of your ingredients
    - Think about actions - can you accomplish that action by assigning or reassigning a value? can you accomplish that action by using an operator (such as addition)
    - Don't forget to PROVE YOUR CODE WORKS every step of the way by using `console.log`! When in doubt, log it out!
  - DOM accessors
    - DOM document object model
    - `document.querySeletor()` - take any css selector and find the FIRST MATCHING ELEMENT
    - `document.querySeletorAll()` - grabs **all** matching elements from the DOM and puts them in an ARRAY LIKE OBJECT
    - `document.getElementById()` - takes an id and grabs the matching element from the DOM
    - `document.getElementsByClassName()` - takes a classname and grabs all matching elements and puts them in the array like object
  - Event Listeners
    - DOM events - anything our computer can tell us about what the user is doing to interact with our document
      - eg: mousemove, scroll, click, keypress, etc
    - an event listener is a way to notice or care that one of these events has occurred
    - `element.addEventListener('nameOfEvent', functionToRun)`
      - where `element` is an HTML element that we accessed from the DOM
      - where `nameOfEvent` is eg: `click` `mouseover` `keypress`
      - where `functionToRun` is a function or function name that runs some code
  - Functions
    - functions can take parameters inside their parentheses
      - parameters are like variables - they are names for values
      - parameters are scoped to the function they belong to
      - this is called **function scope** which differs from **global scope**
  - Conditional Logic
    - making decisions on what to do based on some condition
    ```js
    if (condition) {
        // stuff  to do
    }
    ```
    - where `condition` is anything at all tested for truthiness
    - if the condition  coercion results in truth we will run the stuff to do code
    - we can string multiple conditions together using `else` and more `if`
    ```js
    if (condition) {
        //stuff to do
    } else if (other condition) {
        //other stuff to do
    } else {
        // catch all for any other cases
    }
    ```

  ## Resources
  - [Event names](https://developer.mozilla.org/en-US/docs/Web/Events)

  # Day 11 - Functions, Built in Objects/methods, value vs. reference

## Review
- toolkit
  - storing information in variables
  - access the DOM to get HTML elements
  - add event listeners to those elements
  - Conditional logic - if/else statements
  - console.log to prove you are doing what you think you're doing

## Challenge
- create a like button that increases its displayed value each time it is clicked:
![](https://raw.githubusercontent.com/TIY-Austin-Front-End-Engineering/jquery-like/master/likes.gif)

## Notes
- hoisting
  - variable declarations are hoisted to the top of their scope (either global or function)
  - function declarations are also hoisted to the top of their scope
  - however, variable assignment is NOT hoisted
- more detail about js functions
  - block of code that does stuff
```js
  // syntax for declaring a function; prefer the first for hoisting purposes
  function myCoolFn() {}
  var myCoolFn = function() {}
```
  - we must call a function to run it.
```js
  nameOfFunction();
```
  - parameters
    - what goes inside the m&ms of a function declaration
    - locally defined variables aka labels for values the function might used
    - scoped to the function!
  - arguments
    - what goes inside the m&ms of a function call / invocation
    - one argument for each parameter, they are order specific, extra arguments that don't have named params will be ignored
  - return statements
    - functions that have no return value ONLY perform side effects aka they DO stuff but have undefined value
    - in order for a function call to have a value other than undefined, we must **return** something from that function
  - evaluation vs declaration
    - function calls by default evaluate to undefined
    - they will evaluate to their return value if they have one.
    - function declarations always evaluate to undefined, just like variable declarations
- more about the types
  - number operators
    - `+ - / *`
    - shortcut to update a variable `+=`
    - `number++` `++` increment operator adds 1 to a number value; it will MUTATE that variable
    - `--` decrement operator subtract 1 to a number value; it will MUTATE that variable
  - string props/methods
    - recommend running string props/methods ON the variable that stores the string rather than the sting itself
    - `string.length` equals the number of characters in a string
      - where `string` is ANYTHING THAT EVALUATES TO A STRING
  - array props/methods
    - `array.length`
    - be aware that many array methods mutate the original array
  - pass by value vs pass by reference
    - labels that point to primitive values store THE VALUE not a reference to it.
    ```js
    var a = 0;
    var b = a;
    a = 1;
    b //evaluates to 0;
    ```
      - they forget where they got their value from
    - not so for arrays and objects. they store a reference;
    ```js
    var a = [1,2,3]
    var b = a;
    a[0]=5;
    a; // evaluates to [5,2,3];
    b; // evaluates to [5,2,3];
    ```
  - built in objects
    - document object
    - HTML element object
    - event object
      - the argument that was automatically passed into our event listener function by the browser
    - Math object
      - does math for you!
      - `Math.random()` givs a random number between 0 and 1
      - `Math.ceil()`
      - `Math.floor()`
      - `Math.round()`
      ```js
      // random number between 1-10
      Math.ceil(Math.random()*10)
      ```
    - console
      - `console.log()`
        - console is an object
        - log is a method aka a property on an object that is also a function
        - prints any and all arguments to the console
      - `console.assert()`
        - way to test whether something is true
        - takes 2 arguments, the first is a truth test, the second is an error message.
        - the truth test can be ANYTHING, but it will be coerced into a boolean
        - the error will print ONLY if the truth test fails. Otherwise you see nothing
    - window object
      - declaring global variables
<!-- - updating the `window.location.hash` -->

## Resources
- [String docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
- [Array docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

# Day 12 - location.hash, Loops, forEach, filter, map reduce

## Review
- reverse a string
  - splitting strings is awesome
  - array methods are plentiful, don't reinvent the wheel
- true or false on a vowel
  - or ||  / and && character
  - `||` will evaluate to the **first** truthy value it finds, or the last falsy value. `1 || 2` evaluates to`1`, which is truthy. `0 || 2` evaluates to `2` which is also truthy.
  - `&&` will evaluate to the **last** truthy value it finds or the first falsy value. `1 && 2` evaluates to `2`, `0 && 2` evaluates to 0

## Notes
- location.hash
  - listen to it!
    -  `window.addEventListener('hashchange', functionName)`
  - update it!
    - use an anchor tag with a `#` preceded href
    - do it programmatically with `location.hash = 'someLocation'`
      - where `someLocation` is the string after the hash
- what is a render function?
  - a function that puts content into the DOM
- accessing properties in an object
  - use `.` notation when you know the name of the property and are accessing it directly
  - use `[]` "bracket" notation when you have the property name in string form OR stored in a variable.
```js
var userRequest = 'ponies';
// all three of these are accessing exactly the same values
data.ponies.title;
data['ponies'].title;
data[userRequest].title;
```
- Loops!
  - for
    ```js
    for (startingCondition; testForCompletion; afterEachLoopDo) {
      //code to run every time the loop goes
    }
    ```
    ```js
    for (var i = 0; i < array.length; i++) {
      console.log(array[i]);
    }
    ```
      - where `startingCondition` is usually a counter variable declaration: `var i = 0;`
      - where `testForCompletion` is usually the length of an array or the number of times to do the loop `var i < array.length;`
      - where `afterEachLoopDo` is usually an incrementer on the counter: `i++`
      - inside the loop we usually reference the ith element in the array `array[i]`
  - loop over elements to add event Listeners
  - loop over elements to remove a class from each one
  - loop over elements to change their contents all at once
- Callback methods
  - a function that is passed to another function as an argument is called a callback function
  - callback functions always receive their arguments by their calling functions, not by us.
  - we can only give names to those parameters, or leave them unnamed and ignore them.
  - examples - click handlers, array methods:
- Array methods! - the loop's more user friendly cousin!
  - all 4 take a callback function as their argument
  - the callback will be called for each item in the array. It receives each item in the array one at a time as its argument
  - `.forEach()`
    - does not return anything, only DOES STUFF aka has side effects
    - useful for putting a list of things into the DOM, or console logging a bunch of things individually
  - `.filter()`
    - returns an array
      - that array contains the same values as the original array, but potentially FEWER of them
    - in the callback we must return a truth test. that truth test determines what gets put into my new array
  - `.map()`
    - returns a new array
      - it is the same length as the original array
      - it's values are related to the original array, but different
    - in the callback we return the value we want to be placed in the new array
  - `.reduce()`
    - the only one whose callback differs.
    - returns a single item of our chosing - it could be an array, object, string, whatever
    - we build that object over time by returning it from the callback function.

## Resources
- [array.forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/foreach)
- [array.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [array.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
- [array.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

# Day 13 - forEach, filter, map, reduce, jquery

## Review
- cdn, css reset
  - cloud server network
  - css reset equalizes starting point across browsers
- add class
  - `element.classList.add('className')`
  - where element is an HTML element that was accessed from the DOM
  - where className is the name of the class you want to add to the element
  - this only works on an individual element, not a list of elements
- formatting stuff we put into the DOM

## Challenge
Write a function called sum that will return the sum of ANY NUMBER of arguments. eg:
```js
sum(1, 2, 5) // evaluates to 8
sum(4, 2) // evaluates to 6
sum(9, 34, 25, 1, -3) //evaluates to 66
```
HINT: you will need the special `arguments` keyword

## Notes
- finish the array method examples
  - if you need to filter and map to get your answer, make sure you filter first! or you won't have access to the full item
  - the sandwich analogy:
    - we can first filter all the ingredients in the house to be just the ingredients needed for a sandwhich
    - map over them to get sliced ingredients
    - reduce them into sandwiches
    - forEach to eat them (no return value, just does something)
  ![](../images/map-reduce.png)
- jquery
  - used for:
    - DOM manipulation
    - Event handling
  - include in project
    - include in a script tag pointing to the jquery cdn
  - select elements
    - `$('cssSelector')`
      - where `cssSelector` is any valid css selector
      - will return a set of jQuery wrapped elements - all that match the selector
  - get vs set
    - `jQueryWrappedElements.text()`, `jQueryWrappedElements.html()`
      - where `jQueryWrappedElements` is any set of elements selected with the jQuery selector (see above)
      - used with no arguments, these functions return the `textContent` or `innerHTML` of the first element in the `jQueryWrappedElements` set.
      - used with any string argument, these functions will replace `textContent` or `innerHTML` of ALL the elements in the set.
      - with `.html('htmlString')` the `htmlString` will be parsed as HTML and element tags will be turned into elements
      - with `.text('string')` the `string` will NOT be parsed as HTML, and element tags will be placed into the DOM exactly as they appear in the string
  - create an element
    - `$('actualHTMl')`
      - where `actualHTML` is a string of html to create
      - this element is created, but not stored OR put into the DOM
      - to store it, put it in a variable.
      - to put it in the DOM, use the `.html()` method above, or the `.append()` or `.prepend()` methods below:
  - `.append(elementOrString)`, `.prepend(elementOrString)`
    - where `elementOrString` is an HTML element, a jQuery wrapped element or set of elements, or a plain text string
    - `elementOrString` will be parsed as HTML and added to the element on which the method is performed.
    - `.prepend(elementOrString)` will add `elementOrString` as the **first** child of the element it is performed on
    - `.append(elementOrString)` will add `elementOrString` as the **last** child of the element it is performed on
  - `.addClass(className)`, `.removeClass(className)`
    - where `className` is a string of the class to add or remove
    - will add or remove the class from ALL elements in the jQuery set of elements at once.
  - `.on()`
    - the jQuery way of adding event listeners, nearly identical to `.addEventListener()`
    - will apply to all elements in the jQuery set of elements, rather than only on one at a time
  - `.toggleClass(className)`
    - as the name implies, will toggle a class, so just like add or remove class, but if the class is there, it removes it, if the class is not there it will add it.

## Resources
- [jQuery docs](http://jquery.com/)

# Day 14 - SPAs, gh-pages, jQuery and the data attribute

## Review
- using classes to change behavior

## Challenge
Write a function letterCount() that takes a string and returns an object with the count of each letter that is in the string.

```js
letterCount("hello world");
// will return:
// {
//   h: 1,
//   e: 1,
//   l: 3,
//   o: 2,
//   w: 1,
//   r: 1,
//   d: 1
// }
```

## Notes
- new file structure:
![file-structure](../images/file-structure.jpg)
- gh-pages
  - github will serve files in a gh-pages branch
  - `git subtree push --prefix dist origin gh-pages`
  - pattern for finding the site live
- SPAs
  - single page app - meaning that all our content lives on a single HTML page, which we manipulate to show different data and elements using javascript and css.
  - For safety, we wrap all of our DOM accessors and runtime code in a document ready block
  ```js
  // function declarations and variables that don't depend on DOM can go out here
  $(document).ready(function() {
    // write code here
  });
  ```
  - start with a good set of wireframes and/or a good description of what the app should do.
  - Build a mock up using only HTML and CSS, hard-coding in examples that will later be dynamically created with JS.
  - Think through the data structure needed for the application. Build out a mock of that data.
  - Now you're ready to start JavaScripting! Figure out what your user is going to do first, in an ideal world. Start there!!
    - This may mean adding an event listener for a click event
    - Or it may mean building a few elements that the user expects to see dynamically (rather than leaving them the hard coded versions in your mockup)
- data attribute
  - useful for keeping track of some unique information about an item in the DOM and how it relates to our JS data set.
  - any HTML attribute that is preceded by a `data-`. For example:
  ```html
  <ul>
    <li data-index="0">Some value</li>
    <li data-index="1">Some other value</li>
    <li data-index="2">value</li>
  </ul>
  <ul>
    <li class="message" data-id="7lsi3ls08l">A message with a unique id!</li>
    <li class="message" data-id="298laflk4w">A message with a unique id!</li>
    <li class="message" data-id="38ohlsflsk">A message with a unique id!</li>
    <li class="message" data-id="kjf7wrjdfl">A message with a unique id!</li>
    <li class="message" data-id="c98hlsnfoi">A message with a unique id!</li>
  </ul>
  ```
  - we set them either by hard coding them in HTML or with the `.attr()` method in jquery (see below)
  - we access them with the `.data()` method in jQuery
    - will return an object, where the keys of the object are the attribute name without the preceeding `data-`. From the example above: `{index: 0}` or `{id: '298laflk4w'}`
- `.attr()` jQuery method
  - used to access or change attributes in HTML elements.
  - get (access) an element's attribute by passing in one string argument, the name of the attribute.
  - set (change) an element's attribute by passing in 2 string arguments (name of attribute and attribute value)
  - or set multiple attributes at once by passing in an object of key (attribute name ) value (attribute value ) pairs.
  ```js
  var linkAddress = $('a').attr('href'); // returns the href of the first matching a tag
  $('a').attr('href', 'http://google.com'); // changes the href of all matching a tags to google.com
  $('li').attr({'data-index': 0, class: 'fancy-list-item'}); // adds or changes BOTH the data-index attribute and the class of all matching lis
  ```

  # Day 17 - JSON, AJAX intro

## Review
- `querySelectorAll('selector')` vs `$('selector')`
  - jquery version returns a jquery wrapped elements
  - the primary benefit is not having to loop to apply changes to multiple elements at once
  - easier traversing the DOM

    ```js
    //vanilla
    var divs = document.querySelectorAll('div');
    for (var i = 0; i < divs.length; i++) {
      divs[i].classList.add('coolDiv');
    }
    //jqeury
    $('div').addClass('coolDiv');
    var newDiv = $('<div></div>') // making a new div
    ```



## Challenge
write a function `names()` which takes a string of comma-separated names (first and last) and then returns an object where each first name is a key, and each last name is a value

```js
names("George Washington, John Adams, Kanye West")
  //  {
  //     George: "Washington",
  //     John: "Adams",
  //     Kanye: "West"
  //   }
```

## Notes
- AJAX - asychronous javascript and xml
  - 4 verbs - CRUD
    - create, read, update, delete
    - HTTP verb counterparts: POST, GET, PUT, DELETE
  - to make an ajax request: `$.ajax(settings)`
    - where `settings` is an object that configures the ajax request
    ```js
    // example settings object:
    var requestSettings = {
      url: 'the url where i want to make the request to',
      type: 'GET' // either 'GET', 'PUT', 'POST', 'DELETE',
      success: function(response) {
        // what to do when the data returns from the server successfully
        // this callback always receives the response from the server as its first argument
      }
    }
    ```
      - `'jsonp'`
        - always set the `dataType` to `'jsonp'` when `crossorigin` requests are an issue. you will need this for tonight's homework.
    - see below for link to settings documentation
- API - application interface
  - usually refers to the way i can interface / interact with a an applications data
  - many web applications make their data publicly available through a JSON API
- JSON - JavaScript Object Notation
  - a way of passing data around the internet, using JS objects and arrays.
  - JUST LIKE JS objects! except:
    - keys are always in double quotes
    - JSON does NOT ALLOW trailing commas
    ```js
    //js
    {
      name: 'Jess Scheuring',
      age: 32,
    }
    // json
    {
      "name": "Jess Scheuring",
      "age": 32
    }
    ```

## Resources
- [The Event Loop video](https://www.youtube.com/watch?v=8aGhZQkoFbQ) (until minute 17)
- [jQuery ajax settings configuration](http://api.jquery.com/jquery.ajax/#jQuery-ajax-settings)

# Day 18 - AJAX PUT POST DELETE

## Review
- turning repeated code into DRY code with functions
- filter, map, reduce functions MUST return something! Otherwise, just use forEach
  - forEach - nothing to store!
    - applies a callback function to every item in an array
    - RETURNS NOTHING. great for doing stuff, like logging or adding to the console.
  - filter
    - filters an array via boolean test,
    - returns whole items from the original array in a new arry
  - map
    - applies a callback to each item in an array
    - returns a new array full of the return value of the callback
  - reduce
    - applies a callback to each item in an array as well as the return item from the previous call
    - returns a single something, the ultimate return value of the callback
- moving the function outside the success/event listener/filter etc.
  - copy the whole function declaration
  - give it a name
  - refer to it by its name, without the m&ms when you pass it as the argument

## Challenge
- use `setTimeout()` to create a button that becomes disabled and displays: 'loading...' after it is clicked. It should return to normal after 4 seconds.
- [my solution](http://codepen.io/nicerhugs/pen/Lkjpja?editors=1011)

## Notes
- REST - representation state transfer
  - RESTful api, REST architecture
  - Tiny Pizza Server, a basic REST api:  `http://tiny-za-server.herokuapp.com/collections/<anythingYouWant>`
  - Stores "noun-based" data for an application in "endpoints", or "services"
  - We can interact with those endpoints with the HTTP verbs by making AJAX requests
  - collection endpoints are usually pluralized noun names eg `/unicorns`
  - individual items are usually "namespaced" by id after the collection eg `/unicorns/uniqueID`
- POST - create a new item on the server
  - must include a `data` property in the ajax settings object. That data should be a javaScript object.
- DELETE - delete a single item on the Server
  - should be namespaced by id
- PUT - modify (edit, update) a single item on the server
  - should be namespaced by id
  - must include a `data` property in the ajax settings object that includes ONLY the data you want to modify
- Data attribute, storing state in the DOM
  - prefer storing arbitrary data in `data-<something>` attributes if using the DOM to store data is necessary
  - access those attributes using the `.data()` method in jQuery
  # Day 19 - Constructors

## Review
- adding elements to the DOM with jquery (nested structure)
- event listener that results in ajax request
- data attribute, identifying a particular element's backing data

## Challenge
An isogram is a word that has no repeating letters, consecutive or
non-consecutive. Implement a function that determines whether a
string that contains only letters is an isogram. Assume the empty
string is an isogram. Ignore letter case.

```js
//example function calls and their expected outputs:
isIsogram( "Dermatoglyphics" ) == true
isIsogram( "aba" ) == false
isIsogram( "moOse" ) == false // -- ignore letter case
```

## Notes
- Constructors!
  - constructors are functions that are used to create objects
    - they are like **factories that make objects** that come pre-loaded with properties and methods
  - constructors are named with capital letters
  - to use a constructor, you must use the `new` keyword:
  ```js
    var jess = new Person();
    // jess is now an object!
  ```
  - inside the constructor function body, `this` refers to the object being constructed.
    - therefore we can set properties on the objects we are making like so:
    ```js
    function Person() {
      this.name = 'jess'
    }
    ```
    - in the above example, every object I make with the `Person` constructor would have its `name` property set to `'jess'` This is how we would set default properties on our new objects.
    - to initialize the new object but with specific information that we pass in, we can use the constructor functions parameters:
    ```js
    function Person(name) {
      this.name = name
    }
    new Person('jess');
    ```
    - in the above example the new person object would have a name of 'jess', but not all objects would have this name.

    # Day 20 - Constructors and Prototypes

    ## Review
    - Constructors
    - Github partner flow
      - 1 person makes a repo and hooks it up like normal
      - that person adds other partners as collaborators
      - collabs must accept via email
      - collabs do not git init, instead they clone the project to their local machine
        - `git clone <the clone url> <path to folder>`
      - EVERYONE EVERYONE WORKS ON A FEATURE BRANCH
        - make a new branch `git checkout -b <branchName>`
        - checkout an existing branch `git checkout <branchName>`

    ## Challenge
    - Modify the `String` prototype to have a `shout` method that makes the string all capitals and adds 5 exclamation points afterwards
    - Create a `Counter` constructor that allows us to increment and decrement easily. It should have an increment and decrement method. They should change the value by 1 by default, OR by any number if they are given a number as an argument

    ## Notes
    - EVERYTHING in javascript is an object!
    - EVERYTHING in javascript is an **instance** of a constructor
    - we _can_ make methods on the constructor, but that makes a million copies of the same function. Instead, we can **share** that function between all copies of the object via the prototype.
    - THUS, Methods should live on the prototype
      - a prototype is an object that other objects can look up methods on.
      - if an object needs access to a method, but cannot find it on itself, it can look on its prototype. if it cannot find the method there, it will look on THAT object's prototype.
      - Inside a method on a prototype `this` refers to the instance the method was called on
      - All objects (even those made by a contructor) point to the `Object.prototype` by default.
        - This gets hooked up when we use the `new` keyword
        - To add methods to a particular constructor's prototype:
        ```js
        function User(username) {
          this.username = username;
        }
        User.prototype.greet = function() {
          console.log('hi, my name is ' + this.username);
        }
        ```
        - To create "inheritance" from one constructor/prototype to another:

        ```js
        function User() {
          // user constructor code goes here
        }
        function Admin() {
          User.apply(this, arguments);
          // admin constructor code goes here
        }
        Admin.prototype = Object.create(User.prototype);
        Admin.prototype.constructor = Admin;

        ```

        # Day 21 - Build Tools, NPM, ES6, Underscore

## Review
- Models and Views - separation of concerns
- Why SPAs

## Challenge
Write your own function called `forEach` that takes an array or array like object and a callback as its two arguments, and works like the `.forEach()` method. Do not use the `.forEach()` method in your function.

If you finish, write a `map`, `filter`, and `reduce` function, as well.

## Notes
- Build Tools
  - popular ones:
    - Gulp, Grunt, Broccoli, Webpack
    - NPM - Node Package Manager
      - NPM helps us keep track of project dependencies.
        - for example, if the project needs 'jquery' we can add it as a dependency: `npm install --save jquery`
        - if the project needs babel in order to compile, we can add it as a dev-dependency: `npm install --save-dev babelify`
      - NPM also allows us to run and automate 'scripts', and manage configurations for our 'build environment'. for example, `npm run build` will run the code found in the `scripts.build` key of our package.json file on the command line.
    - the spa-scaffold tool comes with some development dependencies, and a bunch of scripts and configuration. They build a file structure for a new project, watch those files for changes, and compile a dist folder for production use.
      - instructions for using it are in its README, and it is linked at the bottom of these notes.
- ES2015
  - ES stands for 'EcmaScript', which is the language specification that javascript follows.
  - add a configuration file to your project called `.jshintrc` to turn of atom jshint warnings.
    - this is a json file that needs the following to make atom ok with es2015:
    - `{"esversion": 6}`
  - Babel
    - Babel is the compiler that helps us use es2015, since it is not fully supported by the browsers yet
    - it is included by default in the spa-scaffold
  - let, const
    - `let` and `const` replace the `var` keyword for making new variables
    - `let` is block scoped, which means it will stay inside of for loops, or if statements when it was declared in them.
    - `const` is for values that do not change, whereas `let` variables can represent values that may change or be re-assigned.
  - template strings
    - use backticks to surround a string rather than single or double quotes
    - escape variables with `${}` to "concatenate" the strings
    ```js
    let name = 'Jess'
    let greeting = `Hello ${name}, how are you today?`
    ```
  - arrow functions
    ```js
    filter(function(item) {
      return item.active;
    });

    filter(item => {
      return item.active;
    });
    ```
    - arrow functions do not create a new scope. This is helpful for callback functions when we want to maintain the same `this` as exists outside the callback.
  - modules
    - modules allow us to keep our code cleaner and more organized, and not 'crowd the global namespace'.
    - modules have 'module scope', and all code they contain is run only when the file in which they reside is imported.
      - runtime code in a module only runs once, no matter how many times it is imported. However, functions and objects/arrays that are exported from a module may be run (for functions) or modified (for objects/arrays) multiple times.
        - every time you run an imported function, the code within that function will run again.
        - likewise, every time you import an exported object, it will still hold on to all the changes that it has been through from other interactions.

## Resources
- [The SPA Scaffold Repo](https://github.com/TIY-Austin-Front-End-Engineering/spa-scaffold)
- [Babel](https://babeljs.io/)

# Day 22 - Review jQuery SPA, Backbone Router

## Review

## Challenge

## Notes
- getting started/setup
  - clone scaffolding
    - copy `clone with https` url from [here](https://github.com/TIY-Austin-Front-End-Engineering/spa-scaffold)
    - command to clone `git clone <url> <directory to install into>`
      - if you don't specify the directory it will MAKE a new directory as a child of your current location called whatever you are cloning.
  - move into the project directory
  - remove git history of the scaffolding project
    - `rm -rf .git`
  - add a new git repo as you always have done
  - run `npm install` to build your files and start your sever
  - after you see the sever message in the console, check your site at http://localhost:8080
  - work on your project in the app folder
- Draw out wireframes, and make sure you know what your application is going to do on each page
- Do some data modeling for my application
- Stub out some data
- Start writing our code
  - created basic layouts with html (and css)
  - write javascript in the entry.js file. move 'discrete' features to their own modules as you are able.
  - install dependencies as they come up : `npm install --save <packageName>`
  - check code every step of the way as soon as possible, come up with hypothesis about what you expect to see, and troubleshoot when that doesn't happen
  - to create "global variables", but modularly, you can create a module for that data (for example a "session"), and import it anywhere you need it.

  # Day 23 - Underscore, Backbone

  ## Review
  - setInterval lag on refresh
    - wait to empty the area until you have everything ready to be loaded back in (don't do it before your ajax is successful, for example)

  ## Challenge
  use jquery's ajax and the underscore library to group the data found at `tiny-za-server.herokuapp.com/collections/unicorns` into an object whose keys are color names and values are the unicorns of that color.

  ## Notes
  - Underscore
    - a functional utility library that makes manipulation of data sooo much easier
    - includes functions that work on arrays, objects, or either.
    - all functions are namespaced with the `_` character, like so:
    ```js
    _.map(anArray, aCallback);
    ```
  - Backbone
    - Router
      - configure with
        - list of routes,
        - function or each route
      - turn it on
        - create an instance of it (`var router =  new Router()`)
        - start watching for hashchanges: `Backbone.history.start()`
      - parameterized routes
        - have a `:` in their path name
        - whatever comes after the `:` will be passed to the function as an argument
    - Model
      - configure with
        - default values,
        - a root URL so they know where to save to
        - any custom methods they should be able to do
      - create instances
        - you can pass in attributes for them when you create them
        - you can set new attributes by using the `.set()` method
        - you can get the attributes by using the `.get()` methods
        - you can save it to the server with the `.save()` method

  ## Resources
  - [our codepen groupby example](http://codepen.io/nicerhugs/pen/bZYQyV?editors=0011)

  # Day 24 - Backbone Collections and Events

## Review

## Challenge

## Notes
- Router responsibilities
  - keeps track of which route or 'page' a user wants to see
  - calls the different render functions and hooks them up with the models/collections that back them
- Model responsibilities
  - keeping track of a particular piece of data
  - should have custom functionality should data on it need to be manipulated
  - emits events when that data changes or when it is created or destroyed
  - can also be responsible for synching with the server, but more likely its collection will do that for it
- Collection responsibilities
  - houses a bunch of models
  - keeps track of those models and any changes to them, emitting events when changes occur (adding, removing, updating)
  - synching with the server (`.fetch()`)
- View or render function responsibilities
  - render itself and return itself
  - render and populate itself with its children
  - listen to its own data source and update itself when the data changes
  - listen to user events and pass along info as needed
- `someCollection.create()` like making a new model, saving that model to the server, AND adding it to the collection all at once
- by listening to events emitted by models and collections, views can update 'automatically' by re-rendering when the data they are representing changes.

# Day 26 - BaaS, Kinvey, Authentication

## Review
- why to not save a timestamp already converted with moment when you save it
- don't name variables with $s unless the variable represents an html element or jquery wrapped element.
  - naming conventions:
    - capital letter: for constructors
    - `$`: for dom elements
    - `_`: usually for "private" methods, or methods that are used by other functions but not by the developer directly
- deleting an item from the menu (see review folder)
- exporting "global" variables

## Challenge
- Write a function that takes a card number as a string and returns `true` if the credit card entered is valid, `false` otherwise.
- Starting with the first digit and continuing with every other digit, multiply by 2
- Sum all doubled and untouched digits in the number
- If that sum is a multiple of 10, the number is valid

For example, given the card number 4408 0412 3456 7893:

```
Step 0: 4 4 0 8 0 4 1 2 3 4 5  6 7  8 9  3
Step 1: 8 4 0 8 0 4 2 2 6 4 10 6 14 8 18 3
Step 2: 8+4+0+8+0+4+2+2+6+4+1+0+6+1+4+8+1+8+3 = 70
Step 3: 70 % 10 == 0
```
```
isValid('4408 0412 3456 7893') // true
isValid('4417 1234 5678 9112') // false
isValid('5000000000000000') // false
```

## Notes
start from scratch or modify the existing app?
- back end
  - REST: 'resources' or 'services' represent nouns
  - can do things we on the front end cannot
    - persist data
    - manipulate data before or after saving/retrieving from db
    - send emails
    - protect access to data
      - on the front end we should attempt to make it impossible for a user to make an unauthroized request
    - run scheduled code
- Authentication
  - cookie based auth
  - token based auth
    - oauth
    - custom authorization
- back end as a service
  - examples: firebase, backendless, parse, Kinvey
- kinvey

## Resources
- [kinvey session docs](http://devcenter.kinvey.com/rest/guides/users)
- [kinvey security docs](http://devcenter.kinvey.com/rest/guides/security)
- [kinvey data docs](http://devcenter.kinvey.com/rest/guides/datastore)

# Day 27 - Backbone Views

## Review
- server errors
  - 200 it worked
  - 300 no change
  - 400 your request is bad
  - 500 something wrong on the server
  - the Network tab is your friend - you can view all your request headers, all the response headers, any data you send to the server with your request, and the full content of the response from the server as well. it's your best bet for troubleshooting ajax requests
- models/collections
  - generic
    - represent the data of our application
    - keeping the data separate from the visual presentation
  - backbone specific, but also maybe other frameworks as well
    - easier to send and retrieve data from the server
    - other custom functions that modify the data can live on them
    - ability to emit events and be listened to
      - we updated the app to use an actual session Model for login and logout

      # Day 28 - Review, BB Views, Data Store

      ## Review

      ## Challenge

      ## Notes
      - specific backbone methods for models, collections, Views
        - model methods
          - `.save(objectOfAttributes)` - saves a model to the server, based on the idAttribute and urlRoot properties; it will fire a change event; takes an object of attributes we want to save to our model; will `POST` or `PUT` depending on whether that model already has an id
          - `.fetch()` - GET a model from th server based on its urlRoot and idAttribute; fires a change event IF anything on the model changed after it gets the data from the server
          - `.set()` - sets attributes to a model; fires a change event; can accept 2 values, the first being attribute name, second being value OR an object of attributes
          - `.get()` - the way we access attributes on our model, takes a single argument which is the attribute we want to access
          - `.unset()` - clear a particular attribute
          - `.clear()` - which will wipe out everything on the model
          - `.destroy()` - which destroys the model and fires a destroy event
          - `.validate()` - which you set up on the constructor, automatically this runs before saving to the server, and if the function returns false the server save won't happen
          - `.parse()` - which you set up on the constructor as well, it modifies the data that comes back from the server before setting those attributes to the model
          - custom methods - you will write any time you want to manipulate data but beyond just setting or getting a single attribute
        - collection methods
          - `.fetch()` - GET requests all the models for that collection using the url property; fires a add event for any models it finds that weren't already in the collection, a change event for any changes to models that were in the collection, and a remove event for any models that weren't on the server but were in the local collection
          - `.create()` - POST a single NEW model to the server; fires and add event, takes 2 arguments, the first is attributes for that model, the second is any modification to the jquery ajax request
          - `.get()` - returns a model in the collection based on its id. only if the model is already in our collection, doesn't make any server requests
          - `.set()` - updates the collection based on models you pass to it - we don't call this very often, usually we rely on fetch to do this for us, can fire add, remove, and change events based on what happens
        - view methods/properties
          - `.render()` - doesn't do anything by default, but by convention we are going to use it to stuff the element the view represents with its template and any backing data
          - `.el`, and `.$el` - the element the view represents and the element wrapped in jquery
          - custom functions - usually event handlers, which we reference in the events object
        - router methods
          - `.navigate()` - which updates the location.hash and can also trigger the associated function, but you have to pass `{trigger: true}` as the second argument for that to occur, first argument is the string of the route name you want to go to
          - custom methods - which are usually triggered by the routes object when a user navigates to a particular route
      - any of the ajax methods for backbone (.save, .fetch, etc) we can pass modifications to the ajax request.
        - we are already doing that with our success or error functions, other modifications occur in the same object:
        ```js
        model.save(null, {
          success: function() {
            //do stuff on success
          },
          url: 'http://theDifferentUrl.com/saveHere/instead'
        });
        ```
      - initialize
        - a function that lives on any backbone object, such as a view, model, collection or router.
        - customize it to run code when a new instance is created
        - most often we use this for data backed views; we would fetch the data we need in initialize, and set up the listener to the model or collection for changes.
      - debugging server errors
        - if you see a AJAX error in the console:
          - click on the error to view it in the network tab
          - click on the request itself (it's usually red)
          - look at the 'preview' tab to see if the response came back with helpful info
          - look at the 'headers' tab to check the headers specifically (like Authorization) and the data sent as well (in the 'request payload' at the bottom of the tab)
      - list view children
      - logout
      - zombie views
      - localStorage

      # Day 29 - Data Store, Backbone Review, Agile

## Review

## Challenge

## Notes
- data stores
  - create a single object that keeps track of all your application state
  - it should contain instances of any collections or models needed
  - it can also contain other 'application state' such as whether you are actively fetching from the server, or which page of blog posts you are currently showing to the user (if you are paginating your posts)
- style guides
  - there are design style guides that guide you in when and how to use colors, fonts, etc.
  - there are code style guides that guide you in when and whether to:
    - use semi-colons
    - use var, let, or const, and in what circumstances
    - name variables in a certain way, with a certain case
    - etc.
- parameterized routing (see examples folder)
  - views should set up their own event listeners to listen to the data they use
  - set up listeners and fetch data in the view's initialize function
  - the initialize function will receive anything you pass into the constructor call - that would be a good place to pass along the url parameter (like the post id)
- Agile
  - project management style popular in software development
  - based on the idea that everything changes, so we should be prepared for change
  - build software in small, incremental pieces
  - break down a project into the smallest possible features that are 'releasable' and work on a feature at a time.
    - features are written as "stories"
      - user story: 'as a <Type of user> i need to <do something> so that i can <desired outcome>'
      - bug story: some existing feature has a bug that needs fixing
      - developer story: if some code needs to be implemented (like chores) that aren't really a feature that the user interacts with
  - scrum
    - break a project into "sprints" or smaller segments of time during which you focus on particular features
    - stories move through phases within a sprint:
      - 'backlog' (stories that are waiting to be done in a future sprint)
      - 'ready' (stories that are part of this sprint and need to be started)
      - 'in progress' (stories someone is working on actively)
      - 'in testing' (stories that are 'complete' but waiting for approval from team/testers etc)
      - 'complete'
    - daily standup - a SHORT meeting (no one ever even sits down) in which you describe:
      - what you did
      - what you plan to do
      - what, if anything, is blocking you
    - make estimates for a story - how long will it take you to complete it?

## Resources
- [extreme programming](http://extremeprogramming.org)

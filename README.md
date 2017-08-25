# Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?
* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
IE7 allowed only two concurrent connections per host. But most browsers today allow more than that. IE8 allows 6 concurrent connections, Chrome allows 6, and Firefox allows 8.

So if your web page only has 6 images, for example, then it'd really be pointless to spread your images across multiple subdomains
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?
`doctype` informs the browser which version of HTML (or XML) you used to write the document. Doctype is a declaration, not a tag; you can also refer to it as "document type declaration", or "DTD" for short

* What's the difference between full standards mode, almost standards mode and quirks mode?
Full standard: strictly adhere to W3C spec  
Almost standard: have some quirks  
Quirk mode: compact the old website
* What's the difference between HTML and XHTML?

**Document Structure**
XHTML DOCTYPE is mandatory
The xmlns attribute in <html> is mandatory
<html>, <head>, <title>, and <body> are mandatory
**XHTML Elements**
XHTML elements must be properly nested
XHTML elements must always be closed
XHTML elements must be in lowercase
XHTML documents must have one root element
**XHTML Attributes**
Attribute names must be in lower case
Attribute values must be quoted
Attribute minimization is forbidden

* Are there any problems with serving pages as `application/xhtml+xml`?
* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
set for customr field in HTML element
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
  * cookie have expire date
  * sessionStorage will be cleared after the browser restart
  * localStorage will remain if you don't clear it manually

* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
async will load your script asynchronously, that is load it in pararllel with other stuff and execute it immediately after the loading  
defer will load your script asynchronously as well, but it will execute it after all the document has been parsed and just before `DOMContentLoaded`

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
The browser will start to show the content only when css is loaded, so we put the css to the top of our webpage.  
The js will need to wait till last because we will try to present the visual element in the webpage while js is loading, besides js can only manipulate the dom tree after the dom tree has been parsed.

* What is progressive rendering?
Progressive rendering is the name given to techniques used to render content for display as quickly as possible.

It used to be much more prevalent in the days before broadband internet but it's still useful in modern development as mobile data connections are becoming increasingly popular (and unreliable!)

Examples of such techniques :

Lazy loading of images where (typically) some javascript will load an image when it comes into the browsers viewport instead of loading all images at page load.
Prioritizing visible content (or above the fold rendering) where you include only the minimum css/content/scripts necessary for the amount of page that would be rendered in the users browser first to display as quickly as possible, you can then use deferred javascript (domready/load) to load in other resources and content.
* Have you used different HTML templating languages before?

I have used EJS for my Node.js Project
I have heard of Jade.

#### CSS Questions:

* What is the difference between classes and IDs in CSS?
ID should be unique
classes don't have to be unique

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
normalizing css is better, it dosen't remove all the default style, also fix some browser bugs, and modular.

* Describe Floats and how they work.

* Describe z-index and how stacking context is formed.
* Describe BFC(Block Formatting Context) and how it works.
It has height, width, top/bottom padding/margin

* What are the various clearing techniques and which is appropriate for what context?
clear: both
overflow
empty div
* Explain CSS sprites, and how you would implement them on a page or site.  
Multiple Image combined together into a single image. The image then use background-position to show different part of it. It help to increase the page load speed since it reduce the number of HTTP request.

* What are your favourite image replacement techniques and which do you use when?
lazy loading

* How would you approach fixing browser-specific styling issues?

* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
`visibility: hidden`
* Have you ever used a grid system, and if so, what do you prefer?
Bootstrap
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?

* How do you optimize your webpages for print?
Use an extra style sheet for printing
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
border-box: height and width includes the content, padding and border.
content-box: height and width only includes the content.

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?  
Tell the browser to user the border-box model instead of the content box model.
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
inline dosen't have width, height, cannot set top and bottom margin/padding
* What's the difference between a relative, fixed, absolute and statically positioned element?
fixed and absolute set the element to not be in the document flow

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
Bootstrap
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

#### JS Questions:

* Explain event delegation
* Explain how `this` works in JavaScript
* Explain how prototypal inheritance works
* What do you think of AMD vs CommonJS?
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?
add brackets
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
declaration expression constructor respectively

* What's the difference between `.call` and `.apply`?
.call(this, arguemnts1, arguments2, ...)
.apply(this, [arguments1, arguments2, ...])
* Explain `Function.prototype.bind`.

* When would you use `document.write()`?
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
  EJS, etx.
* Explain "hoisting".
process the variable and function declaration before other code
* Describe event bubbling.
event emitted from child elements to their respective parent element
* What's the difference between an "attribute" and a "property"?
attribute is a term used in HTML
property is used for object
* Why is extending built-in JavaScript objects not a good idea?
It might cause some undesired side effect
* Difference between document load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
== will do coercion when the two are not the same type
* Explain the same-origin policy with regards to JavaScript.

* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
```
function duplicate(array) {return array.concat(array)}
```
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
"Ternary" means composed of three parts, it's the only JS operator that take in three operands
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
```
var returnString;
for(var i = 0; i <20; i++) {
  returnString = "";
  if (i%3===0) {
    returnString += "fizz";
  }
  if (i%5===0) {
    returnString += "buzz";
  }
  console.log(returnString, i)
}
```
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
  only object and array is mutable, primitive are immutable.
  Use `Object.freeze` to freeze code.
  mutable means can be changed. primitive cannot be changed once it is created. we can only change its pointer.
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
function declaration will be hoisted while function expression won't be.

#### Testing Questions:

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?
Allow parallization to improve speed
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
URL converts to IP address through UDP request
three way handshake to establish the TCP connection
Http get request is sent to retrieve HTML, CSS, JS and other assets(if image on the other domain then the above process will repeat)
additional request might be sent to backend API to obtained some other data
DOM tree
CSSOM tree
JavaScript Execute
connection closed.

* What are the differences between Long-Polling, Websockets and Server-Sent Events?
* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* What are HTTP methods? List all HTTP methods that you know, and explain them.
get, head, post, put, delete, options, connect
#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
1020 all will be converted to string

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```


*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
"goh angasal a m'i"

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```
the expression in `window.foo` will be executed before the OR operator due to operator precedence, so the value of window.foo is bar.

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
first will execute, second will throw a reference error



*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
no trick here, 2

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
foo.x = undefined
bar.x = {
  n:1
  x: {n:2}
}

This is very tricky. foo.x actually will be evaluated first to become {n: 1}.x and then the assignment begins, the `foo = {n: 2}` point our pointer to {n: 2}, then the memory that previously stored {n: 1} gets updated to {n:1, x: {n: 2}} which is the placa that bar points to.

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
one
three
two

#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Who inspires you in the front-end community?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).

# Document Object Model (DOM)

A specification for browsers to create a model of HTML and how Javascript can interact within it. Not HTML or Javascript, the DOM is a set of rules agreed upon by all modern browser makers. It does two things:

1. Makes the model of the HTML page
2. Controls access and updating the HTML page

The DOM takes a tree structure in that all nodes flow from a single trunk, the Document. Nodes then branch off of the Document object in numerous directions. Nodes can also have child and sibling elements, similar to branches on a family tree. 

## Four Types of Nodes

* Document - The top of the tree i.e. the starting point
* Element - The structural components of the page (ex. div, table, td)
* Attribute - The descriptive parts of the element contained inside their open tags (ex. style, id)
* Text - The content containing element of the page that cannot contain another element (ex. p, li)

## Working with the DOM tree

### Access the elements

#### Select an individual element node 
* `getElementById()` uses the value of an element's unique id attribute 
* `querySelector()` uses a CSS selector and returns first match

#### Select multiple elements (nodelists)
* `getElementsByClassName()` selects all elements matching class name
* `getElementsByTagName()` selects all elements matching tag name
* `querySelectorAll()` selects all matching elements using CSS

#### Traverse between elements
* `parentNode()` selects parent of current element
* `previousSibling` selects previous sibling of current element
* `nextSibling` selects next sibling of current element
* `firstChild` selects first child of current element
* `lastChild` selects last child of current element

### Work with elements

#### Text Nodes
* `nodeValue` access/update contents of text node

#### HTML Content
* `innerHTML` access/update child elements and text content
* `textContent` access/update just text content
* `createElement()` adds element node to tree
* `createTextNode()` adds text node to tree
* `appendChild()` or `removeChild()` manipulate the DOM by adding / removing an element

#### Access / Update Values
* `className` or `id` you can change the class or id attribute of an element
* `hasAttribute()`, `getAttribute()`, `setAttribute()`, `removeAttribute()` check an attribute's existence, get the attribute's value, update the attribute's value, and remove an attribute

### Example

```
// Select the element and store it in a variable.
var el = document.getElementById('one');

// Change the value of the class attribute.
el.className = 'cool';
```

```
<!DOCTYPE html>
<html>
  <head>
    <title>JavaScript &amp; jQuery - Chapter 5: Document Object Model - Initial Page</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/c05.css">
  </head>
  <body>
    <div id="page">
      <h1 id="header">List King</h1>
      <h2>Buy groceries</h2>
      <ul>
        <li id="one" class="hot"><em>fresh</em> figs</li>
        <li id="two" class="hot">pine nuts</li>
        <li id="three" class="hot">honey</li>
        <li id="four">balsamic vinegar</li>
      </ul>
    </div>
  </body>
</html>
```




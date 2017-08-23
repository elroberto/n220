# Writing a Javascript Program

There are three primary areas of concern for the developer of Javascript. They are Content, typically written as `.html` files. Presentation, typically `.css` files or hard coded into the HTML. Lastly, there are Javascript files written either in a `.js` document or inline inside the HTML. 

## Content

There are other requirements for an HTML document to be complete, but here is a simple HTML snippet. Pay close attention to the words inside the `<` and `\>` tags. 

```
<body>
  <h1>N220 Syllabuls</h1>
  <h2></h2>
  <p>This page contains the syllabus for N220</p>
</body>
```

## Presentation

Adding on to our HTML document, we may want to add a stylesheet for the purposes of making our content more aethestically pleasing or accessible to different audiences. 

```
p {
    margin: 0 0 0 50px;
    font-weight: bold;
    text-align: center;
    border-right: 1px solid #bcbdc0;
    border-bottom: 1px solid #bcbdc0;
    border-left: 1px solid #bcbdc0;}
```

Can you tell which tag we stylized? It is any content inside the `<p>` tag. Now we only need to include our stylesheet in the HTML document to activate our CSS rules. 

```
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="../css/index.css" />
  </head>
  <body>
    <h1>N220 Syllabuls</h1>
    <h2></h2>
    <p>This page contains the syllabus for N220</p>
  </body>
</html>
```

## Behavior

We have now dealt with Content and Presentation layers, let's look at the Behavior layer. You will notice there is an empty `<h2>` tag in the HTMl. Let's use Javascript to update that tag with a time based greeting. 

```
var today = new Date();
var hourNow = today.getHours();
var greeting;

if (hourNow > 18) {
    greeting = 'Good evening!';
} else if (hourNow > 12) {
    greeting = 'Good afternoon!';
} else if (hourNow > 0) {
    greeting = 'Good morning!';
} else {
    greeting = 'Welcome!';
}

document.write('<h2>' + greeting + '</h2>');
```

All we need to do is put that program logic in a JS file, then include it in our HTML document. 

```
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="../css/index.css" />
  </head>
  <body>
    <h1>N220 Syllabuls</h1>
    <script type="text/javascript" src="js/add-content.js"></script>
    <p>This page contains the syllabus for N220</p>
  </body>
</html>
```

Obviously, this is not the most useful change, nor did we implement it in the most elegant way. As we progress, we will learn many different behaviors Javascript can perform, and how we can elegantly manipulate the Document Object Model (DOM) to suit our needs. 

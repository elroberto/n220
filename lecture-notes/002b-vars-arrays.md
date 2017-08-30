# Variables and Arrays 
## Variables
Variables store values. They’re just names that point to a value. Values can be of the following types:

* [Numbers](javascriptbook.com/c02/js/numeric-variable.js) 
* [Strings](javascriptbook.com/c02/js/string-variable.js) (text)
* [Booleans](javascriptbook.com/c02/js/boolean-variable.js) (true/false)
* HTML Elements
* HTML Inputs

You can use [shorthand](javascriptbook.com/c02/js/shorthand-variable.js) when declaring vars. And it seems obvious, but you can also [update variables](javascriptbook.com/c02/js/update-variable.js).

## Six Rules for Naming Variables 

1. Begins with *letter*, dollar sign, or underscore. 
2. Only contains letters, dollar sign, or an underscore. 
3. Cannot contain use reserved keywords (ex. var). 
4. Case sensitivity is followed.
5. Should describe what is being contained.
6. Should use camel case where appropriate. 

## Arrays
An array is a special type of variable. It stores a list of values. Consider using arrays when working with lists or sets. 

Creating an array:

```
var colors;

colors = ['red', 'blue', 'yellow'];
```

In the preceding array, `colors[0]` is red, `colors[2]` is yellow. Arrays always begin counting at 0. You can access array values by using the number or array key of the value you wish to access. You can access the length of an array by using the length property (ex. `colors.length`)

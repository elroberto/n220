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

## Operands
You can do more with variables than just assign single values. Variable operands let you manipulate the values inside the variables.

```
var a = 4;
var b = 2;

//addition
var c = a + b; //6

//subtraction
var d = a - b; // 2

//multiplication
var e = a * b; //8

//division
var f = a / b; //2

//modulo
var g = a % b; // 0
```

### Modulo
Also Known As “remainder” The part left over after division

```
7 % 3 //1
12 % 10 //2
```

Question
Let’s say I have a variable myVar and I want to subtract 2 from it, and store that value back into the variable?

How do I do that?

## Incrementing/Decrementing

```
var a = 5;

//incrementing
a = a + 1; //a == 6

//decrementing
a = a - 3; //a == 3

//multiplication
a = a * 2; //6

//division
a = a / 3; //2
```

### Incrementing/Decrementing Shorthand
```
var a = 5;

//incrementing
a += 1; //a == 6

//decrementing
a -= 3; //a == 3

//Multiplication
a *= 2; //6

//Division
a /= 3; //2
```

## String Concatenation
One can also use the plus sign to add strings together. This is called String concatenation.

```
var first = "Hello";
var last = "World";
var else = first + last; //'HelloWorld';
```

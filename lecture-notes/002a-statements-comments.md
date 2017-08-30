# Variables and Arrays
## Introduction
All languages have vocabulary and grammatical rules. That is, the rules that govern how they are interpreted. Javascript is no different. In fact, Javascript, and programming languages in general, have very specific rules that have to be adhered to. If not, the compiler, which is baked into the web browser, cannot interpret your program and will throw an error. 

Speaking of web browser, because your program will run natively in the browser (remember that the Document is simply a sub-object of the Browser Window), your instructions will need to instruct the browser how to interact with the user. Any errors in your program will be caught by the browser. Sometimes the user will see them as well. Other times, we will need to inspect the browser's console to see the errors. 

## Statements
A statement is an individual instruction the computer can follow. For example:

`document.write("Hello World");`

Remember, Document is an object. That object has a method called `write`. That method outputs text to the html file. In this case, it outputs `Hello World`. This is a simple output statement.

Another example is for variable assignmentt, which we will discuss shortly.

`var today = new Date();`

Often, statements are wrapped in conditional logic. Such as..

```
var hourNow = today.getHours();

if (hourNow > 18) {
  document.write("Good Evening!");
}
```

The first line in this script is a condition check. If the condition evaluates to true, the code then runs the second line. We will talk more about conditionals later. For now, let's add some documentation explaining this code. 

```
//set a variable with the current hour of the day
var hourNow = today.getHours();

//if later than 6pm, change greeting
if (hourNow > 18) {
  document.write("Good Evening!");
}
```

This is how you add comments to code. Generally speaking, your comments should be pithy and general. Enough for the person maintaining your code to understand, but not too much to where it overshadows your actual code logic. 

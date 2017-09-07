# Functions
## General
Functions group statements to perform a specific task. In other words, a group of related statements. Here are some key elements of functions:

1. Parameters
2. Return value
3. Typically called or invoked (optional)
4. Uses reserved JS keyword 'function'

Below is an example of a function with an input and a return value. 
```
function multiplyValue(inputValue){
	var value1 = 8;
	return inputValue * value1;
}
```

This function has a name 'multiplyValue' and needs to be called or invoked in your code. You could do this in Javacript, or inside an HTML button. 

```
//Call function from Javascript
multiplyValue(13);

//Call function from HTML
<button onclick=multiplyValue(13)>
```

## Variable Scope
As shown in the `multiplyValue()` function above, functions can have variables. In the case of called functions, those variables are temporary. This means they are only stored while the function is being invoked. This is important since it means they do not use space until they are called. It also has the benefit of being protected from colliding with other variable names that are inside scope. If a variable is declared inside a function with the `var` keyword, it is referred to as a local variable. Variables declared outside of functions are referred to as global variables. Generally speaking, it is best practice to limit the amount of global variables used. 

## Anonymous Functions and Function Expressions
Often we want to use functions as expressions instead of statements. We typically do this when we only want to run code once within a task. Here are some other places we use Function Expressions:

* As an argument when a function is called
* In objects to assign a property's value
* In event handlers/listeners
* To prevent script conflicts

Here is an example of a function expression:

```
var multipliedValue = (function() {
  return 8 * 13;
})
```

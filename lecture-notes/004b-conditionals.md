# Evaluation and Decisions

## Logical Operators

Comparison operators (==, !=, <, >, etc) usually return values of true or false. Logical operators help you evaluate the results of multiple comparisons. 

`((5 > 4) && (4 < 5)) //true`

This statement actually has 4 operands and 3 expressions. You can probably cound the operands, but can you find the expressions? `5 > 4` and `4 < 5` are both expressions. Expression 1 and Expression 2 combine to form a third expression, which in this example, evaluates to true. 

Here are the rest of the logical operators:

Operator | Description 
:---: | :--- 
&& | Tests more than one condition
\|\| | Tests at least one condition
! | Inverts a single boolean value

Also keep in mind that logical expressions are evaluated from left to right, and exit, or short circuit, once the conditional is satisfied. For example, `true || false` stops after the first expression because it is true and the logical or only needs one condition. Here are some other examples:

```
true && true //true
true && false //false
true || false //true
false || false //false
!true //false
!false //true
```

Try to guess if the output is true or false:

```
var score1 = 8;   // Round 1 score
var score2 = 8;   // Round 2 score
var pass1 = 6;    // Round 1 pass mark
var pass2 = 6;    // Round 2 pass mark

// Check whether user passed both rounds, store result in variable
var passBoth = (score1 >= pass1) && (score2 >= pass2);

// Create message
var msg = 'Both rounds passed: ' + passBoth;

// Write the message into the page
var el = document.getElementById('answer');
el.innerHTML = msg;
```
What would you need to change to get the output to change?

## IF Statements

Comparison and logical operators are natural segways into IF statements. These statements check a condition, and execute areas of the program accordingly. See if you can tell what the below if statement is trying to do:

```
var gameActive = true;
var score = 75;    // Score
var msg = '';      // Message

function congratulate() {
  msg += 'Congratulations! ';
}

if (gameActive == true && score >= 50) {  // If score is 50 or more
  congratulate();
  msg += 'Proceed to the next round.';
} else {
  msg += 'Sorry, try again';
}

var el = document.getElementById('answer');
el.innerHTML = msg;
```

How might we modify this for a condition where the score is less than 50?

## Switch Statements

Often a switch statement evaluates (and reads) faster than and if/else statement. See for yourself:

```
switch (level) {
  case 'One':
  title = 'Level 1';
  break;
  case 'Two':
  title = Level 2';
  break;
  default:
  title = 'No title';
  break;
}
```
See if you can read the code above. How might you translate that into an if/else statement?

## Unary Operator

Because of type coercion in Javascript, you can check equality with a single operand. This is called a Unary Operator. For example..

```
var score = 90;

if(score){
  console.log("test has been taken");
}
```
As long as score is set to something other than `(false, 0, '')`, this expression will evaluate to true. Be careful with this mode of conditional checking, because it often leads to unexpected results. For example..

```
var score = '0';

if(score){
  console.log("test has been taken");
}
```
Here, score actually evaluates to true, even though the variable is set to the string '0'. You may or may not desire this result. 


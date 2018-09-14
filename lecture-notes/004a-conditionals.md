# Evaluation and Decisions

## Decision Making and Evaluation

Programs analyze values to determine if they match expected results. Using results, you can decide which path to take. We typically use comparison operators embedded in conditional if/then/else statements to make those decisions. 

```javascript
if (gpa > 3.6) {
  document.write('You made the Dean\'s list');
} else {
  document.write('Try again');
}
```

In the above example we are using `>` comparison operator. There are several others you will often use:

Operator | Description
:---: | :---
== | Checks if values are the same
=== | Checks to see if values and data types are the same
!= | Checks if values are not the same
!== | Checks to see if values and data types are not the same
\> | Checks if one value is greater than another
\>= | Checks to see if one value is greater than or equal to another
\< | Checks to see if one value is less than another
\<= | Checks to see if one value is lesser than or equal to another

In any condition, there is typically one operator and two operands (see below). Operands can be expressions.  
```javascript
//Comparing two operands
'IU' == 'UK' //false
'Hello' == 'Hello' //true

'IU' != 'UK' //true
'Hello' != 'Hello' //false

'3' === 3 //false
'3' === '3' //true

'3' !== 3 //true
'3' !== '3' //false

4 > 3 //true
4 < 3 //false
4 >= 3 //true
4 <= 4 //true

//Comparing expressions as operands
((5+5) > (4+4)) //true

```
What is the output of the following script:

```javascript
var pass = 50;   // Pass mark
var score = 90;  // Score

// Check if the user has passed
var hasPassed = score >= pass;

// Write the message into the page
var el = document.getElementById('answer');
el.innerHTML = 'Level passed: ' + hasPassed;
```

How about now:

```javascript
var score1 = 90;     // Round 1 score
var score2 = 95;     // Round 2 score
var highScore1 = 75; // Round 1 high score
var highScore2 = 95; // Round 2 high score

// Check if scores are higher than current high scores
var comparison = (score1 + score2) > (highScore1 + highScore2);

// Write the message into the page
var el = document.getElementById('answer');
el.innerHTML = 'New high score: ' + comparison;
```

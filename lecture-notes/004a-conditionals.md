# Evaluation and Decisions

## Decision Making and Evaluation

Programs analyze values to determine if they match expected results. Using results, you can decide which path to take. We typically use comparison operators embedded in conditional if/then/else statements to make those decisions. 

```
if (gpa > 3.6) {
  document.write('You made the Dean's list');
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
```
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

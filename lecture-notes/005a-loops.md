# Loops

Loops check a condition, then cycle through a code block. Sometimes they cycle the code a specific number of times, other times the number of cycles is dependent on some other variable. There are three basic types of loops in Javascript:

1. For loop
2. While loop
3. Do while loop

For loops are used when you know the number of cycles you need to perform. While loops are for unknown numbers. Do while loops are the same as while loops, except the condition is checked at the end of the loop instead of the beginning. This is useful if you want the loop to execute a last time before breaking out of the code block. 

## For loops

```
//outputs 0123456789
for (i=0; i < 10; i++){ 
	console.log(i);
}
```

The `i = 0` is the initialization. The `i < 10` is the condition, and the `i++` is the update. We can change the initialization value, the condition, or the update depending on how we want to structure our loop. 


## While loops
```
var colors = ['red','yellow','blue'];
var i = 0;

while (colors[i]) {
	console.log(colors[i]);
	i++;
}
```

Here a while loop is used because the length of colors is uncertain. Initialization occurs outside the loop, the condition is inside the parenthesis, and the update is inside the code block itself. 

## Do while loops
```
do {
    text += "The number is " + i;
    i++;
}
while (i < 10);
```

You can see this is very similar to the while loop, except the code block occurs prior to the condition check. 

## Keywords

### break
Causes termination of the loop and tells the Javascript interpreter to move to the next statement outside the loop.

### continue
Causes the current iteration/cycle of the loop to stop and tests the condition again to see if the loop should continue. 

## Loops and Arrays
As you can see from our colors example, Loops are often used to iterate through a list of array values. 

## Performance
Loops can be a source of performance degradation in your scripts. Each time you drop the CPU into a loop, Javascript execution is effectively stopped while it processes the code block. You always want to be mindful that your loop has an exit condition, thus not creating infinite looping. Also keep in mind how many iterations your loop will process, and maximize it's effeciency in those iterations. And be very careful with loops inside loops. Sometimes they are necessary, but proceed with caution. 

## Examples

### For loop

```
var scores = [24, 32, 17];      // Array of scores
var arrayLength = scores.length;// Items in array
var roundNumber = 0;            // Current round
var msg = '';                   // Message

// Loop through the items in the array
for (var i = 0; i < arrayLength; i++) {

  // Arrays are zero based (so 0 is round 1)
  // Add 1 to the current round
  roundNumber = (i + 1);

  // Write the current round to message
  msg += 'Round ' + roundNumber + ': ';

  // Get the score from the scores array
  msg += scores[i] + '<br />';
}

document.getElementById('answer').innerHTML = msg;

```

### While loop
```
var i = 1;       // Set counter to 1
var msg = '';    // Message

// Store 5 times table in a variable
while (i < 10) {
  msg += i + ' x 5 = ' + (i * 5) + '<br />';
  i++;
}

document.getElementById('answer').innerHTML = msg;
```

### Do while Loop
```
var i = 1;       // Set counter to 1
var msg = '';    // Message

// Store 5 times table in a variable
do {
  msg += i + ' x 5 = ' + (i * 5) + '<br />';
  i++;
} while (i < 1); 
// Note how this is already 1 and it still runs

document.getElementById('answer').innerHTML = msg;
```



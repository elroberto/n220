# Events

An event is a way for the application, more specifically browser in our case, to interrupt an application to react to some input or change in state. In Javascript, you can:

* Create events
* Trigger code in response to events
* Change the application state

## Event Types

* User Interface ex. browser loads the page `load`
* Keyboard ex. user first presses a key `keydown`
* Mouse ex. an element is clicked `click`
* Focus ex. an element loses focus `blur`
* Form ex. user submits form `submit`
* Mutation ex. change made to document `DOMSubtreeModified`

[Listing of all events and supported browsers](https://www.quirksmode.org/dom/events/index.html)

## Things to watch out for

* Non-modern browsers (IE 8 especially) does not support some of the Events functionality demonstrated below
* Passing parameters is a bit different
* 3 ways to call events

## Process

## HTML Event Handler (do not use)

`<button onclick="myFunction()">Click me</button>`

## JS Event Handler (also not recommended)

`element.onevent = functionName;`

### Using Event Listeners
1. Select element (UI events use window object)
2. Indicate event (sometimes called binding)
3. State the code you want to run when the event occurs

```javascript
function checkUsername() {                             // Declare function
  var elMsg = document.getElementById('feedback');     // Get feedback element
  if (this.value.length < 5) {                         // If username too short
    elMsg.textContent = 'Username must be 5 characters or more'; // Set msg
  } else {                                             // Otherwise
    elMsg.textContent = '';                            // Clear msg
  }
}

var elUsername = document.getElementById('username');  // Get username input
// When it loses focus call checkUsername()
elUsername.addEventListener('blur', checkUsername, false);
```

`elUsername` is the element or target. It will listen on the `blur` event. Finally, `checkUsername` should run once the event is fired. 

### Using Event Listeners with Parameters

```javascript
var elUsername = document.getElementById('username');   // Username input
var elMsg      = document.getElementById('feedback');   // Error msg element

function checkUsername(minLength) {                     // Declare function
  if (elUsername.value.length < minLength) {            // If username too short
    // Set the error message
    elMsg.innerHTML = 'Username must be ' + minLength + ' characters or more';
  } else {                                             // Otherwise
    elMsg.innerHTML = '';                              // Clear msg
  }
}

elUsername.addEventListener('blur', function() {        // When it loses focus
  checkUsername(5);                                     // Pass argument here
}, false);
```

Notice `blur` event is bound to an anonymous function, which then calls `checkUsername(5)` with a parameter.

### Using Event Listeners with Event Object

An Event contains data about the event in an object form. This object is passed as a parameter to the event handler. Developers use `e` as the event object variable. 

```javascript
function checkLength(e, minLength) {         // Declare function
  var el, elMsg;                             // Declare variables
  if (!e) {                                  // If event object doesn't exist
    e = window.event;                        // Use IE fallback
  }
  el = e.target || e.srcElement;             // Get target of event
  elMsg = el.nextSibling;                    // Get its next sibling

  if (el.value.length < minLength) {         // If length is too short set msg
    elMsg.innerHTML = 'Username must be ' + minLength + ' characters or more';
  } else {                                   // Otherwise
    elMsg.innerHTML = '';                    // Clear message
  }
}

var elUsername = document.getElementById('username');// Get username input
if (elUsername.addEventListener) {           // If event listener supported
  elUsername.addEventListener('blur', function(e) {  // On blur event
    // NOTE: This function is checkLength() - not checkUsername()
    checkLength(e, 5);                             // Call checkLength()
  }, false);                                       // Capture in bubble phase
} else {                                           // Otherwise
  elUsername.attachEvent('onblur', function(e) {   // IE fallback onblur
    // NOTE: This function is checkLength() - not checkUsername()
    checkLength(e, 5);                             // Call checkLength()
  });
}
```




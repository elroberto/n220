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

## Process

1. Select element (UI events use window object)
2. Indicate event (sometimes called binding)
3. State the code you want to run when the event occurs

```
var divRef = document.getElementById("myDiv");
divRef.addEventListener("mouseover", eventLogger);

function eventLogger(event) {
	console.log("I've been found!");
} 
```

`divRef` is the element or target. It will listen on the `mouseover` event. Finally, `eventLogger` should run once the event is fired. 

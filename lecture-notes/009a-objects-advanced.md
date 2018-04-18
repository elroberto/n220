

# Return values
A returned value is publicly available

```javascript
function getValue() {
	var a = 10;
	return a;
}
```

In the above function, `a` is a private variable, but it can be accessed through the return. 

```javascript
var myValue = getValue(); 
console.log(myValue); //outputs 10
```

You can also return an object, function, or multiple functions with return values. 

```javascript
function getObject(){
	var myObj = {
		'key1':'val1',
		'key2':2 
	}
	return myObj;
}

var myObject = getObject();
console.log(myObject); //{'key1':'val1', 'key2':2}


function getFunction(){
	var myFunction = function(){
		console.log('i am a private function');
	}
	return myFunction;
}

var myFunction = getFunction();
console.log(myFunction); //outputs function(){ console.log("im a private function"); }

function getFunctions(){
	var myFunctions = {
		'function1': function() {
			console.log('private function 1');
		},
		'function2': function() {
			console.log('private function 2');
		}
	}
	return myFunctions;
}

var myFunctions = getFunctions();
console.log(myFunctions); //{func1: function(){ console.log("private function 1")}, func2: function(){ console.log("private function 2") }}

```

# Objects and Privacy

Objects are fundamental to Javascript. Arrays, Functions and Objects (obviously) are Objects. Objects are simply key/value pairs. Key names are strings, values are strings, numbers, booleans, and objects (including arrays and functions). Values that are functions are methods. When a method is invoked, `this` variable is set to the instance value of the object.  

* Public
	* Contructor
	* Prototype
* Private
* Privileged

```javascript
function Container(name) {
	this.appName = name;

	function dec(){
		if (secret > 0) {
			secret -= 1;
			return true;
		} else {
			return false;
		}
	}

	var secret = 3;
	var that = this;

	this.service = function() {
		return dec() ? that.appName : null;
	}
}

Container.prototype.stamp = function(){
	return 'app name ' + this.appName;
}

var testModule = (function() {
	var counter = 0;
	return {
		incrementCounter: function(){
			return counter++;
		},
		resetCounter: function (){
			console.log('counter value reset to ...' + counter);
			counter = 0;
		}
	};
})();
```

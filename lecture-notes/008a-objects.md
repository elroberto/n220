# Objects

A complex data type in Javascript, an object is a grouping of properties (variables) and methods (functions) to create a model of something.

* Properties - variables that belong to an object
* Methods - functions that belong to an object

Both properties and methods have a name value called a **key**. The value of a property is always one of (String, Number, Boolean, Array, Object). The value of a method is always a function(). 

```javascript
var hotel = {
  name : 'Quay',
  rooms : 40,
  booked : 25,
  checkAvailability : function() {
    return this.rooms - this.booked; // Need "this" because inside function
  }
};
```

The keyword `this` is used to reference properties inside the object. You may also see `this` used to reference properties in global object scope (ex. `this.innerWidth` references the window object's width).

There are two ways to access an objects properties / methods: Dot notation and Constructor notation. 

## Dot Notation

```javascript
// Update the HTML
var elName = document.getElementById('hotelName'); // Get element
elName.textContent = hotel.name;                   // Update HTML with property of the object

var elRooms = document.getElementById('rooms');    // Get element
elRooms.textContent = hotel.checkAvailability();   // Update HTML with property of the object
```

## Constructor Notation

```javascript
// Update the HTML
var elName = document.getElementById('hotelName'); // Get element
elName.textContent = hotel['name'];                   // Update HTML with property of the object

var elRooms = document.getElementById('rooms');    // Get element
elRooms.textContent = hotel['checkAvailability']();   // Update HTML with property of the object
```

You can also create an object using the Constructor Notation:

```javascript
var hotel = new Object();

hotel.name = 'Park';
hotel.rooms = 120;
hotel.booked = 77;
hotel.checkAvailability = function() {
  return this.rooms - this.booked;  
};
```

Sometimes you want to create several objects with the same prototype. You can use the Constructor notation to accomplish this:

```javascript
// Create the template for objects that are hotels
function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function() {
    return this.rooms - this.booked;
  };
}


// Create two hotel objects
var quayHotel = new Hotel('Quay', 40, 25);
var parkHotel = new Hotel('Park', 120, 77);


// Update the HTML for the page
var details1 = quayHotel.name + ' rooms: ';
    details1 += quayHotel.checkAvailability();
var elHotel1 = document.getElementById('hotel1');
elHotel1.textContent = details1;

var details2 = parkHotel.name + ' rooms: ';
    details2 += parkHotel.checkAvailability();
var elHotel2 = document.getElementById('hotel2');
elHotel2.textContent = details2;
```


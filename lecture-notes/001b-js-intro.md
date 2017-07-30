# Intro to Programming w/ Javascript

## What is a script?

Series of instructions (e.g. recipe)

## High Level Functionality

1. Access Content
2. Modify Content
3. Program Rules
4. React to Events

## Objects and Properties

Objects are models of things in the real world. In Javascript, objects can have properties, events, and methods. Here is a sample object:

Object Instance | Car
---- | ----
Make | BMW
currentSpeed | 30mph
color | silver
fuel | diesel

It is important to note that BMW is not the object. Car is the object. We can have multiple cars that use the same model as the BMW car. They each have a Make, currentSpeed, color, fuel, but they are different instances of that object. An instance of an Object is an implementation of that object's properties for another thing. 

## Events

In Javascript, Objects can have Events. Events are ways users interact with Objects. From a computational perspective, an Event is a way for the user to interrupt processing to do something else. If we stick to our Car object example from before, we can imagine a couple of events that may be useful. 

Event | Action
---- | ----
brake | car slows down
accelerate | car speeds up

## Methods

Object methods are used to encapsulate similar chunks of programming logic. Typically they are used to get or set object properties, or manipulate the object in some other way. Let's create methods for our brake and accelerate events. 

Method | Action
---- | ----
changeSpeed() | Increases or decreases currentSpeed property

1. As the driver speeds up in our `Car` object, the `accelerate` event fires. 
2. The `accelerate` event calls `changeSpeed()`, which increases the value of the `Car::currentSpeed` property
3. The value of the `currentSpeed` property reflects how fast the car is traveling

## Web Browser as Object

The web browser is an instance of a `Window` object you will interact with many times as a programmer. 

Object Instance | Window
---- | ----
Location | http://google.com

## DOM

The web browser loads a location, which then builds a `Document` object. 

Object Instance | Document
---- | ----
URL | http://google.com
lastModified | 07/20/2017 10:13:00
title | Google.com

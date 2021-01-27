#Object-Oriented Programming, HTML Tables,
Domain Modeling - From the Duckett HTML book:Chapter 6: 
“Tables” (pp.126-145);

+ A table represents info in a grid format.
+ The  <table> element is used to add tables to a webpage; a table is drawn out row by row. Each row is created with the  <tr> element. Inside each row there are a number of cells represented by the  <td> element. (or <th scope="col" OR +"row"> if its a header). 
+ You can make cells of a table span more than one row or column using the  <td rowspan="2"> and  <td rowcolumn="2"> attribute. for long tables U can split the table into a  <thead>, <tbody> and  <tfoot>.

+ From the Duckett JS Book - Chapter 3: “Functions, Methods, and Objects” (pp.106-144);

### Creating an Object Constructor Notation

     var hotel = new Object();
hotel.name: 'Quay';
hotel.rooms: 40;
hotel.booked: 25;
hotel.gym: true;
hotel.roomTypes: ['twin', 'double', 'suite'];
hotel.checkAvailability = function() {
    return this.rooms - this.booked;
  };

to update a property
hotel.name = 'Park'; OR
hotel['name'] = 'Park';
to delete a property
delete hotel.name;
hotel.name = ''; // to clear value

### Creating Many Objects Constructor Notation

     function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function() {
    return this.room - this.booked;
  };
}
var quayHotel = new Hotel('Quay', 40, 25);
var parkHotel = new Hotel('Park', 140, 55);

### This - keyword
its scope and meaning depends on how it is used; local inside a function, inside an object, or global.
### storing Data
in Variables
+ Arrays
+ individual Objects
+ multiple objects (object creator function)
+ Arrays are objects with index numbers  [0] as individual properties - ARRAYS SEQUENCE IS IMPORTANT / STORED
+ Arrays inside an object Objects inside an Array
###Built in Objects

+ Browser Object
+ Document Object DOM
+ Global Javascript Object

## Summary
+ Functions allow you to group a set of related statements together that represent a single task.
+ Functions can take parameters (info required to do their job) and may return a value.
+ An object is a series of variables and functions that represent something from the real world around you. The selection of their describing keys is about what is important to store/define/use/know/ and use on a webpage.
+ In an object variables are known as properties of the object, functions are known as methods of the object.
+ Web browsers implement objects that represent both the browser window and the document loaded into the browser window.
+ JavaScript has several built in objects, such as String, Number, Math, Date. Their properties and methods offer functionality that helps you write scripts. List on page 128.
+ Arrays and Objects can be used to create complex data sets and both can contain each other.

## Domain Modeling

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

Define a constructor and initialize properties To define the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation of an EpicFailVideo object.

Property Data Type epicRating 1 to 10 Number hasAnimals true or false Boolean Here's an implementation of the EpicFailVideo constructor function.

     var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

EpicFailVideo.prototype.dailyLikes = function() {
  var viewers, percentage;

  viewers = this.generateRandom(10, 30) * this.epicRating;

  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }

  return Math.round(viewers * percentage);
}

EpicFailVideo.prototype.weeklyLikes = function() {
  var total = 0;

  for (var i = 0; i < 7; i++) {
    total += this.dailyLikes();
  }

  return total;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.weeklyLikes());
console.log(corgiFail.weeklyLikes());

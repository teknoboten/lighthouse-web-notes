# Object Oriented Programming

when we program in an object oriented way it:
  - reduces repetition 
  - makes our code more modular (and reusable, which === less code to write)
  - uses *objects* 

oop !== functional programming

js is not *strictly* oo - it also supports functional programing



## object terminology

objects are:
  - collection of key / value pairs which are also called *properties*
  - the properties represent the object's *state*
  - when the property value is a function, it's called a method
  - methods provide the object's *behaviour*


### this
  - it's a keyword
  - context matters
  - the value it represents depends on how and where it was called
  - usually we will use it inside an object's method 


## best practices
  - functions should only affect things within their own scope
  - this reduces risk of unintentially modifying other things

### disclaimer
  - js isn't necessarily the best language to learn oop with 
  - it may not be the best, but it's the one we've got


## a note / disclaimer / fyi about js classes
  - classes are a *key* and *v popular* feature in oop
  - js objects are based on *prototypes*, not classes
  - support for classes was added in js es6 
  - this didn't add any functionality, just different syntax
  - old code will use prototpyes but that's the old and busted way to do it
  - that said, we will still have to understand them eventually
  - so just know that this is currently a _gap_ we have in our knowledge



  # Classes

  - they are a blueprint / *template* we use to make new *instances* of an object
  - use the **new** keyword when we create a new object instance using a class


```javascript

class Pizza {

  constructor() {
    this.toppings = ["cheese"];
  }

  addTopping(topping) {   //<- this is a method
    this.toppings.push(topping);
  }

}

let pizza1 = new Pizza();

Pizza.addTopping();       //<- this won't work, bc methods are only availble on the actual instances we create with the pizza class

pizza1.addTopping("pineapple");

console.log(pizza1.toppings); //returns [ 'cheese', 'pineapple' ]

```

  - classes are capitalized
  - should be a noun


## constructor

a *constructor* is a special kind of method that is executed when a new instance of our class is created

  - we can use this to set default values for any new instance of the objects's properties



### primitives as objects

  - primitives have constructors but... don't use them



# inheritance

- create new classes based on existing classes 
- limits duplication between classes
- uses the keyword **extends**

*example:*
student and mentor are both people, so we create a person class that includes the states / properties / behaviours / methods that are shared between thee. then we extend the person class.

```javascript 

class Person {

  constructor(name, age, funfact) {...} // all people have these props
  
}

class Student extends Person {

  enroll(class) { this.program = program }  //specific to students

}

class Mentor extends Person {

//other stuff specific to mentors
}

```


  - methods on the parent class are available to the child classes
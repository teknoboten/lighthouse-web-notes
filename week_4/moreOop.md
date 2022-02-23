# ooooops super

### method overide

  if we want to change the functionality of a method that exists in the parent class so that the child class behaves differently, we can use a *method override*


```javascript

//superclass
class Person {

  constructor(name, age, funfact, email) {
    this.name = name;
    this.funfact = funfact;
  }
  bio(){
    return `hi, my name is ${this.name} and ${this.funfact}`;
  }
}

//subclass #1
class Student extends Person {
  enroll(cohort) {
    this.cohort = cohort;
  }
}

//subclass #2 which has a method override of the parent class bio() method
class Mentor extends Person {
  bio(){
    return `i am a mentor at lighthouse labs. my name is ${this.name} and ${this.funfact}.`
  }
}
```

this works ok but isn't **the best**

we can d.r.y up this code with the *super* keyword:


```javascript

class Mentor extends Person {
  bio() {
    return `I'm a mentor at Lighthouse Labs. ${super.bio()}`;
  }
}
```




# getters and setters

getters and setters let us be more *idiomatic* aka we can talk like people.

behind the scenes, the keywords *get* and *set* bind an ojbects proberty to a function

but WHY????

  - lets us validate data before assigning it 
  - compute the value as needed instead of storing it (bc its more fun to compute) 
  - gives us our object a nicer interface

example:

```javascript

  get price() {
    const basePrice = 10;
    const toppingPrice = 2;
    return basePrice + this.toppings.length * toppingPrice;
  }

  set size(size) {
    if (size === 's' || size === 'm' || size === 'l') {
      this._size = size;
    }
  }
}
  ```


# Dependancy Injection

  - a fancy way to say "we are passing an object the data it needs rather than making the object get that data for us" 
  **- a great design patttern!**
  


# goals / benefits of OOP

**abstraction**
  - we don't need to know how a car works in order to drive it
  - keep the more complex stuff out of the way

when we do this correctly, it makes it easier to make small changes to our code without having to refactor the whole thing

  example: adding pizza toppings
    - addTopping("cheese") 
    - instead using pizza.toppings.push("cheese") 



## single responsibility

  - a class should only have one reason to change
  - a class should only ever have one job
  - we use *inheritance* to reduce duplicate code


## property value shorthand

  when defining an object, you don't need to define the key if you are passing in variables that have the same name / value as the desired property

const x = 4;
const y = 1;
const obj = { x, y };

# Objects 

**Everything that is NOT a primitive, is an object**

Things that are not objects:
1. String
2. Boolean
3. Number
4. null
5. undefined
6. Symbol
7. BigInt


Symbols
- we won't use symbols much
- they are always unique (s
- we might use this when constructing objects
- just don't think about them
- used when optomizing for performance

Bigint
- bigInt 
- number data type has an upward limit and will die
- probably won't come up when you're using javascript 
- more likely to do work like this in lower level language (c, python)

Null / Undefined 
- these both mean nothing

Undefined
- this variable has not been given a value yet (unintentional)

Null
- intentioanlly nothing


## Objects ##

Mainly used to store data

*Accessing data*

can access data 2 ways

- dot or square bracket notation
- can't use a variable with dot notation
- use square bracket notation!! 


```javascript
const person = {
  name: "serra",
  location: "squamish"
}

let keys = ["name", "location"];
for (const property of keys) {
  console.log(person[property]);
}

```

### Calling Functions 

*With primitives*

NOTE: primitives in js are **passed by value**

when we call a function with a primitive variable, the function will only update the COPY passed to the function

*With Objects*

Note: objects are **passed by reference**

this means if we call a function using an *object* as a parameter, the function recieves the actual variable (not a copy)



## Object Methods 

Objects can store functions! we call them methods!

the keyword **this** lets us access the data within the object

we can add things during the object declaration OR we can also add them after


```javascript
const car = {
  name: "morty";
  fuelLevel: 0,
  maxFuel: 100,
}

const refuel = () => {
  //some function using this.keyword
  const amountOfFuel = this.maxFuel - this.fuelLevel
  return amountOfFuel;
}

car.refule = refule;

console.log(car.refule());
```

# Looping over objects

const destinations = ['vancouver', 'toronto', 'montreal'];

Note: use a for... in loop
  - the for...in loop gives you access to the *keys* 
  - for..of will not give you the keys

  **hashmap**

  - sometimes an object is not called an object
  - key / value stores 


# Think about the future

















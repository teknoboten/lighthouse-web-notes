# Week 2

## Primitave Data Types
1. String
2. Number
3. Boolean
4. Null
5. Undefined
6. Symbol

*Everything* else is an object. Even things like: dates

## A lot of things about objects

- they are made up of key / value pairs
- the key is *almost* always a string 
- the value can be either a primitive OR an object

```javascript

> person["address"]["street"]

```

use Object.keys() to access... the keys

### Iteration using (for...in)[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in]

- we can't iterate over the values of an object in the same way as an array
- we can use a *for...in* statement instead

```javascript 
var planetMoons = {
  mercury: 0,
  venus: 0,
  earth: 1,
  mars: 2,
  jupiter: 67,
  saturn: 62,
  uranus: 27,
  neptune: 14
};

for (var planet in planetMoons) {
  var numberOfMoons = planetMoons[planet];
  console.log("Planet: " + planet + ", # of Moons: "+ numberOfMoons);
}
```

note: some unexpected results can happen when there are inherited properties
- sometimes an additional filtering step is necessary 


## Functions as Objects

Functions are *first class* objects
  - they can be stored as variables
  - they can do everything other objects can do (like have properties)

*runner functions*

*callback function*
  - this is a function that is passed into another ("reciever") function 
  - often used while iterating through arrays with forEach
  - allow us to pass **behaviour** between functions 


## Anonymous (callback) Functions

  - callback functions are often defined anonymously inline in the reciever function 
  - the reciever function will give that parameter a name anyway

  ## Arrow Functions

(fun fun function)[https://www.youtube.com/watch?v=6sQDTgOqh-I]

"because they are so terse, we can use functions in a new way"

we can create functions that are: 

    1. small
    2. inline
    3. single-purpose

note: they don't get a value assigned for *this*

all three of these are the same:

```javascript
x => x * 2;

(x) => { return (x * 2); };

function (x) { return (x * 2); }
```

# (Higher Order Functions)[https://www.youtube.com/watch?v=BMUiFMZr7vk]

Any function that operates on other function is considered a *higher order function*
  - this includes functions that use callbacks
  - also includes built in functions like forEach, filter etc

  Note: Higher order functions are a big part of *functional programing*

  "functions are not even real" -*niko*


.filter - loops through the array and passes each element to the callback function

# MAP

- goes through an array and transforms each element using a callback function!
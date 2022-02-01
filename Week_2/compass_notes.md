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


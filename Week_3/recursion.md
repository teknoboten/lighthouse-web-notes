# Object Methods and 'this'

*Assign a function as an object property*

```javascript
const person = {
  firstName: 'Rufus',
  middleName: 'Red',
  lastName: 'Grant',
}

console.log(`hello, ${person.firstName} ${person.lastName}!`);
```

We can refactor this to make it easier to greet our person:

```javascript
const person = {
  firstName: 'Rufus',
  middleName: 'Red',
  lastName: 'Grant',
  fullName: function() {  
    return this.firstName + ' ' + this.lastName;
}

console.log(`hello, ${person.fullName()}!`);
```
This is called a **method**

# .This 

- it's complicated
- normally refers to the object it was called on

# Recursion 

- is an alternative to using a loop
- is a function that calls itself until it doesn't (stop condition is met)
- it is a type of *control flow*



```javascript

//don't do this (infinite loop):
const sayHelloForever = (num) => {
  console.log(`hello, ${person.fullName()}!`);
  sayHelloForever(num+1);
}

sayHelloForever(0);
//returns: RangeError: Maximum call stack size exceeded

//instead
const sayHelloTenTimes = (num) => {
  if (num < 10){
    console.log(`hello, ${person.fullName()}!`);
    sayHelloTenTimes(num+1);
  }
}
sayHelloTenTimes(0);

```

*recursive case*    
num <= 10

if this is true, the function will continue

*base base*
num > 10

if this is true, the function will NOT call itseld 

note: a function must have one of each of these in order to be recursive!

### Writing a recursive function

- start by defining the base and recursive case

## When to use recursion??

- if the problem you are trying to solve is just a smaller version of the problem you have already solved, you can use recurion instead of a loop
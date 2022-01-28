# Mod 1 Notes

Not sure how I feel about taking notes this way but here goes. 

## Understanding Problems with Pseudocode 
##### (sudocode??? lol)

**Understand the problem**

- what are the inputs / "ingredients" of our problem?
- what is the desired output? 
    - if the desired output is not known, try calculating a bit of it by hand to identify patterns
    - this helps us determine if it's even possible / makes sense, given the known info, which can help us avoid wasting time on impossible / the wrong question
    - sometimes people who don't know how computers work ask us to solve the wrong thing

**Use PsuedoCode**
  - separate the 'what' from the 'how'


## Function Best Practices

[Reference](https://eloquentjavascript.net/03_functions.html#h_eVDWIAuyBK)

**Growing Functions**
  - if you can't easily come up with a good name for a function, you might need to further clarify your concept
  - resist the urge to be unnecessarily clever, unless you're going to need it

example:

instead of:

```javascript
function printZeroPaddedWithLabel(number, label) {
  let numberString = String(number);
  while (numberString.length < 3) {
    numberString = "0" + numberString;
  }
  console.log(`${numberString} ${label}`);
}

function printFarmInventory(cows, chickens, pigs) {
  printZeroPaddedWithLabel(cows, "Cows");
  printZeroPaddedWithLabel(chickens, "Chickens");
  printZeroPaddedWithLabel(pigs, "Pigs");
}

printFarmInventory(7, 11, 3);
```

do this:

```javascript

function zeroPad(number, width) {
  let string = String(number);
  while (string.length < width) {
    string = "0" + string;
  }
  return string;
}

function printFarmInventory(cows, chickens, pigs) {
  console.log(`${zeroPad(cows, 3)} Cows`);
  console.log(`${zeroPad(chickens, 3)} Chickens`);
  console.log(`${zeroPad(pigs, 3)} Pigs`);
}

printFarmInventory(7, 16, 3);
```

**Functions and Side Effects**

- We call functions either for their *side effects* or *return value*
- Sometimes both
- Functions that create values are easier to reuse

A *pure* function produces no side effects and has no dependancies 
  - That does not necesarily mean that *nonpure* functions are always bad

**Naming Functions**

- name your functions beginning with *action words* like createUser, or sendUserData
- use camelCase

**Pass in the Data Needed**
- Ideally, functions should not read outer scoped variables
- Instead, that data should be passed in as a parameter 

This makes our functions more reusable! ✅

```javascript
const person = "Martha";

// BAD
const sayHelloBadly = function() {
  console.log(`Howdy, ${person}`);
}
sayHelloBadly(); // Works, but not ideal!

// GOOD
const sayHelloGoodly = function(name) {
  console.log(`Howdy, ${name}`);
}
sayHelloGoodly(person);
```


# Test Driven Development 

"this is all just words" -*ian*


- import / export 
- every file has a built in module object
- module.exports starts out as an empty object
- we can assign things to it 
- that gives other js files access 
- we can now import those functions into other files using 'require'
- common import

```javascript
console.log(module);

//test.js
const someFunction = () => {...};
module.exports = { someFunction, }

//file 2
const { someFunction } = require('test');

```


# Mocha

- it is a test runner
- install it with npm 

*describe*  and  *it*

- we need to learn to read project specifications and use words to describe what we want our code to do

javascript has it's own built in assertion library that we import 

```javascript

//test.js

describe('test the numVowels function', () => {
  it('always returns an integer', () => {
    const actual = numVowels();
    assert.strictEqual(typeof(actual), "number");
  })
  it('return 0 for a word with no vowels', () => {
    const actual = numVowels();
    assert.strictEqual(actual, 0);
  });
  it('return 0 for an empty string', () => {
    assert.strictEqual(numVowels('orange'), 3);
  })

});

//numVowels.js

function numVowels (str) {
  const vowels = [];
  let count = 0;

  for (const character of str )
    if(vowels.includes(character)) {
      count += 1;
    }
    return count;
}

```

ask yourself: 
what is the simplest code we can write to make the tests pass?

the happy path: 
tests that ... make us happy?

better example: 

```javascript

 it('support upper/ lower case', () => {
    assert.strictEqual(numVowels('Apple'), 2);
  })

```

- when we want to add functionality, we can write a test to make sure we dont' add *regression errors*


# Problem decomposition

- break a big problem down into smaller problems
- this is **very important**



## (Chai)[https://www.chaijs.com/]

- it's an assertion library 
- use this instead of the built in js assert 

should / expect / assert
- it's syntax sugar

npm i chai from the project root dr

const { expect } = require('chai'); 
- in the test file

- call it with *npm test*


*functions can be tested if:*

- it has side effects (operates on an object)
- it returns a value (even if it doens't have side effects)

note:  console.log statements are not (practically) testable


cast input to a string: 
String(input)



# defensive programming

- write code that can't be accidentally broken or misused
- example: use const instead of let 


**array destructuring:**

const data = [1, 2];
const digits = data[0];
const times = data[1];

can be written as: 

const [digits, times] = [1, 2];
- creates const with the given names and assigns the value of the coordinating element

combine it with a for loop:

for (const [digits, times] of data) {
  let accum = [];
  accum += repeatOne(digits, times);
  return accum.join(', ');
}

## Behaviour Driven Development

- code specifications are written in such a way that test code can be automatically parsed into tests
- rarely used in practice

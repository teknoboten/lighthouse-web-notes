# Week 1 technical lecture notes

use for of 

```javascript
for (const num of nums) {
  console.log(num)
}
```
instead of oldschool for loops!!

```javascript

let sum = 0;

for (const num of nums) {
  sum += Number(num);
};

```

use the Number function instead of parseInt?

note: NaN typeof === number (bc js was written by a crazy person)
note: NaN !== NaN
note: there's a isNaN function, use that!

## continue
use continue; to skip a value when interating over an array

## isInteger 
checks... if something is an integer 
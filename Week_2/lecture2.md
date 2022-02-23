
# Arrow Functions
- you can't use arrow functions when you define methods!!!

*use filter to check for capitals:*
  - capitalize the first letter and then compare it to the actual first letter
  - if this returns true, the name is added to the new array
  - otherwise it's skipped


```javascript 
const properNouns = ["cat", "David", "creek", "Stevie", "car"].
  filter(name => name[0].toUpperCase() === name[0]);
```

- filter
- map
- forEach <- don't use this
- reduce  <- is the best

# Reduce! 

*lots of stuff learn about this*
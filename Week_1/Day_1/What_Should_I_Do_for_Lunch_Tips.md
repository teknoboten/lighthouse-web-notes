### Tips

Try experimenting with the comparison operators (`<`, `>`, `===`, etc.) in the node REPL, which you can launch using the `node` command in Vagrant.

Work on your code iteratively – that means in small pieces. 

To help you figure out how to use `hungry` and `availableTime` inside your function, try outputting their values to the Terminal as follows.


```javascript

const whatToDoForLunch = function(hungry, availableTime) {
  if (!hungry) {
    console.log("Get back to work already!");
  } else if (availableTime < 20) {
    console.log("Grab a quick snack in the lab!");
  } else if (availableTime >= 20 && availableTime <= 30) {
    console.log("Go on then, try new place!");
  } else if (hungry && availableTime > 30) {
    console.log("Don't kid yourself, you're in bootcamp, not on vacation!");
  }
};
```
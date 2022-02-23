# async  programming

when part of the code runs separately from the main thread and lets the main thread know when it's done.

ex: preparing for a party, you send your friend to get cups and ask them to let you know when they're done, so you can keep getting things ready. if this was being done synchronously, you would be "blocked" and have to just sit there and wait for your friend to come back, which is annoying and inefficeint. 

-> i/o (reading / writing to disk / network) are time consuming tasks that are best to offload to a secondary queue so the rest of the application can continue to run without having to just sit there and wait

## async callbacks

- not all apis we encounter support synchronous functions so we have to understand async
- we can't alway predict in what order async functions will complete
- there are different methods for async flow control! (promises, async / await)

**user events** -> can occur at any point, so we need to be able to handle them asynchronously! 

process.stdin / process.stdout -> deal with standard input / output

*process.stdin.on* <- registers a callback

(*node readline module*)[https://github.com/nodejs/node/blob/master/doc/api/readline.md]
  - reads one line at a time, from any input stream
  - we will use stdin 




# async return values (aka callbacks!)

-> *synchronous* functions can return data but **async functions cannot**

instead, async functions will pass their returned data to the provided *callback function*, which will do whatever we want with the data.

aka:

```javascript

//sync function
return data;

//async function
callback(data)

```

this is because a synchronous function will finish executing *before* we get our data back, so it's impossible for the function to return this data. 

so instead, we give it a callback and say, hey, when the data gets back, you do your thing, and i'll just keep doing my thing over here.




# async programming

note: **javascript is single threaded**

aka 
  - the js runtime is not asynchronous so we have to fake it 
  - it's all a facade 
  
*interleving*
  - switching between tasks to make it seem like it is async

*blocking* 
  - all js blocks other code from running unless it is explicity designed to be async

*js primary execution environment*
  - where most code lives
  - synchronous

*js callback queue*
  - secondary environment
  - async functions go here to run in the background
  - long running functions are pushed off the primary environment and stored in the callback queue
  - 
  
js will use interleving to switch between the primary exec and callback queue 

there is *always* a callback

## set timeout

setTimeout(() => {
  console.log('third')
}, 1000 );

adds the callback to the after 1 second

## fs

  - low level package 
  - node package
  - lets us interact with the fs 
  
  fs.readFile
      - defaults to async
      - reads the data once the filesystem has completed 
      - the callback is what happens AFTER the synchronis




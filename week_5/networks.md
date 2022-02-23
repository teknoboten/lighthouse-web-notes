# networking

**net** node module lets us use tcp
  
**.on**
  
  - lets expects an event name and function that should be executed when that event happens

  conn.on("event name", () => {
  // code that does something
});

  - must use event names as defined by node
      -> "connect" is executed when a successful connection is made
      -> other events include.... disconnect? error? 


*event handler* defines what to do when an event occurs



# HTTP

is text based / human readable

requests include:
  path: url
  method: (GET / POST / PUT / DELETE / etc)


responses include:

  code: 400 - user screwed up  500 - server screwed up
  body: resource that was requested (ideally)


headers (both request and response) contain key-value pairs of information


# request 

node module that uses http / net to request stuff
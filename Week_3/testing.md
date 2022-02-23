# automated testing

- the practice of writing code to programatically test the actual code we want to write
- saves testing / debugging time
- makes it easier to program 
- makes it easier to come back to code after a while
- makes us think harder / better / (faster / stronger) about our code 


## types of testing

**unit testing**
- focuses on on small bits of code, ie induvidual functions
- if the code relies on a database or network, it's not a unit test
- should be simple. if they're hard, your code might be bad
- great for preventing regressions
- mocha

**integration testing**
- tests how the code integrates with the rest of the system
- more complex to write / set up than unit tests
- may require complicated test environments


**funtional / E2E testing**:
- tests the complete functionality of an application
- for web dev it will include an automated browser
- can be difficult / complex to set up and maintain 
- should be used to test common user interactions
- selenium / phantomJS / casperJS
- 80% of testing should be off the happy path / 20% on


### get off (the happy path)[https://effectivecio.com/2009/11/02/the-happy-path/]

*happy path* is when the user experience works as desired



# bdd (behaviour driven developement) 

- we think about our app's behaviour in terms of user stories
- stories can be broken down into testable scenarios

**mocha**
- it's delicious
- also a testing framework

**chai**
- it's an assertion library
- also delicious


install mocha with the --save-dev flag makes it a (development dependency)[https://nodejs.dev/learn/npm-dependencies-and-devdependencies]

dependancy: package is listed as a dependancy in package.json 
devDependency: added to the devDependencies list in package.json
  -> these are packages required for dev, not production (ie, testing)
  -> you can use the --production flag to install without devDependancies

  

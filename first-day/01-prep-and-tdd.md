# 20-2-2022- First class reading notes:

## Async/Await Function:

**Aynchronous** :which means that it has an event loop that allows you to queue up an action that won’t take place until the loop is available.
It simply allows us to write promises based code.

**Await**:
Await function is used to wait for the promise. It could be used within the async block only. It makes the code wait until the promise returns a result. It only makes the async block wait.

## Promises:

are used to handle asynchronous operations in JavaScript.

#### Benefits of Promises 

1. Improves Code Readability
2. Better handling of asynchronous operations
3. Better flow of control definition in asynchronous logic
4. Better Error Handling

#### A Promise has four states: 

1. **fulfilled:** Action related to the promise succeeded
2. **rejected:** Action related to the promise failed
3. **pending:** Promise is still pending i.e. not fulfilled or rejected yet
4. **settled:** Promise has fulfilled or rejected

#### Example:
var promise = new Promise(function(resolve, reject) {
  const x = "geeksforgeeks";
  const y = "geeksforgeeks"
  if(x === y) {
    resolve();
  } else {
    reject();
  }
});
   
promise.
    then(function () {
        console.log('Success, You are a GEEK');
    }).
    catch(function () {
        console.log('Some error has occurred');
    });

#### Promise Consumers

Promises can be consumed by registering functions using .then and .catch methods.

1. **then()**
then() is invoked when a promise is either resolved or rejected. It may also be defined as a career which takes data from promise and further executes it successfully.

2. **catch()**
catch() is invoked when a promise is either rejected or some error has occurred in execution. It is used as an Error Handler whenever at any step there is a chance of getting an error.

## Callback Functions:

 functions are objects. we can also pass functions as parameters to other functions and call them inside the outer functions. 
    const message = function() {  
        console.log("This message is shown after 3 seconds");
        }
        setTimeout(message, 3000);

 **Anonymous Function**:
    setTimeout(function() {  
        console.log("This message is shown after 3 seconds");
    }, 3000);

**Arrow Function**:
    setTimeout(() => { 
        console.log("This message is shown after 3 seconds");
    }, 3000);

## Test-Driven Development

#### Testing:

1. Testing is verifying our application does what it should.
2. There are two types of tests: manual and automated.
3. Tests assert that your program will behave a certain way. 
4. Then the test itself proves or disproves that assertion.
   
#### Test-Driven Development
Test-driven development is the act of first deciding what you want your program to do (the specifications), formulating a failing test, then writing the code to make that test pass. It is most often associated with automated testing. Although you could apply the principals to manual testing as well.
**With TDD, test logic precedes application logic.**
**Project setup**

1. Create an NPM project: npm init.
2. Create id.js and add it to the project’s root.
3. Install Jest: npm install jest --D
4. Update the package.json test script

**How Do We Write a Test?**
Tests are just functions that receive a couple of arguments. We can call our test with either it() or test().
*Recap*
Jest is a testing suite and has a built-in assertion library.
A test is just a function whose arguments define the test.
Specifications define what our code should do and are ultimately what we test.
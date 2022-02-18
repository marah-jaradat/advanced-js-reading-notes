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
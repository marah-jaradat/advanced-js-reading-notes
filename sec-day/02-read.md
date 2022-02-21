# 21-2-2022- Second class reading notes:

## Writing middleware for use in Express apps:

**Middleware** functions are functions that have access to the request object (req), the response object (res), and the next function in the application’s request-response cycle. The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware.

*Middleware functions can perform the following tasks:*

1. Execute any code.
2. Make changes to the request and the response objects.
3. End the request-response cycle.
4. Call the next middleware in the stack.

**Some of middleware functions:**

1. Middleware function myLogger: This function just prints “LOGGED” when a request to the app passes through it.
*Types of express middleware*

- Application level middleware (app.use)
- Router level middleware (router.use)
- Built-in middleware (express.static,express.json,express.urlencoded)
- Error handling middleware (app.use(err,req,res,next))
- Thirdparty middleware (bodyparser,cookieparser)

    **Example**
        const myLogger = function (req, res, next) {
        console.log('LOGGED')
        next()
        }

        app.use(myLogger)

        app.get('/', (req, res) => {
        res.send('Hello World!')
        })

1. Middleware function requestTime: the app now displays the timestamp of your request in the browser.

    **Example**
        const requestTime = function (req, res, next) {
        req.requestTime = Date.now()
        next()
        }

        app.use(requestTime)

        app.get('/', (req, res) => {
        let responseText = 'Hello World!<br>'
        responseText += `<small>Requested at: ${req.requestTime}</small>`
        res.send(responseText)
        })

2. Middleware function validateCookies: validates incoming cookies and sends a 400 response if cookies are invalid.
   **Example**
        const cookieValidator = require('./cookieValidator')

        const app = express()

        async function validateCookies (req, res, next) {
        await cookieValidator(req.cookies)
        next()
        }

        app.use(cookieParser())

        app.use(validateCookies)

        // error handler
        app.use((err, req, res, next) => {
        res.status(400).send(err.message)
        })

## Clases

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.
*Declaration:* One way to define a class is using a class declaration. To declare a class, you use the class keyword with the name of the class.


## Review, Research, and Discussion:

1. Name 3 real world use cases where you’d want to change the request with custom middleware.
   - Data Management
   - uthentcation
   - Logging Middleware

2. True or false: The route handler is middleware?
   False.

3. In what ways can a middleware function end the process and send data to the browser?
   - res.send()
   - res.end()
   - res.render()
  
4. At what point in the request lifecycle can you “inject” middleware?
   After receiving the request, before sending the response "between them"

5. What can cause express to error with “Request headers sent twice, cannot start a second response”.
   when the server trying to send another response for the same request, but it is already sent a request.


## Document the following Vocabulary Terms

*-Middleware*: functions that have access to the request object (req), the response object (res), and the next function in the application’s request-response cycle.

*-Request Object*: is the HTTP request and has properties for the request.

*-Response Object*: represents the HTTP response that an Express app sends when it gets an HTTP request.

*-Application Middleware*: Middleware is software that provides common services and capabilities to applications outside of what’s offered by the operating system. 

*-Routing Middleware*: Routing is responsible for matching incoming HTTP requests and dispatching those requests to the app's executable endpoints.

*-Test Driven Development*:is a process of modifying the code in order to pass a test designed previously.

*-Behavioral Testing*:is a testing of the external behaviour of the program, also known as black box testing. It is usually a functional testing.

## Preview:

1. Which 3 things had you heard about previously and now have better clarity on? Test Driven Development , Difference between Response and Request Objects, Better understanding of classes and their implementation
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo? Im quite intrigued about the middleware and its uses and how to render a side view of it , learning more about the scenarios where i need to use custom made middleware and how to create them and how to know that i need one , even tho i answerd false in the 2nd question it was only based on what i read but i didnt quite understand it
3. What are you most excited about trying to implement or see how it works? A middleware to authenticate validity of an entered credit card if thats possible

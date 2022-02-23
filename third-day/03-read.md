# 23-2-2022- Third class reading notes:

## Data Modeling:

is the process of creating a data model for the data to be stored in a database. This data model is a conceptual representation of Data objects, the associations between different data objects, and the rules.

**The two types of Data Modeling Techniques are**
    1. Entity Relationship (E-R) Model
    2. UML (Unified Modelling Language)

**Types of Data Models**
    1. Conceptual Data Model:
    2. Logical Data Model:
    3. Physical Data Model:

**Advantages of Data model:**

- The main goal of a designing data model is to make certain that data objects offered by the functional team are represented accurately.
- The data model should be detailed enough to be used for building the physical database.
- The information in the data model can be used for defining the relationship between tables, primary and foreign keys, and stored procedures.
- Data Model helps business to communicate the within and across organizations.
- Data model helps to documents data mappings in ETL process
- sHelp to recognize correct sources of data to populate the model

**Disadvantages of Data model:**

- To develop Data model one should know physical data stored characteristics.
- This is a navigational system produces complex application development, management. Thus, it requires a knowledge of the biographical truth.
- Even smaller change made in structure require modification in the entire application.
- There is no set data manipulation language in DBMS.
   
### SQL

 It allows you to create a relational database and query it entirely in the browser. You can try it in this online demo. It uses a virtual database file stored in memory, and thus doesn't persist the changes made to the database. However, it allows you to import any existing sqlite file, and to export the created database as a JavaScript typed array.

### SQL vs NoSQL Database Differences 

SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database.


### Sequalize
Sequelize is a promise-based Node.js ORM tool for Postgres, MySQL, MariaDB, SQLite, Microsoft SQL Server, Amazon Redshift and Snowflake’s Data Cloud. It features solid transaction support, relations, eager and lazy loading, read replication and more.

Sequelize follows Semantic Versioning and the official Node.js LTS schedule. Version 7 of Sequelize officially supports the Node.js versions ^12.22.0, ^14.17,0, ^16.0.0. Other version might be working as well.

## Review, Research, and Discussion:

1. Name 3 advantages to Test Driven Development
   1. Better program design and higher code quality
   2. Detailed project documentation
   3. TDD reduces the time required for project development
   4. Code flexibility and easier maintenance
   
2. In what case would you need to use beforeEach() or afterEach() in a test suite?
   for example, if we are testing for a console log and we don't need to flood the console with the actual console.log output, we can use beforEach to add a mockImplementation before each test case to only check if the console.log method was called without actually outputting to the console during the tests. the opposite is achieved by using mockRestore method afterEach or afterAll test cases to negate this process and restore the (non-mocked) implementation.


3. What is one downside of Test Driven Development
   a. It slows down the development process.
    b. Challenging to support and maintain. c. It is difficult to learn

4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
   JavaScript classes, introduced in ECMAScript 2015, are primarily syntactical sugar over JavaScript's existing prototype-based inheritance. The class syntax does not introduce a new object-oriented inheritance model to JavaScript.

5. Why REST?
   Because it is easy to uderstand, provides faster data interchange format, it makes chaching easier and it is flexible.


## Document the following Vocabulary Terms

- functional programming: s a programming paradigm—a style of building the structure and elements of computer programs—that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.
  
- object-oriented programming (OOP): is a programming paradigm that relies on the concept of classes and objects. It is used to structure a software program into simple, reusable pieces of code blueprints (usually called classes), which are used to create individual instances of objects.
  
- class: are a template for creating objects. They encapsulate data with code to work on that data. 
  
- super:  keyword is used to access and call functions on an object's parent.
  
- this: the this keyword refers to an object.
Which object depends on how this is being invoked (used or called).
When used alone, this refers to the global object.
In HTML event handlers, this refers to the HTML element that received the event.

- Test Driven Development (TDD): s a process of modifying the code in order to pass a test designed previously.
  
- Jest: testing framework designed to ensure correctness of any JavaScript codebase. 
  
- Continuous Integration (CI): is a development practice wherein developers merge changes in their code as often as possible in order to detect and locate errors quickly.
  
- REST: is an improved way to handle function parameter, allowing us to more easily handle various input as parameters in a function. The rest parameter syntax allows us to represent an indefinite number of arguments as an array.
  
- Data Model: is the process of diagramming data flows. When creating a new or alternate database structure, the designer starts with a diagram of how data will flow into and out of the database.


## Preview:

1. Which 3 things had you heard about previously and now have better clarity on?
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
3. What are you most excited about trying to implement or see how it works?
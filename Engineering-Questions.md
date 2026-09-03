# Engineering Questions

## JavaScript

## TypeScript
1. What is TypeScript, and why would you use TypeScript instead of plain JavaScript for a Node.js backend application?
   Ans: TypeScript is a statically typed superset of JavaScript. It adds features like static typing, interfaces, generics and compile-time type checking. In a Node.js backend, I would use TypeScript because it catches many type-related errors during development, provides better IDE support and makes large codebases easier to maintain and refactor.
2. What is an interface in TypeScript, and why would you use an interface in a backend application?
  Ans: An interface defines the structure or contract of an object, including its properties and their types. We use interfaces to make our code type-safe, reusable, and consistent, so we don't have to define the same object structure repeatedly.
3. What is the difference between interface and type in TypeScript?
   Ans: Both interface and type can define object structures. Interfaces are mainly used for defining object contracts and can be extended using extends. Type aliases are more flexible because they can also represent unions, intersections, primitives, tuples and other types.
4.If you had to define a User object with id, name, and email, would you use interface or type? And why?
   Ans: I would use an interface because I'm defining the structure of an object, and interfaces can be extended when I need to create a more specific structure.
5. type UpdateEmployee = Partial<Employee>; What does Partial<Employee> do, and why would it be useful for an update API?
   Ans: Partial<Employee> makes all properties of the Employee type optional. It's useful for update APIs because we may update only one or a few fields instead of sending the complete employee object
6. Pick vs Omit You want an API response containing only id, name, and email. And you want another type containing everything except password. Which utility type would you use in each case, and why?
   Ans: Pick is used when I want to select specific properties from a type. For example, Pick<User, 'id' | 'name' | 'email'> gives me only those fields. Omit is used when I want everything except certain properties. For example, Omit<User, 'password'> prevents the password from being included in the response.
7. Enum - Why would you use an enum here instead of simply using a string for the campaign status?
   Ans: I would use an enum when a property has a predefined set of allowed values. For example, a campaign can only be pending, processing, completed, or failed. Using an enum provides type safety and prevents invalid status values from being used throughout the application.
   

   
## Node.js

1. What actually happens when an HTTP request reaches a Node.js server?

2. Why is Node.js called single-threaded?
Ans: Node.js is called single-threaded because JavaScript execution happens on a single main thread. The V8 engine executes JavaScript on this thread, and the Event Loop runs on the same main thread. However, Node.js itself can use additional threads internally through libuv for certain operations, so saying Node.js has only one thread is not completely accurate.

4. If Node.js is single-threaded, how can it handle thousands of concurrent requests?
Ans: Node.js uses an event-driven, non-blocking I/O architecture. When a request performs an I/O operation such as a database query, network request, or file operation, Node.js doesn't block the main JavaScript thread waiting for it to finish. It delegates or registers the operation and continues processing other requests. When the operation completes, its callback or promise continuation becomes ready, and the Event Loop executes it. Because one thread can coordinate many I/O operations without waiting for each one, Node.js can handle a large number of concurrent connections efficiently.
5. What exactly is the Node.js event loop?

6. What is libuv and why does Node.js need it?

7. When does Node.js use the thread pool?

8. What happens when I use await with a database query?

9. What happens when CPU-intensive code runs inside Node.js?

10. What is the difference between concurrency and parallelism?

11. What happens inside Node.js when 10,000 requests arrive at roughly the same time?

12. What is a Thread?
Ans: A thread is a small unit of execution inside a program.

13. What is callstack?
Ans: The Call Stack is a LIFO data structure used by JavaScript to keep track of function execution. When a function is called, it is pushed onto the stack, and when it finishes, it is popped from the stack.

14. What is the Callback Queue?
Ans: The Callback Queue is a queue where callback functions wait until the Call Stack is empty.
OR
Callback Queue stores callbacks that are ready to execute, and the Event Loop moves them to the Call Stack when the Call Stack is empty.


## HTTP & Networking

## Databases

## PostgreSQL

## Redis

## Kafka

## Elasticsearch

## Distributed Systems

## System Design

## Linux

## Docker

## Security

## Performance

## Observability

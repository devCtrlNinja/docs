# Engineering Questions

## JavaScript

## TypeScript

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

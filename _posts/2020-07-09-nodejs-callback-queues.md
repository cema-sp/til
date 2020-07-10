---
layout: post
title:  "Node.js Callback Queues"
date:   2020-07-09
categories: node
---

Learned some about Node.js internals and Callback Queues in particular.
It appeared Node.js maintains multiple prioritized queues to handle callbacks.

**Call Stack** - keeps track of the function currently being executed and of its origin.
**Event Loop** - responsible for code execution.
**Callback Queues** - hold callback functions of completed asynchronous operations.

![Node.js Callback Queues]({{ site.baseurl }}/assets/2020-07-09-nodejs-callback-queues-01.png)

In order of priority

1. **Microtask** queue - `process.nextTick`, `Promise` 
2. **Timer** queue - `setTimeout`, `setInterval` 
3. **IO** queue - file system, network 
4. **Check** queue - `setImmediate` 
5. **Close** queue - closing HTTP connection, stream, etc

___

**Links**

- [A deep dive into queues in Node.js](https://blog.logrocket.com/a-deep-dive-into-queues-in-node-js/)

---
layout: post
title:  "Node.js streams"
date:   2020-05-21
categories: node
---

TIL that Node.js [streams] could be extremely useful when you need to process 
a paginated API and batch or just consume it in a functional fashion.

~~~js
await pipeline(
  fetchRecords,
  JSONParser,
  changeDateFormat,
  queueBatch(queueUrl)
)
~~~

___

**Links**

- [Node.js streams documentation][streams]

[streams]: https://nodejs.org/api/stream.html

---
layout: post
title:  "Single Table Design"
date:   2020-05-29
categories: architecture, aws, dynamodb
---

Working mostly with relational databases it is fascinating and eyes-opening to 
learn about DynamoDB **Single Table Design**.

DynamoDB tables consist of keys and attributes. What is interesting is that
keys and attributes do not have to be homogenous, means it is possible to
store absolutely different records in the same DB and sucessfully operate that
structure.

![DynamoDB tables]({{ site.baseurl }}/assets/2020-05-29-single-table-01.png)

**Primary key** - is a partition key _OR_ partition + sort keys

**Partition key** - a top-level primary identifier. The data would be split by that key

**Sort key** - used for sorting and querying.
Could be composed from multiple values and queried by prefixes.

**Secondary index** (local, global) - allows additional querying scenarios.
Local - with the same partition key as the original table.


### Single Table Design

The main reason for using a single table in DynamoDB is to retrieve multiple,
heterogenous item types using a single request.

![Single Table]({{ site.baseurl }}/assets/2020-05-29-single-table-02.png)

___

**Links**

- [one](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-general-nosql-design.html)
- [two](https://www.jeremydaly.com/how-to-switch-from-rdbms-to-dynamodb-in-20-easy-steps/)
- [three](https://www.alexdebrie.com/posts/dynamodb-single-table/)
- [four](https://www.trek10.com/blog/dynamodb-single-table-relational-modeling/)

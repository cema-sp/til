---
layout: post
title:  "Clean Architecture Terms"
date:   2020-05-22
categories: architecture
---

I've heard those terms multiple times but never actually thought about their 
origin or proper use.

Researching class naming conventions and concerns separation I found 
references to [Clean Architecture][Clean Architecture paperback] book by Robert C. Martin.

Listing the terms I've selected to introduce for the Team

- **Model** (Entity, Aggregate) - a representation of a business entity.
  Encapsulates associated business logic. Typically responsible for persistence.
- **Domain Service** (Interactor) - domain logic that relies on two or more entities.
- **Use Case** (Application Service) - a list of actions or event steps
  typically defining the interactions between a User and a system to achieve a goal.
- **Gateway** - an adapter between the application and a 3rd party API.

![Clean Architecture]({{ site.url }}/assets/2020-05-22-clean-arch-01.jpg)
![Clean Architecture]({{ site.url }}/assets/2020-05-22-clean-arch-02.png)
![Clean Architecture]({{ site.BASE_PATH }}/assets/2020-05-22-clean-arch-02.png)
![Clean Architecture]({{ site.baseurl }}/assets/2020-05-22-clean-arch-02.png)

___

**Links**

- [Clean Architecture paperback]
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Implementing Clean Architecture - What is a use case?](http://www.plainionist.net/Implementing-Clean-Architecture-UseCases/)
- [A Case For Use Cases](https://webuild.envato.com/blog/a-case-for-use-cases/)

[Clean Architecture paperback]: https://www.amazon.com/Clean-Architecture-Craftsmans-Software-Structure/dp/0134494164

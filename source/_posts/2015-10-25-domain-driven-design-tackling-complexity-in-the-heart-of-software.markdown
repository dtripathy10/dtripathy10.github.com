---
layout: post
title: "Domain Driven Design - Tackling Complexity in the Heart of Software"
date: 2015-10-25 05:53:14 +0530
comments: true
categories: [Book Notes, Enterprise Software Architecture, DDD]
---

### About
----
+ Author : [Eric Evans](https://domainlanguage.com/)
+ Review : [Amazon](http://www.amazon.in/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215/ref=sr_1_1?s=books&ie=UTF8&qid=1445764127&sr=1-1&keywords=Domain-Driven+Design%3A+Tackling+Complexity+in+the+Heart+of+Software)

### Notes
----

##### Putting the Domain Model to Work

+ Brainstorming/Knowledge Crunching session: To find a simple model for tackle the complexity
+ Ubiquitous Language: for collaboration
+ Hands-On Modellers: Binding model and implementation
+ Technology Agnostic Architecture

##### The Building Blocks of a Model-Driven Design

+ Smart UI Anti pattern
+ Architecture Concerned: Layered Architecture, Hexagonal Architecture
+ Domain Model Architecture: Entity, Value Object, Service, Modules
+ Managing Lifecycle of Domain Object: Aggregate(Ownership), Factory, Repository
+ Aggregate has the right to query the repository, and factory has the right to create a domain object by using Repository
+ Separate Domain Model and database schema
+ Separate artifacts for bounded context including database schema

#### Refactoring towards Deeper Insight

+ Contineous Learning: Improve the Ubiquitous Language
+ Refactoring towards deeper insight
+ Supple Design

#### Strategic Design

+ Bounded Context
+ BC leads to Integration Problem -> Contineous Integration
+ Comunication between BC
+ Context Map

#### Further Design Pattern

+ Aspect-oriented programming 
+ Command Query Responsibility Segregation
+ Event Sourcing (Accounting Entry )

### More Resouces:
----

+ [Getting Started With DDD When Surrounded By Legacy Systems](http://domainlanguage.com/ddd/strategy/GettingStartedWithDDDWhenSurroundedByLegacySystemsV1.pdf)
+ [What I've learned about DDD since the book (London-2009)](https://www.youtube.com/watch?v=lE6Hxz4yomA)
+ [Design and Agile in DDD (NYC-2010)](https://www.youtube.com/watch?v=f00jUC64osw)
+ [Development of Further Patterns of Enterprise Application Architecture](http://martinfowler.com/eaaDev/)
+ [CQRS, Task Based UIs, Event Sourcing agh!](http://codebetter.com/gregyoung/2010/02/16/cqrs-task-based-uis-event-sourcing-agh/)
+ [CQRS Journey - Microsoft](https://msdn.microsoft.com/en-us/library/jj554200.aspx)
+ [domain driven design](http://martinfowler.com/tags/domain%20driven%20design.html)




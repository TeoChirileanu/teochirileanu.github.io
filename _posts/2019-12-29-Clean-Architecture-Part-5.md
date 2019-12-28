---
title: 'Clean Architecture Series: Frameworks'
author: Teodor
layout: post
---

Frameworks are good things - they can relieve you of great pains when developing software. However, committing to a certain framework is like marrying that framework (i.e. you’re bound to using it for the rest of the life cycles of that application). Like Uncle Bob put it: “For better or for worse, in sickness and in health, for richer, for poorer, forsaking all others, you will be using that framework!”. 

Using a certain framework is an important decision that should not be taken lightly. The use of Frameworks has become more popular nowadays and for a good reason. Generally speaking, people of the community write frameworks that are relevant for themselves and their co-workers because they want to help and give back. They have encountered difficulties and now are ready to share their knowledge of overcoming these difficulties with others. 

The most important thing to note about Frameworks is that they are good given a specific context, and should not be considered Architectures. One great mistake that developers do is to commit to a certain framework and build their application in and around that framework - a place where the Architecture solely must be. 
Frameworks are not architectures - and they do not have your best interests at heart, because they have been built with other purposes in mind; namely, to solve the problems of the creator of that framework and of those close to him.

We can think of the relationship between the developer and the author of a framework as being an Asymmetric Marriage (i.e. one-directional). That is, you make a huge commitment to using that framework, but the author of the framework makes no commitment whatsoever. 
Wrapping the architecture of your application around a framework has a huge effect on the overall coupling of the system. Polluting the business objects with framework-specific elements such as attributes or certain fields is a mistake lots of programmers do and puts their effort at great risk.

Suppose the framework makes it easier for you to start building your application, but what after? As the product matures, you will often find certain features of that framework to not help you as much as they did in the beginning. Moreover, as time passes and new versions are released, you will probably find out that old features, which you made use of, have disappeared. Even more painful is when another new and shiny framework is released and you would like to try it out, but you can’t because the core business logic of your application depends on that old rusty framework of yours! Not to mention that if the framework becomes unsupported and dies, your application will fall along with it.

The Solution

The best solution is to use the framework, not to marry it. Date it a few times, see how it behaves in different circumstances, decide what you like about it, what you don’t and take action. If it corresponds to your need, keep it. If it doesn’t, replace it or don’t use it at all.
A Framework does not influence the architecture of a system. It should be treated as detail and kept at a distance from the business rules. 

Let’s take a few examples.

The Spring framework is one of the most popular dependency injection frameworks for Java. Its power to automatically wire dependencies comes in handy on most projects. But a good Architect will not pollute the Business Objects with '@Autowired' attributes. In fact, Business Objects should know nothing about your application using Spring.

Entity Framework

One of the most popular ORM Frameworks for .NET is Entity Framework. Many architects make the mistake of specifying this framework as the default way of accessing data. Despite being a well written and flexible framework, it is just a mechanism of accessing persisted data - thus it is to be considered as detail and should be kept behind a well-defined data persistency interface

Conclusion

Frameworks are details and using them should be a decision, not a given. In a good architecture, frameworks are separated from business rules and use cases and belong to the outermost layers of the application.

Examples: Spring, Entity Framework, Ninject, Moq
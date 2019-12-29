---
title: 'SOLID Series: The Open Closed Principle'
author: Teodor
layout: post
---

In this article we are going to discuss the Open-Closed As noted by the author of the principles himself, the Open-Closed principle is the most important of concepts in object-oriented programming.

While all SOLID Principles are certainly important, some are more important than others. One of the most important, if not the most important is the Open-Closed principle, which dates back to Object-Oriented programming itself (see Bertrand Meyer and his Eiffel programming language).

In short, the O Principle states that an application should be open for extensions, but closed for modification. What the principle tries to say is that we should be able to add new functionality to a piece of software (e.g. a new feature) all while preserving the existing behavior.

Even though it is not a trivial task, keeping an application extensible while maintaining its current functionality is essential in software development – it is this that makes software soft (i.e. easy to change). One of the ways of achieving this goal is through polymorphism, which we will discuss in the following sections. 
Polymorphism

In OO (Object Oriented) programming, the only way to access an object is through a reference, which is declared at compile-time and can be of only one type. Polymorphism (composed of the Greek words polús and morphḗ) enables an object to take many forms (i.e. implementations) but to retain its base type. For example, a Transaction may hold a reference to an object of type currency, that we’ll call the parent.  If the parent has three children (i.e. implementations), we should be able to use any of these three objects (implementations) by using the same reference (that is, to the parent). In general, polymorphism comes into two flavors: dynamic and static. We’ll start describing Dynamic Polymorphism first, then detail Static Polymorphism. Note: we’ll be using C#.

Of all OO principles, the Open-Closed principle is probably the most important. Achieved using both static and dynamic polymorphism, “The Big O” remains fundamental for building modern, extensible and maintainable software applications.
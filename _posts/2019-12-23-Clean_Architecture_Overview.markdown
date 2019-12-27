---
title: 'Clean Architecture Series: Overview'
author: Teodor
layout: post
---

Clean Architecture represents a collection of patterns, practices, and principles used to create modern, high quality and elegant software systems that are simple to understand, flexible, testable and maintainable. Clean Architecture is a robust alternative to the traditional 3-layer, database-centric architecture, which has been used for decades and is known for its limitations.

## The Goal of Software Architecture

As Robert Martin (the author of the book “Clean Architecture”) stated: “The goal of Software Architecture is to minimize the human resources required to build and maintain the required system.

One simple metric that can be used to determine the quality of software architecture is to measure the effort required to meet the customers’ requirements. If the effort is low and continues to stay so during the lifetime of the system, then the architecture of that particular system is good. On the contrary, if that effort increases with each release, the architecture is bad and it will most probably become the reason why the system will die.

## What is Architecture

Let’s take an example from classic architecture. Suppose you want to build a house. Do you start building some walls, paint them green? Of course not. You first need to define the shape of the house, its outward appearance, decide where the main entrance will be, plan the layout of the rooms and so on. Architecture is about taking a series of decisions to fulfill your need: a comfortable house to live in.
Software architecture is not very different from classical architecture - it’s still about carefully combining low- and high-level decisions to build something that creates business value. But in the case of Software Systems, the final product is not something concrete, but rather something more abstract: an Application.

## What is Software build-out of

We are talking about Software Systems, but we need first to define what they are. The building block of any Software System is the Component. These components can be grouped to form sub-systems, which serve a specific purpose in the overall system. Furthermore, components are families of classes that share common functionality and depend on each other. In their turn, a class is made out of properties and methods.

## The Purpose of Software Architecture

The primary purpose of Software Architecture is to support the life cycle of a system. Given that the main phases of software development have remained the same for the last decades, a good Architect will create a system that is easy to understand, fun to develop, quick to deploy, a pleasure to operate and a joy to maintain. The ultimate goal of Software Architecture is to minimize the lifetime cost of a software system while maximizing overall programming efficiency.
The strategy behind the power of clean architecture is leaving as many options open, for as long as possible.

One of the greatest misconceptions in building software systems is to create something that just “works”, and this implies making lots and lots of emotionally driven decisions. While it is true that they might seem to work fine, most of these systems have problems in other areas such as ongoing development, deployment, and maintenance (the latter being the most expensive). Clean Architecture acknowledges the critical role of proper system behavior while considering its overall health.

## How does it work

Software provides two main types of value: behavioral and structural. Behavior value is given by how the system behaves under certain circumstances, while structural value derives from the fact that the structure of a system can be easily changed and adapted to new business needs. The latter is more important because it’s what makes software soft (i.e. easy to change).
Thus a soft software system that can quickly adapt to new requirements is of more value than one with a rigid structure that doesn’t allow agility to come into play. Consequently, the way to keep software soft is to keep options open for as long as possible.

## Keeping options open

Every software system out there can be decomposed into two major elements: Policy and Details. While policies define the “why” and “what” needs to be done, details specify “how” things should be done. Policies concern behavior, while details concern the structure through which the policies are implemented on machines. Therefore Policies are where the real value of a system lies, while details help policies come alive, in the form of software products (i.e. software applications).

The options that need to be kept open are details that don’t matter. For the Good Architect, leaving options open means that instead of taking premature decisions regarding specific implementation details, he will acknowledge Policy as the most essential element of a system, thus deferring decisions about details for as long as possible.

Truth be told, the more you wait on making a decision, the better that decision will be. The longer you wait before deciding on details, the more experiments you can try. The more experiments you can run, the more information of value you will gain. Ultimately, the more information you have on a certain topic, the better the decision will be in the long run.

## Conclusion

The Good Architect will understand and separate policies from details to the point that the policy has no knowledge of the details and does not depend on them in any way. Moreover, he will enforce policy design in a way that decisions about low-level details can be deferred for as long as possible, thus maximizing the number of decisions not made.

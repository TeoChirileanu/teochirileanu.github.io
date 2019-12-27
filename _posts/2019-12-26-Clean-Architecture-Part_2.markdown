---
title: 'Clean Architecture Series: Business Rules and Use Cases'
author: Teodor
layout: post
---

As mentioned in the previous articles, every Software System can be divided into Policies and Details. Describing behavior, the Policies are considered to be high-level while the Details, which concern how the Policies are actually implemented, are considered low-level.
Ideally, the Clean Architecture should be seen more like a “Plugin Architecture” i.e. an Architecture describing that at the heart of the system lie the Business Rules, with lesser concerns being plugged into that system (from where the term Plugin comes from).

To better understand what is meant by a “Plugin Architecture”, just think about your Personal Computer. Does it need headphones to run? No, it doesn’t. Does it need a keyboard or a mouse to work? Not necessarily. Does it even need a display to boot? Not at all! All it takes for a computer system to work is a CPU and some Memory. Therefore these main components can be thought of as Business Rules of a PC, while the other components (mainly I/O devices) are viewed as Plugins to the PC. 
The power of Plugins rests in their natural ability to be disposable and easily interchangeable, without affecting the core functionality of the system (Think about PNP - Plug’N’Play functionality).

So, what are exactly those Business Rules?

Business rules are the reason why a software system exists because they carry the code that makes (or saves) business money, regardless of whether they are executed manually or in an automated way. 
Business rules should be the most independent and reusable code in the system.
Business rules are composed of Critical Business Procedures and Critical Business Data. Because these are very close to each other, they are to be grouped together in a single object, called Entity. 
Entities consist of a small set of business procedures that operate on business data. Let’s take a few examples of how to model these Entities.

Let’s take a simple example. We would like to build a game in which the application generates a random number, takes a guess from the user and then informs him of the result of his guessing. From this information, a simple Entity could be created in the following way: the Critical Business Data would consist of the generated number, while the Critical Business Procedures would be Checking another number against the generated one and Informing the User about the result of his guess. This candidate Entity would like this:

Now imagine you want to borrow some money from a bank. You take it, and in a fixed time, you must return the original amount (called the principal) plus the interest. This is called making a loan. Here, the Critical Business Data is represented by the Principal and the Interest Rate (from which the Interest is computed). Two candidates for the Critical Business Procedures would be Making a Payment, Applying the Interest and maybe even Charge a Late Fee. 

Finally, let’s look at a little bit more complex example. Suppose we want to build a Money Exchange Application. The money is made by exchanging foreign currencies at a custom exchange rate. Let’s see how the Transaction Entity would look like now:

In this example, the relationship between the Exchange Information and the User Information is so close that they have to reside together in the same Object, called Transaction. Another crucial point is to persist the transaction somewhere, otherwise, there wouldn’t be any audit available Finally, the transaction information consisting of the exchange and use data along with the exchange rate and amount due is given to the user.

A Use Case is an informal description of what a system should do. It is a way of telling an automated system how to behave and how it should act given certain conditions. Technically, Use Cases encapsulate and implement all the use cases of a system. They control the flow of data coming from and into the Entities and dictate how these Entities should use their Critical Business Rules to achieve the main goal of a Use Case.
In simple terms, a Use Case specifies input provided by the User, the output is shown to that User, and a brief description of the steps involved in producing the output.
It is important to mention that Use Cases are interface-agnostic. They do not describe how the system appears to the user or how the information is being delivered to the User e.g. based solely on the Use Case, one cannot tell whether the application is delivered by Web, as a Console or as a Pure Service. Their job is to simply expect data as an input and to produce data as an output. 

In this article, we saw that software systems exist because of the value they bring to the business. These business rules are at the heart of the Modern Plugin Architecture, while Use Cases give meaning to these rules by embodying real uses case of a software application.
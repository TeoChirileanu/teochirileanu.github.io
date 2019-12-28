---
title: 'Clean Architecture Series: The Web'
author: Teodor
layout: post
---

For many of today’s systems, the Web is the way to go. Want to build a new application? You would want it to be delivered over the Web, of course, because this is what everybody else is doing, right? Wrong. GUIs are a manner of sending (and sometimes getting) the information to (and from) the user. It has nothing to do whatsoever with the business core of the application and therefore should be regarded as a detail. In how many ways can a system be delivered? Well, the simple answer is endless. However, the most popular ways of delivering software systems are in the form of a Desktop Application, Web Application, Mobile Application or as a Pure Service. As we can see, the Web is a GUI. And GUIs are details that should be kept separate from the business rules. When the Web was introduced back in the 1990s, it completely revolutionized how software systems were built and deployed. Everybody was throwing away their beloved client-server architectures and were rapidly embracing the new cool kid in the town. Today, many of us think that the Web changed everything. 

It seems like the Web changed a lot...

Did it? No, not at all. Putting the pieces of the puzzle together, we can see that the Web was nothing more than one of the oscillations in our incertitude between centralizing computing power and distributing it. In the beginning, there were computer rooms with punch cards. Then mainframes with smart green-screen terminals (which closely resemble today’s browsers) appeared. After that, we built central minicomputers with arrays of dumb terminals. After a while, the Client-Server architecture was introduced, where all the processing would take place in server farms. The Web changed that paradigm allowing clients to become “smarter” by enabling (eventually huge) Javascript applications to run inside their browsers. Lately, we’ve changed our mind again and moved some of the Javascript back into the server with Node. We can say about the Web that is one of the many trends that come and go and therefore should not rely on it as being the Standard. 

All these oscillations - they’re making me crazy!

Unfortunately, all these oscillations cause harm to applications depending on them. The long term solution is to create an architecture that is oscillation resilient (i.e. whose core functionality remains the same, despite trend changes). The only way to resist to these changes is to push trends such as the Web as far as possible from the central core of the system by decoupling Business Rules from the UI.

But today’s applications seem so be so closely tied to their GUI!

It may not be easy to make a clear distinction between the UI and the Application, but another layer of abstraction can and should be put in place. If we can think about the Application as being a suite of Use Cases that perform computations on behalf of the user, we could also think about the GUI providing and showing data from and to the user. 


To conclude, though it may take several iterations to get this kind of decoupling just right, the benefits of applying the Separation of Concerns principle will save everybody lots of headaches and sleepless nights.
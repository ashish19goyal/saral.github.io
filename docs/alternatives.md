---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---


---
# Alternative architectures
In this document we discuss alternative architectures to Saral

## Platform as a service
Efforts are being made by cloud service providers to build Platform as a service to achieve similar objectives.

![Platform as a service](images/Serverless-technologies.png "Platform as a service")

### Advantages of Paas
- Reduce administration and focus on end objective
- Auto scaling
- Pay per use
- Durability and resilience
- Automated backups

### Cons of Paas
- Technology and cloud lock-ins
- Complex procedure to determine the right amount of resources as per performance requirements
- Learning curve for cloud specific technologies and terminologies
- Each of the cloud services have specific limitations making it difficult for general purpose use. E.g. AWS lambda can run functions for a maximum of 5 minutes only.

## Difference between Saral and PaaS

Historically, creating software applications has been like preparing food at home.
- You have to get all the ingredients from the grocery store.
- You have to know the recipes.
- You have to know how to cook.
- You have to know what ingredients can work together and what not.
- After the dish is prepared you have to know how to store it till it's served.

Some people do not want to cook at home. They are too busy to cook for themselves. So they go to a subway outlet. The subway attendant asks them what they want to have.
- Subway has already procured the required ingredients
- It asks you to chose your bread
- It asks you how would you like your bread - baked or grilled
- It asks you if you like to have a cheese slice
- It asks you for the patty to put in
- It asks you for all the toppings to put in
- It asks you for all the sauces to put in
- It charges you as per the customizations made on top of the base price
  This is similar to what most PaaS providers do. So, PaaS is Subway.

Some people are even more lazy. They just want the food. They do not want to take the toil to decide what to put in and how much. These people go to a full service restaurant
- Waiter asks you what would you like to have (requirements gathering)
- You can ask the waiter about various available dishes and their ingredients.
- You place order for a dish that best meets your expectation
- Your dish is prepared by an experienced chef while you chat with your fellow friends.
- You pay for the dish, not the ingredients or customizations.

This is Saral for you.


## Functions as a service
Faas is a part of the PaaS. Here devlopers can create their logic as small functions. These functions are hosted on the cloud. They can be executed independently from anywhere as required. The functions are stateless, i.e., they do not store any state. This allows for rapid scaling as it needs only compute to run these functions.


### Why do we use FaaS?
FaaS allows developers of the system to inject their custom logic in a big templatized system design. This allows reuse of the big system design templates. Developers do not have to write the whole system from scratch. They can pickup an existing system. Create their custom logic as functions hosted on FaaS. Then inject these functions into the existing system.

### What are the issues with FaaS?
There are following fundamental problems with this approach
- There has to be an existing system that can be templatized. Functions in FaaS itself don't do anything unless there is a system that can call them.
- Its a lot of overhead (due to network issues) to call a external FaaS endpoint to execute a simple logic. This brings additional complexities (like retries, throttling, circuit breaker) that need more frameworks to handle them. This increases the complexity of the existing system.
- Its difficult to version control these along with the calling application. Every function acts like a independent microservice that evolves on its own. This is too granular.

### How Saral manages this?
Saral allows developers to define custom logic as user-defined-functions. It incorporates all the goods of FaaS like statelessness. At compile time, these are interpreted by Saral and converted to a program. The program is packaged along with the calling system. It is hosted on the same machine where the rest of the system is running.

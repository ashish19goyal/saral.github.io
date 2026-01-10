---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Home
nav_enabled: true
nav_order: 1
---
## About
Our objective is to create a software design framework/language for software developers that covers all the aspects of Software development lifecycle, including
1. Design (including Documentation and Visualization)
2. Implementation
3. Testing
4. Optimization
5. Deployment
6. Monitoring

We are calling it `Saral`, meaning Simple. Software developers will only need understanding of System Design and tools like Saral to build and manage any software application.

## Context
Every few decades, technology has been moving towards a higher level of abstraction to hide the underlying complexities. Today, the complexities in Software development have again reached a point where managing it in its existing form is unviable and too expensive. A simple change in a big enterprise software costs thousands of dollars in terms of developers time and computational resources for development/testing/release. 

Not long ago, we started with manually toggling 1s and 0s in the earliest computers. As the number of transistors in the first computers started to increase, we moved to machine codes. With further development in hardware, we could build more and more complex applications. These needed more machine code. So, we moved to assembly language. As our memory and CPU density further increased, we had to move from assembly languages to programming languages like C and Fortran. Then as the applications grew even more complex, it needed collaboration between multiple software developers. So we moved to higher level programming languages like Java and C# that were cross platform and had contributions from other developers in the form of libraries.

Today, again we need another abstraction as the applications built today are distributed, intregrated and AI enabled. These applications span distributed storage systems and have to support multiple user interfaces at the same time. e.g., a video and music streaming site like youtube can be accessed via laptops, mobile, TVs, projectors, smartwatches etc.

## Goals
- **Complete SDLC**: Should cover all aspects of SDLC including development, testing, release, deployment, monitoring.
- **Easy to understand** for existing software developers.
- **Deterministic**: Produce the same results when implemented in any of today's technologies
- **Cloud Native and agnostic**: Should be able run on any cloud platform or edge devices. Multi-cloud support 
- **Incremental Development**: Should be able to use Saral to define the software projects that exist today.
- **Unified and distributed**: Saral should adopt a distributed first ideology (microservices). As that’s the need of today’s software development. It should also support unified application (monolithic) generation for rapid testing in a limited scale environment.
- **Source control and Collaboration**: Saral should support `Source control` and `Team collaboration` using code repositories.
- **Move from how to what**: Descriptive not imperative

## Market Research
Gartner estimates that a third of business users want to create software applications to solve their problems. There are not enough resources available with the IT teams to meet this demand. To solve this problem, a lot of low-code/no-code solutions are proposed. Gartner estimated a $30 billion market for low code by 2025. About 65% of application development by 2030 will be low code.
Following attempts have been made to solve this problem in different ways -
- Microsoft power apps, power fx
- Wix website builder
- Builder.ai
- Retool
- OutSystems
- Oracle APEX
- Salesforce

## Problem space
- **Simplify Software development variations**: A software developer today works with a myriad of tools and libraries. She doesn’t write all the code herself. Most of her time is spent in choosing the right tools and upgrading to the right version of the libraries. With Saral, there should not be a need to choose or update library or tools individually. Saral makes opinionated choices about these. The developer needs to only choose and upgrade Saral version.
- **Optimize developer experience**: Software developers have to focus more on the syntax and structure of the code rather than its outcomes. This is a waste of the mindshare of arguably some of the best minds. The syntax and structure is defined by the programming language and the framework. It can be automated, so that the human mindshare can go to actual problem solving. Numerous other attempts are being made in the same direction. E.g. advanced IDEs like intellij and VS code, github co-pilot etc.
- **Version control**: It has to be structured to make it work with version control.
- **Automated testing**: The idea of Saral aligns with `Behaviour Driven Testing`. Existing frameworks of unit testing, integration testing and load testing are too fragmented and solution oriented, i.e., they test what is created. Saral should be more requirements oriented.
- **Continuous deployment**: Everyday changes have to be released without any downtime. This should be as simple as the click of a button. Saral will give feedback to the developer on the possible impact of the release. The developer will take a decision on accepting the changes. Then Saral will deploy everything without any downtime. This is the approach being implemented by modern deployment managers, e.g., Terrform
- **Observability**: This is one of the biggest challenges for software developers today. There are multiple solutions available for managing this. E.g. logging, metrics, profiling, tracing etc. Saral would provide this out of the box on a unified platform for working across deployed artifacts.
- **Resiliency**: Saral can implement the best practices for resiliency at every touch point between deployed artifacts and external systems.

## References
- [Domain Driven Design by Eric Evans](https://www.domainlanguage.com/)
- [Low-Code and the Democratization of Programming](https://learning.oreilly.com/library/view/low-code-and-the/9781098112592/copyright-page01.html) by the O’Reilly Editorial Team
- [Power Fx](https://powerapps.microsoft.com/en-us/blog/introducing-microsoft-power-fx-the-low-code-programming-language-for-everyone/) by Microsoft
- [Getting started with Serverless](https://learning.oreilly.com/learning-paths/learning-path-getting/9781492042099/) by Sam Newman
- [From mathematics to generic programming](https://learning.oreilly.com/library/view/from-mathematics-to/9780133491791/ch02.html#ch02lev1sec1)
- [Introduction to Compilers and Language Design](http://compilerbook.org)
- [Data Mesh](https://www.oreilly.com/library/view/data-mesh/9781492092384/)
- [Jhipster](https://www.jhipster.tech/)
- [DSL platform](https://docs.dsl-platform.com/)
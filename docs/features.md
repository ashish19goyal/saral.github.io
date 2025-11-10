# saralpy
A java library to create and manage applications

## Features
- Application development as monolith or microservices. After designing the service, user should be able to produce monolithic or microservice artifcats for the application.
- Event storming
- Domain driven design to be provided by user
- Design in terms of events, aggregates and bounded context. Give  user the option to include generic sub-domains in their systems. e.g. authentication, authorization, reporting engine, website etc
- Ability to visualize the application design diagramatically
- Download application code along with docker images and scripts for setup
- Publish application
- Deploy application on 3rd party clouds
- Perform incremental releases
- User should be able to visualize the design of their applciation in the form of c4 diagrams

## Focus
- Generate c4 diagrams for the design in progress
- Generate backend code as monolith or microservices.
- microservices should have both transaction processing and analytics capabilities
    - it means microservice should completely abstract internal data design
    - it should expose rest APIs for both transaction processing and analytics
    - the APIs for analytics should be streaming APIs
- Implement Saral as a python library that can be executed from notebook UI
- Use a library of connectors - explore Apache Camel
- Accept "user defined functions" - explore how to convert python UDF to java

## UI design approach
- Think of UI design in terms of domain model
- Developer should define the data model as a refletion of their domain model
- Developer should then define the pages and components and interactions between them
- Developer should map the data model to the pages and components
- From the data model, saral will figure out what is global state vs page level state vs component level state
- Saral should automatically build the state transitions and state updates for the application
---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Modelling
nav_order: 4
---
## Modelling

## Unified modelling language
- The modelling language should be able to clearly communicate the meaning of the concepts it represents.
- Declarative style language to make it easier for the developers to comprehend its meaning.
- One model should underlie implementation, design and team communication.
- The modelling process should be intuitive and follow a step-by-step approach. e.g. Event storming. 

## Event storming
- Event storming is for discovery. Its not designed for translation of requirements into an application design.
- We need a modelling language that can take the results of an event storming workshop as input.  
- Stakeholders: Business, tech, UX

### Vocabluary of Event storming and Domain Driven Design
- Domain events (Orange): A state transition happening in the system. Every Event storming workshop starts with identifying domain events on a timeline.
- Problem areas (purple): Based on their experience, stakeholders list down potential problems/challenges with each domain event.
- Commands (blue): An action started by a user. This typically triggers a domain event. This is also used to analyze User experience UX.
- Actors (Yellow): Users interacting with the system. Further refined into personas. 
- Read models (Green) - Data needed by the user to make a decision
- Policy (lilac) - A reactive logic based on some domain event. A command is triggered based on some event.
- Aggregates (yellow) - These are the logical entities that encapsulate a group of domain events/commands/policies etc. Aggregates should be completely contained within and independent of each other, i.e., mutually exclusive and exhaustive. 

### Sources of Domain events
- Commands
- External systems integrations
- Other domain events
- Time based policies (cron jobs)

## From event storming to application desgin
- Bounded contexts become modules/micro-services
- Aggregates become services within bounded contexts
- Commands become API endpoints
- Policies become service constraints and business logic
- Domain events become events

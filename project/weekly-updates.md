---
title: Weekly Updates
---

# Weekly Project Updates

## Week 1
- [ ] Planned project scope  
- [ ] Drafted proposal  

## Week 2
- [ ] Initiated Git repository.
- [ ] Reviewed Java encapsulation, inheritance, classes, objects, collections and lists.
- [ ] Set up core functionality of app; classes and file structure.

## Week 3 
- [ ] Created a timeline for key deliverables of the project.
- [ ] Finalized project proposal.
- [ ] Configured pom.xml with dependencies for Spring Web, Spring Boot, JPA, and Lombok.

Reflection: I think having a clear timeline with key deliverables is key for this project, as it prevents me from spending more time than necessary , or less time than necessary because I know exactly what i need to have completed each week in order to have the project done in 10 weeks. 

## Week 4 
- [ ] Populated a Trello board with key features and deliverables, with the timeline.
- [ ] Bootstrapped the project using Maven, create a file structure and include Spring Boot dependencies.
- [ ] Designed modular classes for the Data Model aspect of my project, produce an entity relational diagram.

Reflection: The biggest obstacles so far have been time , but I decided to invest more time in the project than necessary since I am a part time student, so I have the free time to allocate towards the project. The other obstacle was creating actionable clear deliverables so I know what i need to do when i sit down at my computer but getting Trello set up has solved that.


## Week 5
- [ ] Scaffolded my project structure for Spring Boot
- [ ] Implemented in- memory CRUD operations (service layer) 
- [ ] Outlined REST endpoints in my Controller file (controller layer)
- [ ] Ran my Spring Boot application, and tested the REST endpoints using Postman
- [ ] Wrote a simple README that will enable someone to start my application
  
Relection: One thing I realized this week is that model-view-controller is actually a lot less complicated than it sounds. I think once you build something with it you realize its just a way of organizing files, its a simple pattern that scales up really well. 

Goals for week 6: I plan to transition from in-memory CRUD to postgreSQL, writing migration scripts for this, and then test the CRUD endpoints against the database. Essentially just transitioning to a database as the repository layer.

## Week 6
- [ ] Transitioned the repository layer from in-memory storage to PostgreSQL.
- [ ]Used H2 for testing and PostgreSQL with proper user permissions for the production database.
- [ ]Implemented full CRUD functionality with repository:
- [ ]Verified through integration testing that all three entities are correctly persisted in a permanent database.

Reflection: Testing was both frustrating and insightful this week. I solidified my understanding of unit tests vs. integration tests: unit tests validate small pieces of functionality, while integration tests ensure that components work together properly. Setting up tests has proven extremely valuable, as it allows me to quickly verify changes. Debugging was aided by Microsoft Copilot, which caught tricky issues like JSON serialization errors caused by circular references—something I hadn’t realized would be an issue. Overall, I gained a lot of insight into how to structure and test a Spring Boot application with a real database.

Goals for week 7: I plan to implement authentication and authorization using Spring Security. The goal is to make the project more realistic and secure, protecting sensitive patient data.



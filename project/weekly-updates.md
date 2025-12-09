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

### Reflection: I think having a clear timeline with key deliverables is key for this project, as it prevents me from spending more time than necessary , or less time than necessary because I know exactly what i need to have completed each week in order to have the project done in 10 weeks. 

## Week 4 
- [ ] Populated a Trello board with key features and deliverables, with the timeline.
- [ ] Bootstrapped the project using Maven, create a file structure and include Spring Boot dependencies.
- [ ] Designed modular classes for the Data Model aspect of my project, produce an entity relational diagram.

### Reflection: 
The biggest obstacles so far have been time , but I decided to invest more time in the project than necessary since I am a part time student, so I have the free time to allocate towards the project. The other obstacle was creating actionable clear deliverables so I know what i need to do when i sit down at my computer but getting Trello set up has solved that.


## Week 5
- [ ] Scaffolded my project structure for Spring Boot
- [ ] Implemented in- memory CRUD operations (service layer) 
- [ ] Outlined REST endpoints in my Controller file (controller layer)
- [ ] Ran my Spring Boot application, and tested the REST endpoints using Postman
- [ ] Wrote a simple README that will enable someone to start my application
  
### Relection:
One thing I realized this week is that model-view-controller is actually a lot less complicated than it sounds. I think once you build something with it you realize its just a way of organizing files, its a simple pattern that scales up really well. 

Goals for week 6: I plan to transition from in-memory CRUD to postgreSQL, writing migration scripts for this, and then test the CRUD endpoints against the database. Essentially just transitioning to a database as the repository layer.

## Week 6
- [ ] Transitioned the repository layer from in-memory storage to PostgreSQL.
- [ ] Used H2 for testing and PostgreSQL with proper user permissions for the production database.
- [ ] Implemented full CRUD functionality with repository:
- [ ] Verified through integration testing that all three entities are correctly persisted in a permanent database.

### Reflection:
Testing was both frustrating and insightful this week. I solidified my understanding of unit tests vs. integration tests: unit tests validate small pieces of functionality, while integration tests ensure that components work together properly. Setting up tests has proven extremely valuable, as it allows me to quickly verify changes. Debugging was aided by Microsoft Copilot, which caught tricky issues like JSON serialization errors caused by circular references—something I hadn’t realized would be an issue. Overall, I gained a lot of insight into how to structure and test a Spring Boot application with a real database.

Goals for week 7: I plan to implement authentication and authorization using Spring Security. The goal is to make the project more realistic and secure, protecting sensitive patient data.

## Week 7
- [ ] Configured Authentication using JSON Web Tokens using Spring Security.
- [ ] Added Authorization to REST endpoints.
- [ ] Created unique Roles with different permissions for each endpoint.
- [ ] Wrote and passed unit and integration tests to ensure robustness and reliability, 

### Reflection: 
This week was one of the most difficult because I found the Spring Security architecure to be complex and overwhelming, with a lot of boilerplate code that I found difficult to understand. I apporached this to try and understand what indidividual piece did before moving into details. For example knowing what a SecurityFilterChain was before exploring each part of it. I have noticed the most frequent challenges stem from unpredictable bugs, usually stemming from version incompatibilities and outdated dependencies. These are so difficult because I struggle to trace it through the code, since most times it is technically not from incorrect code.

Goals for week 7: I will be containerizing my base REST API model using docker, ensuring it can run reliably in the cloud, or any other computer. I will write the dockerfile, build and run the container locally, and update my README file with build/run instructions. This will ensure employers can access my project and use it.

## Week 8 

- [ ] Learned and implemented Docker for containerizing the Spring Boot application.

- [ ] Wrote a Dockerfile to package the app into a runnable image using a JDK base image.

- [ ] Built and ran the container locally using an in-memory H2 database for initial testing.

- [ ] Created a Docker Compose file to run a multi-container setup with separate containers for the app and PostgreSQL database.

- [ ] Configured environment variables, volumes for data persistence, and healthchecks to ensure the database was ready before the app started.

- [ ] Successfully connected the Spring Boot app to the PostgreSQL container and tested end-to-end functionality.

### Reflection:
This week was all about Docker. I learned how it eliminates the classic “it works on my machine” problem by packaging the entire environment into portable containers. Everything went smoothly until end-to-end testing, where I ran into issues that I initially thought were caused by my JWT security setup. After troubleshooting, I realized I wasn’t rebuilding my Maven JAR file before running Docker Compose, so the image kept using outdated code.

This experience taught me how crucial it is to properly rebuild artifacts before deployment and helped me understand why developers value tools like Docker—it makes setup, testing, and deployment consistent across environments. It also deepened my appreciation for automation and CI/CD workflows that prevent small but time-consuming mistakes.

Goals for Week 6: Next, I will focus on deploying the Dockerized app to AWS using Elastic Beanstalk or ECS. I plan to ensure the database connectivity still works, set up basic monitoring, and use S3 for storing static files or backups. I will also update my README to include AWS deployment instructions so others can run and test the project easily.



## Week 9
- [ ] Created an updated .yml configuration file specifically for AWS deployment.

- [ ] Deployed the containerized application to AWS Elastic Beanstalk.

- [ ] Configured the multi-container setup to pass AWS health checks successfully.

- [ ] Updated the README to include specific deployment instructions for AWS.

- [ ] Integrated Amazon S3 to store static files, backups, and sample data.

### Reflection:
Last week I attempted to learn what I could about AWS. I decided to go with the strategy of deploying a multi-container Docker application using Elastic Beanstalk. To do this, I had to upload my Docker Image to the Elastic Container Repository and enable IAM security configurations. I spent the majority of my time debugging deployment errors—struggling with .zip file configurations, .yml version mismatches, and IAM permissions. The deployed instance initially failed health checks because my security settings blocked endpoint access, requiring me to create a specific "health check" endpoint. After 26 versions and much frustration, I finally got it working!

Goals for Week 10: Now that the cloud aspect is mostly complete, I will focus on building the machine learning classifier service using NLP concepts. I plan to load a HuggingFace model for PHI detection, create a REST endpoint for the NLP microservice, write unit tests, and ensure integration with the Patient & ClinicalNote models.

## Week 10
- [ ] Researched HuggingFace models for PII classifying (Named Entity Recognition) and selected ab-ai/pii_model.

- [ ] Implemented a prototype redaction service in Google Colab to redact PII from text strings.

- [ ] Refactored the Colab implementation into a local FastAPI microservice within the VSCode project.

- [ ] Integrated the microservice into the Java application, allowing the ClinicalNote creation operation to call the redaction service automatically.

### Reflection:
This week was really fun because I got to apply NLP concepts in a deployed modality rather than just running Python code in Colab. Writing actual NLP-powered services in a development environment presented new challenges, such as configuring the environment to use my HuggingFace token and ensuring the lack of a GPU wouldn't throttle performance. The source of most confusion has been on the DevOps side—managing three separate .yml files (local, Docker/Postgres, and AWS) with different URLs and properties has required significant troubleshooting.

Goals for Week 11: I will finalize the microservice and move towards full integration. I plan to use Pytest for the phi_redactor, write JUnit and Mockito tests for the Java service, and repackage the project using Maven to run a full multi-container test. Finally, I aim to redeploy the project with the added NLP service to Elastic Beanstalk.

## Week 11
- [ ] Finalized the NLP microservice and implemented testing protocols at each application level.

- [ ] Wrote Pytest scripts to simulate HTTP requests and test the microservice in isolation.

- [ ] Verified that the Java service correctly receives and deserializes JSON from the Python service.

- [ ] Conducted end-to-end testing using Postman to ensure the platform performs as expected when deployed on AWS.

### Reflection:
I noticed that as the complexity of the application grows, it takes significantly longer to thoroughly test everything. I now have to test the microservice in isolation, then the Java integration, and finally the full AWS deployment via Postman. Balancing this work with three job interviews in two days made productivity difficult, but I managed to finish the core NLP service integration.

Goals for Week 12: I decided to add a CI/CD pipeline using Github Actions to demonstrate DevOps skills to potential employers. I will also construct a Postman collection to visualize the project flow (replacing a full frontend) and focus on improving documentation, error handling, and input validation to surface root causes of errors more clearly.

## Week 12
- [ ] Set up an automation testing framework using Github Actions to run Python tests on every push.

- [ ] Configured environment secrets to securely pass the HuggingFace token to the CI/CD pipeline.

- [ ] Created a comprehensive Postman collection to demonstrate the full app workflow (Login -> Create Patient/Samples/Notes -> Redaction -> Deletion).

- [ ] Verified regression testing: ensured that new features didn't break the existing NLP classifier.

### Reflection:
This class has been great. Every time I start a project it usually fizzles out, but seeing everyone else's progress inspired me to deliver something I can be proud of. Completing this project has shown me how far I've come, allowing me to apply multiple technologies like Spring, AWS, Github Actions, and FastAPI—many of which I wasn't familiar with before. The most valuable thing I learned in CSPB is the ability to learn and apply new technologies as they evolve.

Goals for Final Submission: I need to finalize error handling to keep users on the "happy path," create a thorough README with instructions for all deployment types (local, Docker, AWS), create a metrics table for the NLP classifier (latency, precision, recall, F-1), and record the final demo video.


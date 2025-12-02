# The Healthcare API: An AI-Enabled HIPAA Compliant Patient Management System  
**Author:** Matthew Martin  
**Course:** CSPB 3832 – NLP  

---

## Introduction

The Healthcare API began with the idea of learning new tech stacks (Java, Spring Boot, Docker, AWS) by creating a project that was in an industry that I was familiar with (Biology/Medicine), and incorporating aspects of computer science that I was passionate about (Machine Learning/NLP/Data modeling and management). I wanted to connect my background with my computer science education and allow myself to have an entry on my resume that would help tell a story. My motivation was to expand my knowledge in each aspect of the tech stacks and gain experience applying them in a context that reflected my interest.

This project will allow me to gain knowledge in new tech stacks, with a focus on the devops aspects of software engineering and machine learning. It will help me build familiarity with new tech tools like Java, Spring Boot, Docker, and AWS, while simultaneously connecting my biology background with my computer science education.

---

## Goals, Timeline, and Deliverables

### **Core API Development (Weeks 1–3)**  
- Create a Spring Boot application with biological data models.  
- Implement CRUD operations for patient data and biological samples.  
- Add user authentication and authorization.  
- Set up PostgreSQL database.  
- Implement error handling.

### **Containerization and Deployment (Weeks 4–5)**  
- Dockerize the application.  
- Create docker-compose for local development and multi-containerization.  
- Deploy to AWS Elastic Beanstalk.

### **ML Integration (Weeks 6–7)**  
- Implement an NLP model that classifies clinical notes for HIPAA compliance and redacts PHI.  
- Utilize a Hugging Face transformer pre-trained for PII sequence classification.  
- Create a FastAPI microservice for the ClinicalNote endpoint to call.

### **Advanced Features and Portfolio (Weeks 8–10)**  
- Prepare detailed documentation (README) covering deployment, containerization, and testing.  
- Develop Postman collections demonstrating full API functionality.  
- Create a video demo explaining the project and showing the workflow.

---

## Background

This project matters because I have been focusing on a niche area of computer science to be a more competitive applicant, this area being Bioinformatics/Healthcare Software Engineering/Biotech AI. This project involves expanding my knowledge in these specialties so that I can better secure these roles but also perform well in them. I will learn all the technologies necessary, gain experience applying ML in a domain-relevant context, and create something industry relevant.

Throughout my academic and personal background, I have been involved with the fields of medicine and biological science. My family works in healthcare, and I have a biology degree and healthcare experience. I was inspired to pursue a CS degree because during clinical research work, I saw powerful software tools used for COVID-19 research and wanted to build things like that.

In the CSPB program at CU Boulder, my personal mission was simple: **create technology that helps people**.

At AstraZeneca, I supported the Viral Clearance team by creating software for data integration that helped move treatments into testing phases faster and supported AI/ML modeling. Combined with taking NLP, that experience made me wonder what a small example of AI automating a healthcare problem would look like.

I also wanted more practice with backend development, REST APIs, MVC, and DevOps. I’ve used many cloud-based EHR systems, so I built an API that mimics that space, with an AI-powered PHI-redaction microservice.

---

## Methodology, Materials, and Methods

When approaching the technologies for this project, I wanted to challenge myself with tools commonly seen in job postings for roles I want. This meant learning:

- **Java**  
- **Spring Boot + Spring Security**  
- **Docker**  
- **AWS Elastic Beanstalk**  
- **FastAPI**  
- **Hugging Face transformers**

### **Learning Java**
I started with a YouTube overview and completed the W3Schools Java tutorial. I focused on Java-specific features that differ from languages I already knew like C#. I practiced with small exercises and built a mini project before moving into Spring.

### **Learning Spring & Spring Boot**
I followed the official documentation and quickstart guides. I built a basic Spring Boot REST API, then expanded into the actual healthcare API. For Spring Security, I used tutorials, documentation, and some boilerplate code from GeeksforGeeks which I adapted to my needs.

### **Learning DevOps & AWS**
AWS was the hardest part. I used:
- My background from the AWS Cloud Practitioner course  
- Documentation  
- YouTube walkthroughs  
- OpenAI to help structure deployment steps  
- Stack Overflow for errors  

Elastic Beanstalk ended up being the best fit for this project after comparing deployment options for a Dockerized API.

### **Learning Docker**
Docker was more straightforward. I used the official docs and a short video explaining images, containers, and multi-container setups. Then I created Dockerfiles and a docker-compose setup for the project.

### **Learning NLP & Hugging Face**
I used class material from CSPB NLP, then explored the HuggingFace `ab-ai/pii_model`. I followed the model card and a Colab example to learn how to call the model in a microservice context.

---

## Results

### **What I Learned**
- Test-driven development, happy path vs. unhappy path, and guiding users toward the happy path  
- Java development practices, Maven, Spring Boot, Spring Security  
- JUnit and Mockito for testing  
- Integrating ML models into deployed microservices  
- FastAPI fundamentals  
- MVC design patterns and high-level software design  
- Docker containerization and solving the “works on my machine” problem  
- AWS Elastic Beanstalk for deployment and scaling  

### **How I Know I Learned It**
I can explain these tools, reproduce the workflows, deploy ML services, and build or debug Java projects. I'm not an expert in every detail, but I understand all concepts used in this project well enough to use them independently.

### **Project Assessment**
The project succeeded because it met all deliverables:
- 100% unit and integration test success  
- Docker-compose fully working  
- `/upload` endpoint creates clinical notes  
- Model redacts PHI and stores de-identified text  
- Compliance reports are generated correctly  
- Full workflow runs reliably  

It's not as polished as I'd like, but it exceeded the baseline goals.

---

## Discussion / Reflection

### **Did I Meet My Goals?**
Mostly, yes. I wish I had time for extra layers of error handling, deeper test coverage, NLP model metrics, and polish.

### **Why Was I Successful?**
I managed my time aggressively. Planning in Trello with structured deliverables prevented confusion and kept me moving weekly. Breaking tasks down and frontloading planning made everything easier.

Even if it wouldn’t impress every engineer, the project feels very “me.” It combined my background, my motivations, and my effort into something that only I would have built.

---

## Conclusion

Looking back, I can clearly see how much I learned—not only technical skills, but how to plan, troubleshoot, and execute a large multi-tech project. Early on, I had no idea what it would take to build something involving backend development, NLP, database modeling, Docker, and AWS all at once. Now I know I can handle it.

Finishing this gave me confidence in my ability to work in healthcare AI roles. It made the field feel realistic instead of aspirational. There is a lot I would improve—more testing, metrics, polish, maybe a UI—but the core functionality is real and functional.

This project convinced me that combining biology and CS was the right path, and it showed how I can keep building projects at this level going forward.

---

## References / Bibliography

- W3Schools. *Java Tutorial.*  
  https://www.w3schools.com/java/

- Spring. *Spring Boot: First Application Tutorial.*  
  https://docs.spring.io/spring-boot/tutorial/first-application/index.html

- YouTube. *Docker in 3 Minutes.*  
  https://youtu.be/DQdB7wFEygo?si=WjNbz3MmHrshpn2w

- Spring. *Spring Security Documentation.*  
  https://docs.spring.io/spring-security/reference/index.html

- AWS Skill Builder. *AWS Cloud Practitioner Essentials.*  
  https://skillbuilder.aws/learn/XUFYCSXHEU/aws-cloud-practitioner-essentials/GKB2YNYHCF

- Docker. *Docker CLI and Multi-Container Reference.*  
  https://docs.docker.com/reference/cli/docker/

- OpenAI. *ChatGPT.*  
  https://chatgpt.com/

- Hugging Face. *ab-ai / pii_model.*  
  https://huggingface.co/ab-ai/pii_model

- Stack Overflow. *AWS Elastic Beanstalk Deployment Troubleshooting.*  
  https://stackoverflow.com/questions/32645540/aws-elastic-beanstalk-deployment-failed

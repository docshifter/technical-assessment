### Technical Assessment for Software Engineer at DocShifter

#### Overview
This assessment evaluates your expertise in Java 21, Spring Framework, cloud-native services, DevOps practices, and system design. It focuses on document conversion and process automation, aligning with DocShifter's core business. The assessment consists of four sections, each designed to test different aspects of your skillset.

#### Section 1: Java and Spring Framework

**Task 1: Implement a Document Conversion Microservice**

Create a Spring Boot Application that converts documents from one format to another.

**Requirements:**
- Use Java 21 and Spring Boot 3.x.
- Implement a REST API with endpoints for:
  - Uploading a document
  - Requesting a conversion
  - Checking conversion status
  - Downloading the converted document
- Use Apache PDFBox or a similar library for actual conversion.
- Implement proper error handling and logging.
- Use Spring Data JPA with an in-memory database (H2) to store document metadata and conversion status.
- Include comprehensive unit and integration tests.
- Implement rate limiting to prevent API abuse.
- Fine-tune the JVM to handle memory spikes effectively.

**Bonus:**
- Use Spring Cloud Stream with a message-broker (i.e RabbitMQ / ActiveMQ Artemis) for asynchronous processing of conversion requests.
- Implement a caching mechanism


#### Section 2: Cloud and DevOps

**Task 2: Containerization and CI/CD Pipeline**

Set up a complete CI/CD pipeline for the microservice created in Task 1.

**Requirements:**
- Create a `Dockerfile` to containerize the application.
- Use GitHub Actions to create a CI/CD pipeline that:
  - Builds the project
  - Runs all tests
  - Performs static code analysis (e.g., with SonarQube)
  - Builds and pushes a Docker image to a registry
  - Deploys to a Kubernetes cluster (you can use minikube for local testing)
- Provide Kubernetes manifest files for deploying the application.
- Implement a blue-green deployment strategy.

**Bonus:**
- Set up monitoring and alerting using Prometheus and Grafana.
- Implement a chaos engineering test in your pipeline to ensure resilience.

#### Section 3: Front-End Development

**Task 3: Develop an Angular Web Application**

Create an Angular 16 web application that interacts with the microservice API.

**Requirements:**
- Implement a responsive design using Angular Material.
- Create a dashboard showing recent conversions and their statuses.
- Implement a file upload feature with drag-and-drop functionality.
- Display real-time conversion progress using WebSockets.
- Implement proper error handling and user notifications.
- Write unit tests for components and services.

**Bonus:**
- Implement user authentication and role-based access control.
- Add a feature to schedule document conversions for a future time.

#### Section 4: System Design

**Task 4: Design a Scalable Document Processing Platform**

Design a high-level architecture for a cloud-native, scalable document processing platform.

**Requirements:**
- Provide a detailed architecture diagram.
- Design for high availability, fault tolerance, and horizontal scalability.
- Include components for:
  - Document ingestion (handling various input methods)
  - Processing queue management
  - Conversion microservices for different document types
  - Result storage and retrieval
  - Monitoring and logging
- Explain how you would handle:
  - Sudden spikes in conversion requests
  - Large documents that take a long time to process
  - System failures during conversion processes
- Discuss security considerations and how you would address them.

**Bonus:**
- Propose an AI-driven component that could enhance the document conversion process or provide additional value to users.

#### Submission Guidelines

- Submit your solution as a GitHub repository.
- Include a comprehensive README with:
  - Setup and run instructions for all components
  - Explanation of architectural decisions
  - Any assumptions made
  - Ideas for future improvements
- Ensure all code is well-commented and follows best practices.

#### Evaluation Criteria

- Code quality, readability, and adherence to best practices
- Completeness and correctness of implemented features
- Test coverage and quality
- Scalability and resilience of the designed system
- Creativity in bonus implementations
- Quality of documentation and explanations

#### Timeline
You have 10 days to complete this assessment. This extended timeline allows for a more thorough implementation and documentation of your solution.
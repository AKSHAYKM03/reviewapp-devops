# ReviewApp – Java Spring Boot Application with DevOps

## Project Overview

ReviewApp is a Java-based web application built using Spring Boot and Maven. This project is used to practise application build, containerization, CI/CD automation, database integration, and cloud deployment.

The project demonstrates how a Java application can be built and deployed using modern DevOps tools and practices.

## Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Java |
| Framework | Spring Boot |
| Build Tool | Maven |
| Database | MariaDB |
| Version Control | Git, GitHub |
| CI/CD | Jenkins |
| Containerization | Docker |
| Container Orchestration | Kubernetes |
| Cloud Platform | AWS |
| Operating System | Linux |

## Project Structure

```text
reviewapp/
│
├── src/                 # Application source code
├── target/              # Maven build output
├── Jenkinsfile          # Jenkins pipeline configuration
├── pom.xml              # Maven dependencies and build configuration
├── dockerfile           # Docker image configuration
├── dbdockerfile         # Database Docker configuration
├── deployment.yaml      # Kubernetes deployment configuration
├── review.aws_ec2.yml   # AWS EC2 deployment configuration
└── README.md            # Project documentation
```

## Prerequisites

Install the following tools before running the project:

- Java JDK
- Maven
- Git
- Docker
- Jenkins (for CI/CD)
- Kubernetes (for container orchestration)
- AWS account (for cloud deployment)

## Running the Application Locally

**1. Clone the repository**

```bash
git clone https://github.com/AKSHAYKM03/reviewapp-devops.git
cd reviewapp-devops
```

**2. Build the application**

```bash
mvn clean package
```

**3. Run the application**

```bash
java -jar target/ReviewApp-0.0.1-SNAPSHOT.jar
```

Make sure the MariaDB database is running and the database connection settings are correctly configured before starting the application.

## Docker

Build the Docker image:

```bash
docker build -f dockerfile -t reviewapp .
```

Run the container:

```bash
docker run -d -p 8080:8080 --name reviewapp reviewapp
```

## Jenkins CI/CD

The repository includes a `Jenkinsfile` for pipeline automation.

The CI/CD workflow can include:

1. Source code checkout from GitHub.
2. Maven application build.
3. Build verification.
4. Docker image creation.
5. Application deployment.

## Kubernetes Deployment

The repository includes a Kubernetes deployment manifest.

Apply the deployment:

```bash
kubectl apply -f deployment.yaml
```

Check deployment status:

```bash
kubectl get deployments
kubectl get pods
kubectl get services
```

## Learning Objectives

- Understanding Java application build processes using Maven.
- Managing source code using Git and GitHub.
- Automating builds using Jenkins.
- Containerizing applications using Docker.
- Understanding Kubernetes deployments.
- Practising database integration.
- Learning application deployment on AWS EC2.

## Original Project Credit

This project is based on the training repository provided by **YagneshTrainer**.

Original repository: https://github.com/YagneshTrainer/reviewapp

My repository: https://github.com/AKSHAYKM03/reviewapp-devops

This repository is maintained as part of my hands-on Java, Cloud, and DevOps learning journey.

---

**Maintained by AKSHAY K M**

GitHub: https://github.com/AKSHAYKM03

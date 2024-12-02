# **BookshopDeployment-Code**

This repository contains the **frontend (React)** and **backend (Spring Boot)** code for the **bookshop application**, which is part of the **AppDeploymentProject-Infrastructure**. The repository uses **CI/CD pipelines** to automate Continuous Integration (CI) to **DockerHub** and Continuous Deployment (CD) to **Kubernetes (EKS)**.

## **CI/CD Pipelines**

- **Integration Pipeline**: Automatically triggered when changes are pushed to the repository. It:
  - Builds both frontend (React) and backend (Spring Boot) code.
  - Creates Docker images for both parts using respective Dockerfiles.
  - Pushes the images to **DockerHub**.

- **Deployment Pipeline**: Automatically triggered after the build pipeline completes. It:
  - Rolls out a **rolling update** to the Kubernetes deployment.
  - Updates the application by creating new pods from the updated Docker images and gradually terminates the old pods.

## **Key Features**

- **CI/CD Integration**: Fully automated pipelines to handle code building and deployment.
- **Dockerized Application**: Both the frontend and backend are packaged into Docker images for seamless deployment.
- **Rolling Updates**: Ensures zero downtime by gradually replacing old pods with new ones during deployment.

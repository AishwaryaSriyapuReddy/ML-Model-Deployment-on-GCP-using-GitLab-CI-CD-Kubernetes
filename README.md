# ML-Model-Deployment-on-GCP-using-GitLab-CI-CD-Kubernetes

## Table of Contents
📌 [Project Overview](#project-overview)  
📊 [Architecture](#architecture)  
⚙️ [Tech Stack](#tech-stack)  
🔄 CI/CD Pipeline Stages  
📊Project Workflow  
🧪 CircleCI Pipeline Testing  
🔄Model Deployment  
📝 Future Enhancements  

## Project Overview
This project is a practical MLOps implementation showcasing the building, testing, versioning, and deployment of a machine learning model with **GitLab as both an SCM and CI/CD automation platform**. In comparison to other projects where GitHub and Jenkins or CircleCI were used, this project showcases GitLab's native DevOps features, making it a robust all-in-one enterprise-grade machine learning workflow tool.

The machine learning task's core is a basic **Support Vector Machine (SVM) model** trained on a limited dataset to maintain the focus on deployment, automation, and infrastructure. The model pipeline, after being created and modularized, is containerized with **Docker**, pushed to **Google Container Registry (GCR)**, and deployed to **Google Kubernetes Engine (GKE)** with the help of **GitLab CI/CD pipelines**.

You'll also create a Flask-driven web app to host model predictions through an intuitive interface, supporting real-time input and output for end users.

## Architecture
GitLab CI/CD automates the pipeline from code commit to deployment by building Docker images, pushing them to Google Container Registry (GCR), and deploying them to a Google Kubernetes Engine (GKE) cluster. This enables seamless, scalable, and containerized ML app deployment directly from source control.

<img width="7623" height="600" alt="image" src="https://github.com/user-attachments/assets/2be2f09a-a2aa-4294-9c19-066ed7249ba3" />

## Tech Stack
| Category        | Tools Used                              |
|----------------|------------------------------------------|
| Language        | Python, HTML, CSS                       |
| ML Model        | Support Vector Machine (SVM)            |
| Web App         | Flask                                   |
| Data & Code Version Control | GitLab              |
| CI/CD           | GitLab CI/CD Pipelines                  |
| Containerization| Docker                                  |
| Registry        | Google Container Registry (GCR)         |
| Deployment      | Google Kubernetes Engine (GKE)          |
| Cloud Platform  | Google Cloud Platform (GCP)             |

## Project Workflow

1. **Project Setup**: Virtual environment, modular folder structure, logging & exception setup.
2. **Notebook Testing**: Run exploratory code in Jupyter to finalize model & preprocessing logic.
3. **Modular Code Implementation**: Move logic to classes/methods for production readiness.
4. **Flask App Development**: Create user-friendly UI for predictions.
5. **Training Pipeline**: Unified script for data processing & model training.
6. **Code & Data Versioning**: Use GitLab repositories (instead of GitHub/DVC).
7. **GCP Setup**: Create service accounts, container registry, Kubernetes cluster.
8. **CI/CD Pipeline**: Use `.gitlab-ci.yml` to automate build → test → deploy process.
9. **Deployment**: Dockerize app → Push to GCR → Deploy to GKE via GitLab pipeline.

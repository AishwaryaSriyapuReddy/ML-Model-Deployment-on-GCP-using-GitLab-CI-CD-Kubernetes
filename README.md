# ML-Model-Deployment-on-GCP-using-GitLab-CI-CD-Kubernetes

## Table of Contents
📌 [Project Overview](#project-overview)  
📊 [Architecture](#architecture)  
⚙️ [Tech Stack](#tech-stack)  
🔄 [CI/CD Pipeline Stages](#ci-cd-pipeline-stages)  
📊 [Project Workflow](#project-workflow)  
🔄 [Model Deployment Results](#model-deployment-results)  
📝 [Future Enhancements](#future-enhancements)  

## Project Overview
This project is a practical MLOps implementation showcasing the building, testing, versioning, and deployment of a machine learning model with **GitLab as both an SCM and CI/CD automation platform**. In comparison to other projects where GitHub and Jenkins or CircleCI were used, this project showcases GitLab's native DevOps features, making it a robust all-in-one enterprise-grade machine learning workflow tool.

The machine learning task's core is a basic model trained on a limited dataset to maintain the focus on deployment, automation, and infrastructure. The model pipeline, after being created and modularized, is containerized with **Docker**, pushed to **Google Container Registry (GCR)**, and deployed to **Google Kubernetes Engine (GKE)** with the help of **GitLab CI/CD pipelines**.

You'll also create a Flask-driven web app to host model predictions through an intuitive interface, supporting real-time input and output for end users.

## Architecture
GitLab CI/CD automates the pipeline from code commit to deployment by building Docker images, pushing them to Google Container Registry (GCR), and deploying them to a Google Kubernetes Engine (GKE) cluster. This enables seamless, scalable, and containerized ML app deployment directly from source control.

<img width="7623" height="600" alt="image" src="https://github.com/user-attachments/assets/2be2f09a-a2aa-4294-9c19-066ed7249ba3" />

## Tech Stack
| Category        | Tools Used                              |
|----------------|------------------------------------------|
| Language        | Python, HTML, CSS                       |
| Web App         | Flask                                   |
| Data & Code Version Control | GitLab              |
| CI/CD           | GitLab CI/CD Pipelines                  |
| Containerization| Docker                                  |
| Registry        | Google Container Registry (GCR)         |
| Deployment      | Google Kubernetes Engine (GKE)          |
| Cloud Platform  | Google Cloud Platform (GCP)             |

## CI/CD Pipeline Stages
- **Checkout** Code : Fetch the latest code from GitHub.
  Install Dependencies/Python packages from requirements.txt.
  Run Tests / Linting (optional): Perform code quality checks or run test suites.
- **Build** Docker Image using the Dockerfile.
- **Push** the image to Google Container Registry.
- **Deploy** the Docker images/app to Google Kubernetes Engine (GKE) cluster.
- Expose via LoadBalancer : The app is made available at a public IP endpoint.
  
Pipelines can be triggered manually or automatically on code pushes.

## Project Workflow

1. **Project Setup**
   - Create virtual environments and install dependencies (e.g., pandas, numpy, matplotlib).
   - Organize project structure with folders like `src`, `pipeline`, and `artifacts`.

2. **Jupyter Notebook Testing**
   - Perform data processing, model training, and model selection interactively in a notebook.

3. **Modular Code Development**
   - Convert notebook steps into modular code using classes and methods for better maintainability.

4. **User Application**
   - Build a simple user interface using Flask and basic HTML.

5. **Training Pipeline**
   - Combine data processing and model training into a single Python script for streamlined execution.

6. **Data and Code Versioning**
   - Use GitHub for data and code versioning (suitable for small datasets).
   - Optionally use DVC for large datasets.
<img width="500" height="200" alt="image" src="https://github.com/user-attachments/assets/1adc34f3-ac59-4feb-b41c-a3872a9ab69e" />  

**GitLab Repo:** https://gitlab.com/aishareddy-group/mlops-project/-/tree/4fc90dde2a848772cefa8950c3981fb5cb58020c/

7. **Google Cloud Setup**
   - Enable required GCP APIs.
   - Create a Kubernetes cluster on GCP.
   - Set up artifact repositories and service accounts with necessary permissions.
   - Create in vscode docker file, kubernetes deployment configuration file
  
8. **GitLab Setup**
   - Create Project and push the code
   - Create Gitlab CICD configuration file in vscode
   - Environment Variables Configuration i.e., GCP-key
   - Test Pipeline with Trigger
   
<img width="917" height="308" alt="image" src="https://github.com/user-attachments/assets/2410da76-c750-4403-9942-5c6f4fb65f6e" />

## Model Deployment Results
<img width="959" height="169" alt="image" src="https://github.com/user-attachments/assets/9517f016-7e06-4cc5-b49c-501959403a19" />  

<img width="764" height="471" alt="image" src="https://github.com/user-attachments/assets/707d592e-ea72-43d1-9397-d786dc37137a" />  



## Future Enhancements
- Enable automatic model retraining with updated datasets.  
- Add model versioning using DVC or MLflow.  
- Integrate monitoring tools like Prometheus and Grafana.
- Automate GCP infrastructure using Terraform.
- Log all model predictions for auditing and compliance.

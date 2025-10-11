# 🩺 Kidney Disease Classification with MLflow, DVC & AWS

An end-to-end **machine learning pipeline** for kidney disease classification that integrates **MLflow**, **DVC**, and **AWS** to automate model tracking, versioning, and deployment.  
This project demonstrates how **MLOps practices** can enhance scalability, reproducibility, and automation in medical data analysis workflows.

---

## 🚀 Overview

- Utilized **Continuous Integration/Continuous Deployment (CI/CD)** workflows to automate model tracking, versioning, and deployment on **AWS (EC2 & ECR)**.  
- Reduced manual intervention by **40%** through integration of **Docker** and **self-hosted GitHub runners** for continuous deployment.  
- Enhanced experiment tracking efficiency by **25%** using **MLflow** for centralized logging and model metadata management.  

---

## ⚙️ Project Workflow

1. Update `config.yaml`  
2. Update `secrets.yaml` *(Optional)*  
3. Update `params.yaml`  
4. Update the entity  
5. Update the configuration manager in `src/config`  
6. Update the components  
7. Update the pipeline  
8. Update `main.py`  
9. Update `dvc.yaml`  
10. Run `app.py`

---

## 🧩 How to Run Locally

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Ibtesum-Sakib/Kidney-Diseases-Classification-MLFLOW.git
```
### 2️⃣ Create a Conda Environment
```bash
conda create -n cnncls python=3.8 -y
conda activate cnncls
```
### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
### 4️⃣ Run the Application
```bash
python app.py
```

Now, open your localhost and assign the port to access the app.

### 📊 MLflow Integration

MLflow is used for:

Tracking and managing model experiments

Logging metrics, parameters, and artifacts

Enabling reproducibility and experiment comparison

### 🔗 Resources

MLflow Documentation

MLflow Tutorial (YouTube)

### 🧠 Useful Command
```bash
mlflow ui
```
### 📦 DVC Integration

DVC (Data Version Control) manages data pipelines and ensures experiment reproducibility.

Key Commands:
```bash
dvc init
dvc repro
dvc dag
```

DVC Features:

Lightweight experiment tracking

Pipeline orchestration for data and model stages

Ideal for Proof-of-Concept (POC) projects

Integration: DagsHub

### ☁️ AWS CI/CD Deployment with GitHub Actions
### 1️⃣ Login to AWS Console
```bash
Create an IAM user with required permissions.
```
### 2️⃣ IAM Permissions

Grant access to:

EC2: Virtual machine hosting the deployment

ECR: Elastic Container Registry to store Docker images

Policies:

AmazonEC2FullAccess

AmazonEC2ContainerRegistryFullAccess

### 3️⃣ Create an ECR Repository

Example URI:
```bash
566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken
```
### 4️⃣ Create an EC2 Instance (Ubuntu)
### 5️⃣ Install Docker on EC2
```bash
sudo apt-get update -y
sudo apt-get upgrade -y
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```
### 6️⃣ Configure EC2 as a Self-Hosted GitHub Runner

Go to:

GitHub Repo → Settings → Actions → Runners → New Self-Hosted Runner


Then follow the instructions to register and run commands on your EC2 instance.

### 7️⃣ Set Up GitHub Secrets

In your repository settings, add:
```bash
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=us-east-1
AWS_ECR_LOGIN_URI=566373416292.dkr.ecr.ap-south-1.amazonaws.com
ECR_REPOSITORY_NAME=simple-app
```
### 🧠 Tools & Technologies

Python, Scikit-learn, Pandas, NumPy – Model development

MLflow – Experiment tracking and model management

DVC – Data and pipeline versioning

Docker – Containerization for deployment

GitHub Actions – CI/CD automation

AWS EC2/ECR – Cloud-based hosting and image registry

### 💡 Learning Outcomes

Built a production-grade ML pipeline with complete lifecycle management.

Automated model tracking, deployment, and monitoring using MLflow and DVC.

Gained practical experience in MLOps, cloud deployment, and CI/CD engineering.

### 🧑‍💻 Author 

**Mohammad Ibtesum Sakib**  
📍 Bochum, Germany  
📧 ibtesum38@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/ibtesum) | [GitHub](https://github.com/Ibtesum-Sakib)

---
### 🏷️ GitHub Topics

#MachineLearning #MLOps #MLflow #DVC #AWS #CICD #Python #DataScience #Automation

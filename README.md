# CI-CD-Pipeline-for-Scalable-Python-Application

## Project Overview

This project demonstrates an end-to-end **CI/CD pipeline** for deploying a Python web application on AWS using Infrastructure as Code.
The infrastructure is provisioned using **Terraform**, while **Jenkins** automates the build and deployment process through integration with **GitHub**.

The architecture follows a scalable and production-style design using **AWS VPC, EC2, Application Load Balancer, and Auto Scaling**.

---

## Architecture

GitHub → Jenkins → Terraform → AWS Infrastructure → Python Application Deployment

Components used:

* Custom VPC
* Public and Private Subnets
* Internet Gateway
* EC2 Instances (Application servers)
* Application Load Balancer (ALB)
* Auto Scaling Group
* Jenkins CI/CD Pipeline
* Terraform Infrastructure as Code

---

## Tech Stack

**Programming & Scripting**

* Python
* Bash

**DevOps Tools**

* Git
* GitHub
* Jenkins
* Terraform

**Cloud Platform**

* AWS (EC2, VPC, ALB, Auto Scaling, IAM)

**Operating System**

* Linux (Ubuntu)

---

## Project Structure

```
CI-CD-PythonProject
│
├── app
│   ├── app.py
│   └── requirements.txt
│
├── terraform
│   ├── main.tf
│   ├── provider.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── jenkins
│   └── Jenkinsfile
│
└── README.md
```

---

## Application Description

A simple **Python Flask web application** is deployed on EC2 instances.
The application returns a message confirming successful deployment through the CI/CD pipeline.

Example endpoint:

```
http://<load-balancer-dns>
```

---

## Infrastructure Provisioning (Terraform)

Terraform is used to provision the AWS infrastructure including:

* VPC creation
* Public and private subnet configuration
* Internet gateway and route tables
* Security groups
* Application Load Balancer
* EC2 launch template
* Auto Scaling group

Terraform enables **repeatable and automated infrastructure deployment**.

---

## CI/CD Pipeline (Jenkins)

The Jenkins pipeline automates the deployment process.

Pipeline stages include:

1. **Clone Repository** – Jenkins pulls the latest code from GitHub
2. **Terraform Init** – Initializes Terraform configuration
3. **Terraform Plan** – Validates infrastructure changes
4. **Terraform Apply** – Deploys AWS infrastructure automatically

The pipeline can be triggered automatically using **GitHub Webhooks**.

---

## Deployment Workflow

1. Developer pushes code to GitHub
2. GitHub triggers Jenkins using Webhooks
3. Jenkins executes the pipeline
4. Terraform provisions or updates AWS infrastructure
5. Application is deployed to EC2 instances behind a Load Balancer

---

## Prerequisites

Before running this project, ensure the following tools are installed:

* AWS CLI
* Terraform
* Jenkins
* Git
* Python 3

AWS credentials must also be configured.

---

## Setup Instructions

### Clone the repository

```
git clone https://github.com/your-username/CI-CD-Pipeline-for-Scalable-Python-Application.git
cd CI-CD-PythonProject
```

### Initialize Terraform

```
cd terraform
terraform init
```

### Deploy Infrastructure

```
terraform apply
```

---

## Key Features

* Infrastructure provisioning using Terraform
* Automated deployment pipeline using Jenkins
* Scalable AWS architecture
* High availability using Application Load Balancer
* Auto Scaling for dynamic workload handling
* GitHub integration for CI/CD automation

---

## Learning Outcomes

Through this project, the following concepts were implemented:

* Infrastructure as Code using Terraform
* Continuous Integration and Continuous Deployment with Jenkins
* AWS networking and compute services
* CI/CD automation using GitHub and Webhooks
* Deployment of cloud-based scalable applications

---

## Future Improvements

* Add monitoring using CloudWatch
* Implement Terraform modules
* Add automated testing in Jenkins pipeline
* Implement multi-environment deployments (dev / staging / prod)

---

## Author

**Abinaya**

DevOps & Cloud Enthusiast

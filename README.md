🚀 Scalable Spring Boot Application on AWS

This project demonstrates how to deploy a scalable, highly available Spring Boot application on AWS using DevOps tools and Infrastructure as Code (IaC) principles.

🛠️ Tech Stack

Jenkins – CI/CD automation

Packer – Custom AMI creation

Ansible – Server configuration management

Terraform – Infrastructure provisioning (IaC)

AWS Services

EC2

Application Load Balancer (ALB)

Auto Scaling Group (ASG)

RDS

Secrets Manager

CloudWatch

📌 Architecture Overview
flowchart LR

    Developer -->|Push Code| GitHub
    GitHub -->|Webhook Trigger| Jenkins

    Jenkins -->|Build & Test| SpringBootBuild
    Jenkins -->|Create AMI| Packer
    Packer -->|Provision via| Ansible
    Packer -->|Custom AMI| AWSAMI

    Jenkins -->|Trigger IaC| Terraform
    Terraform -->|Provision| VPC
    Terraform -->|Provision| ALB
    Terraform -->|Provision| ASG
    Terraform -->|Provision| RDS

    ASG -->|Launch EC2 from AMI| EC2
    EC2 -->|Registered To| ALB
    ALB -->|Route Traffic| EC2

    EC2 -->|Connect| RDS
    EC2 -->|Send Logs| CloudWatch

# Scalable Spring Boot Application on AWS

This project demonstrates how to deploy a scalable and highly available Spring Boot application on AWS using DevOps tools and Infrastructure as Code.

## Tools Used
- Jenkins – CI/CD automation
- Terraform – Infrastructure provisioning
- Packer – AMI creation
- Ansible – Server configuration
- AWS – EC2, ALB, Auto Scaling, RDS, Secrets Manager, CloudWatch

## Workflow
1. Jenkins builds the Spring Boot application
2. Packer creates a custom AMI using Ansible
3. Terraform provisions AWS infrastructure
4. Application runs behind an Application Load Balancer
5. Logs are sent to CloudWatch

## Author
Vibhakar Kumar

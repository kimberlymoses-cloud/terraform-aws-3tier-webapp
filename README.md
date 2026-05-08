# terraform-aws-3tier-webapp
Hands on lab experience using Terraform

# Terraform AWS 3-Tier Web Application

## 🚀 Project Overview
Deployed a highly available 3-tier web architecture on AWS using Infrastructure as Code (Terraform). Zero manual AWS Console clicks. This mirrors real-world Solutions Architect workflows.

**Architecture**: Internet → ALB → EC2 Web Servers (Multi-AZ) → Private Subnets
**Why it matters**: Demonstrates VPC networking, security groups, load balancing, IaC, and high availability — core SAA exam + job requirements.

## 🏗️ Architecture Diagram

Internet
|
v
[Application Load Balancer] ← Public Subnets (us-west-2a, us-west-2b)
|
v
[EC2 Web Server 1] [EC2 Web Server 2] ← Private Subnets (Multi-AZ)
|
v
[Security Groups: Web SG → DB SG] ← Least-privilege access

🎯 Skills Demonstrated
VPC Design: Public/private subnet tiering across 2 AZs
Security: DB isolated in private subnet, only web SG can access port 3306
High Availability: Multi-AZ EC2 + ALB health checks
IaC: 100% reproducible infrastructure, version controlled
SAA Concepts: Matches exam domains 1 & 3 — Design Resilient/Secure Architectures

Next Steps
Add RDS MySQL in private subnet
Add NAT Gateway for EC2 patching
Remote state with S3 + DynamoDB locking
GitHub Actions CI/CD for
terraform plan

👩🏽‍💻 Author
Kimberly Moses — AWS SAA in Progress | RRT → Cloud Engineer
Former Registered Respiratory Therapist combining 7+ years clinical expertise with AWS infrastructure. Building HIPAA-eligible architectures.

# terraform-aws-3tier-webapp
Hands on lab experience using Terraform

# Terraform AWS 3-Tier Web Application

## 🚀 Project Overview
Deployed a highly available 3-tier web architecture on AWS using Infrastructure as Code (Terraform). Zero manual AWS Console clicks. This mirrors real-world Solutions Architect workflows.

**Architecture**: Internet → ALB → EC2 Web Servers (Multi-AZ) → Private Subnets
**Why it matters**: Demonstrates VPC networking, security groups, load balancing, IaC, and high availability — core SAA exam + job requirements.

## 🏗️ Architecture Diagram

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/3b2843bf0b81c9cf9ae3145e1bb62464468cecfa/Install%20Teraform.png)

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/b62f84e83d294a844409882774b36a0f14a721b2/VPC%20with%20public%3Aprivate%20subnets%20across%202%20AZs.png)

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/d8daf0525e625e24d8e01a3e89d53fb71b4e90f1/VPC%20with%20public%3Aprivate%20subnets%20across%202%20AZs.1.png)

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/0c1cbe3e54765f2c76ac75128aa1c3f09a80fa75/Firewall%20rules%20for%20database.png)

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/5a709b97343cb1d85d4d7ac7108fafd85ea656ef/Web%20servers%20autoinstalls%20Apache.png)

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/bb055ca8fe2eac0973f2cbbc0a55b091ec782901/Web%20servers%20autoinstalls%20Apache.1.png)

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/921be4c6028ce3f4fad0fee4376ddd50a2c3bb75/Load%20balancer%20in%20front%20of%202%20servers.png)

[image alt](https://github.com/kimberlymoses-cloud/terraform-aws-3tier-webapp/blob/c20602161e8a498ef72c7a1b9279ddfce5be81a8/Load%20balancer%20in%20front%20of%202%20servers.1.png)



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

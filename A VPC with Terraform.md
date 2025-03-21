# AWS VPC Deployment with Terraform

## Cloud Provider
- Amazon Web Services (AWS)

## Objective
This guide walks through deploying a **Virtual Private Cloud (VPC)** on AWS using **Terraform**. The goal is to automate network infrastructure provisioning efficiently while ensuring scalability and security.

### Steps to Complete:
1. Install Terraform [Download Terraform](https://www.terraform.io/downloads.html)
2. Set up and initialize the Terraform workspace.
3. Design the network architecture (Recommended: [Draw.io](https://www.draw.io/)).
4. Deploy the following AWS resources using Terraform:
   - Virtual Private Cloud (VPC)
   - Route Tables (Public & Private)
   - Route Table Associations
   - Internet Gateway
   - Elastic IP
   - NAT Gateway
   - EC2 Instances (1 Public, 1 Private) - Amazon Linux 2 AMI
   - Security Groups
5. Validate the connectivity between the instances.
6. Destroy the Terraform-managed infrastructure.
7. Confirm the complete deletion of all resources.

### Network Architecture
![AWS VPC Architecture](Image.png)

---
## Infrastructure as Code (IaC) Overview

### **What is Infrastructure as Code (IaC)?**
**Infrastructure as Code (IaC)** is the practice of defining and managing IT infrastructure using code instead of manual configurations. This approach enables automation, consistency, and version control.

#### **Benefits of IaC:**
- **Automation:** Eliminates manual errors and speeds up deployments.
- **Consistency:** Ensures uniformity across different environments (Dev, Test, Prod).
- **Version Control:** Changes are tracked and can be rolled back if necessary.
- **Scalability:** Infrastructure can be modified dynamically with minimal effort.

---
## Terraform Fundamentals

### **What is Terraform?**
Terraform is an open-source tool from **HashiCorp** for defining, provisioning, and managing infrastructure using **HashiCorp Configuration Language (HCL)**. It supports multiple cloud providers, making it ideal for multi-cloud deployments.

#### **Key Features:**
- **Cloud-Agnostic:** Works across AWS, Azure, GCP, and other platforms.
- **Declarative Approach:** Users define the desired infrastructure state, and Terraform handles the execution.
- **State Management:** Uses a state file to track deployed resources and changes.
- **Plan & Apply:** Users can preview changes before applying them.

### **What is the Terraform State File?**
A **state file** is used by Terraform to track the infrastructure's current state. It serves as a reference to ensure consistency between the deployed resources and the defined configurations.

#### **Why is the State File Important?**
- **Resource Mapping:** Links real-world resources to Terraform configurations.
- **Optimization:** Reduces unnecessary API calls for faster deployments.
- **Dependency Management:** Maintains relationships between resources.
- **Collaboration:** Enables shared access to infrastructure definitions.

---
## When to Use Infrastructure as Code
IaC is essential in various scenarios, including:

1. **Cloud Infrastructure Management:** Automate cloud resource provisioning.
2. **Multi-Environment Consistency:** Ensure uniformity across development, staging, and production environments.
3. **Disaster Recovery:** Quickly restore infrastructure using predefined scripts.
4. **Scaling & Load Balancing:** Dynamically adjust infrastructure as needed.
5. **Version Control & Auditability:** Track infrastructure changes over time.
6. **Collaboration Across Teams:** Standardize infrastructure management across multiple teams.
7. **Hybrid & Multi-Cloud Strategies:** Deploy resources across multiple cloud providers.
8. **Security & Compliance:** Define infrastructure policies as code to enforce best practices.

---
## Resources
- [Terraform Official Documentation](https://www.terraform.io/)
- [Terraform Module Registry](https://registry.terraform.io/)

## Cost Considerations
- Most services used in this deployment fall under AWS Free Tier.

## Estimated Completion Time
- Approximately **30 minutes**

## Pro Tips
- Properly indent Terraform files for readability.
- Create **dependencies** where necessary to ensure correct resource creation order.
- Consider pre-generating an **AWS Key Pair** to enable SSH access to EC2 instances.

---
## Deployment Output
![Terraform Deployment Output](Image.gif)

###Steps to run a plan 
# Self-Healing NGINX Platform (AWS)

## Why AWS?
AWS provides mature, well-integrated primitives (ALB + Auto Scaling Groups)
that naturally support self-healing, load balancing, and N+1 capacity with
minimal configuration and no additional services.

## Requirements Mapping

1. **Self-healing**
   - EC2 Auto Scaling Group automatically replaces terminated instances.

2. **Self-provisioning (IaC only)**
   - Entire stack is deployed using Terraform.
   - Re-running `terraform apply` results in no changes (idempotent).

3. **N + 1 Capacity**
   - Minimum of 2 EC2 instances behind an Application Load Balancer.

4. **Static Web Page**
   - Default NGINX welcome page served on port 80.

5. **Templates**
   - Terraform (latest version). 

## Architecture diagram

<img width="5047" height="6680" alt="Mermaid Chart - Create complex, visual diagrams with text -2025-12-18-123119" src="https://github.com/user-attachments/assets/6f5eed9c-d822-4fc2-8643-222d38a237cc" />




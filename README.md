
# AWS Infrastructure with Terraform

This Terraform configuration creates a complete AWS infrastructure with the following components:

## Architecture Overview

- **VPC** with DNS support
- **Public Subnet** with Internet Gateway access
- **Private Subnet** with NAT Gateway for outbound access
- **Bastion Host** in public subnet for SSH access
- **Private EC2 Instance** in private subnet
- **S3 VPC Endpoint** for private S3 access
- **Security Groups** with proper access controls
- **IAM Roles** for S3 access from EC2

## Prerequisites

1. AWS CLI configured with appropriate credentials
2. Terraform installed (>= 1.0)
3. SSH key pair generated (`ssh-keygen -t rsa -b 2048`)

## Deployment Steps

1. **Clone and Navigate**
   ```bash
   cd terraform-aws-infrastructure
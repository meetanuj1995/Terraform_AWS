# AWS Infrastructure Deployment with Terraform

This repository contains Terraform code to deploy infrastructure on AWS. The infrastructure includes a Virtual Private Cloud (VPC), subnets, an Internet Gateway, a Route Table, security groups, EC2 instances, an S3 bucket, and an Application Load Balancer (ALB).

### Architecture:
The Terraform configuration deploys the following resources:

1. VPC with a specified CIDR block.
2. Subnets: Two public subnets in different availability zones.
3. Internet Gateway: To allow internet access.
4. Route Table: With a default route to the Internet Gateway.
5. Security Group: Allowing HTTP and SSH access.
6. EC2 Instances: Two instances in different subnets.
7. S3 Bucket: A simple S3 bucket.
8. Application Load Balancer: Distributing traffic between the EC2 instances.

### Pre-requisites:
- Terraform installed on your machine.
- AWS account and IAM user with the necessary permissions.
- AWS CLI configured with your AWS credentials.

### Configure AWS CLI:
  Set up the AWS CLI with your credentials.

### Set Up Your Project Directory:
  Create a directory for your Terraform project and navigate into it.

### Create Terraform Configuration Files:
+ main.tf: *The main configuration file where you define the resources you want to create.*
+ variables.tf: *Defines the input variables for your Terraform configuration.*
+ outputs.tf: *Defines the outputs of your Terraform configuration.*
+ provider.tf: *Specifies the provider (AWS in this case) and any provider-specific configurations.*
+ terraform.tfvars: *Defines the values for the input variables.*

### Initialize Terraform:
  Initialize the Terraform working directory. This step downloads the provider plugins and sets up the backend for storing the state.

### Plan the Deployment:
  Generate an execution plan to preview the actions Terraform will take to achieve the desired state.

### Apply the Configuration:
  Apply the Terraform configuration to deploy the resources on AWS.

### Access the Application:
  After the deployment is complete, you can access your application using the DNS name of the load balancer, which will be provided as an output.

### Cleanup:
  Finally, destroy the infrastructure to avoid ongoing costs.




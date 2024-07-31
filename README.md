# AWS Cloud Resume API Challange

### Introduction

This project illustrates a serverless architecture for a Resume API utilizing AWS Lambda and DynamoDB. The Lambda function fetches resume data from DynamoDB and returns it in JSON format. The setup includes GitHub Actions for automated deployment and Terraform Cloud for infrastructure management and resource provisioning.

### Prerequisites

- Install terraform
- configure AWS CLI
- Terraform Cloud

### Operational Overview

- API Gateway: Directs requests to the AWS Lambda function.
  -AWS Lambda: Runs serverless code to retrieve resume data from DynamoDB based on the provided ID and returns it in JSON format.
- DynamoDB: A NoSQL database that stores and structures resume data for efficient retrieval by the Lambda function.

### Setup and Deployment

1. Define your Infrastructure Using Terraform:
   - Start by configuring your AWS infrastructure with Terraform. Your Terraform configuration files, including main.tf, will specify the necessary resources such as Lambda functions, DynamoDB tables, S3 buckets, and API Gateway.
   - Review and adjust main.tf to meet your infrastructure needs.
2. Deploy with Terraform Cloud:
   - Utilize Terraform Cloud for deploying your resources. Terraform Cloud offers a collaborative environment for executing and managing your Terraform configurations.
   - Link your GitHub repository with Terraform Cloud to automate the management of your Terraform state file and trigger deployments.
   - Set up Terraform Cloud to monitor changes in your GitHub repository, automatically triggering runs and applying updates when modifications are made to your Terraform configurations.
   - Ensure your Terraform Cloud workspace is configured with the necessary AWS credentials and variables.
3. Upload DynamoDB Items:
   - Incorporate an additional step in your GitHub Actions workflow to upload JSON data to DynamoDB. This ensures that the database is updated with the latest resume information as part of the continuous deployment process.
4. Deploy API:
   - Verify that your API Gateway and Lambda function are correctly deployed and properly linked. This should be managed through your Terraform configuration, with updates applied via Terraform Cloud.

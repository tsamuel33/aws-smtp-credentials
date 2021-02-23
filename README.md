# aws-smtp-credentials
CloudFormation template to generate SMTP credentials

## Purpose
This template creates a Lambda-backed custom resource type for creating SMTP credentials via AWS CloudFormation. The username and password are stored in Parameter Store as a SecureString under the names "smtp-username" and "smtp-password".

## Resources
The template deploys the following resources:
* IAM User
* IAM Group
* IAM Policy
* IAM Access Keys
* IAM Role
* CloudWatch Log Group
* Lambda Function
* Systems Manager Parameters

## Requirements
The following high-level requirements are necessary to execute the template:
* The IAM user/role that deploys the template must have permissions to create the resource types listed above other than the Systems Manager parameters
* A KMS key that allows use by Systems Manager must exist in the account.

# AWS Security Groups and IAM Roles Implementation

This repository demonstrates the implementation of **AWS Security Groups** and **IAM Roles** for securing resources and managing access permissions within AWS.

## Overview

- **Security Groups:** Act as virtual firewalls to control inbound and outbound traffic to AWS resources (like EC2 instances).
- **IAM Roles:** Used to grant permissions to entities such as EC2 instances, Lambda functions, or users to interact with other AWS services securely.

This repository contains example scripts and configurations for setting up both Security Groups and IAM Roles.

---

## Task 1: Implement Security Groups

### Objective:
- Create and configure **Security Groups** for EC2 instances, controlling inbound and outbound traffic.

### Steps:
1. **Create a Security Group:**
   - Define inbound and outbound rules to allow specific traffic, such as SSH, HTTP, or custom ports.
   
2. **Attach the Security Group to an EC2 instance:**
   - Ensure that only the allowed traffic reaches your EC2 instance.


# Task 2: Implement IAM Roles

## Objective
The goal of this task is to create and configure IAM (Identity and Access Management) Roles that securely grant access to specific AWS services (e.g., S3, DynamoDB) for EC2 instances or other AWS resources without the need to hardcode credentials.

## Steps

### 1. Create an IAM Role
1. Navigate to the IAM Dashboard in the AWS Management Console.
2. Select **Roles** from the left-hand navigation menu.
3. Click on **Create Role**.
4. Choose the type of trusted entity:
    - **AWS Service**: Select the service that will use this role (e.g., EC2 or Lambda).
5. Click **Next: Permissions**.
6. Attach the necessary policy to grant access to specific AWS services like S3 or DynamoDB:
    - For example, select **AmazonS3FullAccess** or **AmazonDynamoDBFullAccess** depending on your use case.
7. Click **Next: Tags** (optional), and then **Next: Review**.
8. Name your role (e.g., `EC2-S3-Access-Role`) and provide a description (optional).
9. Click **Create Role**.

### Now we can Attach the IAM Role to an EC2 Instance or Lambda Function 

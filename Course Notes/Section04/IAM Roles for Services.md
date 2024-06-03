# IAM Roles for Services

AWS Services also use IAM roles and permissions.

Common roles include:

- EC2 Instance Roles
- Lambda Function Roles
- Roles for CloudFormation

## Creating IAM Roles for Services

In the AWS Console, go roles => create role. There is an option to create a role for an AWS service. During that process, you can select options for which service the new role applies to (ex: EC2) and some limitations on that service. For example, in the walkthrough we created an EC2 service with permissions for IAM: Read Only.

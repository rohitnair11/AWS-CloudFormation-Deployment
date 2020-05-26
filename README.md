# AWS-CloudFormation-Deployment

In this project, AWS CloudFormation is used to create the infrastructure and then deploy an Apache Web Server application on AWS. The web application is already stored in the AWS S3 bucket.  

The following components are created using the CloudFormation script:  
* VPC
* Public Subnets
* Private Subnets
* Internet Gateway
* Internet Gateway Attachment
* NAT Gateways
* Public Route Table
* Private Route Table
* Load Balancer
* Auto Scaling
* IAM Roles
* Load Balancer Security Group
* Web Server Security Group
* Web App Launch Configuration
* Listener

A Launch Configuration is created in order to deploy the four servers, two located in each of the private subnets.  
An IAM role is created to access the application code stored in the S3 bucket.  

---

### Dependencies
##### AWS account
You would require to have an AWS account to be able to build cloud infrastructure.  
##### AWS CLI
The AWS command line tool should be installed to run the script.  

--- 

### Running Instructions
To create a new stack, you need to run the create.sh script by providing the stack name, script file and the parameters file.  
```$ ./create.sh <StackName> deploy-script.yml params.json```  

To update an already created stack:  
```$ ./update.sh <StackName> deploy-script.yml params.json```

---

### Note
Make sure you delete the stack and all other created resources to avoid charges.

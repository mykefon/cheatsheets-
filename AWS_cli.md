AWS CLI cheat sheet that covers some of the most common commands and options:

## Configuration and Authentication

aws configure: Configures your AWS credentials, including your access key and secret access key.

aws sts get-caller-identity: Displays the IAM user or role that is currently authenticated.

# EC2 Instances

aws ec2 run-instances: Launches a new EC2 instance.

aws ec2 describe-instances: Lists information about all running EC2 instances.

aws ec2 start-instances: Starts one or more stopped EC2 instances.

aws ec2 stop-instances: Stops one or more running EC2 instances.

aws ec2 terminate-instances: Terminates one or more EC2 instances.

# S3 Buckets

aws s3 mb s3://[bucket-name]: Creates a new S3 bucket with the specified name.

aws s3 ls: Lists all S3 buckets in your account.

aws s3 cp [source] [destination]: Copies a file from a local source to an S3 bucket.

aws s3 sync [source] s3://[bucket-name]/[destination]: Syncs the contents of a local directory to an S3 bucket.

# Lambda Functions

aws lambda create-function: Creates a new Lambda function.

aws lambda update-function-code: Updates the code for an existing Lambda function.

aws lambda invoke: Invokes a Lambda function.

aws lambda list-functions: Lists all Lambda functions in your account.
# CloudFormation Stacks

aws cloudformation create-stack: Creates a new CloudFormation stack.

aws cloudformation update-stack: Updates an existing CloudFormation stack.

aws cloudformation describe-stacks: Lists information about all CloudFormation stacks in your account.

aws cloudformation delete-stack: Deletes a CloudFormation stack.

# Elastic Beanstalk

aws elasticbeanstalk create-application: Creates a new Elastic Beanstalk application.

aws elasticbeanstalk create-environment: Creates a new Elastic Beanstalk environment.

aws elasticbeanstalk update-environment: Updates an existing Elastic Beanstalk environment.

aws elasticbeanstalk describe-environments: Lists information about all Elastic Beanstalk environments in your account.

## Note: 

This is not an exhaustive list, and there are many other AWS CLI commands and options available. However, these are some of the most commonly used commands that should be sufficient for most basic AWS workflows.

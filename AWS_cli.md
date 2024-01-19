AWS CLI cheat sheet that covers some of the most common commands and options:

## Configuration and Authentication

aws configure: Configures your AWS credentials, including your access key and secret access key.

aws sts get-caller-identity: Displays the IAM user or role that is currently authenticated.

aws sts get-caller-identity --query Account --output text: This command retrieves your AWS account ID associated with the current AWS CLI configuration.

aws sts assume-role --role-arn <role-arn> --role-session-name <session-name>: Use this command to assume an IAM role and obtain temporary security credentials. Replace <role-arn> with the ARN of the IAM role, and <session-name> with a name for the assumed role session.

aws sts get-session-token --duration-seconds <duration-seconds>: This command generates temporary session credentials (access key, secret access key, and session token). Specify the desired duration of the session in <duration-seconds>.

aws configure set mfa_serial <mfa-serial>: Use this command to enable MFA by specifying the MFA device ARN in <mfa-serial>.

aws s3 ls --region <region-name>: This command overrides the default region specified in the AWS CLI configuration and sets the region for a specific command. Replace <region-name> with the desired AWS region.

aws ec2 describe-regions --query 'Regions[].RegionName' --output text: This command lists all the available AWS regions that you can use in your commands.

aws configure --profile <profile-name>: Use this command to create a new named profile in the AWS CLI configuration. Replace <profile-name> with the desired name for the profile.

aws configure list: This command displays the current AWS CLI configuration, including the active profile, default region, and default output format.
export AWS_PROFILE=<profile-name>: Use this command to set the AWS profile to use if you have multiple profiles configured in the AWS CLI. Replace <profile-name> with the name of the desired profile.

aws configure set default.output <output-format>: Use this command to set the default output format for AWS CLI commands. Replace <output-format> with the desired format, such as "json", "text", "table", etc.

aws sts assume-role --role-arn <role-arn> --role-session-name <session-name> --external-id <external-id>: This command assumes an IAM role and requires providing an external ID for additional security. Replace <role-arn> with the ARN of the IAM role, <session-name> with a name for the assumed role session, and <external-id> with the external ID associated with the role.

aws <command> --profile <profile-name>: By appending --profile <profile-name> to an AWS CLI command, you can specify the AWS profile to use for that specific command. Replace <profile-name> with the desired AWS profile.

export AWS_ACCESS_KEY_ID=<access-key>
export AWS_SECRET_ACCESS_KEY=<secret-access-key>
export AWS_SESSION_TOKEN=<session-token>:  Use these commands to set the environment variables for AWS CLI authentication. Replace <access-key>, <secret-access-key>, and <session-token> with the appropriate values.

aws configure list-profiles: This command lists all the profiles configured in the AWS CLI.

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

1. aws cloudformation create-stack --stack-name STACK_NAME --template-body file://template.json --parameters ParameterKey=Key,ParameterValue=Value --capabilities CAPABILITY_IAM

2. aws cloudformation update-stack --stack-name STACK_NAME --template-body file://template.json --parameters ParameterKey=Key,ParameterValue=Value --capabilities CAPABILITY_IAM

3. aws cloudformation describe-stacks: Lists information about all CloudFormation stacks in your account.

4. aws cloudformation delete-stack --stack-name STACK_NAME

5. aws cloudformation delete-stack-drift-detection-status --stack-drift-detection-id DETECTION_ID

6. aws cloudformation describe-stack-drift-detection-status --stack-drift-detection-id DETECTION_ID

7. aws cloudformation detect-stack-drift --stack-name STACK_NAME

8. aws cloudformation list-stack-resources --stack-name STACK_NAME

9. aws cloudformation get-template --stack-name STACK_NAME

10. aws cloudformation validate-template --template-body file://template.json

11. aws cloudformation describe-stack-resources --stack-name STACK_NAME

12. aws cloudformation list-stacks

# EKS

1. aws eks create-cluster --name <cluster-name> --role-arn <eks-service-role-arn> --resources-vpc-config subnetIds=<subnet-ids>,securityGroupIds=<security-group-id>

2. aws eks --region <region> update-kubeconfig --name <cluster-name>

3. aws eks --region <region> describe-cluster --name <cluster-name>

4. aws eks list-clusters --region <region>

5. aws eks delete-cluster --region <region> --name <cluster-name>

6. aws eks --region <region> list-nodegroups --cluster-name <cluster-name>

7. aws eks --region <region> tag-resource --resource-arn arn:aws:eks:<region>:<account-id>:cluster/<cluster-name> --tags Key=<key>,Value=<value>

8. aws eks --region <region> update-nodegroup-config --cluster-name <cluster-name> --nodegroup-name <nodegroup-name> --scaling-config minSize=<min-size>,maxSize=<max-size>,desiredSize=<desired-size>

9. aws eks --region <region> update-cluster-version --name <cluster-name> --kubernetes-version <new-version>

10. aws eks --region <region> list-add-ons --cluster-name <cluster-name>


# Elastic Beanstalk

aws elasticbeanstalk create-application: Creates a new Elastic Beanstalk application.

aws elasticbeanstalk create-environment: Creates a new Elastic Beanstalk environment.

aws elasticbeanstalk update-environment: Updates an existing Elastic Beanstalk environment.

aws elasticbeanstalk describe-environments: Lists information about all Elastic Beanstalk environments in your account.

## Note: 

These are some of the most commonly used commands that should be sufficient for most basic AWS workflows.You can find more information and options for each command in the AWS CLI documentation: https://awscli.amazonaws.com/v2/documentation/api/latest/index.html

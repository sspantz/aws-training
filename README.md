# AWS Training

## Table of Contents
- The AWS Fundamentals: 
    - IAM => *DONE on 2 Jun 2022*
    - EC2 
    - Load Balancing
    - Auto Scaling
    - EBS
    - EFS
    - Route 53
    - RDS
    - ~~ElastiCache~~
    - S3
    - CloudFront
- The AWS CLI: 
    - CLI setup => *DONE on 2 Jun 2022* 
    - usage on EC2
    - best practices => *DONE on 2 Jun 2022* 
    - SDK
    - advanced usage
- In-Depth Database comparison: 
    - RDS
    - Aurora
    - DynamoDB
    - ~~Neptune~~
    - ~~ElastiCache~~
    - ~~Redshift~~
    - ElasticSearch
    - Athena
- Monitoring, Troubleshooting & Audit: AWS CloudWatch, CloudTrail
- AWS Integration & Messaging: 
    - SQS
    - SNS
    - Kinesis
- AWS Serverless: 
    - AWS Lambda
    - DynamoDB
    - API Gateway
    - ~~Cognito~~
- AWS Security best practices
    - KMS
    - SSM Parameter Store
    - IAM Policies
- VPC & Networking in depth
- AWS Other Services Overview: 
    - ~~CICD (CodeCommit, CodeBuild, CodePipeline, CodeDeploy)~~
    - CloudFormation
    - ECS
    - ~~Step Functions~~
    - ~~SWF~~
    - ~~EMR~~
    - ~~Glue~~
    - ~~OpsWorks~~
    - ~~ElasticTranscoder~~
    - ~~AWS Organizations~~
    - ~~Workspaces~~
    - ~~AppSync~~
    - ~~Single Sign On (SSO)~~
- Tips to ROCK the exam

## Concepts
1. region => zone
2. console
3. Route 53 => global => no region
4. aws global infrastructure => regional list => services


## IAM Permissions
- Users, Group and Policies 
  - Consists of
    - Version:policylanguageversion,alwaysinclude“2012-10- 17”
    - Id:anidentifierforthepolicy(optional)
    - Statement:oneormoreindividualstatements(required)
  - Statements consists of
    - Sid:anidentifierforthestatement(optional)
    - Effect:whetherthestatementallowsordeniesaccess (Allow, Deny)
    - Principal:account/user/roletowhichthispolicyappliedto
    - Action:listofactionsthispolicyallowsordenies
    - Resource:listofresourcestowhichtheactionsappliedto
    - Condition:conditionsforwhenthispolicyisineffect (optional)
- Remove users
  - add permissions back to users
  - play with policies => visual editor => JSON
- MFA => try to config on your phone => QR code => add accounts
  - root user
  - IAM users 
- Account settings => password policy
- Access to AWS options
  - aws management console, protected by password + MFA
  - cli => cli key, protected by access keys => generated through the AWS Console => aws-cli => open source
    - A tool that enables you to interact with AWS services using commands in your command-line shell
    - Direct access to the public APIs of AWS services
    - You can develop scripts to manage your resources
    - It’s open-source https://github.com/aws/aws-cli
    - Alternative to using AWS Management Console
  - sdk, protected by access keys => language specific APIs
    - Language-specific APIs (set of libraries)
    - Enables you to access and manage AWS services programmatically
    - Embedded within your application
    - Supports
    - SDKs(JavaScript,Python,PHP,.NET,Ruby,Java,Go,Node.js, C++)
    - Mobile SDKs (Android, iOS, ...)
    - IoT Device SDKs (Embedded C, Arduino, ...)
    - Example: AWS CLI is built on AWS SDK for Python
- Best Practice
    - Don’t use the root account except for AWS account setup • One physical user = One AWS user
    - Assign users to groups and assign permissions to groups
    - Create a strong password policy
    - Use and enforce the use of Multi Factor Authentication (MFA)
    - Create and use Roles for giving permissions to AWS services
    - Use Access Keys for Programmatic Access (CLI / SDK)
    - Audit permissions of your account with the IAM Credentials Report • Never share IAM users & Access Keys
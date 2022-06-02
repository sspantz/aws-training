# AWS Training

## Table of Contents
- The AWS Fundamentals: 
    - IAM
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
    - CLI setup
    - usage on EC2
    - best practices
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
- Password Policies
- MFA
  - root user
  - IAM users 
- Account settings
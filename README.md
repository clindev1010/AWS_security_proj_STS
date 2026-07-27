# AWS Security Project: STS (SERVICE TOKEN SERVICE)

- Cloud Structure Processes
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/11b71c4c-04c4-49a2-846e-48426cd6fdcf" />


-Traditional setup of Cloud system infrastructure
- ( Multiple AWS accounts, Dev, Staging, Prod, Shared Services)
<br>
<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/32f3ca8f-72e3-4eb1-a828-97ec7ff47bca" />


-
-
-
<br>
<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/9eb5fcd7-cb07-4785-84e2-680c39ce5352" />
-account A has a Lambda/ ECS or a task that needs to do something in Account B
- It has permissions to assume a role that lives in Account B
- When Account B exposes the role in a trust policy & it says I trust account A to suit me and it has a permissions policy attached to it
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/7ccca7b0-d568-4b8e-90ed-5db8e6858a22" />

Account A calls STS and callsback credentials
No long lived keys for attackers

-In Account A:
1. Build End to end Lambda calls public API that calls realtime location of ISS (space station)
2. It assumes a role in account B via STS and dumps ajacent results into S3 bucket
<img width="1265" height="773" alt="image" src="https://github.com/user-attachments/assets/1a11af27-c72a-49fb-b973-4951320259f1" />


STEP-by-step Approach
Select S3
<img width="592" height="349" alt="image" src="https://github.com/user-attachments/assets/f92635b0-b786-4efc-90b4-dd7c9769ce1a" />

<br>
<img width="1240" height="947" alt="image" src="https://github.com/user-attachments/assets/441295b0-1415-4a1c-9a19-cff920c5767e" />

<br>

<img width="536" height="350" alt="image" src="https://github.com/user-attachments/assets/4405e67a-9173-44f0-afe2-b53c21ecc52b" />


PROMPT CONTINUE step
AWS Cross-Account Lambda Inventory Project Guide

Act as an expert AWS Solutions Architect and AWS instructor.

I am a beginner with AWS and want to build a complete cross-account inventory solution using only the AWS Management Console and simple Python code.

Goal

Build a working solution where:

AWS Account 1 hosts a Lambda function.
AWS Account 2 contains AWS resources to inventory.
Lambda in Account 1 assumes a role in Account 2 using AWS STS.
Lambda collects information (starting with EC2 instances).
Lambda writes the results into an S3 bucket in Account 1.
The solution follows AWS security best practices.
Requirements

Guide me one step at a time.

Do NOT skip any clicks.

Assume I have never used AWS before.

For every step include:

Which AWS account to log into.
Which AWS Console page to open.
What to search for.
Every button to click.
Every value to enter.
Every checkbox to select.
Every policy to create.
Every trust relationship to configure.
Every permission required.
How to verify each step before continuing.

For every IAM policy:

Explain why it is needed.
Explain what each permission does.
Follow the principle of least privilege.

For every role:

Explain who assumes it.
Explain why it exists.
Explain how AWS STS uses it.

For every AWS service used (IAM, STS, Lambda, S3, CloudWatch, EC2):

Explain its purpose.
Explain how it fits into the overall architecture.
Code

When code is needed:

Provide complete Python code.
Explain every line.
Do not omit imports.
Use boto3.
Include comments.
Testing

After each major step:

Show me how to verify that it worked.

Include:

Expected console output
Expected Lambda response
Expected CloudWatch logs
Expected S3 objects
Common mistakes
How to troubleshoot them
Error Handling

For every step include common errors such as:

AccessDenied
AssumeRole failures
Missing permissions
Bucket policy issues
IAM trust relationship problems
Region mismatch
Lambda timeout
Serialization errors

Explain how to identify and fix each one.

Architecture

Draw ASCII diagrams throughout the guide showing:

IAM Roles
Trust relationships
STS AssumeRole flow
Lambda execution flow
S3 uploads
Cross-account communication
Best Practices

Explain:

Least privilege IAM
Why STS is safer than access keys
Why cross-account roles are preferred
CloudTrail auditing
CloudWatch logging
S3 encryption
IAM naming conventions
Security considerations
Final Deliverable

By the end of the guide I should have:

Account 1 running a Lambda function.
Account 2 configured with a cross-account IAM role.
Lambda successfully assuming the role.
EC2 inventory collected.
Results stored as JSON in S3.
CloudWatch logs showing successful execution.

Finally, explain how to expand the solution to inventory additional AWS services such as:

IAM
Lambda
ECS
EKS
RDS
DynamoDB
S3
VPC
Route 53
CloudTrail
CloudWatch
Config
Security Hub
GuardDuty
Organizations
Secrets Manager
Systems Manager
SNS
SQS
API Gateway

After the basic solution works, explain how to extend it to inventory 10, 100, or 1,000 AWS accounts using AWS Organizations and automated role assumption.

This prompt is designed to produce a thorough, tutorial-style walkthrough that explains both the "how" and the "why" behind each step.




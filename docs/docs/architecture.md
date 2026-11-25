HealthTechGov – System Architecture

Overview

The project uses GitHub and AWS services to manage application development and automate deployment.

Architecture Components

1. GitHub

Stores application source code and manages team collaboration.

2. AWS CodePipeline

Automates the software delivery workflow.

3. AWS CodeBuild

Builds and tests the application.

4. Amazon EC2

Hosts the deployed application.

5. Amazon CloudWatch

Monitors application performance and logs.

6. AWS IAM

Controls access to AWS resources.

Workflow

1. Developer pushes code to GitHub.
2. CodePipeline detects the changes.
3. CodeBuild builds and tests the application.
4. The application is deployed to EC2.
5. CloudWatch monitors application activity.

Expected Result

An automated and organised software deployment process.

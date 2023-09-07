# Day 51: CI/CD pipeline on AWS - Part 2 🚀 ☁

![Parag Pallav Talks](https://img.shields.io/badge/Parag%20Pallav%20Singh-ED225D?style=for-the-badge&logo=pug&logoColor=C0FFF4) ![AWS](https://img.shields.io/badge/AWS%20CodeDeploy-FF9900?style=for-the-badge&logo=amazonaws)

## Understanding CodeDeploy

CodeDeploy is a deployment service that automates application deployments to Amazon EC2 instances, on-premises instances, serverless Lambda functions, or Amazon ECS services. You can deploy a nearly unlimited variety of application content, including:
- Code
- Serverless AWS Lambda functions
- Web and configuration files
- Executables
- Packages
- Scripts
- Multimedia files

## Setup
Follow this for steps guided https://docs.aws.amazon.com/codedeploy/latest/userguide/getting-started-codedeploy.html

You need to take care of following tasks
- Setting up
- Create a service role for CodeDeploy
- Limit the CodeDeploy user's permissions
- Create an IAM instance profile for your Amazon EC2 instances

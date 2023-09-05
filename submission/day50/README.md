# Day 50: CI/CD pipeline on AWS - Part-1 ☁

![Parag Pallav Talks](https://img.shields.io/badge/Parag%20Pallav%20Singh-ED225D?style=for-the-badge&logo=pug&logoColor=C0FFF4) ![AWS](https://img.shields.io/badge/AWS%20CodeCommit-FF9900?style=for-the-badge&logo=amazonaws)
## Understanding CodeCommit

AWS CodeCommit is a secure, highly scalable, fully managed source control service that hosts private Git repositories.
It is a version control service hosted by Amazon Web Services that you can use to privately store and manage assets (such as documents, source code, and binary files) in the cloud.

The following figure shows how you use your development machine, the AWS CLI or CodeCommit console, and the CodeCommit service to create and manage repositories:

<kbd>![image](https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/138e92f5-b146-45c5-a44e-38402468b2e8)</kbd>

## Setup
Follow this to setup CodeCommit: https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up.html

Basically you need to take care of the following things
1. Setting up user, user permissiona and policies using AWS IAM
2. Setting up using Git credentials
3. Setting up your local development 
4. Making your project repository.

Once all setup, you will end with something like this, with your respective project files

<kbd><img width="959" alt="image" src="https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/2584d446-e382-4cdb-bffa-5d24b9f58e38"></kbd>

Now you will be able to perform Git operations between your local environment and CodeCommit.✌🏼



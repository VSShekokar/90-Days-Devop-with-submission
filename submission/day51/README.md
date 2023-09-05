# Day 51: CI/CD pipeline on AWS - Part 2 🚀 ☁

![Parag Pallav Talks](https://img.shields.io/badge/Parag%20Pallav%20Singh-ED225D?style=for-the-badge&logo=pug&logoColor=C0FFF4) ![AWS](https://img.shields.io/badge/AWS%20CodeBuild-FF9900?style=for-the-badge&logo=amazonaws)

## Understanding CodeBuild
AWS CodeBuild is a fully managed continuous integration service that compiles source code, runs tests, and produces ready-to-deploy software packages.
You just specify the location of your source code and choose your build settings, and CodeBuild will run your build scripts for compiling, testing, and packaging your code.

<kbd>![image](https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/d8af73f2-72b2-42a1-becf-f1d7e6a2c18e)</kbd>

## Setup
Follow this to setup CodeBuild: https://docs.aws.amazon.com/codebuild/latest/userguide/getting-started.html

You need to take care of the following steps
- Create the source code
- Create the buildspec file
- Create two S3 buckets
- Upload the source code and the buildspec file
- Create the build project
- Run the build

If everything is setup, Codebuild looks like this

<kbd><img width="960" alt="image" src="https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/9a022d4a-1716-461c-9cc6-f49233354a42"></kbd>


## What is a buildspec file
A buildspec is a collection of build commands and related settings, in YAML format, that CodeBuild uses to run a build. 
Without a build spec, CodeBuild cannot successfully convert your build input into build output or locate the build output artifact in the build environment to upload to your output bucket.
To use it better, refer [AWS Buildspec File](https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html)


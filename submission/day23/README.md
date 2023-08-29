# Day 23 Task: Jenkins Freestyle Project

<img src="https://img.shields.io/badge/Parag%20Pallav%20Singh-black?style=for-the-badge&logo=docker"/>
<img src="https://img.shields.io/badge/Jenkins Freestyle Project-ffff33?style=for-the-badge&logo=jenkins"/>

# Task-01

### Create a agent for your app. ( which you deployed from docker in earlier task)

1. Access your Jenkins dashboard through a web browser.
2. Navigate to "Manage Jenkins" and then select "Manage Nodes and Clouds." In this section, you'll be able to create a new agent for your Jenkins setup.

<kbd>![image](https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/aa986482-e765-4274-99b0-36f6440f475a)

3. Click on the "New Node" option.
4. Give a suitable name to the agent (e.g., "agent-docker").
5. Select "Permanent Agent" and then click "OK."

<kbd>![image](https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/0f474f5c-ed22-4f56-866b-d393711f9ec8)

6. Define the number of executors (simultaneous build processes) for the agent.

<kbd><img width="660" alt="image" src="https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/51c129a7-e133-48b1-80be-441be8dba7ca">

<kbd><img width="680" alt="image" src="https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/29a255a6-50e6-48d1-a706-8088bb128fa3">

7. Select the suitable launch method. For simplicity, you can opt for "Launch agent by connecting it to the master."
8. Save the Configuration: Click "Save" to finalize the new agent setup.

### Create a new Jenkins freestyle project for your app.

1. We will be using [React Django App](https://github.com/paragpallavsingh/react_django_demo_app) for this.
2. Login to Jenkins: Access your Jenkins dashboard using a web browser.
3. Create a New Project: Click on "New Item" to create a new project.
4. Choose Project Type: Select "Freestyle project" as the project type and provide a name for your project.
5. Configure Source Code Management: In the project configuration, specify details like the source code repository URL and the branch to build.
6. Define Build Steps: Under the "Build" section, add build steps such as executing shell commands or running scripts required for your project.
```
 docker build . -t django-app
 docker run -d -p 8001:8001 django-app:latest
```
7. Save and Build: Click "Save" to create the project. You can manually trigger builds using the "Build Now" button.

<kbd><img width="959" alt="image" src="https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/57b29a5b-5401-4cfe-b7d0-85d06df0b15b">

Running on port 8001. [**Make sure your port is defined in inbound security rules which you are using for your app**]

<kbd><img width="479" alt="image" src="https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/18dc6277-160a-4f00-b227-d6f1d9b10efa">

# Task-02

### Create Jenkins project to run "docker-compose up -d" command to start the multiple containers defined in the compose file

After following all steps, all you need is to update the script a bit as given below

```
echo "code cloned"
docker-compose down
docker-compose up -d --no-deps --build web
echo "code deploy"
docker-compose down
```
### Set up a cleanup step in the Jenkins project to run "docker-compose down" command to stop and remove the containers defined in the compose file.

Since you will need to remove your container after this demo, I've added a `docker-compose down` command. Please make sure to remove this while trying and you don't your app to be down.

<kbd><img width="641" alt="image" src="https://github.com/paragpallavsingh/90DaysOfDevOps/assets/40052830/a0cbb857-0ffb-4913-907b-50d0b45f03e4">

## Note of thanks🤗 and two good references:
1. Rohan Balgotra's [blog](https://namg.hashnode.dev/jenkins-freestyle-project-for-devops-engineers-day-23-task)
2. Namrata Gupta's [blog](https://devxblog.hashnode.dev/jenkins-freestyle-project-for-devops-engineers#heading-creating-the-agent-for-app)

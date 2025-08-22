# CI/CD by Jenkins
This project is intended to create a Jenkins pipeline as a template whoever can use it for their own automation.

Demonstration by Docker image.<br>
I use WSL (Ubuntu) on Windows.

```
docker run -d \
  --name jenkins \
  -p 8080:8080 \
  -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  jenkins/jenkins:lts-jdk17
```

Once run the command, we can access the Jenkins GUI
Then, we can find the initial password location /var/jenkins_home/secrets/initialAdminPassword

Get the initial password 
```
docker exec -it  jenkins  cat /var/jenkins_home/secrets/initialAdminPassword
```
Follow the Screens until installation is completed. ( default is fine )

## First cicd project

Select Newproject -> Multibranch Pipeline






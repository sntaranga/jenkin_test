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

## Plugin required
Install Blue Ocean Aggregater

## First cicd project

Select Newproject -> Multibranch Pipeline

**Please make sure you have the correct filename in the Script Path field of the Build Configuration. Unless very hard to notice it.**

Note: I added a sleep command in Jenkins file to see how the flow happened

This is a simple template for CI/CD implementation using Jenkins and this can be used for a starting point for  your production-grade deployments.

![Blue Ocean view of the pipeline](jenkins.png)

**If  gitlab is used, use AccessToken for password.**

# Try It yourself. It is easy


## Disclaimer of Liability

The information, materials, and work provided in connection with this project are delivered “as is” and without warranties of any kind, either express or implied. The author/contractor assumes no responsibility or liability for any errors, omissions, or outcomes resulting from the use of this project.

By using or implementing any part of this project, you agree that the author/contractor shall not be held liable for any direct, indirect, incidental, consequential, or special damages, including but not limited to loss of data, business interruption, or financial loss, arising out of or in connection with the use of this project.

It is the responsibility of the user or organization to review, test, and validate all outputs and ensure compliance with applicable laws, regulations, and standards before implementation.

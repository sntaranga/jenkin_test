# CI/CD by Jenkins
This project is intended to create a Jenkins pipeline as a template whoever can use it for their own automation.

Demonstration by Docker image.

docker run -d \
  --name jenkins \
  -p 8080:8080 \
  -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  jenkins/jenkins:lts

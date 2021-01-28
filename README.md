# Technical-test-PT-Takalab

## 1 Can you please simply explain how the infrastructure flows?
-> Answer = 
- Planning the application => Code the application => Build docker docker image/compose application => Testing application from server => Deploy it application from kubernetes => Operate the application => Monitor running application using grafana.

## 1.2 
- Planning the application
= Prepare all technology that we need to deploy the application. ex : AWS, github, docker, nginx, jenkins, ansible, kubernetes
- Code the application 
= Prepare to make the docker images for deploying application an give the proxy with the nginx
-> in Docker application
   : docker build -


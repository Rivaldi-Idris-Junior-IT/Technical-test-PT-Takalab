# Technical-test-PT-Takalab

## 1 Can you please simply explain how the infrastructure flows?
-> Answer = 
- Planning the application => Code the application => Build docker docker image/compose application => Testing application from server => Deploy it application from kubernetes => Operate the application => Monitor running application using grafana.

## 1.2 
- Planning the application
= Prepare all technology that we need to deploy the application. ex : AWS, github, docker, nginx, jenkins, ansible, kubernetes
- Code the application 
= Prepare to make the docker images for deploying application an give the proxy with the nginx
- in Docker application
   - Build docker image =  docker build -t namedockerhub/app:tag
   - Push docker image in dockerhub = docker push namedockerhub/app:tag
   - Pull docker image in dockerhub = docker pull namedockerhubandapp:tag
   - Build container and running another image = docker compose up -d 
   - Checking container = docker ps -a 
   - Stop container running = docker compose down   
- in Jenkins
   - Deploy in jenkins usually using with ui application to deploy app. 
   - Running the build app with jenkinsfile in our repository
- in Anisble
   - Check connection ansible all -m ping
   - Running file ansible with configuration to deploy in file yml command = ansible playbook -i hosts namefile.yml    
- in Kubernetes 
   - Running kubernetes file with all configuration in kubernetes = kubectl apply -f namefile.yml
   - Check log pods = kubectl logs -n namespace value
   - Check namespace in running = kubectl get all -n backend-frontend
   - Delete/stop service deploy kubernetes = kubectl delete -n namespace value

## 2 Imagine there is deployment that you need to handle. There are 5 backend services, and 1 worker service, and 2 front end services, 2 mobile apps applications, connected to 2 databases (PostgreSQL for relationalDB, mongoDB for historical data) and required data caching. Can you create a good infrastructure using diagrams for handling that deployment.
- number 2 in pdf to see infrastructure

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
![Arsitektur Deploy -2](https://user-images.githubusercontent.com/34388205/106200412-844f5d00-61e9-11eb-8807-8da5870a8a2e.jpg)

## 3 English Test
![Screenshot from 2021-01-29 04-37-54](https://user-images.githubusercontent.com/34388205/106203841-997aba80-61ee-11eb-88d9-d17ffd7ebc9f.png)

## Personality Test 1
![Screenshot from 2021-01-29 04-46-36](https://user-images.githubusercontent.com/34388205/106204008-d8a90b80-61ee-11eb-8159-688515ea4d7b.png)

## Personality Test 2


